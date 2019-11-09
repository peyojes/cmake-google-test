 # CMake with Google Test
 
 This project shows how to add Google Test project to a CMake project. This project automatically download google test 
 and add this sources and binary to the CMake project.  
 
 ## Prerequisites
 
 You need :
 - compiler (GCC, MinGW or other),
 - CMake program and on the Linux Make.
 
 ## Build and run on the Linux
 
 Create directory build:
 ````
 mkdir build
 cd build
 ````
 
 and get into this folder.
 
 ````
 cmake ..
 make
````
 
 ## Running the tests
 
 In the build directory:
 
 ```` 
 ./unit_test
 ````

## License
This project is licensed under the MIT License.