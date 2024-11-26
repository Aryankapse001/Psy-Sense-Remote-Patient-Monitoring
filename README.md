Overview
 Psy-Sense is a wearable prototype device designed to monitor the physiological state of
 individuals in real-time. It integrates multiple sensors to track vital health metrics such as pulse
 rate (BPM), body temperature, and oxygen saturation (SpO₂). The device uses an OLED display
 for real-time data visualization and operates using the I2C protocol for efficient communication
 between sensors and the microcontroller.

 Features
 1. Pulse Rate Monitoring (BPM):
 ○ Measures heart rate using the MAX30105 sensor.
 ○ Computes average heart rate using real-time data.
 2. Body Temperature Monitoring:
 ○ Tracks body temperature with the Adafruit MLX90614 infrared temperature
 sensor.
 ○ Provides readings in both Celsius and Fahrenheit.
 3. Oxygen Saturation (SpO₂):
 ○ Calculates SpO₂ levels using IR and Red light data via the MAX30105 sensor.
 4. Real-Time Visualization:
 ○ Displays heart rate, temperature, and elapsed time on a 128x32 OLED screen.
 5. Alert System:
 ○ LEDindicators notify when there is no finger detected on the sensor or when the
 monitoring session ends.
 6. Compact and Efficient:
 ○ UsesI2Cprotocol for efficient communication.
 ○ Lightweight and wearable for continuous monitoring.
 
 Technical Details
 1. Hardware Components:
 ○ Microcontroller: Arduino-compatible board.
 ○ Sensors:
 ■ MAX30105(Pulse Rate and SpO₂).
 ■ Adafruit MLX90614 (Temperature).
 ○ Display: 128x32 OLED screen.
 ○ Indicators: LEDs for alerts.
 2. Libraries Used:
○ Wire.h: I2C communication.
 ○ MAX30105.h: MAX30105 sensor operations.
 ○ Adafruit_MLX90614.h: MLX90614 temperature sensor.
 ○ Adafruit_GFX.h and Adafruit_SSD1306.h: OLED display graphics.
 ○ spo2_algorithm.h and heartRate.h: Algorithms for SpO₂ and heart rate
 calculations.
 3. Functions:
 ○ PulseRate: Detects heartbeats using IR light absorption and calculates BPM.
 ○ SpO₂:Computes oxygen saturation using the SpO₂ algorithm.
 ○ Temperature: Reads ambient and object temperature.
 ○ Display Update: Dynamically updates data on the OLED display.

 Code Summary
 ● Initialization: Configures sensors, OLED display, and LEDs.
 ● DataProcessing:
 ○ Heart rate and SpO₂ are calculated using IR and Red light values.
 ○ Temperature is read and averaged for accuracy.
 ● Alerts:
 ○ LEDblinks if no finger is detected.
 ○ Timer-based LED indicates the end of the monitoring session.
 ● Display: Continuously updates the OLED with elapsed time, BPM, and temperature.
 
 Key Learning and Experience
 ● Integration of multiple sensors using the I2C protocol.
 ● Development of real-time data processing algorithms for health monitoring.
 ● Hands-on experience with embedded systems and wearable device prototyping.
 ● UseofOLEDdisplays for compact and efficient data visualization.
