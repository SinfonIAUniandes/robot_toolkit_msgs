cmake_minimum_required(VERSION 2.8.3)
project(robot_toolkit_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  std_msgs
  sensor_msgs
)

add_message_files(
  FILES
  navigation_tools_msg.msg
  depth_to_laser_msg.msg
  vision_tools_msg.msg
  camera_parameters_msg.msg
  audio_tools_msg.msg
  speech_msg.msg
  speech_parameters_msg.msg
  audio_localization_msg.msg
  motion_tools_msg.msg
  animation_msg.msg
  set_angles_msg.msg
  misc_tools_msg.msg
  leds_parameters_msg.msg
  face_detection_msg.msg
  path_msg.msg
  special_settings_msg.msg
  touch_msg.msg
  speech_recognition_status_msg.msg
  text_to_speech_status_msg.msg
  )

add_service_files(
  FILES
  navigation_tools_srv.srv
  vision_tools_srv.srv
  audio_tools_srv.srv
  motion_tools_srv.srv
  misc_tools_srv.srv
  speech_recognition_srv.srv
  tablet_service_srv.srv
  go_to_posture_srv.srv
  get_input_srv.srv
  set_speechrecognition_srv.srv
  set_output_volume_srv.srv
  point_at_srv.srv
  set_open_close_hand_srv.srv
  set_angle_srv.srv
  move_head_srv.srv
  get_segmentation3D_srv.srv
  set_move_arms_enabled_srv.srv
  navigate_to_srv.srv
  Tshirt_color_srv.srv
  set_stiffnesses_srv.srv
  battery_service_srv.srv
  say_to_file_srv.srv
  set_words_threshold_srv.srv
  set_security_distance_srv.srv
  )
  
generate_messages(DEPENDENCIES std_msgs  sensor_msgs)

catkin_package( CATKIN_DEPENDS message_runtime std_msgs )



