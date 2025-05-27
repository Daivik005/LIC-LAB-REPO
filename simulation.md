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

