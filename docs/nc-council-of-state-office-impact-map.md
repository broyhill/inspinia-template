# North Carolina Council of State Office Impact Map

## Purpose

This Markdown document defines one comprehensive research and data-building task:
map every North Carolina Council of State office by its constitutional role,
departmental structure, regulatory authority, core functions, jurisdiction, and
affected voter categories.

The immediate scope is the 10 statewide elected executive offices that make up
the North Carolina Council of State. The same schema can later be extended to
federal, legislative, judicial, county, municipal, school board, sheriff, and
special district offices across all 100 counties.

## Source baseline

The Council of State consists of the officers established in Article III of the
North Carolina Constitution. NC.gov describes 10 popularly elected executive
branch officials: Governor, Lieutenant Governor, Secretary of State, State
Treasurer, State Auditor, Attorney General, Commissioner of Agriculture,
Commissioner of Insurance, Commissioner of Labor, and Superintendent of Public
Instruction.

Primary official sources used for this task:

- NC.gov executive branch overview: <https://www.nc.gov/your-government/executive>
- NC.gov government overview: <https://www.nc.gov/your-government>
- North Carolina Constitution, Article III: <https://www.ncleg.gov/Laws/Constitution/Article3>
- NC Governor: <https://governor.nc.gov/>
- NC Boards and Commissions: <https://bc.governor.nc.gov/BoardsAndCommissions>
- NC Lieutenant Governor: <https://ltgov.nc.gov/about>
- NC Secretary of State: <https://sosnc.gov/>
- NC Department of Justice: <https://ncdoj.gov/about-ncdoj/duties-and-responsibilities/>
- NC Department of Agriculture and Consumer Services: <https://www.ncagr.gov/about-ncdacs>
- NC Department of Insurance: <https://www.ncdoi.gov/about-doi>
- NC Department of Labor: <https://www.labor.nc.gov/about-ncdol/divisions>
- NC Office of the State Auditor: <https://www.auditor.nc.gov/about-office-state-auditor>
- NC Department of State Treasurer: <https://www.nctreasurer.com/divisions>
- NC Department of Public Instruction: <https://www.dpi.nc.gov/about-dpi>

## Deliverable definition

Build a source-backed office impact map that answers these questions for each
office:

1. What is the elected office?
2. What is the constitutional or statutory source of the office?
3. What department, agency, board, commission, or administrative apparatus does
   the office lead or influence?
4. What divisions, bureaus, sections, programs, or boards sit under or connect
   to that office?
5. What laws, regulations, standards, licensing programs, budgets, grants,
   audits, enforcement powers, appeals, appointments, procurement decisions, or
   policy levers does the office control or materially influence?
6. What geography is affected: statewide, county, municipal, district, school
   attendance area, judicial district, highway division, regional office, or
   other jurisdiction?
7. Which voter categories and constituencies are affected?
8. What datasets are required to make the map complete and maintainable?

## Council of State office list

| Office | Election and role context | Department or administrative center |
| --- | --- | --- |
| Governor | Statewide elected chief executive | Office of the Governor; appointed Cabinet; boards and commissions |
| Lieutenant Governor | Statewide elected second executive officer | Office of the Lieutenant Governor; Senate presiding role; ex officio education boards |
| Secretary of State | Statewide elected executive officer | Department of the Secretary of State |
| State Auditor | Statewide elected executive officer | Office of the State Auditor |
| State Treasurer | Statewide elected executive officer | Department of State Treasurer; State Health Plan; retirement systems; LGC staff |
| Superintendent of Public Instruction | Statewide elected executive officer | Department of Public Instruction |
| Attorney General | Statewide elected executive officer | Department of Justice |
| Commissioner of Agriculture | Statewide elected executive officer | Department of Agriculture and Consumer Services |
| Commissioner of Insurance | Statewide elected executive officer | Department of Insurance |
| Commissioner of Labor | Statewide elected executive officer | Department of Labor |

## Standard data schema for every office

Use this schema for the Council of State and for later expansion to local,
judicial, and federal elected offices.

### Office identity fields

- `office_name`
- `office_level`: federal, state, judicial, county, municipal, township,
  school, special district
- `branch`: executive, legislative, judicial, independent, mixed
- `is_partisan`
- `election_cycle`
- `term_length`
- `district_or_jurisdiction_name`
- `jurisdiction_type`
- `jurisdiction_geography`
- `current_officeholder`
- `appointing_authority_if_any`
- `succession_or_vacancy_process`

### Authority fields

- `constitutional_authority`
- `statutory_authority`
- `administrative_code_authority`
- `budget_authority`
- `rulemaking_authority`
- `licensing_authority`
- `enforcement_authority`
- `investigation_authority`
- `audit_or_oversight_authority`
- `appointment_authority`
- `board_or_commission_memberships`
- `emergency_authority`
- `limits_on_authority`

### Program and division fields

- `department`
- `division`
- `bureau`
- `program`
- `service`
- `grant_or_funding_stream`
- `regulated_entity_type`
- `licensed_entity_type`
- `inspection_or_audit_subject`
- `appeal_or_review_body`
- `public_records_or_registry`

### Constituency fields

- `affected_voter_categories`
- `affected_industries`
- `affected_public_employees`
- `affected_private_workers`
- `affected_students_or_families`
- `affected_local_governments`
- `affected_state_agencies`
- `affected_taxpayers`
- `affected_consumers`
- `affected_licensees`
- `affected_vulnerable_populations`
- `affected_geographic_regions`
- `equity_or_access_considerations`

