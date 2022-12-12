cmake_minimum_required(VERSION 3.0.2)
project(upo_sgg_msgs)

find_package(catkin REQUIRED COMPONENTS
	std_msgs
	sensor_msgs
	geometry_msgs
	vision_msgs
	message_generation
)

add_message_files(FILES
	IndividualHypothesis.msg
	RelationHypothesis.msg
	SceneGraphHypothesis.msg
	SceneDigest.msg

)

add_service_files(FILES
	FetchControl.srv
)

#add_action_files(DIRECTORY action FILES
#	(Action files go here)
#)

generate_messages(DEPENDENCIES
	std_msgs
	sensor_msgs
	geometry_msgs
	vision_msgs
)

catkin_package(
	CATKIN_DEPENDS
		std_msgs
		sensor_msgs
		geometry_msgs
		vision_msgs
		message_runtime
)
