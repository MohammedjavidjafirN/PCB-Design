This project implements a 12V DC motor driver using an H-Bridge topology, designed to provide bidirectional control and speed regulation of a DC motor. The circuit integrates power electronics and embedded control, using an ESP32 microcontroller to generate PWM control signals and a TC4427A gate driver IC to efficiently drive the MOSFETs.
The H-Bridge is constructed using four N-channel MOSFETs (IRLZ24NPBF) arranged in a full-bridge configuration. This arrangement allows the polarity of the voltage across the motor to be reversed, enabling both forward and reverse rotation. The motor is powered using an external 12V supply, while the switching behavior is controlled through PWM signals from the ESP32.
The PWM signals are fed into the TC4427A dual MOSFET gate driver, which amplifies the control signals and provides sufficient current to rapidly charge and discharge the MOSFET gates. This ensures fast switching, reduced switching losses, and improved efficiency compared to directly driving MOSFETs from the microcontroller.

By controlling the switching sequence of the MOSFETs:

1.One diagonal pair of MOSFETs turns ON → motor rotates in one direction
2.The opposite diagonal pair turns ON → motor reverses direction
3.PWM applied to the enable path → controls motor speed

The design demonstrates a complete motor control system, combining high-current switching, logic-level control, and efficient gate driving
