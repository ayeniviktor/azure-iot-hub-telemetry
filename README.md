# azure-iot-hub-telemetry
An end-to-end Azure IoT pipeline capturing data from a Raspberry Pi Simulator to an Azure Storage Account and virtualized on Excel



# Getting Started with Azure IoT Hub: End-to-End Telemetry Pipeline

  ## Project Overview
    This project demonstrates the implementation of a cloud-based Internet of Things (IoT) data pipeline using Microsoft Azure. The goal was to establish a secure connection with an edge device, ingest real-time simulated environmental telemetry data, process it via a       Stream Analytics Engine, and deliver structured data for business intelligence and visualization.



  ## Architecture Workflow
    1. **Data Generation:** Raspberry Pi Web Simulator mimics real-world sensor outputs.
    2. **Ingestion:** Azure IoT Hub securely captures the live telemetry data streams.
    3. **Cold Storage:** Azure Blob Storage archives the raw JSON telemetry payload.
    4. **Stream Processing:** Azure Stream Analytics filters, transforms, and outputs the stream into a structured CSV format.
    5. **Data Visualization:** Microsoft Excel utilizes line and area charts to identify operational trends.

---

  ## Technical Components & Tools Used
    * **Cloud Platform:** Microsoft Azure
    * **IoT Edge Management:** Azure IoT Hub, Raspberry Pi Web Simulator
    * **Storage Solutions:** Azure Cloud Storage Account (Blob Storage)
    * **Stream Processing:** Azure Stream Analytics
    * **Data Visualization:** Microsoft Excel

---

  ## Step-by-Step Implementation

    ### Step 1: Azure IoT Hub Provisioning
    <img width="1366" height="721" alt="Screenshot 2026-06-12 003350" src="https://github.com/user-attachments/assets/54ac4dd3-aa79-4aea-821b-368fb1418fff" />

      * I created and configured a scalable **Azure IoT Hub** instance within the Azure Portal.
      * I set up the pricing tiers and resource groups to ensure optimized resource management.

    ### Step 2: Device Registration & Simulation
      * I registered a unique device identity inside the IoT Hub to obtain a secure primary connection strings.
      * I configured the **Raspberry Pi Web Simulator** using the device connection string.  
      (LINK to the Raspberry Pi Web Simulator : https://azure-samples.github.io/raspberry-pi-web-simulator/)
      * Then I successfully initiated a live stream of Temperature and Humidity telemetry payloads from the simulator to the Azure cloud.
      
    ### Step 3: Configuring Cloud Storage
      * I provisioned an **Azure Storage Account** with a dedicated container.
      * This container acted as the long-term historical archive ("cold storage") for the unstructured data packets flowing from the IoT Hub.

    ### Step 4: Stream Analytics & Data Transformation
      * I developed an **Azure Stream Analytics Job**, which made it easy to set up real-time analytic computations on data streaming from                the IoT device, to bridge the real-time input stream with our target destinations.
      * I configured the IoT Hub as the input stream and mapped an output path to format the incoming JSON data directly into an accessible **CSV        file**.
      * Then I started the streaming job to process the data actively.

    ### Step 5: Data Analysis & Visualization
      * I exported the processed CSV data into **Microsoft Excel**.
      * I converted the processed data into **Line Charts** to track continuous variable trends over time (Temperature spikes) and **Area Charts**       to visualize the volume and scope of the environmental metrics.

---


### Key Takeaways & Skills Learned

    * **Cloud Architecture:** I gained hands-on experience routing telemetry data smoothly across between different cloud infrastructure.
    * **IoT Security:** I learnt how to safely register devices and manage individual connection tokens.
    * **Data Pipelines:** I developed a practical understanding of Extract, Transform, and Load (ETL) principles using Stream Analytics.


    Internet of Things (IoT) | Data Visualization | Data Pipelines | Cloud Storage | Interactive Data Visualization | Data Storage Technologies

---

  ### License
    This project is for portfolio. Feel free to review the code and fork the repository for personal testing. 
