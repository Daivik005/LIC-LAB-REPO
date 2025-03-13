Experiment-1

Question : Given that POWER, P=100µ W; Perform DC Analysis, Transient Analysis and AC Analysis for the Given Circuit Designs and also check what happens when the width is increased or decreased of each mosfet;

Procedure

1. Design the CS amplifier circuit using LTSpice.

Connect the required components as per the circuit diagram.

Perform DC analysis to determine the biasing conditions.

Perform transient analysis to study the time-domain response.

Perform AC analysis to extract gain and frequency response characteristics.

Record observations and extract relevant parameters.

Design-1 :

![Screenshot 2025-02-17 093411](https://github.com/user-attachments/assets/a4772ea5-8b4b-479a-a52e-20ceb84e5010)

Using the Formula for Power,
P=V*I
We will get the Values of Id as,
Id= 5.56 * 10^-5 A
Since we are using the 180n nmos, we are only changing the width to get the required current as output.

![Screenshot 2025-02-17 093537](https://github.com/user-attachments/assets/6aacb860-f147-4ffc-86be-38c2fde32651)

Result:

1. DC ANALYSIS:
Procedure for Performing DC Analysis: 

we have to select the dc output print(DC op pnt) in the Edit Simulation Command and Run the Simulation
Here are the simulation values

![Screenshot 2025-02-17 093155](https://github.com/user-attachments/assets/5d834b3c-02f5-40bc-9954-fee564e0c6d2)

2. Transient Analysis:
Procedure for Performing Transient Analysis: we have to select the Transient Analysis in the Edit Simulation Command, Give the stop time as 1ms and Run the Simulation.

![Screenshot 2025-02-17 101420](https://github.com/user-attachments/assets/b4d7d155-ada1-49d2-b545-fb1a90d46f97)

3. AC analysis:
   In the edit simulation we have to go to the ac analysis column and give the necessary constraints.
   Here is the graph for the result

    ![Screenshot 2025-02-17 102036](https://github.com/user-attachments/assets/eec4b3e8-115c-4502-b99b-07b01ec9975a)

Inference

1.Current is directly Propotional to the Width of the Mosfet and the current varies with the change in width.

2.Mosfet saturation ensures the mosfet works as an amplifier and produces the desired negative gain as per the equation Av=-gm*Rd.

3.Q point stability is attained in saturation region thus helping in attaining linear amplification .

4.The Mosfet gain is increased in mid band frequency range (small signal analysis).

5.The Transient analysis reveleas the response of the circuit to time domain ssignal and determines how quickly the circuit responds to variation.

6.AC Analysis helps in designing circuits with desired gain and helps in impedance matching. Also helps in understanding the frequency response and small signal behaviour of the circuit.

2. Design

   Simulation of CMOS amplifier

Aim

Simulate the DC analysis, Transient, and AC analysis of a CMOS amplifier circuit using LTSpice.

Circuit:

![Screenshot 2025-02-17 214012](https://github.com/user-attachments/assets/bd3146b6-3ac1-4904-9133-d192f22915d9)

Procedure

Design the CMOS amplifier circuit.

Naming the NMOS as CMOSN and PMOS as CMOSP.

Apply the DC voltage of VDD = 1.8 V

DC sweep Analysis: Go to the edit simulation command and select the DC sweep option and choose: -Source name= Vin. -type of Sweep= Linear. -start value=0, -stop value =VDD=1.8 V. -increment=0.1.

find the Vin from the vtc curve

DC Analysis:put the appropriate Vin value. go to the Simulate option and select Edit Simulation Command.

Click on DC Analysis, then press OK.Click on Run in the tab menu to obtain the DC operating point Vout .

Set the Length as constant and determine the Width such that ID = 55.5 uA .

Transient Analysis:Modify the Vin voltage source to a sine wave input with:

DC level= 0.9 V

Amplitude= 50 mV

Frequency= 1 kHz

In LTSpice, go to Edit Simulation Command, select Transient Analysis. Set the Stop Time as 5ms, then click OK.

AC Analysis:

In Edit Simulation Command, select AC Analysis.Set the Type of Sweep to Decade.Set Points per Decade to 10.Set the Frequency Range from 0.1 Hz to 1 THz.Click OK. Determine the gain and frequency response of the circuit.

Calculation

ID = 55.5 uA, VDD = 1.8 V

Length M1= 180 nm

Width=200 nm(found by keeping the Length of M1 constant)

Length M2= 180 nm

Width=445 um(found by keeping the Length of M2 constant)\

Result

1. DC sweep

   ![Screenshot 2025-02-17 213936](https://github.com/user-attachments/assets/cb30980f-93a9-4d6c-969c-595a4a5efb2f)

2. DC analysis

![Screenshot 2025-02-17 215058](https://github.com/user-attachments/assets/2eed5ef4-67f7-476e-b5b8-beafde3f5fad)

3. Transient analysis

![Screenshot 2025-02-17 215428](https://github.com/user-attachments/assets/f8175a3b-81f1-442d-a39c-19f06d36d432)

4. AC analysis

![Screenshot 2025-02-17 215630](https://github.com/user-attachments/assets/38343a64-34df-4ded-bd9c-1b6d6a4e73b5)

Gain=5.5 dB

Inference:

1.The Width of the MOSFET directly effects the Drain durrent.

2.By changing the dimensions of the MOSFET -M1 -when varying the width of PMOS there is not a lot of change in the drain current(ie, Id doesn't get effected much).
-M2 -when varying the width of NMOS there is drastic change in the drain current.

3.If width is increased it leads to a higher gain 

4.180 degree phase shift between the input and output waveform.

5.The CMOS amplifier has gain =5.5 dB.(ie, the ouput signal is almost 6 times larger then the input signal)\



