##
##
##


# Creating the executable
add_executable(Test-App 
    "./src/main.cpp" # Main app file
)

##
## Config GLFW 3
##
set(GLFW3_STATIC_LIB_PATH "../Dependecies/glfw3/lib64")
set(GLFW3_INCLUDE_PATH "../Dependecies/glfw3/include") 

# Finding Glfw3 library
find_library(GLFW3_STATIC_LIB 
    libglfw3.a REQUIRED
    PATHS ${GLFW3_STATIC_LIB_PATH}
)

# Linking our application with GLFW3 library
target_link_libraries(Test-App  PUBLIC ${GLFW3_STATIC_LIB})

# Including Header files of GLFW3
target_include_directories(Test-App PUBLIC ${GLFW3_INCLUDE_PATH})

