cmake_minimum_required(VERSION 3.5)

project(DTLSClient LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Qt5 COMPONENTS Widgets Network REQUIRED)

add_executable(DTLSClient
  main.cpp
  MainWindow.cpp
  MainWindow.h
  MainWindow.ui
  DTLSClient.h
  DTLSClient.cpp
  DTLSConfigurationFactory.h
  DTLSConfigurationFactory.cpp
)

target_link_libraries(DTLSClient PRIVATE Qt5::Widgets Qt5::Network)
