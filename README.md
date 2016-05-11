#Learning CMake
###General steps (for Mac OS X only):
####1. Download and Install CMake
  * download CMake from the CMake [download page](https://cmake.org/download/). In this example, the *cmake-3.5.2-Darwin-x86_64.dmg* file.
  * launch Installer by double-clicking on the *.dmg* file, drag and drop CMake onto the Applications folder
  * Once installed, launch CMake (e.g. from Spotlight)
  * :heavy_exclamation_mark:**Add CMake to path**: From the "Tools" menu select "How to Install For Command Line Use". From the popup dialog box, note the cmake-gui path, which in my case is `/Applications/CMake.app/Contents/bin/cmake-gui`

    :heavy_exclamation_mark:**Open Terminal and type**:
    ```
    sudo mkdir -p /usr/local/bin
    sudo "/Applications/CMake.app/Contents/bin/cmake-gui" --install
    ```
    Verify that CMake has been correctly installed to PATH:
    ```
    cmake --version
    ```

####2. Build Up Your First C++ Project (using Terminal command line mainly)
  * Open `Terminal`, switch into your `Desktop` directory by typing the following:
  `cd ~/Desktop` and then press `Enter`; (instead of `Desktop` you can chose anywhere else, as long as you can easily access your project files later on.)
  * Creat an empty directory, name it "myTest" (or anything you like) and switch into it by typing:

  `mkdir myTest && cd $_`

  * Creat two empty files by typing **exactly** the following code:
  ```
  touch main.cpp CMakeLists.txt
  ```
  * Now, go and open up the main.cpp in your favorite text editor, (don't close the Terminal window just yet!! We'll need to come back to it later…), write or copy&paste the following:
  ```cpp
  // This program outputs the message "Hello World!"

  #include <iostream>
  #include <string>
  #include <cstdlib>
  #include <fstream>

  using namespace std;

  int main() 
  {
    cout << "Hello World!\n";    
    return 0;
  }

  ```

  * Open the other file CMakeLists.txt and write or copy&paste the following:
  ```
  cmake_minimum_required(VERSION 2.6)
  project(helloWorld)
  
  add_definitions("-std=c++11")
  add_executable(helloWorld main.cpp)
  
  target_link_libraries(helloWorld)

  ```
    - Notice that the "helloWorld" in the code above is a "random" name I gave to this particular project, it can be anything else but it must be consistent as you will see this later on.

####3. Let CMake Build
  * Save and close both main.cpp and CMakeLists.txt files, go back to your Terminal and creat an empty directory called "build" and switch into it by typing:

  ```
  mkdir build && cd $_
  ```
  * Now enter the following CMake command:

  ```
  cmake ..
  ```
  * … and when it's done, enter another CMake command:

  ```
  make
  ```

  ###(If everything fine, you will see something like `[100%] Built target helloWorld` at the end of the output! I keep my finger crossed for you…)

####4. Run Our first C++!!
Finally enter the CMake command to run main.cpp:

```
./helloWorld
```
**Notice! this is exactly the name we've given to our project and defined in the CMakeLists.txt file in Step 2.**



~~Our session of November will be / has been about cmake.~~

Official [CMake Tutorial](https://cmake.org/cmake-tutorial/) pages. 