### Evidence fields

- `official_source_url`
- `statute_url`
- `administrative_rule_url`
- `budget_url`
- `org_chart_url`
- `annual_report_url`
- `last_verified_date`
- `notes_on_uncertainty`

## Cross-office voter and constituency taxonomy

Use these categories consistently so a voter can be matched to all offices that
affect them.

### Geography

- Statewide voters
- Congressional district voters
- State Senate district voters
- State House district voters
- Judicial district voters
- County voters
- Municipality voters
- Township or precinct voters where applicable
- School district or attendance-area families
- Rural residents
- Urban residents
- Coastal residents
- Mountain residents
- Piedmont residents
- Border-county residents
- Disaster-prone communities
- Transportation corridor communities

### Civic and taxpayer status

- Registered voters
- Unregistered eligible citizens
- Taxpayers
- Property owners
- Renters
- Utility customers
- Public benefit recipients
- Public records users
- Advocacy organizations
- Public meeting participants

### Work and economic status

- Private-sector employees
- Public-sector employees
- State employees
- Local government employees
- Teachers and school personnel
- Law enforcement officers
- Firefighters and rescue workers
- Retirees and pension beneficiaries
- Small business owners
- Corporations and registered entities
- Nonprofits and charities
- Licensed professionals
- Contractors and vendors
- Farmers, foresters, and agribusinesses
- Insurance agents, adjusters, and regulated companies
- Investors and securities professionals
- Workers in high-risk industries
- Unemployed and underemployed workers

### Education and family status

- Public school students
- Charter school students
- Lab school and regional school students
- Parents and guardians
- Early childhood and child care families
- Community college students
- University students
- Students with disabilities
- English learners
- Homeschool and private school families where state policy intersects

### Public safety, legal, and health status

- Crime victims and survivors
- Defendants and incarcerated people where state policy intersects
- Medicaid patients and providers
- Medicare beneficiaries
- Seniors
- People with disabilities
- Consumers affected by fraud or scams
- Patients in regulated insurance markets
- Disaster survivors
- Farmworkers and migrant workers
- Tenants and homeowners affected by safety codes

## Office 1: Governor

### Core role and authority

The Governor is North Carolina's chief executive. The office chairs the Council
of State, carries out state law, serves as ex officio commander in chief of the
North Carolina National Guard, acts as director of the state budget, appoints
many executive branch officials and board or commission members, may veto
legislation, and may grant pardons. Source: <https://governor.nc.gov/>.

The Governor appoints the heads of Cabinet departments. NC.gov identifies the
Governor, the other elected executive officials, the Cabinet, independent
executive agencies such as the Office of Administrative Hearings, Office of the
State Controller, and State Board of Elections, and more than 50 licensing
boards that regulate occupations. Source: <https://www.nc.gov/your-government>.

The Governor also makes appointments to more than 350 boards and commissions
covering major state agencies, licensing, education, transportation, public
safety, environment, health, finance, universities, and other public functions.
Source: <https://bc.governor.nc.gov/MemberResources>.

### Departments, agencies, boards, and commissions to map

Map all Governor-connected units in these groups:

- Office of the Governor
- Cabinet departments appointed by the Governor, including Administration,
  Commerce, Environmental Quality, Health and Human Services, Information
  Technology, Natural and Cultural Resources, Public Safety, Adult Correction
  where applicable, Revenue, Transportation, and Military and Veterans Affairs
- Independent executive agencies that interact with gubernatorial policy or
  appointment authority
- Boards and commissions with gubernatorial appointments
- Emergency management, disaster recovery, and executive order bodies
- State budget and budget execution processes
- Clemency and pardon processes
- Judicial, regulatory, education, transportation, and university appointments
  where statutes give the Governor a role

### Functions and jurisdictions

- Statewide executive leadership
- Budget preparation, budget administration, and executive branch priorities
- Veto, signing, and implementation of legislation
- Executive orders within statutory and constitutional limits
- Emergency coordination and disaster response
- National Guard command role
- Appointment of Cabinet officials and many board and commission members
- Coordination of statewide policy priorities across departments
- Public communication and constituent services
- Clemency and pardon decisions
- Intergovernmental coordination with federal, state, local, tribal, and regional
  partners

### Affected voter categories

- All statewide voters and taxpayers
- State employees and Cabinet agency employees
- Local governments relying on state grants, disaster funds, transportation
  funds, health funds, education funds, and public safety coordination
- Regulated businesses and licensed professionals affected by gubernatorial
  appointments to licensing boards
- Students, parents, teachers, universities, and community colleges affected by
  education appointments and budget priorities
- Drivers, transit users, freight carriers, and neighborhoods affected by
  transportation board and road investment decisions
- Medicaid patients, health providers, seniors, people with disabilities, and
  families affected by DHHS policy
- Disaster survivors and communities in flood, hurricane, wildfire, and storm
  corridors
- Criminal justice stakeholders affected by pardons, executive policy, and
  public safety appointments
- Environmental justice communities affected by appointments, permitting
  priorities, and agency leadership

### Completion checklist

- Inventory every Cabinet department and attach statutory authority.
- Export all Governor board and commission profiles.
- For each board, capture appointing authority, number of Governor seats,
  geography, regulated field, public member requirements, term length, ethics
  coverage, and constituency categories.
- Create a separate appointment impact map for transportation, university,
  health, licensing, public safety, environmental, and local government finance
  boards.

## Office 2: Lieutenant Governor

### Core role and authority

