# Design and Analysis of a Telescopic op amp

## Theory 

# Telescopic op-amp

- A telescopic op-amp is a single-stage, high-gain amplifier commonly used in analog circuit design, especially in low-power and high-speed applications.

- It features a fully differential structure, improving common-mode rejection and noise performance.

- Named "telescopic" due to its stacked transistor configuration (like a telescope), allowing for a compact layout and higher gain per stage.

- The design consists of:

- Differential input pair (usually NMOS for better input common-mode range),

- Current mirror load using PMOS transistors,

- Cascode transistors (both NMOS and PMOS) to increase gain by enhancing output resistance

## Working principle

- Differential Input Conversion:
The amplifier begins with a differential pair (M1 and M2), which senses the input voltage difference and converts it into a differential current.

- Current Steering through Cascode NMOS (M3, M4):
The differential current flows through cascode NMOS transistors M3 and M4. These transistors increase the output resistance, which directly enhances the voltage gain of the amplifier.

- Load with PMOS Transistors (M5, M6):
The output current is mirrored and loaded by PMOS transistors M5 and M6.

- Gain Boost via PMOS Cascode (M7, M8):
Cascode PMOS devices M7 and M8 further increase the output resistance and gain by stacking above M5 and M6.

- Constant Tail Current (M9):
A constant bias current is provided by tail current source M9, which stabilizes the operation of the differential pair.

- High Gain in Single Stage:
The stacking of NMOS and PMOS cascodes in a single gain stage provides high intrinsic gain and good bandwidth.

- Trade-off – Limited Output Swing:
Due to the high number of stacked transistors, the output swing is limited, which is a key design consideration.

- Symmetry and Low Power Operation:
The design is fully symmetrical and supports efficient low-power operation.

- Application Suitability:
Ideal for analog signal processing applications due to its high gain, bandwidth, and power efficiency.

## Design parameters

| **Parameter**               | **Value / Description**                                     |
| --------------------------- | ----------------------------------------------------------- |
| **Technology**              | TSMC 180nm CMOS                                             |
| **Supply Voltage (VDD)**    | 3V                                                          |
| **Gain Target**             | > 40 dB                                                     |
| **Input Pair**              | NMOS (M1, M2)                                               |
| **Tail Current Source**     | NMOS (M9) biased at V4 = 1.35V                              |
| **Cascode NMOS**            | M3, M4 biased with Vb⁺ = 2V                                 |
| **Load Devices**            | PMOS (M5, M6)                                               |
| **Cascode PMOS**            | M7, M8 biased with V5 = 1.5V, V3 = 1.3V                     |
| **Output Nodes**            | Differential: Vout1 and Vout2                               |
| **Common-Mode Input Range** | Limited by cascoding; must stay within bias voltage margins |
| **Output Swing**            | Limited due to stacked transistors (cascoded architecture)  |
| **Power Consumption**       | Low (depends on tail current through M9)                    |

