# object_grabber
Example action server to accept high-level commands to acquire objects.
Objects are defined via object codes in the action message.
A goal contains an object code and a pose describing the frame of the object.
The action server should accept these goal specifications and perform an appropriate
sequence of actions to acquire the specified object at the specified location.

Start up the simulator with:
`roslaunch baxter_gazebo baxter_world.launch`
Enable the robot with:
`rosrun baxter_tools enable_robot.py -e`
Add a table with:
`roslaunch exmpl_models add_cafe_table.launch`
Add a toy block with:
`roslaunch exmpl_models add_toy_block.launch`
Add a small, upright cylinder with:
`roslaunch exmpl_models add_small_cylinder.launch`
Start up CWRU nodes with:
`roslaunch baxter_launch_files baxter_nodes.launch`

## Using the object-grabber action server:
Start up a client (e.g., the example client in this package):
`rosrun object_grabber example_object_grabber_ac` 
This example client node should send (hard-coded) poses to grab the toy block and the small cylinder.
This example client is a stand-in for a more general, perception-based grabber client.   