
## How to build and compile
```
# 1. build phase
# In the root directory (where the root CMakeLists.txt is located)
$ cmake -B myBuild -S .
# 2. Compile phase
$ cd myBuild
$ cmake --build .
# 3. Running the executable
$ cd Test-app
$ ./Test-app
```