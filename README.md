# STM32U5 Azure Out Of the Box Experience
**STM32U5 Azure Out Of the Box Experience** (***OOBE***) is the fastest way to get your [B-U585I-IOT02A](https://www.st.com/en/evaluation-tools/b-u585i-iot02a.html) Discovery Kit up and running with [Azure IoT Central](https://azure.microsoft.com/en-us/services/iot-central/#overview) and [Plug and Play](https://docs.microsoft.com/en-us/azure/iot-develop/overview-iot-plug-and-play). This demonstration reduces software requirements, configuration steps, and start-up time to show how easy it is to leverage IoT solutions with [STM32](https://www.st.com/en/microcontrollers-microprocessors/stm32-32-bit-arm-cortex-mcus.html) microcontrollers and [Azure IoT](https://azure.microsoft.com/en-us/free/iot/?OCID=AID2200277_SEM_2374d74a7482129a983bb63c97ee7177:G:s&ef_id=2374d74a7482129a983bb63c97ee7177:G:s&msclkid=2374d74a7482129a983bb63c97ee7177).  

Goal: Connect the B-U585I-IOT02A Discovery Kit to a free Azure IoT Central Application and publish sensor data (as seen below) within a matter of minutes

![rtaImage](https://user-images.githubusercontent.com/41168224/161152572-60bf37c7-3040-4c23-9a8c-3eb2a0031d40.png)


## 1. Software Requirements

- STM32U5 Azure Quick Connect Package:
  - [Windows](https://github.com/stm32-hotspot/STM32U5_OOBE/raw/main/STM32U5_Azure_QuickConnect_Windows.zip)
  - [MacOS](https://github.com/stm32-hotspot/STM32U5_OOBE/raw/main/STM32U5_Azure_QuickConnect_MacOS.zip)
  - [Linux](https://github.com/stm32-hotspot/STM32U5_OOBE/raw/main/STM32U5_Azure_QuickConnect_Linux.zip)

## 2. Hardware Requirements 
- [B-U585I-IOT02A Discovery Kit](https://www.st.com/en/evaluation-tools/b-u585i-iot02a.html)

![2](https://user-images.githubusercontent.com/41168224/161153562-ac1482e2-8807-46f3-b212-197b3b20cfa5.jpg)

- Micro-USB Cable

![3](https://user-images.githubusercontent.com/41168224/161153676-93d20bce-ec0a-48a3-a13c-ad19955b7e9b.jpg)

## 3. Create an Azure IoT Central Application
- Click the [Quick Connect Application Template](https://apps.azureiotcentral.com/build/new/78386d84-b743-43d7-b0e8-f6d0b06aa0eb) and login with a valid Microsoft account (no subscription required) 

- After choosing a unique Application name, URL, and Pricing plan click ‘Create’

![4](https://user-images.githubusercontent.com/41168224/161153860-65053f1c-16c0-415f-9ad2-9957144286a2.png)

## 4. Add a Device to the Central Application

- In the menu on the left select **‘Devices’**

![5](https://user-images.githubusercontent.com/41168224/161153941-dad4e634-7477-4de1-9421-cef3d96e3061.png)

- Select **‘New’** to add a new device

![6](https://user-images.githubusercontent.com/41168224/161154006-dd5ed58e-d40b-4226-907b-686100d97187.png)

- Enter a unique **‘Device name’** and **‘Device ID’** 

- Choose **‘B-U585I-IOT02A IoT Node 2 discovery kit.’** as the Device Template.

- Make sure **‘Simulate this device’** is not selected

- And select **‘Create’**

![7](https://user-images.githubusercontent.com/41168224/161154084-3554ee3b-0b5a-4446-986b-10b2efc446ff.png)

- Your new device should now populate in the devices tab

![8](https://user-images.githubusercontent.com/41168224/161154154-1f305b0a-d2c6-4c76-b0f2-c60c7cbd31ad.png)

## 5. Collect Connection Credentials

- Click on the **‘Device Name’** of the device you want to connect to

![9](https://user-images.githubusercontent.com/41168224/161154222-0e53724b-4427-49fc-859e-ba04f03a5764.png)

- Click **‘Connect’**


![10](https://user-images.githubusercontent.com/41168224/161154277-5a32b428-ccf8-410b-9f35-8be209be3636.png)

- Here you can view all the required device Connection Credentials

![11](https://user-images.githubusercontent.com/41168224/161154365-c5c89ade-0fc5-4d5a-a87a-b9c1890949b0.jpg)

- In File Explorer Navigate to **STM32U5_Azure_QuickConnect** and open **Config.txt**

![12](https://user-images.githubusercontent.com/41168224/161154417-6ae700e4-50f7-4e7f-9a06-e9dccff6b985.jpg)

- Enter the Wi-Fi **SSID** and **Password** for your 2.4Ghz network

- Copy and Paste the **ID Scope**, **Device ID**, and **Primary Key** into this file and save.

![13](https://user-images.githubusercontent.com/41168224/161154553-5b8c4b95-dbda-4929-9ff3-b9e54f6f82c4.png)

## 6. Run Quick Connect Executable

- Connect your Discovery Kit using the Micro-USB cable as pictured below

![14](https://user-images.githubusercontent.com/41168224/161154652-a30edf8c-4eb0-435b-b5ab-e391bf89b2a5.jpg)

- Ensure that you downloaded the correct **STM32U5_Azure_QuickConnect** package for your operating system above and run the **STM32U5_AZURE_QuickConnect.exe**

![15](https://user-images.githubusercontent.com/41168224/161154700-8c356c91-345f-4683-b437-303d41b16321.jpg)

- Script logs can be seen in the window:

![16](https://user-images.githubusercontent.com/41168224/161154773-94615325-c5d2-46a8-8855-3bba48cc485a.png)

## 8. Monitor Device Activity

- Navigate back to your device in your central application and you can see a summary of the incoming data

![17](https://user-images.githubusercontent.com/41168224/161154845-0b3eefbb-e95a-4804-abeb-af3551e99d2a.png)

- Under **‘Raw data’** specific MQTT messages can be viewed

![18](https://user-images.githubusercontent.com/41168224/161154897-4fabc590-f74d-4f84-b872-e054fb95afd9.png)
