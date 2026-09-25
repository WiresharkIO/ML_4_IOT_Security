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

<img width="1920" height="1080" alt="IOT_system" src="https://github.com/user-attachments/assets/13a063f7-349e-43cc-b9ad-e792ad5dceea" />


---------------------------------
### Updates
---------------------------------


---------------------------------
### References
---------------------------------
#### Dataset

“Sebastian Garcia, Agustin Parmisano, & Maria Jose Erquiaga. (2020). IoT-23: A labeled dataset with malicious and benign IoT network traffic (Version 1.0.0) [Data set]. Zenodo. http://doi.org/10.5281/zenodo.4743746”

> Updates:
1. Added XGBoost classifier and converted it to ONNX model to make it deployable at microcontrollers such as STM32.
This provided an accuracy of 99% for a considerably medium-sized subset of the dataset.
2. Quantized the model using ONNX dynamic quantize.
3. Updated inferencing code to check model output using ONNX runtime.

> To do:
further optimizations of the XGBoost model to reduce memory footprints.
