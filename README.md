# 🚀 CMake Setup for GLFW & GLAD on macOS – Ready for LearnOpenGL!

This project provides a simple CMake setup for using GLFW and GLAD on macOS,
making it easy to follow the tutorials from [LearnOpenGL](https://learnopengl.com/).  

Automatically downloads and configures:
- GLFW
- GLAD
- [STB Image](https://github.com/nothings/stb)
- [GLM](https://github.com/g-truc/glm)

✅ CMake-based build system for macOS

✅ Bootstraped for LearnOpenGL lessons

### Build

```bash
cmake . -B out
cd out
make
./learnopengl
```