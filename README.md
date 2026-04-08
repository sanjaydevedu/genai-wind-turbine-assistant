#1. Problem Statement

    Large-scale wind turbine manufacturers face downtime due to delayed troubleshooting and dependency on human SMEs.

2. Business Objectives
   
    Reduce turbine downtime
    Improve SME productivity
    Enable faster decision-making

3. Solution Overview

    Designed a GenAI-powered assistant using Amazon Web Services services to provide real-time troubleshooting and recommendations.

4. Architecture(Flow and the diagram):

    Flow:
        User query → API
        API → Lambda
        Lambda → Amazon Bedrock
        Model (Amazon Nova Pro) processes
        Response returned
        Logs → Amazon CloudWatch

    Diagram: Please refer to the file name "architecture-diagram.png".

5. Tech Stack

    Compute: AWS Lambda
    API Layer: Amazon API Gateway
    AI: Amazon Bedrock
    SDK: Boto3
    Observability: Amazon CloudWatch

6. Key Features

    Natural language troubleshooting
    SME knowledge augmentation
    Scalable serverless architecture
    Observability with logging + metrics

7. Demo Query/ Prompt:
      a. Why is turbine X overheating?
      b. Incident Report Date – 03-02-2024
        Wind Farm ID – WF-NORTH-ATL-09
        Turbine Model – TB-EX-11000
        Turbine Serial Number – SN-11000-4478
        Operational Hours – 24,965 hours
        Primary Issue – Sudden shutdown triggered automatically by the SCADA system due to abnormal vibration spikes and thermal escalation alerts within the nacelle assembly.
        Mechanical Observation – Severe microfractures detected in Blade B2 near the root junction. Rotor imbalance measured at 3.8 mm/s exceeding the acceptable threshold of 2.0 mm/s.
        Gearbox Status – Metallic particle contamination identified in lubrication oil from Gearbox Unit GB-11000-9921, indicating possible bearing wear.
        Generator Status – Output voltage fluctuation observed between 580–620V despite stable wind conditions.
        Yaw System – Delayed yaw response of approximately 4.2 seconds during gust alignment, causing temporary aerodynamic inefficiency.
        Cooling System – Nacelle cooling fan CF-11000-221 reported intermittent malfunction; internal nacelle temperature peaked at 92°C.
        Electrical Systems – Control panel CP-11000-778 logged repeated inverter fault codes (IFC-32), suggesting power conversion instability.
        Brake System – Hydraulic brake pressure dropped to 48 bar, below the required operational threshold of 60 bar.
        Sensor Diagnostics – Vibration sensor VS-11000-443 showed calibration drift of +6% from baseline parameters.
        Weather Conditions – Wind speed steady at 13–15 m/s with no extreme weather events recorded at the time of failure.
        Last Preventive Maintenance Date – 15-01-2024.
        Last Maintenance Notes – Routine lubrication completed and firmware patch v3.4 applied; no anomalies detected during inspection.
        Potential Root Cause – Progressive gearbox bearing degradation leading to vibration amplification, which caused cascading mechanical stress on the rotor assembly and secondary electrical                 instability   across the generator and inverter systems.
        Operational Impact – Turbine remained offline for 6.5 hours, resulting in an estimated production loss of 4.8 MWh.

9. Output:
    Please see the file with name "Output.jpg"

10. Impact:

    Reduced troubleshooting time by X%
    Improved SME efficiency
    Faster root cause analysis

11. Future Improvements:
    
    Add RAG (Retrieval-Augmented Generation)
    Fine-tuned domain-specific model
