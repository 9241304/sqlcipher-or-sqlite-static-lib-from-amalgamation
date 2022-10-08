## Build sqlcipher or sqlite static lib using simple cmake project description

### Steps to build (using Visual Studio)
1. [Create](https://github.com/9241304/sqlcipher-amalgamation-visual-studio) or download amalgamation
2. Copy sample CMakeLists.txt file from this repository and place it in the same folder with amalgamation files
3. Open Visual Studio Command Prompt (Tools -> Command Line -> Developer Command Prompt)
4. cd to amalgamation folder
5. Create build folder and cd to it
```
> mkdir .build
> cd .build
```
6. Configure the project
```
> cmake .. -G "Visual Studio 17 2022" -A x64 -DCMAKE_DEBUG_POSTFIX=d -DLIB_TYPE=sqlcipher
```
7. Build debug and release
```
> cmake --build . --config Debug
> cmake --build . --config Release
```
