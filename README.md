# IoT-Assignment-3
CREATED WOKWI

This code is designed to read temperature and humidity data from a DHT22 sensor and simulate CO2 values within a specified range. It then sends this data to ThingSpeak, an IoT platform for storing and analyzing sensor data. Here's a breakdown of the code:

1. Libraries: The code includes necessary libraries:
   - `WiFi.h`: Library for connecting to a WiFi network.
   - `DHTesp.h`: Library for interacting with DHT sensors.
   - `ThingSpeak.h`: Library for sending data to ThingSpeak.
   - `<random>`: Standard C++ library for random number generation.

2. Constants and Variables:
   - `DHT_PIN`: GPIO pin connected to the DHT22 sensor.
   - `WIFI_NAME` and `WIFI_PASSWORD`: SSID and password of the WiFi network to connect to.
   - `myChannelNumber` and `myApiKey`: ThingSpeak channel number and API key for sending data.
   - `server`: ThingSpeak server address.
   - `dhtSensor`: Object for interacting with the DHT sensor.
   - `client`: WiFi client object for communication.

3. Function `generateCO2Value()`: This function generates a random CO2 value within the range of 300 to 2000 ppm using C++ standard library facilities.

4. `setup()` function:
   - Initializes serial communication.
   - Sets up the DHT sensor.
   - Connects to the WiFi network.
   - Begins the ThingSpeak client.

5. `loop()` function:
   - Reads temperature and humidity data from the DHT sensor.
   - Generates a simulated CO2 value.
   - Sets the fields for temperature, humidity, and CO2 value in the ThingSpeak data.
   - Attempts to send the data to ThingSpeak.
   - Prints the sensor data and the status of the data transmission.
   - Delays for 10 seconds before repeating the process.

6. Data Sending:
   - The temperature and humidity are read from the DHT sensor directly.
   - The CO2 value is generated randomly within the specified range.
   - The data is sent to ThingSpeak using the `writeFields()` function.
   - The status of the transmission is checked. If the status is 200, it indicates a successful transmission.

7. Serial Output: Provides feedback through the serial monitor regarding the sensor readings, CO2 value, and the status of data transmission to ThingSpeak.

Overall, this code establishes a connection to a WiFi network, reads data from a DHT22 sensor, generates simulated CO2 values, and sends this data to ThingSpeak for storage and analysis.


