# SpaceX Falcon 9 First-Stage Landing Analysis 

![SpaceX Falcon 9 Landing](pictures/spacex_falcon_9.jpg)

## Introduction
SpaceX's Falcon 9 rocket has revolutionized space travel with its reusable rocket technology, significantly reducing the cost of access to space. The Falcon 9 is a two-stage rocket, with the first stage designed to return to Earth and be reused in subsequent missions. This first stage is equipped with landing legs and grid fins to control its descent and ensure a safe landing. This notebook aims to analyze the performance and outcomes of Falcon 9 first-stage landings, focusing on various factors such as payload masses, boosters reused counts, and the impact of different orbits and launch sites.

### Dataset Description
The dataset used in this analysis contains detailed information about SpaceX Falcon 9 launches. The dataset includes:

| **Field**        | **Description**                                                                 |
|------------------|---------------------------------------------------------------------------------|
| **FlightNumber** | The flight number of the Falcon 9 launch.                                       |
| **Date**         | The date of the launch.                                                         |
| **BoosterVersion** | The version of the Falcon 9 booster used.                                     |
| **PayloadMass**  | The mass of the payload in kilograms.                                           |
| **Orbit**        | The orbit in which the payload was deployed.                                    |
| **LaunchSite**   | The site from which the launch took place.                                      |
| **Outcome**      | The outcome of the first stage landing (e.g., success or failure).              |
| **Flights**      | The number of flights the booster has completed.                                |
| **GridFins**     | Whether grid fins were used.                                                    |
| **Reused**       | Whether the booster was reused.                                                 |
| **Legs**         | Whether landing legs were used.                                                 |
| **LandingPad**   | The landing pad used for the booster recovery.                                  |
| **Block**        | The block number of the booster.                                                |
| **ReusedCount**  | The number of times the booster has been reused.                                |
| **Serial**       | The serial number of the booster.                                               |
| **Longitude**    | The longitude of the launch site.                                               |
| **Latitude**     | The latitude of the launch site.                                                |
| **Class**        | The binary outcome of the first stage landing (1 for success, 0 for failure).   |

![SpaceX Falcon 9 Design](pictures/spacex_falcon9_design.jpg)

### Analysis Questions
1. **What is the success rate of Falcon 9 first-stage landings?**
2. **How does the payload mass affect the landing success?**
3. **Which launch sites have the highest success rates?**
4. **What is the trend of landing success over time?**
5. **Does the number of previous flights (reused boosters) affect the landing success?**
6. **How does the presence of grid fins affect the landing success?**
7. **How does the success rate of launches vary across different orbits?**

This notebook will explore these questions to provide insights into the performance and outcomes of SpaceX Falcon 9 first-stage landings.

## What is the success rate of Falcon 9 first-stage landings?

![Falcon 9 First-Stage Landing Success Rate](pictures/success_rates_pie.png)

The success rate of Falcon 9 first-stage landings is approximately `67%`. This means that about two-thirds of the landings have been successful. The pie chart visualization clearly shows the proportion of successful landings compared to failures, indicating a relatively high success rate for SpaceX's landing technology.

## How does the payload mass affect the landing success?

![Payload Mass vs Landing Success](pictures/success_rates_vs_payload_mass.png)

The scatter plot of Payload Mass vs. Landing Success shows the relationship between the payload mass and the success of Falcon 9 first-stage landings. The trendline indicates a slight positive correlation. The calculated correlation coefficient is approximately `0.20`, suggesting a weak positive relationship between payload mass and landing success. This implies that heavier payloads are slightly more likely to result in successful landings, but the effect is not strong.

## Which launch sites have the highest success rates?

![Success Rates by Launch Site](pictures/success_rates_by_launch_site.png)

The analysis reveals that the Kennedy Space Center Launch Complex 39A (KSC LC 39A) has the highest success rate for Falcon 9 first-stage landings at approximately `77.3%`. This is closely followed by Vandenberg Air Force Base Space Launch Complex 4E (VAFB SLC 4E) with a success rate of about `76.9%`. The Cape Canaveral Air Force Station Space Launch Complex 40 (CCAFS SLC 40) has a lower success rate of `60.0%`. This indicates that KSC LC 39A and VAFB SLC 4E are the most reliable launch sites for successful landings.

## What is the trend of landing success over time?

![Trend of Landing Success Over Time](pictures/success_rates_over_time.png)

The trend analysis of landing success over time reveals a general improvement in the success rate of Falcon 9 first-stage landings. By calculating the mean of the success rate, we observe that the success rate has increased steadily over the years. This indicates that SpaceX has been improving its landing technology and procedures, leading to more consistent and successful landings.

## Does the number of previous flights (reused boosters) affect the landing success?

![Success Rates by Number of Previous Flights](pictures/success_rates_by_reused_count.png)

The analysis shows that the number of previous flights (reused boosters) positively affects the landing success rate. Boosters with no previous flights have a success rate of approximately `27%`, while those with one or more previous flights have significantly higher success rates, ranging from `75%` to `100%`. This indicates that reused boosters tend to have better landing success, likely due to improvements and refinements made during their refurbishment and reuse.

## How does the presence of grid fins affect the landing success?

![Success Rates Based on the Presence of Grid Fins](pictures/success_rates_by_gridfins.png)

The analysis reveals that the presence of grid fins significantly improves the landing success rate of Falcon 9 first-stage. Boosters equipped with grid fins have a success rate of approximately `83%`, compared to just `10%` for those without grid fins. This indicates that grid fins play a crucial role in enhancing the control and stability of the booster during landing, leading to higher success rates.

## How does the success rate of launches vary across different orbits?

![Success Rates Based on the Orbit](pictures/success_rates_by_orbit.png)

The analysis shows that the success rate of SpaceX Falcon 9 first-stage landings varies significantly across different orbits. Orbits such as ES-L1, GEO, HEO, and SSO have a perfect success rate of `100%`. In contrast, the GTO orbit has a lower success rate of approximately `52%`, and the SO orbit has a 0% success rate. Other orbits like LEO, MEO, and PO have moderate success rates ranging from `67%` to `71%`. This indicates that certain orbits are more challenging to achieve successful landings.
