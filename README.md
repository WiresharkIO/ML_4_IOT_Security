## Anomaly Detection In IOT Networks

This project is supervised by prof. Sikora, Axel as a part of academics, University of Freiburg.

This repository deals with the analysis and implementation of Intrusion Detection in Industrial Internet Of Things(IIOT) network based on ML models and TinyML Inferences.

### References

#### Dataset

“Sebastian Garcia, Agustin Parmisano, & Maria Jose Erquiaga. (2020). IoT-23: A labeled dataset with malicious and benign IoT network traffic (Version 1.0.0) [Data set]. Zenodo. http://doi.org/10.5281/zenodo.4743746”

> Updates:
Added XGBoost classifier and converted it to ONNX model to make it deployable at microcontrollers such as STM32.
This provided an accuracy of 99% for a considerably medium-sized subset of the dataset.

> To do:
further optimizations of the XGBoost model to reduce memory footprints.
