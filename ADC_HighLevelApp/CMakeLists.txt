#  Copyright (c) Microsoft Corporation. All rights reserved.
#  Licensed under the MIT License.

CMAKE_MINIMUM_REQUIRED(VERSION 3.8)
PROJECT(ADC_HighLevelApp C)

# Create executable
#ADD_EXECUTABLE(${PROJECT_NAME} main.c eventloop_timer_utilities.c)
ADD_EXECUTABLE(${PROJECT_NAME} main.c oled.c sd1306.c i2c.c eventloop_timer_utilities.c )
TARGET_LINK_LIBRARIES(${PROJECT_NAME} applibs pthread gcc_s c)

# Add MakeImage post-build command
INCLUDE("${AZURE_SPHERE_MAKE_IMAGE_FILE}")
