# Data Dictionary — FARS Drunk Driving Analysis (2015–2016)

## FARS_StateSummary_2015_2016.csv
*State-level aggregated summary — 102 rows (51 states × 2 years)*

| Field | Type | Description |
|-------|------|-------------|
| state_name | string | US state name |
| year | integer | Year (2015 or 2016) |
| total_crashes | integer | Total fatal crashes in state/year |
| total_fatalities | integer | Total fatalities in all crashes |
| drunk_crashes | integer | Crashes involving at least one drunk driver |
| drunk_fatalities | integer | Fatalities in drunk driving crashes |
| pct_drunk | float | % of crashes involving drunk driver |
| population | integer | State population (US Census) |
| drunk_fatalities_per_100k | float | Drunk fatalities per 100,000 population |
| predominant_road_type | string | Most common road type for fatal crashes in state |

---

## FARS_CountySummary_2015_2016.csv
*County-level aggregated summary — 2,855 rows*

| Field | Type | Description |
|-------|------|-------------|
| state_name | string | US state name |
| county | string | County name (FIPS codes stripped) |
| year | integer | Year (2015 or 2016) |
| total_crashes | integer | Total fatal crashes in county/year |
| total_fatalities | integer | Total fatalities |
| drunk_crashes | integer | Crashes involving drunk driver |
| drunk_fatalities | integer | Fatalities in drunk driving crashes |
| avg_lat | float | Average latitude of crashes in county (for bubble map placement) |
| avg_lon | float | Average longitude of crashes in county |
| pct_drunk | float | % of crashes involving drunk driver |

---

## FARS_CrashDetail_2015_2016.csv
*Individual crash-level records — 18,130 rows (drunk driving crashes only)*

| Field | Type | Description |
|-------|------|-------------|
| consecutive_number | integer | FARS unique crash identifier |
| year | integer | Year (2015 or 2016) |
| latitude | float | Crash latitude (jittered ±0.001° for visualization) |
| longitude | float | Crash longitude (jittered ±0.001° for visualization) |
| state_name | string | US state name |
| county | string | County name (may be null if not reported in FARS) |
| hour_of_crash | integer | Hour of crash (0–23) |
| time_period | string | Bucketed time: Late Night / Morning / Afternoon / Evening |
| day_name | string | Day of week (Sunday–Saturday) |
| weekend_label | string | Weekend or Weekday |
| month | integer | Month of crash (1–12) |
| number_of_fatalities | integer | Number of fatalities in crash |
| number_of_drunk_drivers | integer | Number of drunk drivers involved |
| junction_type | string | Crash location relative to junction |
| road_type | string | Functional classification of road |
| land_use | string | Urban or Rural |
| collision_type | string | Manner of collision |
| light_condition | string | Light conditions at time of crash |
| weather | string | Weather conditions at time of crash |
| work_zone | string | Whether crash occurred in work zone |
| no_seatbelt | string | Yes/No — any driver wore no seatbelt (from person table) |
| avg_driver_age | float | Average age of drivers involved |
| has_prior_dwi | string | Yes/No — any driver had prior DWI conviction (from vehicle table) |
| has_prior_susp | string | Yes/No — any driver had prior license suspension |
| invalid_license | string | Yes/No — any driver had invalid or no license |
| speeding_involved | string | Yes/No — speeding was a contributing factor |

---

## Notes

- **County null rate:** ~16% of crash records have no county name in the raw FARS data
- **Coordinate jitter:** Latitude/longitude jittered by ±0.001° to visually separate overlapping dots
- **Seatbelt/risk factor source:** Derived from person and vehicle tables (2015–2016 only)
- **Continental US filter:** Records outside lat(24–50) / lon(-125 to -65) excluded
