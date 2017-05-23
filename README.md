% Clean Cpp Project
% chriamue
% May, 2017

---

# CleanCppProject

Notes and thoughts for a clean and simple C++ project workflow.

- [Git](#git)
- [Project Template](#project-template)
  - [CMake](#cmake)
  - [Doxygen](#doxygen)
- [Markdown](markdown)

---

# Git

Use a version control system.

[Github](https://github.com/), [Bitbucket](https://bitbucket.org/) or [Gitlab](https://about.gitlab.com/) are some examples to host code on.

For repositories on my own server I prefer [Gitlab](https://hub.docker.com/r/gitlab/gitlab-ce/) in a Docker container.

---

# Project Template

[https://github.com/cginternals/cmake-init](https://github.com/cginternals/cmake-init) provides an easy to use cmake template project.

Just clone the template.

```bash
git clone https://github.com/cginternals/cmake-init.git CleanProject
```

Then change files in CleanProject as it is described in the ADAPT file.

---

## CMake

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

---

## Doxygen

[Doxygen](http://doxygen.org) will create documentation of your API based on comments within projects source code.

---

# Markdown

Files like README.md written in markdown can simply be viewed in [Github](https://github.com/) and also in [Gitlab](https://about.gitlab.com/).

---

## Pandoc

Markdown files can easily converted to PDF format using pandoc.

```bash
pandoc README.md -o README.pdf
```

You can also convert them to beamer slides.

```bash
pandoc -t beamer README.md -o slides.pdf
```