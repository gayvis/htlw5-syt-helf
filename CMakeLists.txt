cmake_minimum_required(VERSION 3.13)
project(htlw5_syt_raspi C)

set(CMAKE_C_STANDARD 11)

add_executable(htlw5_syt_raspi lcd/sensor_dht11.c libs/lcd_i2c.c libs/lcd_i2c.h)

target_link_libraries(htlw5_syt_raspi wiringPi pthread m)