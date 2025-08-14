# Distributed Anomaly Detection Using Machine Learning Techniques

## Abstract
The Internet of Things (IoTs) is a network of physical objects that use sensors to collect data and transmit them to a central hub. The security of IoT networks has been a growing concern, particularly in critical applications, such as healthcare, where lives may be at stake. Such IoT networks are usually vulnerable to security attacks such as denial of service (DoS) attacks. Anomaly detection is an effective approach to identifying such security threats, but its implementation in IoT networks poses challenges due to the large number of devices involved, their diverse tasks, and resource limitations.

In this research, we propose a distributed anomaly detection system for IoT networks that uses a charge-assignment algorithm to assign two charges to each node in a cluster, with each node serving as both a monitor and a charge. We also propose a behavior-analysis algorithm that consists of two phases: a behavior assessment phase that learns a node's normal behavior and a machine learning assessment phase that continuously evaluates the node's behavior. Monitors keep track of sensed data and transmissions from their charges and use the behavior-analysis algorithm to detect anomalies, resulting in the deactivation of only the faulty node.

We demonstrate the effectiveness of our proposed solution using a simulated IoT system with 24, 48, and 96 IoT programmable devices and bases, and the NS-3 network simulator. Our proposed solution is effective in detecting single faulty nodes per cluster, resulting in a distributed and efficient anomaly detection system for IoT networks.

---

## Files and Their Functions

### `KMeans.py`
This file implements the k-means clustering algorithm used to organize the network into clusters in order to minimize power consumption due to cluster transmissions. It also assigns cluster heads and monitors nodes within each cluster.

### `Node.py`
This file implements the `Node` class, which simulates communication for each node in the cluster. It includes methods for charge assignment, anomaly detection, and communication between nodes.

### `values3.txt`
This file contains the dataset used for clustering, including 3D coordinates for each node and information about cluster heads, monitors, and charges.

### `__MACOSX/`
This directory contains macOS-specific metadata files generated during compression. These files are not part of the project and can be ignored.

---

## How to Run
1. Ensure you have Python installed on your system.
2. Install the required dependencies using:
   ```sh
   pip install pyclustering scipy numpy
   ```
3. Run the `KMeans.py` file to simulate the clustering and anomaly detection process:
   ```sh
   python ITAP/KMeans.py
   ```

---

## Results
The simulation demonstrates the effectiveness of the distributed anomaly detection system in identifying faulty nodes within IoT clusters. The system minimizes energy consumption and ensures efficient detection of anomalies.

---

## License
This project is licensed under the MIT License.