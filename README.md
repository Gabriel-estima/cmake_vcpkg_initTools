## Basic story for the creation of this repo:

I was incredibly tired of having problems with c/c++ libraries...
Therefore I decided to make a basic way to initialize a simple CMAKE project 
with the files needed to implement VCPKG library tools...

## How to get started:

- Create the c/cpp file in a new directory and just run the "cmake_vcpkg_init" command!
- If you get it wrong the first time, the script tells you what is wrong, then just "rm -r *" and try again :)
- Specify the libraries from vcpkg you want and create a simple proto c/c++ program and run "cmake_build"
- After that, all libraries should be visible to your LSP and things should run smoothly
- Every time you want to compile your code, just run "cmake_build" again!!!! It is that easy :D

## Things to know before using:

### Dependencies:
- Install CMAKE (using your preferred package manager)
- Install VCPKG (if you don't have it already, go to their github repo and follow their instructions. It shouldn't be hard)
- Install g++ (also using your preferred package manager)

### What should I know before getting started?

It is recommended to know the basic file structure for CMAKE projects since this repo only provides a fast start for your code.
After that, you should add libraries, include files and manage other things as you see fit (which requires knowlege of CMAKE...).

## Extra Stuff:

This crude repo is basically just for me, but should anyone need anything else related to it, feel free to add it :D
