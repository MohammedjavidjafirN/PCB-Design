Project description:
This project is a custom STM32-based microcontroller development board designed around the STM32F401RE MCU, intended to function as a compact environmental sensor node. The board integrates multiple communication interfaces, stable power regulation, and analog signal conditioning to support real-world embedded applications.The system is powered through a USB OTG interface, which provides the primary input supply (VBUS). This voltage is regulated down to 3.3V using the AMS1117 linear regulator, ensuring a stable operating voltage for the microcontroller and associated peripherals. To further enhance analog performance, a dedicated VDDA filtering network (ferrite bead and decoupling capacitors) is implemented to isolate noise from the digital supply, improving the accuracy of ADC-based sensor readings.

At the core of the design, the STM32F401RE microcontroller manages data acquisition, processing, and communication. The board exposes multiple communication protocols, including:
UART for serial communication and debugging
I2C for interfacing with environmental sensors (e.g., temperature, humidity, pressure)
SPI for high-speed peripheral communication
SWD (Serial Wire Debug) for programming and debugging

An external crystal oscillator is used to provide a stable clock source, ensuring reliable timing for communication protocols and internal operations. Proper decoupling capacitors are placed near the power pins of the MCU to minimize voltage fluctuations and ensure stable performance.The design also includes dedicated header pins for GPIO expansion, enabling easy integration with external modules and sensors. The USB interface supports both power delivery and potential data communication, making the board versatile for embedded system development.
