
cmake_minimum_required(VERSION 2.8)


project (MQTT)



include_directories(./MQTTPacket)

aux_source_directory(. DIR_SRCS)

add_subdirectory(MQTTPacket)


add_executable(MQTT ${DIR_SRCS})

target_link_libraries(MQTT paho-embed-mqtt )

#target_link_libraries(MQTTPacket MQTTClient)

