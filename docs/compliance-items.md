Add a new page "Trámites" (English: "Paperwork & taxes") to La Libreta, with its own item in the bottom navigation. It shows each business the tax forms, registrations, licenses and deadlines that apply to it in New York City. Keep everything else as is.

IMPORTANT RULES
- Do not generate legal or tax content with AI. Show only the items listed below, word for word in meaning, each with its official link. If something is not on the list, do not invent it.
- Footer on the page: "Información general, no es asesoría legal ni de impuestos. Revisado el 10 de octubre de 2026. Confirma en los sitios oficiales o con un preparador certificado. / General information, not legal or tax advice. Reviewed October 10, 2026. Confirm on the official sites or with a certified preparer."
- Show item text in Spanish and English (other app languages may show English for item text). Keep official form names as they are (Schedule C, Form 941, NYS-45...).

1. BUSINESS PROFILE (top of the page, saved in Settings for the current demo_id)
- How is your business set up? "Persona sola / Sole proprietor" (default), "LLC de un dueño / Single-member LLC", "Sociedad o LLC con socios / Partnership or multi-member LLC", "Corporación / Corporation".
- What do you do? (pick all that apply): sells products in a store (default on); sells prepared food or hot drinks; sells on the street or from a cart/truck; sells beer; sells cigarettes, tobacco or vapes; accepts SNAP/EBT; beauty services (salon, barber, nails); home improvement or construction; cleaning or home services; child care; drives passengers with apps; sells online or gets paid through payment apps.
- Do you have employees? (default no). Do you pay contractors? (default no). Do you use a business name that is not your own name? (default no).
- Show a checklist built from the profile, grouped "Federal (IRS)", "Estado de Nueva York / New York State", "Ciudad de Nueva York / New York City". Each item: title, one plain sentence, the form names, when it is due, a button "Ver en sitio oficial / Official site" that opens the link, and a "Ya lo tengo / Done" checkbox saved per demo_id. Show progress "4 de 9 listos / 4 of 9 done".

2. ITEMS (show when the condition is true)
FEDERAL (IRS)
F1 Always. Taxpayer number: use your SSN, or get an ITIN with Form W-7 if you cannot get an SSN. https://www.irs.gov/forms-pubs/about-form-w-7
F2 Always (required if employees, partnership, corporation or multi-member LLC; recommended for everyone, banks often ask). EIN: free from the IRS, online or Form SS-4. Never pay a website for it. https://www.irs.gov/businesses/small-businesses-self-employed/get-an-employer-identification-number
F3 Sole proprietor or single-member LLC. Income tax: Form 1040 with Schedule C (profit or loss from business). Due April 15. https://www.irs.gov/forms-pubs/about-schedule-c-form-1040
F4 Sole proprietor or single-member LLC. Self-employment tax: Schedule SE if net earnings are $400 or more. Due with Form 1040. https://www.irs.gov/forms-pubs/about-schedule-se-form-1040
F5 Always. Estimated tax: Form 1040-ES if you expect to owe $1,000 or more; due April 15, June 15, September 15 and January 15. https://www.irs.gov/forms-pubs/about-form-1040-es
F6 Partnership or multi-member LLC. Form 1065 and a Schedule K-1 for each partner. Due March 15. https://www.irs.gov/forms-pubs/about-form-1065
F7 Corporation. Form 1120 (C corporation, due April 15) or Form 1120-S (S corporation, due March 15). https://www.irs.gov/forms-pubs/about-form-1120
F8 Has employees. Form W-4 and Form I-9 for each employee; Form 941 every quarter (due April 30, July 31, October 31, January 31); Form 940 each year (due January 31); Forms W-2 and W-3 by January 31. https://www.irs.gov/forms-pubs/about-form-941
F9 Pays contractors. Collect Form W-9; file Form 1099-NEC by January 31 for each person paid $2,000 or more in 2026 for services ($600 for 2025 payments). https://www.irs.gov/forms-pubs/about-form-1099-nec
F10 Sells online or uses payment apps. Form 1099-K comes from apps or marketplaces when they paid you more than $20,000 and more than 200 payments in a year. All business income is taxable even without a form. https://www.irs.gov/businesses/understanding-your-form-1099-k
F11 Always. Keep records (sales, purchases, receipts) at least 3 years. La Libreta's "Exportar a Excel" helps. https://www.irs.gov/businesses/small-businesses-self-employed/recordkeeping
F12 Always. Beneficial ownership (BOI) report to FinCEN: U.S. companies no longer file (final rule, August 2026); only foreign companies registered in the U.S. do. https://www.fincen.gov/boi
F13 Accepts SNAP/EBT. Retailer authorization from USDA (FNS). https://www.fns.usda.gov/snap/retailer/apply

