# Move-It
In this project, contains two ROS packages: the my_robot and the ball_chaser. Here the robot has been placed inside your world, and programed to chase white-colored balls-

    drive_bot:
        Created a my_robot ROS package to hold the robot, the white ball, and the world.
        Design a differential drive robot with the Unified Robot Description Format. Added two sensors to the robot: a lidar and a camera. Added Gazebo plugins for your robot’s differential drive, lidar, and camera. 
        
    ball_chaser:
        Created a ball_chaser ROS package to hold your C++ nodes.
        Drive_botC++ node will provide a ball_chaser/command_robot service to drive the robot by controlling its linear x and angular z velocities. The service publishes to the wheel joints and returns the requested velocities.
        Process_image C++ node reads the robot’s camera image, analyzes it to determine the presence and position of a white ball. If a white ball exists in the image, the node requests a service via a client to drive the robot towards it.
        The ball_chaser.launch should run both the drive_bot and the process_image nodes.
