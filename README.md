# LTC-Mapping

LTC-Mapping is a method for building object-oriented semantic maps that remain consistent in the long-term operation of mobile robots. LTC-Mapping prevents duplicate instances of objects in the semantic map, maintaining just one instance for each real object as well as is able to adapt to changes in the scene (e.g. objects that have been moved), keeping the map up-to-date with the real-world. 

An example of a semantic map built from a house of the [Robot@VirtualHome](https://github.com/DavidFernandezChaves/RobotAtVirtualHome) ecosystem:

<div align="center">
  <img src="https://github.com/MAPIRlab/LTC-Mapping-Server/blob/master/Textures/example_semantic_mapping.png?raw=true"/>
</div>

For further details, please refer to the following manuscript:

Matez-Bandera, J. L., Fernandez-Chaves, D., Ruiz-Sarmiento, J. R., Monroy, J., Petkov, N. and Gonzalez-Jimenez, J. **LTC-Mapping, Enhancing Long-term Consistency of Object-oriented Semantic Maps in Robotics**. Under Review.

## License

If you use LTC-Mapping in an academic work, please cite:

```
@article{matez2022,
  title={LTC-Mapping, Enhancing Long-term Consistency of Object-oriented Semantic Maps in Robotics},
  author={Matez-Bandera, J. L., Fernandez-Chaves, D., Ruiz-Sarmiento, J. R., Monroy, J., Petkov, N. and Gonzalez-Jimenez, J.},
  journal={Under Review}
```

## Requeriments

LTC-Mapping is implemented following a distributed architecture. On the one hand, the client version have to be installed in the robots, which are in charge of the data acquisition. On the other hand, the server version should be installed in the server, which is in charge of the building and maintenance of the semantic map. A detailed description of the requeriments of each version is included in their respective repositories.

### LTC-Mapping - Server
The repository of the server version can be found in [LTC-Mapping - Server](https://github.com/MAPIRlab/LTC-Mapping-Server). It requires Unity 3D version 2020.3.18f1.

### LTC-Mapping - Client
The repository of the client version can be found in [LTC-Mapping - Client](https://github.com/MAPIRlab/LTC-Mapping-Client). It requires:
  - [Robotic Operating System (ROS)](https://www.ros.org/). Our scripts are released as ROS nodes.
  - [RosBridge](http://wiki.ros.org/rosbridge_suite). It is necessary in order to establish the communication between ROS (client) and Unity 3D (server).
  - [Detectron2 CNN](https://github.com/DavidFernandezChaves/Detectron2_ros) (Replaceable). Our method uses Detectron2 for object detection. Yet, the object detection algorithm can be easily replaced by another one.

