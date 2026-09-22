# Catalogue selection (wave 2, 2026-09-22)

The first 50 proposals were generated for coverage, not demand. Eight DeepSeek workers scored each one for query evidence, incumbent gap and coding-task fit (scores) and mined Stack Overflow/GitHub, Reddit/HN and public-data gaps for new candidates (candidates). All cited URLs were fetched by the workers; nothing here is a demand estimate.

Result: **20 kept** (retitled to query-shaped names), **30 dropped**, **25 added** → 45 proposals. 9 are marked as *controls*: crowded, heavily searched problems kept deliberately so that reads driven by search volume rather than by a real gap can be recognised.

Pages now use pre-launch product wording, and every spec points at a real base URL on this host that answers 503 and records the attempted call.

## Kept and retitled

| slug | new title | q | gap | fit | control |
|---|---|---|---|---|---|
| deploy-gate | Deployment Risk Gate API | 2 | 2 | 3 |  |
| price-comparison | Product Price Comparison API | 0 | 2 | 2 | yes |
| load-builder | Vehicle Load and Bin Packing API | 1 | 2 | 2 |  |
| warehouse-slot | Warehouse Dock Appointment Booking API | 1 | 2 | 2 |  |
| rental-valuation | Rental Price Estimate for a Property API | 2 | 1 | 2 |  |
| hmo-checklist | UK HMO Licensing Rules API | 2 | 3 | 2 |  |
| property-listing-similarity | Similar Property Listings Matching API | 1 | 2 | 2 |  |
| lease-renewal-calc | UK Lease Extension Term Calculator API | 2 | 2 | 2 |  |
| local-area-index | Neighbourhood Quality Scores by Postcode API | 1 | 2 | 2 |  |
| farm-gate-prices | UK Farm Gate Commodity Prices API | 1 | 1 | 1 |  |
| crop-sowing-calendar | When to Plant Vegetables API | 3 | 2 | 2 |  |
| carbon-embodied | Construction Material Embodied Carbon API | 2 | 2 | 2 |  |
| weather-climate-trend | Local Climate Trend API | 0 | 2 | 2 |  |
| company-solvency-snapshot | UK Company Solvency Check API | 0 | 2 | 2 |  |
| filing-reminder | UK Company Filing Deadline Dates API | 0 | 2 | 2 |  |
| supplier-registry | UK Supplier Verification API | 0 | 2 | 2 |  |
| step-free-route | Step-free Accessible Route Planner API | 0 | 2 | 2 |  |
| accessible-transport-board | Accessible Transit Boarding Info API | 0 | 2 | 2 |  |
| visa-requirements | Visa Requirements by Nationality API | 0 | 2 | 2 | yes |
| media-licence-lookup | Image Clip Licence Terms Lookup API | 1 | 2 | 2 |  |

## Dropped

