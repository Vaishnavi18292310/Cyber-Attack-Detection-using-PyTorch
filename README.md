# Cyber-Attack-Detection-using-PyTorch
<img width="800" height="500" alt="image" src="https://github.com/user-attachments/assets/b9f1482f-51ef-4956-af39-87f767ed85fd" />
</br>
This project involves designing and implementing a deep learning model to detect cyber threats in network traffic logs using the BETH dataset. The model is trained to identify anomalies that could indicate potential cyber attacks, contributing to enhanced cybersecurity measures.

**Project Overview**
---
As a cybersecurity analyst, identifying and mitigating cyber threats is crucial. In this project, a neural network model is built using PyTorch to detect anomalies in network traffic data, specifically focusing on identifying suspicious events. The BETH dataset simulates real-world logs, providing a rich source of information for training and testing the model.

**Dataset**
---
The BETH dataset includes various features extracted from network logs, with a target label sus_label indicating whether an event is malicious (1) or benign (0).

**Features**
- processId: The unique identifier for the process that generated the event.
- threadId: ID for the thread spawning the log.
- parentProcessId: Label for the process spawning this log.
- userId: ID of the user spawning the log.
- mountNamespace: Mounting restrictions the process log works within.
- argsNum: Number of arguments passed to the event.
- returnValue: Value returned from the event log (usually 0).
- sus_label: Binary label indicating a suspicious event (1 is suspicious, 0 is not).

**Model Architecture**
---
The neural network model is a simple feed-forward neural network built using PyTorch's nn.Sequential. The architecture consists of:

- Input Layer: Corresponding to the number of features in the dataset.
- Hidden Layers:
     - 64 neurons, ReLU activation, 30% dropout.
     - 32 neurons, ReLU activation.
- Output Layer: 1 neuron with Sigmoid activation for binary classification.

</hr>
**Training**
---
The model was trained using Binary Cross Entropy loss (nn.BCELoss) and the Adam optimizer. The training loop ran for 20 epochs, with the goal of achieving a validation accuracy of at least 60%.

**Results**
---

Best Validation Accuracy: val_accuracy%