The Lieutenant Governor is the second highest elected official in North
Carolina and has powers in both the legislative and executive branches. The
office presides over the North Carolina Senate and is an ex officio member of
the Council of State, State Board of Education, and State Board of Community
Colleges. Source: <https://ltgov.nc.gov/about>.

### Departments, agencies, boards, and commissions to map

- Office of the Lieutenant Governor
- North Carolina Senate presiding role
- Council of State membership
- State Board of Education ex officio membership
- State Board of Community Colleges ex officio membership
- Any statutory commissions, task forces, or boards where the Lieutenant
  Governor is named or appoints members
- Policy initiatives and working groups led by the office

### Functions and jurisdictions

- Statewide elected executive role
- Presiding officer of the Senate
- Legislative procedure influence through the Senate role
- Education policy influence through State Board of Education membership
- Community college and workforce policy influence through State Board of
  Community Colleges membership
- Public advocacy and statewide constituent engagement
- Council of State voting, consultation, and executive coordination where
  applicable

### Affected voter categories

- All statewide voters
- Senate district residents affected by Senate procedure and legislative debate
- Public school students, parents, teachers, principals, superintendents, and
  local boards of education
- Community college students, faculty, staff, trustees, and workforce partners
- Employers relying on workforce training and career pathways
- Families affected by child care, early childhood, and education policy
  advocacy
- Rural communities served by community college campuses and satellite centers

### Completion checklist

- Map every ex officio board membership and voting status.
- Link Senate rules and constitutional provisions governing the presiding role.
- Track policy initiatives separately from binding legal authority.
- Capture board committee assignments when available.

## Office 3: Secretary of State

### Core role and authority

The Secretary of State leads the Department of the Secretary of State. The
office records and administers public filings, business entity records, securities
regulation, charitable solicitation licensing, lobbying compliance, land records
support, trademarks, notary and authentication services, and other statutory
functions. Source:
<https://sosnc.gov/>.

### Divisions, programs, and registries to map

- Business Registration Division
- Securities Division
- Charitable Solicitation Licensing Division
- Lobbying Compliance Division
- Land Records Management Section
- Notary public commissioning and electronic notary functions
- UCC and secured transaction filings
- Trademarks
- Authentications and apostilles
- Advance health care directive registry or similar public registries where
  applicable
- Publications, administrative rules, and statutory authority pages

Official division examples:

- Business Registration ensures uniform compliance with statutes governing the
  creation of business entities, records information required as public record,
  and provides that information to the public.
  Source: <https://sosnc.gov/divisions/business_registration>.
- Securities administers and enforces state securities laws, including
  registration of securities, firms, and individuals, examination of registered
  firms, and enforcement through administrative, civil, and criminal actions.
  Source: <https://www.sosnc.gov/divisions/securities/about_us>.
- Charities maintains a registry of organizations licensed to solicit charitable
  contributions and licenses professional fundraisers.
  Source: <https://sosnc.gov/divisions/charities>.
- Lobbying Compliance registers lobbyists, lobbyist principals, state liaisons,
  and local government liaisons; receives required reports; publishes searchable
  directories; and administers and enforces assigned portions of the Lobbying
  Act under Chapter 120C.
  Source: <https://sosnc.gov/divisions/lobbying>.
- Land Records assists local governments with indexing, electronic access,
  storage standards, county maps, municipal annexation maps, municipal charter
  amendments, and county boundary maps.
  Source: <https://www.sosnc.gov/divisions/land_records>.

### Functions and jurisdictions

- Statewide business entity filing and public registry administration
- Securities registration, examination, investor protection, and enforcement
- Charitable solicitation licensing and enforcement
- Lobbying registration, reporting, disclosure, compliance review, and
  enforcement for covered state and local government lobbying activity
- Local land records standards and technical assistance
- Notary commission administration
- Official records, publications, certifications, and authentication services
- Public access to business, charity, securities, and land records

### Regulatory authority

Key legal areas include business entity statutes, filing and registered agent
laws, North Carolina Securities Act, charitable solicitation law, the Lobbying
Act, trademark law, telephonic seller registration, land records management, and
other laws listed by the Secretary of State statutory authority page:
<https://sosnc.gov/home/statutory_authority>.

### Affected voter categories

- Business owners, entrepreneurs, corporations, LLCs, partnerships, nonprofits,
  and registered agents
- Investors, investment advisers, broker-dealers, securities salespeople, and
  small businesses raising capital
- Donors, charities, charitable sponsors, professional fundraisers, and
  disaster-relief donors
- Lobbyists, lobbyist principals, state agency liaisons, local government
  liaisons, legislators, appointed officials, journalists, watchdog groups, and
  voters tracking influence on government decisions
- Consumers targeted by securities fraud, charity scams, or misleading business
  mailings
- County registers of deeds, GIS offices, planners, surveyors, real estate
  professionals, title companies, and local governments
- Notaries, attorneys, lenders, banks, and people using authenticated documents
- Researchers, journalists, campaigns, and civic organizations using public
  registry data

### Completion checklist

- Export every public registry and identify data fields, update frequency, and
  search limits.
- Connect each filing type to the statute and administrative rule.
- Separate administrative filing duties from enforcement duties.
- Track fees, penalties, exemptions, and appeal rights.
- Add a lobbying-disclosure subtable for registrants, principals, liaisons,
  quarterly reports, monthly reports during session when required, complaint
  pathways, penalties, and searchable public directories.

## Office 4: State Auditor

### Core role and authority

