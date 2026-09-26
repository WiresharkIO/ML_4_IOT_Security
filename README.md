<img width="1000" height="50" alt="github_asthetics_cyber_security" src="https://github.com/user-attachments/assets/41fc3139-697e-458d-96d6-5f460f4672b7" />

## Anomaly Detection In IOT Networks

This project is supervised by prof. Sikora, Axel as a part of academics, University of Freiburg.

This repository deals with the analysis and implementation of Intrusion Detection in Industrial Internet Of Things(IIOT) network based on ML models and TinyML Inferences.

---------------------------------
### Background
---------------------------------
Why this project?

- This approach acts as a Smart Gateway, which allows data forwarding to the Central node (in our case a "Raspberry Pi 3 Model-B) if it is Benign, and if it is Malicious, it blocks it.

In real enterprise scenario this gateway will be acting as an intermediate node between sensor/consumer devices/etc and the central node (could be a raspberry pi where decision making happens based on the sensor data) to offload security screenings from the central node.

This kind of system is usually deployed to prevent botnet-attacks (a botnet is a network of internet-connected devices infected with malware and controlled remotely by a hacker), where devices get infected through malicious links, phishing emails, or weak passwords.

---------------------------------
### System
---------------------------------

<img width="1718" height="1055" alt="IOT_system" src="https://github.com/user-attachments/assets/65514cf1-e2b2-4617-96f1-61f62ae63771" />


> This system consists of an esp32 based sensor (an acting device, ideally this is the device which should be running packet sniffing and formatting the packets to structured formats using zeek), which sends simulated network information (in current stage of this project, it is the IOT-23 dataset) to the raspberry pi gateway (an acting device, where interception of the incoming data and detection using ML/DL, rule based inference, and ensemble based hybrid inference takes place).

---------------------------------
### Considerations
---------------------------------

This study is meant for designing a system which can act as a gateway to detect anomalies in a network, it focuses on:
- model design and development and/or hybrid ensemble strategies
- deploying developed model on resource constrained device (Raspberry pi 3 model-B in our case))
- communication over local network device(s) (wifi) with mqtt protocol and mosquitto (broker)
- evaluates on-device parameters like latency/memory-consumption
- off-device parameters like FLOPs (for models)
- realtime adherence (yet to be decided on the approach based on the evaluation parameters on-device)

It should be noted that the offloading work of network behaviour by collecting network parameters is done by using IOT-23 dataset, but it can be monitored using combination of tools like tcpdump/wireshark and zeek.

---------------------------------
### References
---------------------------------

Garcia, S., Parmisano, A., & Erquiaga, M. J. (2020). IoT-23: A labeled dataset with malicious and benign IoT network traffic [Data set]. Zenodo. https://doi.org/10.5281/ZENODO.4743745

> Updates:
1. Added XGBoost classifier and converted it to ONNX model to make it deployable at microcontrollers such as STM32.
This provided an accuracy of 99% for a considerably medium-sized subset of the dataset.
2. Quantized the model using ONNX dynamic quantize.
3. Updated inferencing code to check model output using ONNX runtime.

> To do:
further optimizations of the XGBoost model to reduce memory footprints.
