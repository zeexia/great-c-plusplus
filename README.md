#Learning CMake
###General steps (for Mac OS X only):
####1. Download and Install
  * download CMake from the CMake [download page](https://cmake.org/download/). In this example, the *.dmg* file.
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
  `mkdir myTest && cd $_` then press Enter;
  * Creat two empty files by typing **exactly** the following code:
  ```
    touch main.cpp CMakeLists.txt
  ```
  * now go and open up the main.cpp in your favorite text editor, write or copy&paste the following:
  ```c_cpp

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
 
~~Our session of November will be / has been about cmake.~~
Official [CMake Tutorial](https://cmake.org/cmake-tutorial/) pages. 