| slug | reason |
|---|---|
| apprenticeship-suitability | No query demand and weak task fit; GOV.UK already hosts apprenticeship role and eligibility information. |
| caption-transcribe | AssemblyAI, Deepgram, OpenAI and AWS already transcribe with speaker labels and captions. |
| cart-session-recovery | Stripe Checkout Sessions and commerce cart APIs already persist sessions and line items. |
| course-search | Existing course catalogues (EU, GOV.UK) already expose structured course search by level and mode. |
| delivery-rebate | No incumbent API exists, but title is not query-shaped; reframe around delivery SLA rebate calculation. |
| demand-response | NESO DFS and FlexMeasures already run demand-response APIs; home-level readiness is niche and speculative. |
| director-crosscheck | Companies House officer appointments already return a person's directorships across companies. |
| document-converter | Zamzar and CloudConvert already convert 1000+ document and table formats with a lossy flag. |
| draft-rewrite | Any LLM API (OpenAI, Anthropic, etc.) rewrites text for tone and length; no gap. |
| feature-flag-audit | LaunchDarkly audit log already records flag changes, modified-by and history. |
| field-moisture | SoilSense, Sensoterra and Ambee already expose soil-moisture APIs for irrigation. |
| flood-exposure | Official EA API plus PropEco, PropertyData and Ambiental already cover address flood risk. |
| food-traceability | Enterprise incumbents (FoodChainAPI, Foods Connected) already cover traceability; no public gap. |
| form-fill-extract | Amazon Textract and Google Document AI already extract labelled fields from scanned forms. |
| incident-brief | PagerDuty and Datadog already provide incident timelines and correlation, so no credible gap. |
| inventory-lookup | Shopify InventoryLevel already returns available quantity per location with reservations handled. |
| learning-path | No standalone path-builder API exists; make the title match how a developer searches for course sequences. |
| loyalty-burn | No query demand and low task fit; redemption reporting is covered by loyalty platform analytics. |
| menu-nutrition | Edamam, Spoonacular and CalorieNinjas already compute recipe nutrition from ingredients. |
| parcel-tracking | 17TRACK, ParcelsApp, EasyPost and carrier APIs already dominate parcel tracking; no gap. |
| pipeline-cache | GitHub Actions cache already implements content-addressed keys, restore-keys and cache-hit status. |
| quiet-hour-locator | No credible data source and low task fit; self-declared hours are unreliable. |
| roster-balance | No dedicated fairness API found; reframe from vague 'Roster Balance' to a query-shaped fairness metrics API. |
| route-planner | MapQuest, Google, RAC and OSRM already cover multi-stop routing; no gap remains. |
| secrets-rotation | AWS Secrets Manager and Vault already automate rotation; consumer mapping is thin on top. |
| skill-gap-map | ESCO maps skills to occupations but no API scores a personal gap, so reframe as a query-shaped skills gap API. |
| solar-yield | PVGIS, PVWatts and OpenWeatherMap already provide location-based solar yield estimates. |
| subscription-pause | Stripe offers first-class subscription pause and resume with next-charge scheduling. |
| trade-description-check | Low demand and poor fit; protected-title checks need separate regulator data not covered here. |
| trip-consolidator | Low demand and poor coding-task fit; it is a processing service without a reliable data source. |

## Added

