
# Psy-Sense: Wearable Health Monitoring Device  

## Overview  
**Psy-Sense** is a wearable prototype designed to monitor an individual's physiological state in real time. It integrates multiple sensors to track vital health metrics such as pulse rate (BPM), body temperature, and oxygen saturation (SpO₂). The device features an OLED display and uses the I2C protocol for efficient communication between sensors and the microcontroller.  

---

## Technical Details  
- **Microcontroller:** Arduino-compatible board  
- **Sensors:**  
  - MAX30105 (Pulse Rate and SpO₂)  
  - Adafruit MLX90614 (Temperature)  
- **Display:** 128x32 OLED screen  
- **Indicators:** LED alerts  
- **Libraries:**  
  - `Wire.h` (I2C communication)  
  - `MAX30105.h` (Pulse and SpO₂ sensor operations)  
  - `Adafruit_MLX90614.h` (Temperature sensor)  
  - `Adafruit_GFX.h` and `Adafruit_SSD1306.h` (OLED graphics)  
  - `spo2_algorithm.h` and `heartRate.h` (SpO₂ and heart rate algorithms)  

---

## Features  

### Pulse Rate Monitoring (BPM)  
- Measures heart rate using the MAX30105 sensor.  
- Computes average heart rate from real-time data.  

### Body Temperature Monitoring  
- Tracks body temperature with the Adafruit MLX90614 infrared sensor.  
- Provides readings in both Celsius and Fahrenheit.  

### Oxygen Saturation (SpO₂)  
- Calculates SpO₂ levels using infrared (IR) and red light data via the MAX30105 sensor.  

### Real-Time Visualization  
- Displays heart rate, temperature, and elapsed time on a 128x32 OLED screen.  

### Alert System  
- LED indicators notify users when no finger is detected on the sensor or when the monitoring session ends.  

### Compact and Efficient Design  
- Lightweight and wearable for continuous monitoring.  
- Utilizes the I2C protocol for streamlined communication between components.  

---

## Code Summary  
- **Initialization:** Configures sensors, OLED display, and LEDs.  
- **Data Processing:**  
  - Calculates heart rate and SpO₂ from IR and red light values.  
  - Reads and averages temperature data for accuracy.  
- **Alerts:**  
  - LED blinks if no finger is detected.  
  - Timer-based LED indicates the end of the monitoring session.  
- **Display:** Continuously updates the OLED with elapsed time, BPM, and temperature.  

---

## Key Learnings and Experience  
- Integration of multiple sensors using the I2C protocol.  
- Development of real-time data processing algorithms for health monitoring.  
- Hands-on experience with embedded systems and wearable device prototyping.  
- Efficient data visualization using OLED displays.  
