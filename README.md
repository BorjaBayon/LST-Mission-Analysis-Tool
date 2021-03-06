# LST-Mission-Analysis-Tool
Simplistic Mission Analysis Tool for a reusable Lunar Space Tug powered by Electric Propulsion. The main input is the mission transfer time, while the main output is the payload mass that can be delivered by Electric Propulsion (EP) for that transfer time. Additional outputs include cost savings with respect with a mission delivering the same payload mass with Chemical Propulsion (CP). This was done under the following assumptions:
- The HPH is only used for orbit raising. A ΔvLow-Thrust of 8 km/s and a ΔvHigh-Thrust of 4.04km/s were used, both taken from [1] for a transfer from LEO to LLO. For CP, a transfer time of 4 days, and a Isp of 450s (that of LOX+LH2). For EP, thruster operation time is equal to transit time.
-	The vehicle is mainly made up of the specific mass of the Power and Propulsion subsystems. The propulsion subsystem specific mass model is based on [2] and includes the rocket core, PPUs, magnets, thermal and propellant management, and control hardware; Power subsystem mass covers solar panels, structure and radiators. An additional 10% of the propellant mass is allocated for the fluidic management subsystem, very relevant for CP. A fixed mass of 500kg is allocated to cover additional subsystems like AOCS, Comms, the docking adapter to attach the payloads and additional Thermal and Structural components.
-	Constant solar power: no sun occultation (night-time, eclipses, improper panel pointing…). No solar panel degradation over space tug lifetime. A solar panel efficiency of 45%, specific mass of 3.3kg/kW and areal power of 2.5m2/kW were taken from optimistic extensions of “Mid- to Far-term” (5-10 years) expectations from [3] for Advanced Solar Array technologies.
-	Price per kg-to-LEO and mission operations cost were considered as the main cost drivers for this study: propellant cost per kg would be equal for both options, solar panel cost should be down to nowadays COTS options (~1400$/kW), and extensive research and commercialization of radiation-tolerant components with long lifetimes should make their price accessible, too. 
-	The expected mission operations cost was set at a low 1M$/month owing to recent trends towards increased automatization through the use Artificial Intelligence in satellite monitoring.
- The expected price of kg-to-LEO is placed near today’s low-end, at around 5000$/kg. Even if future Heavy Lift Vehicles like SpaceX’s Starship lower said price for a single launch, the amount of launches needed to move cargo to LLO would off-set the savings of the initial launch to LEO. The cost of refueling with In-Situ Resource Utilization (ISRU) propellant in LLO is also assumed to be 5000$/kg of propellant.
-	The space tug launch cost is divided between each of the missions it performs for mission cost estimation purposes.
-	HPH performance comparable to that of present-day estimations for VASMIR, supported on claims (“The VASIMR results may not be indicative of the full potential of helicons”) and experimental data from [4], where hydrogen was used at up to 70kW; values of thrust density of 30mN/kW, Isp of 5000s and thrust efficiency of 72% taken from [5] for Ar are extended to hydrogen (the representative ISRU propellant).
-	Thruster operational lifetime of 50000 hours, five times higher than typical Hall thrusters, based on the electrodeless nature of the thruster (no cathode erosion), assuming maturity of helicon technology and mitigation of other lifetime-reducing issues like plasma impingement on the rear wall [6].

The Mission Analysis Tool outputs were verified by comparing them with results from [7]. Finally, claims made about the benefits of helicons over other EP thrusters (no cathode erosion, can use ISRU propellants, better scaling with power, simpler electronics, lower radio frequencies needed, allowing higher plasma densities) were taken from [4,6].

[1] Thronson, H. et al. Human Exploration Beyond LEO by the End of the Decade: Designs for Long-Duration “Gateway” Habitats. FISO “Gateway” Concepts Study 2010.

[2] Squire, J. P. et al. VASIMR Spaceflight Engine System Mass Study and Scaling with Power. 33rd International Electric Propulsion Conference 2013.

[3] Surampudi, R. et al. Solar Power Technologies for Future Planetary Science Mission. Strategic Missions and Advanced Concepts Office 2017.

[4] Ziemba, T. et al. High Power Helicon Thruster. 41st  Joint Propulsion Conference 2005.

[5] Longmier, B. W. et al. Improved Efficiency and Throttling Range of the VX-200 Magnetoplasma Thruster. Journal of Propulsion and Power 2014, 30, 1.

[6] Ahedo, E.; Navarro-Cavallé, J. Helicon thruster plasma modeling: Two-dimensional fluid-dynamics and propulsive performances. Physics Of Plasmas 2013, 20, 4.

[7] Glover, T. Lunar Cargo Capability with VASIMR Propulsion. Ad Astra Rocket Company Presentation