The Office of the State Auditor is North Carolina's independent fiscal watchdog.
It audits more than $100 billion in state assets and liabilities each year,
investigates alleged fraud, waste, and abuse of taxpayer dollars, and issues
recommendations for government reform. Source:
<https://www.auditor.nc.gov/about-office-state-auditor>.

State law gives the Auditor broad audit and investigation authority over state
agencies and state employees, including access to records and authority to
receive reports through a hotline. Sources:
<https://www.ncleg.gov/enactedlegislation/statutes/pdf/bysection/chapter_147/gs_147-64.6.pdf>
and <https://www.auditor.nc.gov/tipline>.

### Divisions, audit types, and programs to map

- Financial statement audits
- Performance audits
- Information systems audits
- Investigative reports
- Rapid Response special reports
- Federal compliance and single-audit-related work where applicable
- Hotline and tip intake
- Peer reviews and quality assurance
- Legislative reporting and follow-up processes

Official audit type descriptions:
<https://www.auditor.nc.gov/auditsreports/types-audits>.

### Functions and jurisdictions

- Audits of state agencies, state universities, community colleges, and other
  units of state government
- Financial and compliance audits
- Performance audits of economy, efficiency, and program results
- Information systems risk and control audits
- Investigations of fraud, waste, abuse, mismanagement, illegal activity in
  state or federal program administration, and substantial danger to public
  health or safety within statutory authority
- Reports to the Governor, General Assembly, agencies, and the public
- Referral to law enforcement or other agencies where warranted

### Affected voter categories

- All taxpayers
- State employees and state agency leadership
- Public university and community college employees, students, and governing
  boards
- Public benefit recipients whose programs are audited
- Local governments and private entities receiving state or federal funds
  where audit authority reaches them
- Whistleblowers and tipline users
- Legislators and budget writers
- Bondholders and financial market stakeholders relying on credible financial
  reporting
- Communities affected by audited programs in education, health,
  transportation, public safety, technology, and regulatory systems

### Completion checklist

- Build a table of every audit report by agency, program, fiscal year, finding,
  recommendation, management response, and follow-up status.
- Map hotline categories to jurisdiction limits and referral destinations.
- Flag which local government issues belong to the Auditor, Local Government
  Commission, Attorney General, district attorney, or local board.
- Connect audits to appropriations, oversight committees, and agency corrective
  actions.

## Office 5: State Treasurer

### Core role and authority

The State Treasurer leads the Department of State Treasurer, whose mission
includes pension and health plan stewardship, investment and cash management,
financial operations, debt management, local government finance oversight, and
unclaimed property. Source: <https://www.nctreasurer.com/>.

### Divisions, agencies, and programs to map

The Treasurer's division page identifies:

- Financial Operations
- North Carolina Investment Authority
- Retirement Systems
- State and Local Government Finance
- State Health Plan
- Unclaimed Property Division

Source: <https://www.nctreasurer.com/divisions>.

Specific connected bodies and programs include:

- North Carolina Retirement Systems
- Teachers' and State Employees' Retirement System
- Local Governmental Employees' Retirement System
- Consolidated Judicial Retirement System
- Firefighters' and Rescue Squad Workers' Pension Fund
- Legislative Retirement System
- National Guard Pension Fund
- Supplemental Retirement Plans
- State Health Plan
- Local Government Commission
- State Board of Education ex officio membership
- State Board of Community Colleges ex officio membership or designee role
- Debt Affordability Advisory Committee
- North Carolina Capital Facilities Finance Agency
- Cash management and short-term investment fund
- Escheats and unclaimed property

### Functions and jurisdictions

- Manage or oversee public pension assets and retirement administration
- Preserve, protect, and sustain state pension and health plans
- Manage state operating funds and investment programs
- Properly account for funds deposited, invested, and disbursed through the
  Department
- Support state and local debt issuance
- Serve as chair of the Local Government Commission
- Serve as an ex officio member of the State Board of Education under Article
  IX, Section 4 of the North Carolina Constitution
- Serve, or designate a representative to serve, as an ex officio member of the
  State Board of Community Colleges under G.S. 115D-2.2
- Staff the LGC, which approves local government debt, sells local debt on
  behalf of local units, monitors fiscal health, oversees annual independent
  audits, and provides financial administration assistance
- Operate unclaimed property services
- Provide transparency reports, investment reports, financial reports, and
  board materials

Local Government Commission source:
<https://www.nctreasurer.com/state-and-local-government-finance-division/local-government-commission/about-local-government-commission>.

### Affected voter categories

- State employees, teachers, retirees, judges, legislators, firefighters,
  rescue squad workers, National Guard members, and local government employees
- State Health Plan members, dependents, providers, pharmacists, and taxpayers
  funding the plan
- County, municipal, utility, authority, and special district officials seeking
  debt approval
- Local taxpayers affected by debt, bond ratings, water and sewer financing,
  school construction, public buildings, and infrastructure finance
- Bondholders, rating agencies, financial advisers, underwriters, and banks
- People with unclaimed property or escheated funds
- State agencies and universities whose funds are invested or disbursed through
  state systems
- Legislators and oversight committees monitoring pension, debt, and health
  costs
- Public school students, parents, educators, and community college students
  affected by the Treasurer's ex officio education board roles

### Completion checklist

- Map every retirement system by membership category, governing board, assets,
  benefits, employer contribution rates, and statutory authority.
- Map every State Health Plan eligibility class and major vendor relationship.
- Inventory LGC actions by local unit, debt type, amount, approval status,
  repayment source, and affected geography.
- Track unclaimed property claim volumes, dollar amounts, and county-level
  distribution.

