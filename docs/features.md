# Palapa: what we built

**Palapa** · *Habla. Confirma. Listo.* (Speak. Confirm. Done.)
A voice-first cash register for corner stores (bodegas) and other businesses that run on cash in New York. Built on Base44, with ElevenLabs for voice.
Live: https://palapa.base44.app (publish the latest build) · Track: Finance (Banking the Unbanked)

Items marked *(adding now)* are in the Base44 build that started at 3:13 PM and still need a test.

## Key features

1. **Record by voice or text** in Spanish, English or a mix: sales, deliveries, fiado (store credit) and payments.
2. **Receipt-style confirmation** ("¿Así fue?") shows what will change; nothing is saved until "Sí, anótalo".
3. **One sentence updates cash, stock, fiado and sales tax together.**
4. **Home shows the day at a glance:** total sales, tax, net, fiado, inventory alerts and a ledger of today's entries.
5. **Ask your data:** "¿Cuánto vendí hoy?", "¿Qué se está acabando?", "¿Quién me debe?".
6. **Finanzas:** a self-reported monthly statement a lender can review, in Spanish or English, printable, exportable to Excel.
7. **Trámites:** the tax forms, registrations, licenses and deadlines for each type of business (IRS, New York State, New York City), with live deadlines.
8. **Money you can trust:** the AI only fills in fields; code calculates every dollar from a log that is never edited.
9. **Built for the counter:** large type, nine languages, works on a phone, separate layouts for phone and computer where it helps.

## All functionality, by screen

### Header and navigation
- Logo, "Palapa" wordmark and business name; gear icon opens Ajustes.
- Bottom tabs: Hogar, Inventario, Trámites, Finanzas *(Fiado moves to a Home button: adding now)*.

### Hogar (Home)
- **Voice bar** (the one bold element): yellow mic, "Toca para hablar", "Escribir".
- Voice in: ElevenLabs Scribe through a Base44 backend function; falls back to the browser's dictation automatically. Statuses "Te escucho…", "Un momento…"; the recognized text stays visible and editable.
- **"Añade un registro" box** with subtitle "Voz o texto" and an "Enviar" button *(adding now; until then the box opens from "Escribir" with "¿Qué pasó?" and "Registrar")*.
- AI turns the sentence into fields: type, product, quantity, price, customer, amount. Four entry types: sale, delivery, fiado, payment. Fiado phrasings like "Le fié un café a Doña Rosa" work.
- Checks in code: unknown product asks "¿Cuál producto?"; two products asks "Dime un producto a la vez"; price far from the catalog asks to confirm; warns before stock goes below zero.
- **Receipt sheet "¿Así fue?":** entry type tag, line items with unit price, total, "Qué va a cambiar" (cash and stock before and after), "Sí, anótalo", "Corregir", "Cancelar". Card in the language of the sentence. Double taps save once.
- After saving: the sheet slides away, the new line flashes in the ledger, the total counts up, and the message reads "Listo, anotado · Quedan 23 · Coca-Cola lata".
- Reply rule: typed input gets an on-screen reply; spoken input also gets one short spoken reply in the language spoken.
- **"Ventas totales" section:** Ventas totales, Impuestos generados, Neto, plus a small line with cash in and cash out *(adding now; today the top shows "Entró hoy" and "Salió · Neto · Te deben")*.
- **"Vendido a crédito (fiado)" section:** Vendido hoy, Deuda total, "Ver fiado" button *(adding now)*.
- **"Alertas inventario":** low-stock rows *(adding now as its own section; today they sit in "Avisos")*.
- **Avisos:** "Cobra a Don Luis: $7.50", "Vence pronto: ..." tax deadlines, slow-day note.
- **"Lo de hoy" ledger:** time, description, signed amount, Deshacer (undo). Empty day shows an example chip that runs the whole flow.
- Questions answered from the data without creating an entry.

### Fiado (Store credit)
- "Te deben en total"; one row per customer with initials, name and amount owed, or "Al día".
- Tap a customer to see the full history with date and time; "Registrar pago" in each row.

### Inventario (Inventory)
- Nine real corner-store brands: Agua Poland Spring, Café Bustelo, Malta Goya, Coca-Cola lata, Jarritos Tamarindo, Té Arizona, Takis Fuego, Habichuelas Goya, Gansito.
- Each row: name, "Entiende:" (the words the voice understands), price and cost, quantity, pencil to edit.
- Low-stock products first with a "Bajo" chip; "Nuevo producto".
- "Cobra impuesto" switch per product *(adding now: on for drinks and snacks, off for beans and packaged coffee)*.
- Price changes never change past sales.

### Trámites (Paperwork and taxes)
- Business profile: how it is set up, 12 kinds of activity, employees, contractors, business name.
- Checklist from 31 official items (13 federal, 9 New York State, 9 New York City), filtered by the profile, in three collapsible groups with counts; each item expands to its description, forms and official link; "Ya lo tengo" checkbox and progress bar.
- **Próximas fechas** update instantly when the profile changes. On a computer: two columns with the deadlines panel staying on screen. On a phone: a pinned "Próxima: 20 dic · Impuesto de ventas · 3 fechas" bar that expands.
- "Vence pronto" reminders on Home for deadlines within 30 days.
- "De Palapa para tus impuestos": this year's sales, purchases and cash collected *(plus sales tax: adding now)*.
- Disclaimer: general information, not legal or tax advice; reviewed October 10, 2026.

### Finanzas (Finance report)
- Month picker; sample-data banner when it applies.
- Ventas as the big number; Cobrado, Compras, Neto en efectivo, Fiado pendiente, sales count, active days *(plus Impuestos de ventas: adding now)*.
- Weekly sales chart with values on the bars.
- Lender statement with an ES / EN toggle: average weekly sales, weeks with records, steadiness with a one-line explanation.
- All entries behind "Ver todo lo anotado (N)", sample entries tagged.
- Bottom bar: "Imprimir / Guardar PDF" and "Exportar a Excel".

### Ajustes (Settings, gear icon)
- Idioma: Español, English, Português, Kreyòl Ayisyen, Français, Arabic (right to left), Chinese, Russian, Turkish.
- Negocio: business and owner name.
- Voz: read aloud on or off; ElevenLabs voice ID.
- *Impuestos: business location sets the sales-tax rate (New York City 8.875%, Nassau 8.625%, Suffolk 8.625%, Westchester 8.375%, New Jersey 6.625%, or custom): adding now.*
- Reiniciar demo and Borrar todo, each with a confirmation.

## Under the hood

- Append-only log: entries are never edited; undo marks an entry as undone; every number is recomputed from the log.
- Each entry saves its price, cost *(and sales tax: adding now)* at the moment it is confirmed.
- Duplicate-save guard; safety screen instead of a blank page.
- Each browser gets its own demo store (sample September 2026 plus one open fiado); first visit shows "Preparando tu demo…".
- No login, SSN, ID or bank account needed for the demo; API keys stay on the server.
- Built with Base44 (app, database, AI parsing, backend functions, secrets) and ElevenLabs (Scribe speech-to-text, text-to-speech); browser speech as backup.

## Next (not built today)

WhatsApp voice notes; supplier reorders through MCP; private accounts with login; several users for businesses with 5 to 10 employees; validating the Finanzas statement with a credit union or CDFI.