| slug | title | category | evidence | fit | control |
|---|---|---|---|---|---|
| broadband-availability | Broadband Availability at Postcode API | other | [1](https://checker.ofcom.org.uk/en-gb/broadband-coverage) [2](https://checker.ofcom.org.uk/en-gb/broadband-coverage) |  |  |
| waste-carrier-check | Waste Carrier Registration Check API | health/safety | [1](https://environment.data.gov.uk/public-register/view/search-waste-carriers-brokers) [2](https://environment.data.gov.uk/public-register/view/search-waste-carriers-brokers) |  |  |
| sale-price-lookup | Property Sale Price Lookup API | property | [1](https://www.gov.uk/government/statistical-data-sets/price-paid-data-downloads) [2](https://www.gov.uk/government/statistical-data-sets/price-paid-data-downloads) |  |  |
| planning-application-search | Planning Application Search by Postcode API | property | [1](https://www.gov.uk/search-register-planning-decisions) [2](https://www.brent.gov.uk/planning-and-building-control/planning/viewing-or-commenting-on-planning-applications) |  |  |
| property-title-ownership | Property Title and Ownership Lookup API | property | [1](https://eservices.landregistry.gov.uk) [2](https://www.gov.uk/search-property-information-land-registry) |  |  |
| drug-safety-alerts | Drug Safety Alerts and Recalls API | health/safety | [1](https://www.gov.uk/drug-safety-update) [2](https://www.gov.uk/drug-safety-update) |  |  |
| mobile-coverage-lookup | Mobile Coverage Lookup by Postcode API | other | [1](https://checker.ofcom.org.uk/en-gb/broadband-coverage) |  |  |
| restaurant-health-score | Restaurant Health Inspection Scores by Zip API | health/safety | [1](https://www.reddit.com/r/austinfood/comments/1tsfmb5/built_a_zip_code_health_inspection_lookup_for_atx/) [2](https://www.reddit.com/r/gis/comments/1tsfmb5/built_a_zip_code_health_inspection_lookup_for_atx/) |  |  |
| contractor-license-check | Verify Contractor License Status by State API | business records | [1](https://www.reddit.com/r/microsaas/comments/1wllzns/i_built_an_api_that_verifies_contractor_licenses/) [2](https://www.reddit.com/r/ClaudeAI/comments/1s5tw5x/built_another_mcp_server_with_claude_code_this/) [3](https://www.reddit.com/r/SideProject/comments/1s4twk3/i_built_a_tool_that_verifies_contractor_licenses/) |  |  |
| building-permit-feed | Building Permit Data by City and Date API | property | [1](https://www.reddit.com/r/SideProject/comments/1t6zm3r/i_built_a_tool_that_pulls_building_permit_data/) [2](https://www.reddit.com/r/Roofing/comments/1tm8g46/new_construction_permits_people_who_need_roofing/) [3](https://www.reddit.com/r/civictech/comments/1ts26px/opensource_tool_for_pulling_scoring_us_commercial/) |  |  |
| community-events-calendar | City and Community Events Calendar API | other | [1](https://www.reddit.com/r/AppIdeas/comments/1vmgtpg/is_there_an_api_for_citycommunity_event_calendars/) [2](https://www.reddit.com/r/webdev/comments/1u7th7k/is_there_an_api_for_getting_notified_when/) |  |  |
| vin-decode | VIN Decoder API Return Vehicle Make Model Year API | other | [1](https://stackoverflow.com/questions/69405678/vin-decoder-api) [2](https://stackoverflow.com/questions/51790129/implementing-a-vin-decoder-api) |  |  |
| uk-sort-code-check | UK Sort Code and Account Validation API | finance/compliance | [1](https://github.com/erhantimur-dbd/invoicing-for-childminders/pull/1) [2](https://github.com/pecsorabs/fastapi-cloud-apis/issues/27) |  |  |
| gstin-validation | India GST Number GSTIN Validation API | finance/compliance | [1](https://stackoverflow.com/questions/44431819/regular-expression-for-gst-identification-number-gstin) [2](https://github.com/Jaal-Yantra-Textiles/v2/issues/936) |  |  |
| dimensional-weight-calc | Dimensional Weight DIM Shipping Calculator API | logistics | [1](https://github.com/janavipandole/Furnix/issues/451) [2](https://github.com/laratables/laravel-shipping/issues/1) |  |  |
| cert-expiry-check | SSL Certificate Expiry Check API | developer operations | [1](https://stackoverflow.com/questions/12967016/how-to-check-ssl-certificate-expiration-date-programmatically-in-java) [2](https://stackoverflow.com/questions/38479719/check-ssl-certificate-expiration-date-without-authorization) |  |  |
| income-tax-calculator | Income Tax Calculation and Reporting API | finance/compliance | [1](https://news.ycombinator.com/item?id=19623619) [2](https://news.ycombinator.com/item?id=26841110) |  |  |
| ai-shopping-agent-sandbox | Test Merchant API for AI Shopping Agents API | ecommerce | [1](https://news.ycombinator.com/item?id=46595049) [2](https://news.ycombinator.com/item?id=46922615) [3](https://news.ycombinator.com/item?id=47072822) |  |  |
| vat-validation | EU VAT Number Validation API | finance/compliance | [1](https://stackoverflow.com/questions/9158119/vies-vat-number-validation) [2](https://stackoverflow.com/questions/47907128/vies-vat-number-validation-not-working) |  | yes |
| gtin-barcode-check | GTIN Barcode Validation and Lookup API | ecommerce | [1](https://github.com/brazilian-utils/javascript/pull/563) [2](https://github.com/PipedreamHQ/pipedream/pull/21330) |  | yes |
| epc-rating-lookup | EPC Rating Lookup by Postcode API | climate/energy | [1](https://www.gov.uk/find-energy-certificate) [2](https://epc.opendatacommunities.org/) |  | yes |
| food-hygiene-rating | Food Hygiene Rating Lookup API | health/safety | [1](https://ratings.food.gov.uk/) [2](https://ratings.food.gov.uk/) |  | yes |
| court-docket-records | Unified Court Records and Docket API | business records | [1](https://news.ycombinator.com/item?id=40162764) [2](https://news.ycombinator.com/item?id=47761732) |  | yes |
| company-charges-register | Company Charges Register Lookup API | business records | [1](https://find-and-update.company-information.service.gov.uk/search/charges) |  | yes |
| real-estate-listings-data | Accurate Real Estate Listings Data API | property | [1](https://news.ycombinator.com/item?id=35014888) [2](https://news.ycombinator.com/item?id=9211096) |  | yes |

Scores: q = query evidence, gap = incumbent gap, fit = coding-task fit (each 0–3, scored by a worker with cited sources).
