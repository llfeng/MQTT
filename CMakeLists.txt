
cmake_minimum_required(VERSION 2.8)


project (MQTT)



aux_source_directory(. DIR_SRCS)

add_subdirectory(MQTTPacket)

add_subdirectory(MQTTClient)

add_executable(MQTT ${DIR_SRCS})

target_link_libraries(MQTT paho-embed-mqtt paho-embed-mqtt-app)

#target_link_libraries(MQTTPacket MQTTClient)

