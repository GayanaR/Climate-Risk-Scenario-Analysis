# Climate-Risk-Scenario-Analysis
Climate Risk Scenario Analysis for Global Manufacturing Operations aligned with TCFD 

# Climate Risk Scenario Analysis for Global Manufacturing Operations

## Project Overview

**Client/Organization**: \[Confidential or Client Name]
**Industry**: Manufacturing
**Duration**: Jan 2024 – Apr 2025
**Standards Alignment**: TCFD, SBTi, IPCC AR6, IEA NZE 2050, NGFS Scenarios (2023)

This project assessed the exposure of a global manufacturing portfolio to climate-related risks across 12 facilities in North America (Gulf Coast Plant - USA, Mexico Facility - Mexico), Europe (Barcelona Hub - Spain), and Southeast Asia (Hanoi Facility - Vietnam, Manila Plant - Philippines, Mumbai Works - India), along with seven other globally distributed strategic sites. We used dual climate pathways—+1.5°C (orderly transition) and +4°C (hot house world)—to evaluate physical and transition risks.

## Scope & Methodology

### Climate Scenario Frameworks

* **IPCC AR6 (RCP8.5, SSP2-4.5, SSP1-2.6)**: For regional projections on physical hazards
* **IEA Net Zero Emissions by 2050 (NZE 2050)**: For energy transition trajectories and fossil fuel phase-outs
* **NGFS Climate Scenarios (2023)**: Used 'Disorderly', 'Orderly', and 'Hot House World' to evaluate financial and policy-driven impacts

### Facilities Assessed

Selection criteria:

* Contribution to global production revenue
* Exposure to geographically-specific climate hazards
* Criticality in upstream/downstream supply chain
* Diversity in energy mix and regulatory contexts

### Climate Risk Types Assessed

| Risk Category   | Specific Risk Drivers                                                        |
| --------------- | ---------------------------------------------------------------------------- |
| Physical Risk   | Riverine and coastal flooding, drought, cyclones, heat stress, power outages |
| Transition Risk | Carbon pricing, emissions caps, energy transition costs, ESG regulations     |

---

## Repository File Structure

The following datasets, assumptions, and analysis files are included in this repository:

**Assumption Files**:

* `physical_exposure_map.geojson`
* `physical_risks.geojson`
* `scenario_parameters.yml`

**Data Files**:

* `emissions_pricing_2030.json`
* `transition_costs.csv`

**Analysis Notebooks and Outputs**:

* `financial_impact_summary.ipynb`
* `financial_impact_summary.xlsx`
* `physical_risk_analysis.ipynb`

**Meta Files**:

* `README.md`
* `LICENSE`
* `.gitignore`

These files align with the methodologies outlined below and allow for full scenario simulation and sensitivity testing.

---

## Risk Analyses

### Physical Risk (Detailed Explanation)

Physical risks refer to direct climate impacts. Key risks included flooding, heat stress, water stress, and power outages. We applied geospatial analysis using NASA SRTM and CMIP6 datasets, along with local infrastructure maps and GRACE water stress indices.

### Transition Risk (Detailed Explanation)

Transition risks include policy, economic, and regulatory changes such as carbon pricing, ESG rules, and decarbonization costs. We modeled emissions cost trajectories based on NGFS and IEA scenarios, using site-level emissions intensity benchmarks and projected CAPEX for renewable transitions.

---
# Physical Risk 
Physical risks refer to the direct impacts of a changing climate on manufacturing assets and operations. These risks can be acute (event-driven) or chronic (longer-term shifts):

+ Flooding: Coastal and riverine flooding was assessed using NASA SRTM elevation data and flood hazard zones from UNISDR and local municipal data. Facilities under 10 meters elevation within 10 km of a floodplain were deemed high-risk.
+ Heat Stress: Projected increases in Wet-Bulb Globe Temperature (WBGT) from CMIP6 indicate regions (e.g., Southern Europe, South Asia) may experience >30°C WBGT for over 30 days/year, reducing labor productivity and equipment efficiency.
+ Water Stress: Facilities in water-scarce regions (India, Mexico) were flagged using GRACE satellite data and WRI Aqueduct. Water availability thresholds below 1,000 m³/person/year indicate high stress.
+ Power Outages: Higher temperatures and climate-induced disasters increase strain on grids. Sites relying on centralized fossil-based electricity are at elevated risk of operational downtime.

# Transition Risk
Transition risks arise from shifts in policy, regulation, market preferences, and technologies as the world moves toward a low-carbon economy:

+ Carbon Pricing: Regulatory carbon pricing schemes (e.g., EU ETS, Canadian OBPS) forecast to rise to €85/tCO2e in the EU and $60–$85/tCO2e in North America by 2030. Sites with high Scope 1 emissions face increased operating costs.
+ Emissions Caps: Based on SBTi pathways, manufacturing emissions must reduce >40% by 2030 for 1.5°C alignment, impacting production planning and energy sourcing.
+ Energy Transition Costs: Capital investments in on-site solar, electrification of heat, or hydrogen boilers entail upfront CAPEX but yield ROI in 5–7 years. Modeled using IEA LCOE projections.
+ Raw Material Volatility: Policies like EU Fit for 55, Canadian Extended Producer Responsibility (EPR), and global ESG regulations are expected to raise costs of virgin materials by 12–18%.
+ ESG Regulations: Mandatory climate disclosure regimes (e.g., CSRD in Europe, SEC proposals in the U.S.) increase compliance burdens and reputational risk.

