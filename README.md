# UnderstandingLiPoBatteries

Most of the information below comes from the following site. Please visit for further information. Roger's Hobby Center: https://rogershobbycenter.com/lipoguide
LiPo stands for Lithium Polymer. There are certain parameters provide on the batter such as #c which is the Discharge(c) Rating, ####mAh - which is the capacity and #s #.#V - which is the cell count and voltage. These are some of the most important specifications. Please check the datasheets for others.

Voltage/Cell Count
LiPo batteries have a nominal voltage of 3.7v per cell. A battery can have multiple cells. For example, 2s has 2 cells (2 x 3.7 = 7.4V) and a 4s has 4 cells (4 x 3.7 = 14.8V). Older batteries had a different naming convention. Example, 2S2P, which means 2 cells in series and 2 in parallel. 
Side-note: Brushless motors are rated by kV which means “RPM per Volt”. Example, a 3500kV motor runs at 3500RPM for every volt applied.

Capacity
The capacity is measured in mAh. It measures how much power the battery can hold. This tells us how much drain, amperage, can be used in 1 hour. Usually the bigger the capacity the bigger the size and weight of the battery.

Discharge Rating (“c” Rating)
This rating measures how fast the battery can be drained without causing issues to the battery. It does require to know the capacity in Amps to figure out the safe Amp draw. The formula is as follows: #c x Capacity(Amps).
Example: Calculating the c-rating of a 5000mAh at 50c. 50 x 5 = 250A. You can draw 250A and the battery will be ok.
Some data sheets may also provide you with Burst Rating which is the same as c-Rating but it is the highest amperage draw within short periods of time.

Internal Resistance: The Mystery Number
Internal Resistance is a mystery number because it changes over time.
Internal Resistance is the measurement of the difficulty a battery has in delivering a its power to the motor and electronics. It is measured in mOhms. The higher the number, the more difficult it is for the battery to deliver the power to the circuit. The energy lost to the internal resistance is lost as heat. To measure the internal resistance may require specialized equipment. Most modern LiPo chargers do include internal resistance measurement. The internal resistance can be used as a measurement of the battery’s health. If the internal resistance is 0-6mOhms – battery is good, 7-12mOhms – battery is ok, 12-20mOhms – battery is showing signs of decay, and over 20mOhms – battery needs to be replaced. Of course, you might want to take other specifications into consideration as a decayed battery may still meet your circuits specifications. You do need to consider the heat of the battery as the more internal resistance the more heat a battery creates.
Example: A motor with 3500kV rating with 12.6V being delivered to it. Motors RPM is 3500 x 12.6 = 44100 RPM. If the battery has an internal resistance of 0.012Ohms and the circuit draws 65A. Then the voltage drop is 0.012Ohms x 65A = 0.78V. So the actual voltage being delivered to the circuit is 12.6V – 0.78V = 11.82V. At 11.82V the motor’s RPM is 11.82 x 3500 = 41370 RPM, a loss of 2730 RPM. 

Charging LiPo Batteries
LiPo Batteries use a charging system called CC/CV. This means constant current \ constant voltage. The charger will keep the current constant till each battery cell reaches its peak voltage of 4.2V. Once it reaches this voltage it will then switch to constant voltage where it will keep the voltage at 4.2V while the current is reduced. This assures the cells are balanced. Most batteries include additional cabling with a JST-XH connector to make sure the cells are balances. This must be connected to the charger along with the VCC and ground. Be careful when disconnecting the JST-XH connector as it may be hard to remove, and you can damage the wiring. LiPo Batteries should not be charged at no more than 3A. Most LiPo batteries have a Charge Rating of 1c. Using the same formula used to figure out the Discharge Rating you can figure out the amperage you can safely charged the battery.

Balancing
LiPo Batteries require the cells to be balanced meaning for each cell to have the same voltage. This ensures that each cell is discharged equally and at the same time to avoid any issues with them.

Proper Care and Treatment: Discharging (Using the Battery)
LiPo batteries are made from Lithium (alkali metal) which reacts with water and oxygen. The use of the battery causes an excess of Oxygen and Lithium atoms at the cathode and anode. This causes a build up of Lithium Oxide (Li2O) on the cathode and anode. This causes internal resistance.

LVC – Low Voltage Cutoff Module
The LVC electronic module detects the voltage of the battery and divides it by the number of cells to figure out the voltage per cell. LiPo Battery cells cannot fall below 3.0V. The normally cutoff voltage at 3.2V to keep the LiPo Battery cells from going into the critically low range.
