# Autonomous-Driving
Creating a Simulation for Autonomous Car
Steering Control Using Normalized Direction Vector for Autonomous Vehicle Navigation
In autonomous vehicle navigation systems like CARLA, the normalized direction vector plays a crucial role in steering control. Here's how it works:
CARLA (Car Learning to Act) is an open-source, high-fidelity autonomous driving simulator designed for research and development in the fields of autonomous vehicles, robotics, and reinforcement learning. It provides a realistic environment for testing and training AI models for self-driving cars.
Key Features of CARLA
1. Realistic Environment
2. Sensor Simulation
3. Python API
4. Multi-Agent Support
5. Scenario Runner
6. Open-Source and Modular

Applications of CARLA
1. Research and Development
2. Training Perception Models
3. Reinforcement Learning
4. Testing Autonomous Systems


Waypoint in CARLA (Short Explanation):
A waypoint in CARLA represents a specific position on the road network with additional information like lane type and orientation.
Each waypoint has:
1. Location (x, y, z): 3D position in the world.
2. Rotation (yaw): Direction the lane is facing (in degrees).
3. Lane information: Type, lane ID, lane width, etc.

Normalized direction Vector calculation using waypoint:
A waypoint represents a location in the CARLA world. To understand the calculation let’s take an example the current waypoint (car location) and the next waypoint assuming 25 
•	c_x: The x-coordinate of the vehicle's current position.
•	c_y: The y-coordinate of the vehicle's current position.

 Waypoint Position:
•	w_x: The x-coordinate of the target waypoint.
•	w_y: The y-coordinate of the target waypoint.

Direction Vector:
•	x: The x-component of the normalized direction vector.
•	y: The y-component of the normalized direction vector.

Calculate the Differences:
•	(w_x - c_x): The difference in the x-coordinates between the waypoint and the vehicle.
•	(w_y - c_y): The difference in the y-coordinates between the waypoint and the vehicle.

Calculate the Euclidean Distance:
This ensures the direction vector is normalized (i.e., has a magnitude of 1).
           ![image](https://github.com/user-attachments/assets/be3b5942-06c8-428a-b610-165e5577c019)




Normalize the Direction Vector:
The x and y components of the direction vector are calculated by dividing the differences by the Euclidean distance:

![image](https://github.com/user-attachments/assets/0874ef63-ec0b-4090-b531-1257e49ca564)

 

(x, y) is a unit vector pointing from the vehicle's current position to the target waypoint.

•	This normalized direction vector is often used to calculate the steering angle or to guide the vehicle toward the waypoint.
•	For example, the steering angle can be computed using the arctangent of the direction vector:
                 
                  ![image](https://github.com/user-attachments/assets/c016b096-3995-4441-8edb-8332b259e8e7)
                 



The formula calculates the normalized direction vector from the vehicle's position to a target waypoint. This vector is used in navigation systems to determine the direction the vehicle should move or steer. The normalization ensures the vector has a magnitude of 1, making it easier to work with in calculations like steering control.

Conclusion:
The use of a normalized direction vector is a fundamental technique in autonomous vehicle navigation systems like CARLA. By calculating the direction from the vehicle's current position to a target waypoint and normalizing it, we obtain a unit vector that simplifies steering control calculations. This vector is used to compute the steering angle, which guides the vehicle along the desired path.
The normalization process ensures that the direction vector is independent of the distance to the waypoint, making it robust and reliable for real-time navigation. This approach is essential for achieving smooth, accurate, and efficient steering control in autonomous driving scenarios. By leveraging this method, developers can create more responsive and intelligent autonomous vehicles capable of navigating complex environments with precision.