## Office 6: Superintendent of Public Instruction

### Core role and authority

The Superintendent of Public Instruction is the elected head of the Department
of Public Instruction and oversees the public school systems of the state. The
Superintendent is a Council of State member and serves as secretary and chief
administrative officer of the State Board of Education, rather than as a voting
State Board member. Sources: <https://www.dpi.nc.gov/about-dpi>,
<https://ncleg.gov/Laws/Constitution/Article9>, and
<https://ncleg.net/EnactedLegislation/Statutes/PDF/ByArticle/Chapter_115C/Article_3.pdf>.

NCDPI implements state public school laws for pre-kindergarten through 12th
grade public schools at the direction of the State Board of Education and the
Superintendent. NCDPI supports 115 local public school districts, more than
2,500 district public schools, more than 200 charter schools, lab schools, and a
regional school. It supports standards, accountability, finance, teacher and
administrator preparation and licensing, professional development, school
business support, and operations. It manages about $14 billion in state and
federal funds and oversees licensure of about 120,000 teachers and
administrators. Source: <https://www.dpi.nc.gov/about-dpi>.

### Divisions, boards, and programs to map

- Office of the State Superintendent
- State Board of Education secretary and chief administrative officer
  relationship
- Office of the State Board of Education
- Internal Audit
- Deputy Superintendent and agency executive leadership
- School Business Services
- Educator preparation and licensure
- Accountability and testing
- Standards and curriculum support
- Exceptional Children
- Federal programs
- Career and technical education
- District and Regional Support
- Center for Safer Schools
- NC Virtual Public School
- Charter school support and oversight processes
- Textbook and instructional materials adoption
- School connectivity and technology programs
- Public school budget allocations

Official DPI source: <https://www.dpi.nc.gov/about-dpi>.
State Board source: <https://www.dpi.nc.gov/about-dpi/state-board-education>.

### Functions and jurisdictions

- Implement public school laws and State Board policy
- Support every public school unit in the state
- Administer and distribute state and federal education funds
- Oversee educator licensure systems
- Support academic standards, accountability, assessments, and school
  improvement systems
- Provide district operations, finance, technology, and school business support
- Coordinate textbook and instructional materials processes
- Support school safety, connectivity, and targeted assistance to
  low-performing schools and districts
- Provide data, reports, and legislative information about public education

### Affected voter categories

- Public school students and families
- Teachers, principals, superintendents, district staff, and school support
  personnel
- Local boards of education and charter school boards
- County commissioners funding local school capital and operating needs
- Taxpayers funding state, local, and federal education programs
- Students with disabilities, English learners, low-income students, rural
  students, academically gifted students, and students in low-performing schools
- Employers affected by workforce preparation and career pathways
- Colleges and educator preparation programs
- Vendors providing textbooks, technology, transportation, food service, and
  school operations services

### Completion checklist

- Map every public school unit to county, legislative district, State Board
  region, and federal congressional district.
- Connect each state allotment and federal program to eligibility rules,
  recipient schools, affected students, and reporting obligations.
- Track board committee assignments, State Board policies, and Superintendent
  implementation duties.
- Link school board elections and county commission budget authority in the
  later local-office expansion.

## Office 7: Attorney General

### Core role and authority

The Attorney General heads the Department of Justice. The office represents all
state government departments, agencies, and commissions in legal matters;
provides legal opinions to the General Assembly, Governor, and public officials
when requested; consults with judges, district attorneys, magistrates, and local
government attorneys when permitted; may intervene in proceedings on behalf of
the State; may institute proceedings in public interest matters; and handles all
criminal appeals from state trial courts. Source:
<https://ncdoj.gov/about-ncdoj/duties-and-responsibilities/>.

The Attorney General does not generally prosecute specific crimes unless
requested by the local district attorney, does not have authority over local
district attorneys, local law enforcement, or courts, and generally cannot
provide legal advice to private individuals or organizations. Source:
<https://ncdoj.gov/about-ncdoj/duties-and-responsibilities/>.

### Divisions, programs, and bodies to map

- Civil Bureau
- Criminal Bureau
- Consumer Protection Division
- Medicaid Investigations Division
- Public Protection Section
- Environmental Division
- North Carolina State Crime Lab
- North Carolina Justice Academy
- Sheriffs' Education and Training Standards Commission
- Criminal Justice Education and Training Standards Commission
- Law enforcement training and standards functions
- Open government, internet safety, opioid, robocall, scams, and other public
  education initiatives

Source overview: <https://ncdoj.gov/about-ncdoj/>.

### Functions and jurisdictions

- Legal representation for state departments, agencies, and commissions
- Criminal appeals
- Consumer fraud investigation and enforcement
- Medicaid provider fraud and patient abuse investigations and prosecutions
  through the Medicaid Investigations Division
- Environmental legal enforcement and representation
- State Crime Lab evidence analysis
- Law enforcement training through the Justice Academy
- Standards and certification oversight through connected commissions
- Legal opinions and advice to public officials within the law
- Public interest litigation
- Victim, survivor, and public safety policy support

### Affected voter categories

- All residents affected by state legal positions and public interest matters
- Consumers, seniors, scam victims, and fraud victims
- Businesses subject to consumer protection, antitrust, privacy, or fraud
  enforcement
- Medicaid patients, providers, caregivers, and taxpayers
- Crime victims, defendants, district attorneys, sheriffs, police departments,
  magistrates, judges, and local governments
- Law enforcement officers seeking training or certification
- State agencies requiring legal representation
- Environmental justice communities, coastal communities, and people affected by
  air, water, and land enforcement
