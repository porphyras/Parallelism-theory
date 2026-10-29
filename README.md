# Parallel Programming

Labs from the parallel programming course at Novosibirsk State University:
OpenMP and `std::thread` in C++, plus a multithreaded video pipeline in Python.
Most tasks include benchmark scripts that measure speedup, efficiency and the Karp–Flatt metric.

| Task | What it does | Tech |
|---|---|---|
| [first_task](first_task) | Summing a sine table in `float` vs `double` (precision comparison, CMake option) | C++, CMake |
| [Task2_1](Task2_1) | Parallel matrix–vector multiplication | OpenMP |
| [Task2_2](Task2_2) | Parallel numerical integration, speedup plot | OpenMP |
| [Task2_3](Task2_3) | Iterative solver for a linear system: two parallelization variants | OpenMP |
| [Task2_3.2](Task2_3.2) | Same solver: comparing `static` / `dynamic` / `guided` scheduling and chunk sizes | OpenMP |
| [Task3/Task3_1](Task3/Task3_1) | Matrix–vector multiplication with a manual thread pool | `std::thread` |
| [Task3/Task3_2](Task3/Task3_2) | Concurrent task server computing `sin` / `sqrt` / `pow`, with result checks | `std::thread` |
| [Task4](Task4) | Producer–consumer: sensors with different rates and a camera feeding a display window | Python `threading`, OpenCV |
| [Task5](Task5) | Video object detection with YOLO in several worker threads | Python, Ultralytics YOLO |
| [benchmark_tools](benchmark_tools) | Benchmark result analysis | Python |

## Build and run (C++ tasks)

```sh
cd Task2_1
cmake -S . -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build
./run_full_benchmark.sh
```

`run_all_task2_benchmarks.sh` runs every OpenMP benchmark in one go.
