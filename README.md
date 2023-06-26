
# Neural Network Implementation using Operating System Concepts

This project implements a neural network architecture using separate processes and threads on a multi-core processor. The operating system utilizes inter-process communication through pipes to exchange information, such as weights and biases, between processes. Each layer of the neural network is represented as a separate process, while each neuron within a layer is treated as a separate thread. The system leverages the processing power of multiple cores to parallelize the computation of the neural network.


## Features
1. **Parallel Processing:** Utilizes multi-core processing to accelerate computation and improve performance.
2. **Inter-Process Communication:** Uses pipes for efficient information exchange between processes.
3. **Batch Processing**: Divides input data into batches for efficient processing and training.
4. **Backpropagation and Weight Update: [To be implemented]** Implements backpropagation algorithm for gradient calculation and weight/bias updates.
5. **Synchronization and Resource Management:** Ensures proper synchronization and resource allocation for thread safety.
6. **Scalability and Performance Optimization:** Optimizes resource utilization for scalability and optimal performance.
7. **Error Handling and Stability:** Implements robust error handling to maintain stability and reliability.



## Problem Statement

Neural networks are a popular machine learning technique that emulates the structure and function of the human brain to solve complex problems. In a multi-core processor, multiple cores can execute multiple threads simultaneously, thereby increasing the overall processing power of the system. The goal of this project is to design an operating system that utilizes this capability to parallelize the computation of a neural network.

![NeuralNetwork Diagram](https://github.com/arfatkh/MultiThreaded-NeuralNetwork/blob/main/imgs/NN.png?raw=true)


The specific requirements for the implementation are as follows:

1. Each layer of the neural network should be represented as a separate process, and each neuron within a layer should be treated as a separate thread.
2. Inter-process communication (IPC) should be used to exchange information, such as weights and biases, between processes.
3. During training, a batch-based approach should be used, where input data is divided into smaller batches, and each batch is processed by a separate layer in the network.
4. Locking mechanisms should be employed to prevent multiple threads from accessing the same resource simultaneously.
5. During backpropagation, the error signal should be propagated backward through the layers of the network, and the system should update the weights and biases based on the calculated gradients.
6. Process synchronization, memory management, inter-process communication, thread management, and process scheduling should be implemented efficiently.


## Implementation Details

To meet the project requirements, the implementation utilizes system calls and libraries commonly used in operating system labs, such as `fork()`, `wait()`, pipes (both named and unnamed), the pthread library, mutexes, semaphores, and other relevant constructs.

Key aspects  considered during the implementation:

1. Process Management: Each layer of the neural network is represented as a separate process. The operating system handles process creation, termination, and synchronization.
2. Thread Management: Each neuron within a layer is treated as a separate thread. The operating system manages threads efficiently, considering parallel processing and resource sharing.
3. Inter-Process Communication: Information exchange, such as weights and biases, is facilitated through pipes or other suitable forms of inter-process communication.
4. Process Synchronization: Synchronizationenter code here primitives, such as semaphores or locks, are used to ensure that only one process accesses shared resources (e.g., weights and biases) at any given time.
5. Memory Management: The operating system provides mechanisms for memory allocation and deallocation for the neural network processes and threads. Each process and thread has its own memory space to avoid conflicts.
6. Process Scheduling: The operating system schedules processes and threads efficiently to optimize the training process of the neural network.


## Contributors
[![Muhammad Farjad ](https://github.com/BeastMasterGrinder.png?size=40)](https://github.com/BeastMasterGrinder)[  BeastMasterGrinder](https://github.com/BeastMasterGrinder)




