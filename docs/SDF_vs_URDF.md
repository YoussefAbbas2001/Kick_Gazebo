
URDF files are often used in ROS to represent robot models. While SDF can describe a world with multiple robot models, URDF can only describe one robot model.

## What is Different between SDF and URDF:
URDF can be used for specifying only the kinematic and dynamic properties of a single robot in isolation. URDF can not specify the pose of the robot itself within a world. It is also not a "universal" description format since it cannot specify joint loops, and it lacks friction and other properties. Additionally, it cannot specify things that are not robots, such as lights, heightmaps, etc.

On an implementation side, the URDF syntax breaks proper formatting with heavy attributes which in turns makes URDF more inflexible. There is also no mechanism for backward compatibility.

SDF solves all these problems. It is a complete description for everything from the world level down to the robot level. It is highly scalable, and extremely easy to add and modify elements. The SDF format is itself described using XML, which facilitates a simple upgrade tool to migrate old versions to new versions. It is also self descriptive.