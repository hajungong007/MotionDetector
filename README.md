# MotionDetector
MotionDetector for Respberry Pi, based on MOG2 Background Subtraction Methods.

# Build
### Dependencies
* C++11
* OpenCV 3.1.0 with contrib
* CMake

### Windows
* Install OpenCV 3.1 with contrib and CMake.
* Set environment variables according to [OpenCV Setup - Environment Variables](http://docs.opencv.org/doc/tutorials/introduction/windows_install/windows_install.html#windowssetpathandenviromentvariable)
* Launch cmake-gui, create a build folder and configure.
* Open MotionDetector.sln in Visual Studio and compile the projects MotionDetector.

### OS X & Linux
* Install OpenCV 3.1 with contrib and CMake.
* Configure and complie:
	
 1) ``` mkdir build ```
	
 2) ``` cd build ```
	
 3) ``` cmake .. ```
	
 4) ``` make -j4 ```

# Usage
Make sure your Camera working on /dev/video0 
then run `./MotionDetector`

