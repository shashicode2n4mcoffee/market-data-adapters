cmake_minimum_required(VERSION 3.10)
project(MarketDataAdapters)

# Specify C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Add the external directory for QuickFIX
add_subdirectory(external/quickfix)

# Include QuickFIX headers
include_directories(external/quickfix/src)

# Define the executable
add_executable(MarketDataAdapters src/MarketDataAdapters.cpp)

# Link QuickFIX libraries
target_link_libraries(MarketDataAdapters PRIVATE quickfix)