- Nonprofits and advocacy groups involved in public interest cases

### Completion checklist

- Separate statewide legal authority from local prosecutorial authority.
- Map every DOJ division to its statutory authority, client agencies,
  enforcement remedies, and public complaint pathways.
- Inventory consumer complaint categories and enforcement outcomes.
- Connect Justice Academy and standards commission decisions to every sheriff,
  police department, detention officer, telecommunicator, and training academy
  affected.

## Office 8: Commissioner of Agriculture

### Core role and authority

The Commissioner of Agriculture leads the Department of Agriculture and Consumer
Services. The Commissioner is a constitutional officer, a Council of State
member, and is in charge of a department with 20 divisions and more than 2,000
employees. The department implements more than 75 laws and programs and covers
regulatory and service areas including agronomy, animal health, weights and
measures, gas and oil inspection, statistics, food distribution, state farm
operations, food and drug testing, marketing, grading, international marketing,
state fairs, farmers markets, research stations, seed and fertilizer
inspection, plant pest eradication, structural pest control, environmental
issues, soil and water conservation, forest promotion and protection, federal
and state agricultural legislation, and agricultural economic analysis. Source:
<https://www.ncagr.gov/about-ncdacs/commissioner-agriculture/role-commissioner>.

### Divisions and programs to map

Official division source: <https://www.ncagr.gov/divisions>.

Map at minimum:

- Agricultural Statistics
- Agronomic Services
- Budget and Finance
- Environmental Programs
- Food Distribution
- Food and Drug Protection
- Marketing
- Meat and Poultry Inspection
- Plant Industry
- Property and Construction
- Public Affairs
- Research Stations
- Standards
- Structural Pest Control and Pesticides
- Veterinary
- Emergency Programs
- Animal Welfare
- State Fair and Mountain State Fair
- Farmers markets and agricultural centers
- Soil and Water Conservation
- N.C. Forest Service and forest protection programs where under NCDA&CS
- Farmland preservation and agricultural development programs

### Functions and jurisdictions

- Agricultural production support and technical assistance
- Food safety and inspection functions
- Meat and poultry inspection
- Animal health, livestock disease surveillance, testing, and movement
  regulation
- Plant pest, nursery, seed, fertilizer, pesticide, and structural pest control
  regulation
- Weights and measures, package quantity, motor fuel quality, and LP gas
  inspection
- Agricultural statistics and market information
- Domestic and international marketing of North Carolina agricultural products
- Operation of farmers markets, fairs, research stations, and agricultural
  centers
- Soil testing, plant tissue analysis, nematode testing, waste analysis, and
  agronomic recommendations
- Forestry, soil, water, and environmental programs where assigned
- Disaster and agricultural emergency response coordination

### Affected voter categories

- Farmers, ranchers, foresters, nursery operators, beekeepers, livestock
  owners, aquaculture operators, and agribusinesses
- Rural residents, landowners, farm families, and migrant or seasonal
  farmworkers
- Consumers buying food, fuel, pesticides, seed, fertilizer, and measured goods
- Grocery stores, restaurants, processors, distributors, farmers markets, and
  food manufacturers
- Veterinarians, animal shelters, kennels, livestock markets, fairs, and animal
  owners
- Pesticide applicators, pest control businesses, landscapers, nurseries, and
  homeowners
- Drivers and businesses affected by fuel quality and weighing or measuring
  devices
- Forestland owners, communities at wildfire risk, and conservation districts
- Students and families participating in fairs, agricultural education, and
  nutrition programs

### Completion checklist

- Build a division-by-division table of licenses, permits, inspections, tests,
  grants, reports, enforcement actions, and public services.
- Map agricultural programs by county, commodity, watershed, forest district,
  farmers market region, and disaster risk.
- Link every regulated product category to statutes, rules, fees, inspection
  cycles, and complaint pathways.
- Include separate tracking for consumers, producers, processors, and
  intermediaries because the same program may affect them differently.

## Office 9: Commissioner of Insurance

### Core role and authority

The Commissioner of Insurance leads the Department of Insurance. The department
regulates the insurance industry, handles insurance-related complaints, licenses
insurance agents, adjusters, bail bondsmen and other licensees, provides
Medicare counseling, oversees motor clubs and collection agencies, and
investigates insurance fraud. Source: <https://www.ncdoi.gov/about-doi>.

North Carolina has had recent statutory changes involving the Office of State
Fire Marshal. Current mapping should treat Department of Insurance functions
and Office of State Fire Marshal functions as separate records unless the
current statute and official agency pages show a direct reporting relationship.
Current OSFM public information is available at <https://www.ncosfm.gov/>.

### Divisions, programs, and regulated areas to map

From official DOI contact and program pages, map:

- Office of the Commissioner
- Consumer Services
- Seniors' Health Insurance Information Program
- Smart NC or health insurance appeals support
- Agent Services
- Actuarial Services
- Bail Bond Regulatory
- Captive Insurance Companies
- Continuing Care Retirement Communities
- Criminal Investigations
- Financial Analysis and Receivership
- Financial Examination
- Individual Self-Insured Workers Compensation
- Legislative Services
- Life and Health
- Market Regulation
- Professional Employer Organizations
- Property and Casualty
- Regional offices
- Public Information Office
- Company licensing and rates
- Service of legal process
- Insurance fraud reporting

Sources:
<https://www.ncdoi.gov/contact/contact-ncdoi>,
<https://www.ncdoi.gov/insurance-industry/market-regulation>, and
<https://www.ncdoi.gov/assistance-or-file-complaint>.

