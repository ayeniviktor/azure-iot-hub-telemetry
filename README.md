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
      * I created and configured a scalable **Azure IoT Hub** instance within the Azure Portal.
      * I set up the pricing tiers and resource groups to ensure optimized resource management.
<img width="1366" height="721" alt="Screenshot 2026-06-12 003458" src="https://github.com/user-attachments/assets/e59a1f9d-6061-4d25-838b-ea4484f7360e" />


    ### Step 2: Device Registration & Simulation
      * I registered a unique device identity inside the IoT Hub to obtain a secure primary connection strings.
  <img width="1366" height="721" alt="Screenshot 2026-06-12 004120" src="https://github.com/user-attachments/assets/c2f5e198-7f4c-431f-b190-1eba74f62854" />
      * I configured the **Raspberry Pi Web Simulator** using the device connection string.  
      (LINK to the Raspberry Pi Web Simulator : https://azure-samples.github.io/raspberry-pi-web-simulator/)
      <img width="1361" height="679" alt="Screenshot 2026-06-17 165712" src="https://github.com/user-attachments/assets/b1edd16a-ff0c-4e48-9122-b6c336cb1225" />
      * Then I successfully initiated a live stream of Temperature and Humidity telemetry payloads from the simulator to the Azure cloud.

      
    ### Step 3: Configuring Cloud Storage
      * I provisioned an **Azure Storage Account** with a dedicated container.
  <img width="1366" height="721" alt="Screenshot 2026-06-12 024946" src="https://github.com/user-attachments/assets/c346ff5d-1902-466b-a68c-e479d897e478" />
      * This container acted as the long-term historical archive ("cold storage") for the unstructured data packets flowing from the IoT Hub.
  <img width="1366" height="721" alt="Screenshot 2026-06-12 025517" src="https://github.com/user-attachments/assets/b2360fb9-59dd-4a99-8dff-1ed85d12e908" />


    ### Step 4: Stream Analytics & Data Transformation
      * I developed an **Azure Stream Analytics Job**, which made it easy to set up real-time analytic computations on data streaming from                the IoT device, to bridge the real-time input stream with our target destinations.
  <img width="1366" height="721" alt="Screenshot 2026-06-12 015021" src="https://github.com/user-attachments/assets/8dfd3b20-91b4-4dfb-9a07-0b4c41680eea" />
      * I configured the IoT Hub as the input stream and mapped an output path to format the incoming JSON data directly into an accessible **CSV        file**.
      * Then I started the streaming job to process the data actively.
<img width="1366" height="721" alt="Screenshot 2026-06-12 022317" src="https://github.com/user-attachments/assets/f5c71637-bc58-4fb2-b670-c3eb3757c13c" />

      
    ### Step 5: Data Analysis & Visualization
      * I exported the processed CSV data into **Microsoft Excel**.
  <img width="1366" height="721" alt="Screenshot 2026-06-12 031455" src="https://github.com/user-attachments/assets/5d7819c5-5f3d-45cc-8af9-8ad427f981c8" />
      * I converted the processed data into **Line Charts** to track continuous variable trends over time (Temperature spikes) and **Area Charts**       to visualize the volume and scope of the environmental metrics.
<img width="1366" height="721" alt="Screenshot 2026-06-12 032559" src="https://github.com/user-attachments/assets/613b9f25-47b3-4efa-a51f-a837d579b102" />



---


### Key Takeaways & Skills Learned

    * **Cloud Architecture:** I gained hands-on experience routing telemetry data smoothly across between different cloud infrastructure.
    * **IoT Security:** I learnt how to safely register devices and manage individual connection tokens.
    * **Data Pipelines:** I developed a practical understanding of Extract, Transform, and Load (ETL) principles using Stream Analytics.


    Internet of Things (IoT) | Data Visualization | Data Pipelines | Cloud Storage | Interactive Data Visualization | Data Storage Technologies

---

  ### License
    This project is for portfolio. Feel free to review the code and fork the repository for personal testing. 
