# Neural Network Implementation Using Operating System Concepts

This project implements a neural network using separate processes and threads on a multi-core processor. It uses inter-process communication (IPC) with pipes to exchange information between processes. Each neural network layer is a separate process, and each neuron within a layer is a separate thread. This approach leverages multi-core processing to parallelize computations.

</br>

## Features and Key Aspects

1. **Parallel Processing:** Uses multi-core processors to speed up computations.
2. **Inter-Process Communication (IPC):** Utilizes pipes for efficient data exchange between processes.
3. **Batch Processing:** Processes input data in batches for efficiency.
4. **Backpropagation and Weight Update:** [To be implemented] Includes backpropagation for gradient calculation and updating weights/biases.
5. **Synchronization and Resource Management:** Ensures thread safety with proper synchronization and resource allocation. Uses semaphores or locks to control access to shared resources.
6. **Scalability and Optimization:** Enhances scalability and performance through optimized resource usage. Efficiently schedules processes and threads to optimize neural network training.
7. **Error Handling and Stability:** Provides robust error handling for stability and reliability.
8. **Process Management:** Each neural network layer is a separate process, with OS handling creation, termination, and synchronization.
9. **Thread Management:** Each neuron is a separate thread, managed by the OS for parallel processing and resource sharing.
10. **Memory Management:** Provides mechanisms for memory allocation and deallocation for processes and threads.

</br>

## Problem Statement

Neural networks mimic the human brain to solve complex problems. By using multiple cores on a processor, we can run multiple threads simultaneously, enhancing processing power. The goal is to design a system that uses this capability to parallelize neural network computations.

![NeuralNetwork Diagram](https://github.com/arfatkh/MultiThreaded-NeuralNetwork/blob/main/imgs/NN.png?raw=true)

### Requirements:

1. Each neural network layer is a separate process; each neuron in a layer is a separate thread.
2. Use IPC to exchange weights and biases between processes.
3. Process input data in batches during training.
4. Employ locking mechanisms to prevent simultaneous resource access by multiple threads.
5. Implement backpropagation to update weights and biases based on error signals.
6. Efficiently handle process synchronization, memory management, IPC, thread management, and process scheduling.

</br>

## Implementation Details

This project uses system calls and libraries common in OS labs, such as `fork()`, `wait()`, pipes, the pthread library, mutexes, and semaphores.

</br>

## Contributors

[![Muhammad Farjad](https://github.com/BeastMasterGrinder.png?size=40)](https://github.com/BeastMasterGrinder) [BeastMasterGrinder](https://github.com/BeastMasterGrinder)
