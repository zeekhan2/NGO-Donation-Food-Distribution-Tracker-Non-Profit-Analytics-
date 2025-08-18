# Data Dictionary

## locations.csv
- location_id: integer, primary key
- location_name: string (Peshawar, Charsadda, Mardan, Swat, Nowshera, Khyber)
- area_type: string (Urban/Rural)

## donors.csv
- donor_id: integer, primary key
- donor_name: string
- donor_type: string (Individual, Corporate, International Org, Local Org)
- city: string

## beneficiaries.csv
- beneficiary_id: integer, primary key
- household_size: integer (2–7)
- vulnerability: string (Low/Medium/High)

## donations.csv
- donation_id: integer, primary key
- donor_id: integer, foreign key -> donors
- donation_date: date
- donation_type: string (Cash, In-Kind)
- channel: string (Bank, Online, Cash)
- amount_usd: float — cash or estimated in-kind value

## distributions.csv
- distribution_id: integer, primary key
- distribution_date: date
- location_id: integer, foreign key -> locations
- beneficiary_id: integer, foreign key -> beneficiaries
- item_category: string (Rice, Flour, Pulses, Oil, Hygiene Kit, Water, Medicine Pack)
- quantity: float (kg/L or unit count for kits/packs)
- est_value_usd: float — estimated aid value
