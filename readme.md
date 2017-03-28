## C++ Boilerplate
[![Build Status](https://travis-ci.org/banuprathap/valgrind_tutorial.svg?branch=master)](https://travis-ci.org/banuprathap/valgrind_tutorial)
[![Coverage Status](https://coveralls.io/repos/github/banuprathap/valgrind_tutorial/badge.svg?branch=master)](https://coveralls.io/github/banuprathap/valgrind_tutorial?branch=master)
---

### Overview

- A Simple starter C++ Valgrind exercise
- The repository originally had 2 errors and the task was to fix those errors and submit a clean code
- Original valgrind results can be found [here](https://github.com/banuprathap/valgrind_tutorial/blob/master/results/initial.txt)
- Final valgrind output after fixing the errors can be found [here](https://github.com/banuprathap/valgrind_tutorial/blob/master/results/final.txt)

### Fixed Errors

- I had to initialize the boolean variable terminator
- I had to delete the pointer *readings* in **AnalogSensor::Read()**

### Running Valgrind

- Make sure you have valgrind installed in your system. If not run,
```bash
sudo apt-get install valgrind
```
- Clone the repository and inside the repository,
```bash
mkdir -p build
cd build
cmake ..
make
valgrind --leak-check=full ./app/shell-app
```
- To run the function profiler,
```bash
valgrind --tool=callgrind ./app/shell-app
```