### Functions and jurisdictions

- Regulate insurance companies and insurance markets
- Review rates, forms, solvency, market conduct, and company compliance
- License and discipline insurance producers, adjusters, bail bondsmen, and
  related professionals
- Investigate insurance fraud and insurance-related financial crimes
- Receive and process consumer complaints
- Educate consumers about auto, homeowners, renters, health, life, disability,
  long-term care, Medicare supplement, dental, vision, and other coverages
- Support Medicare beneficiaries through SHIIP
- Review market disruptions through market analysis and market conduct exams
- Oversee specified non-insurance regulated sectors such as motor clubs,
  collection agencies, premium finance, and related entities where statutes
  assign responsibility

### Affected voter categories

- Insurance consumers: auto, homeowners, renters, health, life, disability,
  dental, vision, long-term care, Medicare supplement, and other policyholders
- Medicare beneficiaries, seniors, caregivers, and SHIIP volunteers
- Insurance agents, adjusters, bail bondsmen, companies, HMOs, PPOs, premium
  finance companies, motor clubs, collection agencies, and professional
  employer organizations
- Homeowners, renters, drivers, coastal residents, flood-prone communities, and
  disaster survivors affected by insurance availability and rates
- Patients, providers, employers, and employees affected by health coverage
  disputes
- Businesses affected by workers compensation, liability, and commercial
  insurance markets
- Consumers and businesses affected by insurance fraud
- Local governments and emergency-service communities where OSFM or fire code
  issues intersect, subject to separate statutory verification

### Completion checklist

- Separate DOI, OSFM, Building Code Council, fire, manufactured building,
  pyrotechnic, home inspector, and code official functions according to current
  law and official reporting lines.
- Map every license type, regulated entity, complaint type, examination type,
  rate review process, and appeal path.
- Capture market regulation data by line of insurance and company type.
- Link insurance functions to disaster risk, coastal rating territories,
  affordability, and consumer-protection outcomes.

## Office 10: Commissioner of Labor

### Core role and authority

The Commissioner of Labor leads the Department of Labor. The department's
divisions and bureaus carry out regulatory, enforcement, inspection,
consultation, education, and informational programs affecting workplace safety,
wage and hour, boiler safety, elevators, amusement devices, mines and quarries,
retaliatory employment discrimination, and related labor laws. Sources:
<https://www.labor.nc.gov/about-ncdol/divisions> and
<https://www.labor.nc.gov/rules-and-regulations>.

### Divisions and bureaus to map

Official division source: <https://www.labor.nc.gov/about-ncdol/divisions>.

- Administration Division
  - Communications
  - Financial Services
  - Governmental Affairs
  - Human Resources
  - General Counsel
  - Research and Policy
  - Information Technology
- Occupational Safety and Health Division
  - Agricultural Safety and Health
  - East Compliance
  - West Compliance
  - Consultative Services
  - Education, Training and Technical Assistance
  - Planning, Statistics and Information Management
- Standards and Inspections Division
  - Boiler Safety
  - Elevator and Amusement Device
  - Retaliatory Employment Discrimination
  - Mine and Quarry
  - Wage and Hour
- State Board of Community Colleges ex officio membership or designee role
  under G.S. 115D-2.2:
  <https://ncleg.gov/enactedlegislation/statutes/pdf/bysection/chapter_115d/gs_115d-2.2.pdf>

### Functions and jurisdictions

- Enforce the Occupational Safety and Health Act in private sector and state and
  local government workplaces
- Conduct workplace safety and health inspections, complaint investigations,
  accident and fatality investigations, programmed inspections, follow-up
  inspections, and agricultural safety inspections
- Provide free consultative services to employers
- Provide education, training, technical assistance, rules interpretation, and
  recognition programs
- Collect and manage labor and inspection statistics
- Enforce wage payment, minimum wage, maximum hours where applicable, youth
  employment, and related wage and hour rules
- Inspect and regulate boilers and pressure vessels
- Inspect and regulate elevators, escalators, moving walks, aerial tramways,
  amusement rides, and related devices within jurisdiction
- Regulate mine and quarry safety and training
- Investigate retaliation complaints under protected labor and safety statutes
- Serve, or designate a representative to serve, as an ex officio member of the
  State Board of Community Colleges, connecting labor, workforce training,
  apprenticeships, and community college policy

### Affected voter categories

- Private-sector workers and employers
- State and local government employees and public employers
- Farmworkers, migrant housing residents, and agricultural employers
- Construction workers, manufacturing workers, health care workers, food
  processing workers, warehouse workers, logging and arboriculture workers,
  miners, quarry workers, and other high-risk occupations
- Youth workers and parents of minors seeking employment
- Employees with unpaid wage claims
- Employers seeking consultation, training, or recognition
- Building owners, tenants, elevator users, amusement ride patrons, and event
  operators
- Boiler and pressure vessel owners and operators
- Retaliation complainants and whistleblowers
- Local governments and schools operating public workplaces and facilities
- Community college students, faculty, trustees, employers, and workforce
  partners affected by the Commissioner's ex officio community college board
  role

### Completion checklist

- Map every bureau to acts enforced, administrative rules, inspection objects,
  complaint intake processes, penalties, appeals, and exemptions.
- Build a county-level and industry-level workplace risk layer using inspection,
  injury, fatality, and consultation data.
- Separate worker rights, employer obligations, public education, and
  enforcement actions.
- Link labor programs to local economic sectors and vulnerable worker
  populations.

