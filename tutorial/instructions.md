# Welcome to the tutorial!

## Before Starting, set up your commands:
1. Install basic dependencies in the cmd: 

       sudo apt install g++ cmake ninja-build git

2. Clone VCPKG repo in a separate directory (please remember where you clone it) writing: 

       git clone https://github.com/microsoft/vcpkg.git 

3. After that, to finish installing VCPKG, write:

       cd vcpkg && ./bootstrap-vcpkg.sh

4. When that is done, it is necessary to set up the path to VCPKG in your environment variables
5. Then, while still in the environment variables, add the path to this repo's bin to access its commands

**( <span style="color:red">WARNING:</span> This repo was designed to be used with linux distributions...)**

## Basic Tutorial:
In this tutorial you will find a "testDir" directory that contains a basic c++ file that depends on the linear algebra library "eigen3". However, without having it installed, the file should throw errors in the compilation step... so we need a way to install the dependencies with the tools from this repo :D

### Steps:
1. In the directory that contains the "test.cpp" file, run the command **cmake_vcpkg_init**
This command takes 5 parameters:
    - The name you want for your project
    - The name of the executable you will generate in the end
    - The name of the source c/c++ file (in this case "test.cpp")
    - The path to your installation of VCPKG
    - The list of libraries from VCPKG you want to include in your project (from the beginning it comes with fmt, vcpkg-cmake and vcpkg-cmake-config)

It should look something like this:

    cmake_vcpkg_init tutorialProj testExec test.cpp /path/to/vcpkg eigen3

2. After running the command with the structure above, many files should have been created in the directory! 
All of them are needed for the project to be built using CMake and have access to the VCPKG libraries.
Now that the whole base for the project has been set up, run **cmake_build** to compile your project in the "build" directory

       cmake_build

3. Finally, (if there were no errors along the way :D) run the executable with: **./build/testExec**

If you see four weird numbers in a matrix, it means that the libraries were successfully installed and linked and the program
ultimately compiled!



