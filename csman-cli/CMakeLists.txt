set(CSMAN_CLI_SOURCE_DIR ${PROJECT_SOURCE_DIR}/csman-cli)
message(STATUS "Configuring csman-cli: module root path: ${CSMAN_CLI_SOURCE_DIR}")

include_directories(include)

#### sources
set(CSMAN_CLI_SRC
        include/csman/cli/progress.hpp
        src/progress.cpp
        src/main.cpp)

add_executable(csman ${CSMAN_CLI_SRC})
target_link_libraries(csman mozart++)
target_link_libraries(csman csman-core)
target_link_libraries(csman csman-os)