## Required downstream expansion beyond Council of State

The user's full target includes every elective political office in North
Carolina, including federal, state, local, municipal, county, township,
judicial, sheriff, city council, county commission, and school board offices.
After the Council of State map is complete, expand using the same schema in the
following order.

### Phase 2: Federal, state legislative, and judicial offices

- U.S. Senate and U.S. House districts touching North Carolina
- Governor and Council of State completed in Phase 1
- North Carolina Senate districts
- North Carolina House districts
- Supreme Court
- Court of Appeals
- Superior Court judges
- District Court judges
- District attorneys
- Clerks of Superior Court

Fields to add:

- Committees and subcommittees
- Legislative leadership roles
- Appropriations and policy jurisdiction
- Judicial district geography
- Court administration roles
- Prosecutorial district geography
- Case types and affected litigants

### Phase 3: County offices across all 100 counties

Map for every county:

- Board of Commissioners
- Sheriff
- Register of Deeds
- County Board of Education where elected
- Soil and Water Conservation District supervisors
- County-level judicial and court offices where elected
- Any elected tax collector, surveyor, coroner, or legacy office where
  applicable

Fields to add:

- County departments governed or funded
- Budget and tax authority
- Jail, detention, law enforcement, and emergency management authority
- Public health, social services, parks, libraries, planning, zoning, water,
  sewer, solid waste, and economic development roles
- Board committees and appointments
- Interlocal agreements

### Phase 4: Municipal offices

Map for every municipality:

- Mayor
- City council, town council, board of aldermen, or village council
- Municipal school board where applicable
- Municipal judges or other local offices where applicable

Fields to add:

- Form of government
- Ward or at-large election method
- Planning and zoning authority
- Police, fire, utilities, streets, sanitation, parks, housing, and development
  authority
- Boards, commissions, and advisory committees
- Extraterritorial jurisdiction where applicable
- Municipal budget and tax authority

### Phase 5: School boards and education governance

Map:

- Local boards of education
- Charter school governing boards where public accountability applies
- Community college boards of trustees
- State Board of Education
- Superintendent and DPI links

Fields to add:

- Attendance zones
- Capital funding relationships with counties
- Student assignment
- Curriculum implementation
- Personnel policy
- School closure, construction, transportation, and nutrition authority

## Research workflow

1. Create a master office inventory.
2. Assign every elected office a stable ID.
3. Attach geography using official district, county, municipal, precinct,
   school, and judicial boundary data.
4. Attach authority using constitution, statutes, administrative code, local
   charters, ordinances, board bylaws, and official agency pages.
5. Attach organization structure using official org charts, division pages,
   board rosters, budget documents, and annual reports.
6. Attach functions and programs using agency service pages, budget codes,
   grant lists, licensing databases, inspection programs, audit reports, and
   regulatory filings.
7. Attach voter categories using the taxonomy in this document.
8. Add source URLs and last-verified dates.
9. Flag uncertainty when authority is shared, delegated, advisory, limited by
   statute, or recently reorganized.
10. Review each office with subject-matter checks for legal accuracy, geographic
    accuracy, data completeness, and constituency coverage.

## Minimum completeness standard

An office is complete only when it has:

- Constitutional or statutory authority identified
- Jurisdiction geography identified
- Election cycle and term identified
- Department or governing body structure identified
- Divisions, boards, committees, or subunits identified
- Budget or fiscal authority identified
- Regulatory, licensing, inspection, audit, legal, appointment, or enforcement
  authority identified, or explicitly marked not applicable
- Public services identified
- Limits on authority identified
- At least one official source URL per core claim
- All affected voter categories tagged
- County, municipal, district, or statewide geography attached
- Last verified date recorded

## Data products to build from this Markdown task

1. `offices`: one row per elected office.
2. `jurisdictions`: one row per geography or district.
3. `office_jurisdictions`: many-to-many office-to-geography table.
4. `authorities`: constitutional, statutory, administrative, charter, ordinance,
   or policy authority records.
5. `agencies`: departments, boards, commissions, and offices.
6. `divisions`: divisions, bureaus, sections, units, and programs.
7. `functions`: services, rules, inspections, audits, grants, enforcement,
   appointments, hearings, reports, and public records.
8. `constituencies`: standardized affected voter and population categories.
9. `office_constituencies`: many-to-many office-to-constituency tags.
10. `sources`: official URLs and metadata.
11. `uncertainties`: unresolved authority, jurisdiction, or source questions.

## Quality controls

- Prefer official government sources over secondary summaries.
- Record whether an office directly controls, appoints, funds, advises,
  regulates, audits, litigates, or merely influences a function.
- Do not merge legally distinct authorities just because one elected official
  participates in both.
- Separate statewide authority from county, municipal, school, judicial, and
  special-district authority.
- Separate elected authority from appointed board authority.
- Track current law because reorganizations can move functions between
  departments.
- Preserve local variation: county and municipal offices often differ by
  charter, local act, board policy, or election method.
- Include vulnerable and indirectly affected constituencies, not only regulated
  entities.

## Immediate next actions

1. Convert the Council of State sections above into a structured spreadsheet or
   database seed file.
2. For each office, collect the current official org chart and division list.
3. For each division, list programs, laws enforced, regulated entities,
   services, fees, boards, reports, and public datasets.
4. Add geography and constituency tags.
5. Review each office with official statute and administrative code citations.
6. Repeat the schema for state legislative offices, judicial offices, all 100
   county governments, municipalities, school boards, sheriffs, and special
   districts.