NEW YORK STATE
S1 Sole proprietor using a business name. Assumed Name (DBA) certificate with the County Clerk. LLC: Articles of Organization with the NYS Department of State, publish a notice within 120 days, and file a biennial statement every 2 years. Corporation: Certificate of Incorporation with the Department of State. https://dos.ny.gov
S2 Sells products, prepared food, hot drinks or on the street. Sales tax: get a Certificate of Authority from the NYS Tax Department at least 20 days before you start; charge 8.875% in NYC on taxable items (for example candy, soda, bottled water, prepared food, hot drinks; most groceries are exempt); most new sellers file every quarter, due June 20, September 20, December 20 and March 20. https://www.tax.ny.gov/bus/st/register.htm
S3 Always. NY income tax: business income goes on your New York return (IT-201) and NY estimated tax (IT-2105) uses the same quarterly dates; partnerships file IT-204, corporations CT-3 or CT-3-S. https://www.tax.ny.gov
S4 Has employees. Register for unemployment insurance (NYS-100) with the NYS Department of Labor; file NYS-45 every quarter; workers' compensation, disability and Paid Family Leave insurance are required even for one part-time employee; give the wage notice (LS 54, in Spanish if that is the worker's language) at hire; NYC minimum wage is $17.00 per hour from January 1, 2026. https://dol.ny.gov
S5 Sells products in a store. Retail Food Store license from the NYS Department of Agriculture and Markets if you sell food. https://agriculture.ny.gov
S6 Sells beer. Off-premises beer license from the NYS State Liquor Authority. https://sla.ny.gov
S7 Sells cigarettes, tobacco or vapes. Registration with the NYS Tax Department to sell cigarettes, tobacco and vapor products (plus the NYC license in C2). https://www.tax.ny.gov
S8 Beauty services. Appearance enhancement or barber licenses from the NYS Department of State, for the business and for each worker. https://dos.ny.gov
S9 Child care. License or registration with the NYS Office of Children and Family Services. https://ocfs.ny.gov

NEW YORK CITY
C1 Always. NYC Business Express lists every license and permit for your exact business type, and NYC Small Business Services gives free help. https://nyc-business.nyc.gov/nycbusiness/
C2 Sells cigarettes, tobacco or vapes. Tobacco Retail Dealer and Electronic Cigarette Retail Dealer licenses from the NYC Department of Consumer and Worker Protection (DCWP). https://www.nyc.gov/site/dca/businesses/licenses.page
C3 Sells on the street or from a cart/truck. Food: Mobile Food Vending license (for you) and permit (for the cart or truck) from the NYC Health Department. Other goods: General Vendor license from DCWP. Check both on NYC Business Express. https://nyc-business.nyc.gov/nycbusiness/
C4 Sells prepared food or hot drinks. Food Service Establishment permit from the NYC Health Department and a supervisor with a Food Protection Certificate on site. https://nyc-business.nyc.gov/nycbusiness/
C5 Home improvement or construction. Home Improvement Contractor license from DCWP. https://www.nyc.gov/site/dca/businesses/licenses.page
C6 Drives passengers with apps. TLC driver license and a TLC-licensed vehicle from the NYC Taxi and Limousine Commission. https://www.nyc.gov/site/tlc/index.page
C7 Has employees. NYC Earned Safe and Sick Time: employees earn up to 40 hours a year (56 with 100 or more employees); give the Notice of Employee Rights. https://www.nyc.gov/site/dca/index.page
C8 Sole proprietor, single-member LLC, partnership or multi-member LLC. NYC Unincorporated Business Tax: file if your business gross income is over $95,000. https://www.nyc.gov/site/finance/index.page
C9 Always. Free tax help: NYC Free Tax Prep for those who qualify. https://www.nyc.gov/taxprep

3. "PRÓXIMAS FECHAS / UPCOMING DEADLINES"
At the top, show the next 3 deadlines that apply to the profile, computed in code from today's date, using the due dates above (estimated tax, sales tax, Form 941 and NYS-45 quarterly, January 31 forms, March 15 and April 15 returns). Example for the demo profile: "20 dic: impuesto de ventas (NYS)", "15 ene: impuesto estimado (1040-ES, IT-2105)", "15 abr: Form 1040 + Schedule C".
On Hoy, add one line to "Qué hacer hoy" when a deadline is 30 days away or less, for example "Vence pronto: impuesto de ventas, 20 dic".

4. "DE TU LIBRETA PARA TUS IMPUESTOS / FROM YOUR LIBRETA FOR YOUR TAXES"
A small box with this year's totals computed in code from confirmed entries: sales (gross receipts), purchases (goods bought for resale) and cash collected, with the note "Lleva estos números a tu preparador o a NYC Free Tax Prep. / Bring these numbers to your preparer or to NYC Free Tax Prep." If sample entries are included, say "Incluye datos de muestra / Includes sample data".