## Key Findings

### Physical Risks under +4°C Scenario

* High flood risk at Gulf Coast (USA), Vietnam, and Philippines sites: **>\$5M/year disruption**
* Heat stress in Southern Europe: **>30 days/year over 30°C WBGT**
* Water stress flagged in India and Mexico facilities

### Transition Risks under +1.5°C Scenario

* Carbon pricing: **\$25M/year exposure**
* ESG-driven material inflation: **12–18% cost rise**
* Renewable shift CAPEX: **\$10M with 5–7 year ROI**

---

## Financial Impact Analysis (2030 Outlook)

| Climate Driver                 | Financial Exposure Estimate                  |
| ------------------------------ | -------------------------------------------- |
| Carbon Pricing                 | \$25M/year (unmitigated emissions cost)      |
| Physical Infrastructure Damage | \$18M (repair, downtime, insurance premiums) |
| Renewable Transition (CAPEX)   | \$10M (5–7 year ROI horizon)                 |
| Procurement Shift (inflation)  | \$12M/year (low-carbon material premiums)    |

## Carbon Pricing – $25M/year (unmitigated emissions cost)
This represents the annual cost if carbon emissions from manufacturing operations are not reduced or offset by 2030. It's calculated based on projected regulatory carbon prices (e.g., €85/tCO₂e in the EU, ~$60–$85 in North America) and the total Scope 1 emissions footprint of the assessed facilities. If no mitigation (such as fuel switching, electrification, or carbon credits) is implemented, the company could face direct compliance costs of $25 million annually.

# Assumptions:

+ Scope 1 emissions intensity: 0.25 tCO₂e per MWh thermal
+ Carbon price benchmark: weighted average across regulatory zones
+ No carbon offsets or mitigation

## Physical Infrastructure Damage – $18M (repair, downtime, insurance premiums)
This includes the costs associated with climate-driven physical impacts such as flooding, storm damage, and heat-related infrastructure degradation. It combines estimates for asset repairs, lost production from downtime, and rising insurance premiums due to elevated climate risk scores.

# Breakdown:

+ ~$10M in direct repair and downtime at three flood-prone sites (based on recent storm loss averages and modeled exposure)
+ ~$8M in insurance cost increases across high-risk locations

# Assumptions:

+ Damage recurrence probability: 1-in-10-year flood/storm events
+ Based on historical analogs and insurer climate risk re-pricing trends

## Renewable Transition (CAPEX) – $10M (5–7 year ROI horizon)
This reflects the up-front capital investment required to implement renewable energy solutions across key sites—primarily solar PV, wind power procurement, and electrification of thermal processes. Though it raises near-term CAPEX, the cost is expected to be offset through operational savings within 5–7 years.

# Assumptions:

+ CAPEX estimates from IEA LCOE database and RE100 industry case studies
+ 80% renewable electricity substitution target for high-emissions sites
+ Grid parity assumed in Spain, Canada, and Vietnam by 2027

## Procurement Shift (Inflation) – $12M/year (low-carbon material premiums)
As global regulations (e.g., EU Fit for 55, Canadian EPR) tighten, low-carbon and recycled materials will likely cost more than their conventional equivalents. This line item accounts for projected material inflation (12–18%) on key inputs such as steel, aluminum, plastics, and solvents used in the manufacturing process.

# Assumptions:

+ $100M procurement baseline across all sites
+ Premium on low-carbon certified inputs: avg. 14–15%
+ Inflation modeled using historical data from S&P Platts and EU ETS compliance materials


> Detailed assumptions for each driver are documented in:
>
> * `transition_costs.csv`
> * `emissions_pricing_2030.json`
> * `financial_impact_summary.ipynb`

---

## Recommendations

### 1. Resilience & Adaptation

* Site-level flood barriers, rainwater harvesting, on-site power backup
* Diversify production across less-exposed sites

### 2. Decarbonization Strategy

* SBTi-aligned near-term Scope 1 & 2 targets
* 100% renewable electricity by 2027 in EU facilities
* Pilot hydrogen thermal systems in Asia

### 3. Supply Chain Resilience

* Embed emissions reporting in supplier assessments
* Apply internal shadow carbon pricing in procurement

### 4. TCFD Integration

* Publish findings in annual TCFD reports
* Integrate risks into CAPEX gating processes

---

## Assumptions Summary

### Physical Risk Assumptions

* Based on **IPCC RCP8.5** for worst-case
* Site-specific elevation, water scarcity, and flood risk indices

### Transition Risk Assumptions

* NGFS disorderly and orderly transition scenarios
* Carbon pricing: \$50–\$85/tCO₂e by 2030
* LCOE data and RE100 benchmarks for CAPEX estimates

---

## Outcomes Delivered

* Embedded scenario results into 2025–2030 capital planning
* Delivered board-level risk dashboard and facility-level action plans
* Validated science-based targets with **SBTi**
* Published **TCFD-aligned** disclosures in 2024 Annual Report

