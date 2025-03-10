add_executable(myFirstFrontend main.cpp)

target_link_libraries(myFirstFrontend
    PRIVATE
    fmt::fmt
)
