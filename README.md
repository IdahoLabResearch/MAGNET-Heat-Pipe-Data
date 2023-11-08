# MAGNET-Heat-Pipe-Data

Fission batteries are envisioned as nuclear energy systems and associated technology that can be fully utilized in a battery-like operation, where the system is delivered as a ‘plug-and-play’ service. Several key attributes define the desired functionality of these systems: economic, standardized, installed, unattended, and reliable. The construction and operation of unattended, plug-and-play fission batteries will require sufficiently robust hardware and software technologies. Using a digital twin (DT) may reduce costs and risk associated with employing fission batteries through the integration of the disparate systems used in the design, construction, and operation of these nuclear energy systems. A DT employing machine-learning (ML) and physics-based representations to forecast future performance could potentially be used for anticipatory control. Before application of a DT in the fission domain, the DT technology should be validated in a non-fission environment. A DT of a single-heat-pipe test article in the Microreactor AGile Non-nuclear Experimental Testbed (MAGNET) was demonstrated with predictive, self-adjusting capability on 30 March 2022. The test plan stated that: (1) the operators will manually change the temperature set point of the heat pipe to an upper limit or lower limit; and (2) the DT will predict the temperature will go beyond this temperature threshold, and then will update the temperature set point to the baseline temperature without any human intervention. The DT used a two-step process including a least absolute shrinkage and selection operator (LASSO) for variable selection between the sensors followed by vector autoregressive (VAR) models for multivariate forecasting to predict future performance of the heat pipe within MAGNET. Additionally, a physics model was created within the Sockeye framework that would be applied in future tests. With controlled rates of temperature change, the DT successfully self-adjusted the heat pipe before reaching the lower limit under expected conditions. Ultimately, this DT could be leveraged as a foundational framework in future fission battery applications for continuously monitoring and actively self-adjusting a heat pipe.

## Introductory Paper

Wilsdon, K., Hansel, J., Kunz, M. R., & Browning, J. (2023). Autonomous control of heat pipes through digital twins: Application to fission batteries. Progress in Nuclear Energy, 163, 104813.

## Getting Started

### Experiment

* `Multiple_Files` directory - a list of one-minute interval files containing the experimental data.
    * Note: There are time intervals missing because files were only created during the operation of the digital twin instead of the entire experiment.
* `Single_File` directory - full experimental data file.

### Machine_Learning

* A list of files that forecasted the next 10 minutes of operation of the heat pipe. 

See Section `3.2. Machine-learning and artificial intelligence` and `4.2. Machine learning and artificial intelligence` in the journal paper for more information.



## Variable Information
The label/response/y to predict is `Heater Temp`.

* `Time (s)` = time in seconds
* `Date/Time` = this number is the time-zone-independent number of seconds that have elapsed since 12:00 a.m., Friday, January 1, 1904, Universal Time [01-01-1904 00:00:00]. 
    * To convert to datetime, perform the following: Excel -> highlight `Date/Time` column -> Number Formats Dropdown -> Custom -> More Number Formats -> Type = `yyyy-mm-dd hh:mm:ss` -> Ok
* `Heat Pipe TC-01` = thermowell 01
* `Heat Pipe TC-02` = thermowell 02
* `Heat Pipe TC-03` = thermowell 03
* `Heat Pipe TC-04` = thermowell 04
* `Heat Pipe TC-05` = thermowell 05
* `Heat Pipe TC-06` = thermowell 06
* `Heat Pipe TC-07` = thermowell 07
* `Heat Pipe TC-08` = thermowell 08
* `Heat Pipe TC-09` = thermowell 09
* `Heat Pipe TC-10`= thermowell 10
* `Heater Power (W)` = power in watts
* `Heater Temp` = core block temperature

See Section `2.2. Single-heat-pipe test article`, Figure 2, and Figure 3 in the journal paper for more information.

### Has missing values?
No