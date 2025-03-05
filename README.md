# Insect Detection Bot

This project uses an **ESP32-CAM module** and **Edge Impulse** to collect and classify images for insect detection. It enables real-time insect identification, making it useful for agricultural and environmental applications.

## Features
- **ESP32-CAM Image Collection Server**
- **Edge Impulse Model Integration**
- **Insect Classification using Machine Learning**
- **Low-Power, IoT-Compatible Solution**

## Hardware Requirements
- ESP32-CAM module (AI-Thinker or compatible)
- FTDI Programmer (for flashing firmware)
- Power supply (e.g., 5V battery or USB)
- Optional: External LED for better image capture

## Software Requirements
- Arduino IDE with ESP32 board package
- Edge Impulse Studio account
- Required Arduino libraries:
  - `eloquent_esp32cam`
  - `WiFi.h`

## Setup Instructions
### 1. Flash ESP32-CAM
1. Clone this repository:
   ```bash
   git clone https://github.com/nik-krish/insect_detection_bot.git
   ```
2. Open the project in **Arduino IDE**.
3. Install the required libraries mentioned above.
4. Connect ESP32-CAM to FTDI programmer and upload the code.

### 2. Connect to WiFi
- Update your **WiFi credentials** in the code:
  ```cpp
  #define WIFI_SSID "your-SSID"
  #define WIFI_PASS "your-password"
  ```
- Open the **Serial Monitor (115200 baud)** to find the device’s IP address.
- Access the live camera feed at:
  ```
  http://<ESP32_IP>
  ```

### 3. Collect and Label Images
1. Use the web interface to collect images of insects.
2. Upload collected images to **Edge Impulse** for training.
3. Train an **object detection model** for insect classification.
4. Deploy the trained model back to the ESP32-CAM.

### 4. Run Inference for Insect Detection
- Once the model is deployed, the ESP32-CAM can classify detected insects in real-time.

## Usage
- **Farmers**: Detect harmful insects and pests.
- **Researchers**: Monitor insect populations.
- **Smart Gardens**: Automate pest control solutions.

## Sample Insect Detection  

Below is a sample image of the bot:  

![Bot Image](https://github.com/user-attachments/assets/a55cb002-2d96-4264-bf5c-c4f2e61f0e52)  

*Figure: The insect detection bot.*  

Below is a sample image demonstrating the image capture process for training:  

![Training](https://github.com/user-attachments/assets/4db8b147-1acc-451a-934d-aba851ee4ec9)  

*Figure: Capturing images for training.*  

Below is a sample image illustrating the labeling process:  

![Labeling](https://github.com/user-attachments/assets/552c9fe6-ce7d-4965-b16c-9363b0a2bd37)  

*Figure: Labeling images for model training.*  

Below is a sample image captured by the **ESP32-CAM** and processed using **Edge Impulse**:  

![Output](https://github.com/user-attachments/assets/eb04a2f0-dfd7-48b7-bedc-f34890d26be4)  

*Figure: Insect detected using the trained Edge Impulse model.*  

## License
This project is open-source under the **MIT License**.

## Author
Developed by **Nikhil Krishan**

## Contributions
Pull requests and suggestions are welcome! 🎉

