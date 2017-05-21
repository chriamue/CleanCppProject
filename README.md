# CleanCppProject
Notes and thoughts for a clean and simple C++ project workflow.

## Git

Use a version control system.

[Github](https://github.com/), [Bitbucket](https://bitbucket.org/) or [Gitlab](https://about.gitlab.com/) are some examples to host code on.

For repositories on my own server I prefer [Gitlab](https://hub.docker.com/r/gitlab/gitlab-ce/) in a Docker container.

## Project Template

[https://github.com/cginternals/cmake-init](https://github.com/cginternals/cmake-init) provides an easy to use cmake template project.

Just clone the template.

```bash
git clone https://github.com/cginternals/cmake-init.git CleanProject
```

Then change files in CleanProject as it is described in the ADAPT file.

### CMake

[CMake](https://cmake.org/) allows you to easily build your code on different platforms

```bash
mkdir build
cd build
cmake ..
cmake --build .
```

 and to create project files for Visual Studio, Eclipse, Qt Creator, ...

```bash
cmake .. -G "Visual Studio 14 Win64"
```

### Doxygen

[Doxygen](http://doxygen.org) will create documentation of your API based on comments within projects source code.

