cmake_minimum_required(VERSION 3.10)

######################################################################################
# 1) Set your application properties up
######################################################################################

# Define your project name
project(executable)

# Define your the compiler version (if you followed the I-Campus tutorial, it's C++ 23)
set(CMAKE_CXX_STANDARD 17)

# Define language
enable_language(C)
enable_language(CXX)

######################################################################################
# 2) Setup standard paths
######################################################################################

# Include sources from /src
include_directories(${CMAKE_SOURCE_DIR}/src)

# Add /bin for binary compilation
# --> Requires a CMakeList.txt file in /bin
add_subdirectory(bin)

# Add /src for librairies compilation
# --> Requires a CMakeList.txt file in /src
add_subdirectory(src)
