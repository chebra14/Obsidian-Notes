#### Section 2

When to use ROS2
- When using arduino, etc.
	- The more complicated it gets when adding actuators, controllers, sensors.
- Robot software, communication between sub programs
- Goes beyond simple use case

What is it?
- Code separation and communication tools
- Tools and P&P libraries


#### Section 15

Packages
- Separates code into blocks

`ros2 pkg create my_py_pkg --build-type ament_python --dependencies rclpy`

Creates the package in the src folder. Go to the name in visual studio (`code .`), Then whatever nodes you create will be in `my_py_pkg > my_py_pkg`

You can build a specific package in the workspace

`colcon build --packages-select my_py_pkg`

#### Section 17

What is a node?

Nodes are put into packages and then communicate with each other

#### Section 18

Basic format

`#!usr/bin/env python3  
`import rclpy

`def main(args =None):  
    `rclpy.init(args=args)    
    `node = MyNode()`
    `rclpy.shutdown()`

`if __name__ == "__main__":  
    `main()`
`
Mark the node as executable

`chmod +x my_first_node.py`

Launch it

`./my_first_node.py`

executable:

in the console scripts brackets - setup.py

`"py_node = my_py_pkg.my_first_node:main"`

Start the node:

`source .bashrc`
`ros2 run my_py_pkg py_node`


#### Section 19

After making changes to the node, build it, then run it.