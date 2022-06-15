# LTC-Mapping

## Abstract
This paper proposes LTC-Mapping, a method for building object-oriented semantic maps that remain consistent in the long-term operation of mobile robots. Among the different challenges that compromise this aim, LTC-Mapping focuses on two of the more relevant ones: preventing duplicate instances of objects (instance duplication) and handling dynamic scenes. The former refers to creating multiple instances of the same physical object in the map, usually as a consequence of partial views or occlusions. The latter deals with the typical assumption made by object-oriented mapping methods that the world is static, resulting in outdated representations when the objects change their positions.

To face these issues, we model the detected objects with 3D bounding boxes, and analyze the visibility of their vertices to detect occlusions and partial views. Beside this geometric modeling, the boxes are augmented with semantic information regarding the categories of the objects they represent. Both the geometric entities (bounding boxes) and their semantic content are propagated over time through data association and a fusion technique. 

In addition, in order to keep the map curated, the non-detection of objects in the areas where they should appear is also considered, proposing a mechanism that removes them from the map once there is evidence that they have been moved (i.e. multiple non-detections occur). To validate our proposal, a number of experiments have been carried out using the Robot@VirtualHome ecosystem, comparing its performance with a state-of-the-art alternative. The results report a superior performance of LTC-Mapping when modeling both geometric and semantic information of objects, and also support its online execution.

## Requeriments

LTC-Mapping is implemented following a distributed architecture. On the one hand, the client version have to be installed in the robots, which are in charge of the data acquisition. On the other hand, the server version should be installed in the server, which is in charge of the building and maintenance of the semantic map. A detailed description of the requeriments of each version is included in their respective repositories.

- [LTC-Mapping - Server](https://github.com/MAPIRlab/LTC-Mapping-Server)
- [LTC-Mapping - Client](https://github.com/MAPIRlab/LTC-Mapping-Client)

## Example of a Semantic Map Built by LTC-Mapping
Result obtained in the [Robot@VirtualHome](https://github.com/DavidFernandezChaves/RobotAtVirtualHome) ecosystem:
<div align="center">
  <img src="https://github.com/MAPIRlab/LTC-Mapping-Server/blob/master/Textures/example_semantic_mapping.png?raw=true"/>
</div>


