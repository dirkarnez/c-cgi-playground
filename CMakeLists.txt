cmake_minimum_required(VERSION 3.24)

set(CMAKE_FIND_DEBUG_MODE TRUE)

project("c-cgi-playground" C)

# find_package(portaudio 19 EXACT REQUIRED) # PATHS "P:\\Downloads\\cpp-libraries\\portaudio\\build\\cmake\\portaudio")

# if(portaudio_FOUND)
#     message(STATUS "YES")
# else()
#     message(STATUS "NO")
# endif()

add_executable(${PROJECT_NAME}
    "src/main.c"
)

# target_link_libraries(${PROJECT_NAME} portaudio_static)
target_link_options(${PROJECT_NAME} PRIVATE "-static")
