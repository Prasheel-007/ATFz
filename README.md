# Agri TechFarmZ: An IoT-Based Smart Farming and Irrigation Automation System

### The Statement: The Unified AI Smart Farming Ecosystem
### Tagline: A Unified solution to the farmers
#### AI-Crop-IoT: IoT + Software = Accurate Agriculture solution

---

## 📖 About the Project
Agri TechFarmZ is the evolution of a software-based AI crop recommendation system into a fully unified hardware-software ecosystem. Originally built to estimate crop viability using static datasets, this project has been fundamentally upgraded to utilize real-time environmental IoT telemetry. 

Instead of just telling a farmer what to plant, Agri TechFarmZ actively manages the crop's lifecycle. It merges live sensor data with predictive APIs to autonomously handle irrigation, forecast crop yields, track nutrient depletion, and alert farmers to potential crop diseases. It is a complete, low-cost smart farm manager.

## ✨ Key Features & Enhancements

* **Real-Time Environmental Monitoring:** Uses precision sensors to gather accurate, live data on soil moisture, temperature, humidity, and sunlight exposure.
* **AI-Powered Crop Recommendation:** Processes live sensor telemetry alongside agricultural datasets to suggest the highest-yield crop for the current soil state.
* **Expected Yield Estimation:** Based on the recommended crop, current soil profile, and weather data, the AI calculates an estimated yield potential (e.g., tons per acre), giving farmers economic predictability before they plant.
* **Smart Automated Irrigation:** Replaces static, timer-based watering with a demand-driven system. The water pump activates only when the plant genuinely requires hydration.
* **Predictive Weather Integration (Water Saver):** Integrates with Weather APIs. If the soil is dry but rain is forecasted within a few hours, the system overrides the pump to stay off, conserving water and electricity.
* **Disease Risk Alerts:** By continuously analyzing temperature and humidity via the DHT22, the software predicts conditions favorable for fungal growth or pests and sends preventative alerts directly to the farmer.
* **Smart Fertilizer Tracking:** Calculates nutrient depletion based on the specific crop's growth stage and baseline NPK, notifying the farmer exactly when to add specific fertilizers.

## 💡 The Cost-Effective NPK Strategy: The Hybrid Approach
Industrial IoT NPK sensors often exceed ₹7,000 to ₹15,000, making them unaffordable for the average farmer. Agri TechFarmZ solves this by utilizing a highly practical **Hybrid Data Approach**:
1. **The DIY Soil Test:** The farmer uses a low-cost (₹400-₹500) chemical soil testing kit at the start of the season to find the baseline N, P, K, and pH levels.
2. **Manual Input:** The farmer enters these static baseline values into the Agri TechFarmZ mobile app just once per season.
3. **AI Fusion:** Our AI engine merges this static nutrient baseline with the **live, continuously streaming data** from our low-cost IoT sensors to generate highly accurate crop recommendations and dynamic depletion rates.

## 🛠️ Hardware Requirements
### Core Components:
* ✔ **ESP32**: The central microcontroller and IoT gateway.
* ✔ **Soil Moisture Sensor**: To measure volumetric water content.
* ✔ **DHT22**: For monitoring ambient temperature and humidity.
* ✔ **LDR Sensor (Light Dependent Resistor)**: To track daily sunlight hours for accurate crop profiling.
* ✔ **Relay & Water Pump**: Actuators for the automated irrigation process.
* ✔ **OLED Display**: For on-site, real-time data visualization.

### Support Components:
* ✔ Breadboard & Jumper wires
* ✔ Resistors & Power supply
* ✔ *Low-Cost DIY Chemical Soil Test Kit (for NPK baseline)*

## 💻 Software & Tech Stack
* **IoT/Hardware Platform:** C++ (Arduino IDE / PlatformIO)
* **Backend & Machine Learning:** Python, Scikit-learn, Random Forest Regressor (for yield estimation)
* **APIs:** OpenWeatherMap API (for predictive watering)
* **Database & Cloud:** Firebase Realtime Database (for low-latency sensor streaming)
* **Frontend App:** Flutter (Dart) - chosen for superior real-time graph rendering and seamless Firebase integration.

## ⚙️ How It Works (The Ecosystem Flow)
1. **Initialization:** The farmer conducts a simple DIY soil test and inputs the baseline NPK values into the Flutter app.
2. **Data Acquisition:** The ESP32 continuously collects live readings (Moisture, Temp, Humidity, Light) and streams them to Firebase.
3. **Recommendation & Yield Estimation:** The Python backend evaluates the static NPK and live climate profile to recommend the optimal crop and project the estimated financial yield.
4. **Smart Management:** Once planted, the system takes over irrigation. It waters the field only when moisture drops below the crop's specific threshold AND no rain is predicted by the weather API.
5. **Continuous Care:** The app tracks the crop's lifecycle, sending push notifications for fertilizer application and potential disease outbreaks based on real-time climate tracking.
