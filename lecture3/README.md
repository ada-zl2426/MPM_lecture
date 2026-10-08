# lecture3

1)  Profiling measures where the code spent time
2)  .iterrows() is used to go through index and the rows object
3)  %timeit -> used to measure how long  python take to execute per loop on the line
    - -n -> means execute the number of times per run
    - -r -> means execute the number of runs
    - -o -> return an object containing timing results
    Example:
    t = %timeit -o -n 1000 -r 5 calculate()
    print("Average:", t.average)
    print("Best:", t.best)
    print("Worst:", t.worst)
    print("Standard deviation:", t.stdev)
    print("Individual timings:", t.timings)

4)  %%timeit -> measure the codes below it
    Example:
    %%timeit  # will do that
    n = 1_000_000
    total = 0
    for i in range(n):
    total += i

5)  timeit.timeit() -> return total time used to execute the code
    Example:
    t = timeit.timeit(calculate, number=1000)
   
6)  timeit.repeat() -> return a list of timings depend on how many runs is executed
    Example:
    t = timeit.repeat(calculate, number=1000, repeat=5)
    -> return a list of time

7)  Stopwatch approach
    Example:
    import time

    start_time = time.time()  # start the stopwatch

    n = 100_000_000
    s = sum(range(1, n + 1))

    end_time = time.time()  # stop the stopwatch

    wall_time = end_time - start_time
    print(f"Wall Time: {wall_time:.3f} seconds")

8)  Calculate cpu time -> Time the CPU spends actively executing instructions for your program
    start_cpu_time = time.process_time()
    end_cpu_time = time.process_time()

9)  cProfile -> built-in Python profiler that records how often functions are called and how much time they consume.

    -   %prun:  profiles everything executed by the statement you give it, including any functions called along the way.
    -   %%prun:   function below this line will be in profiling results

10) %load_ext line_profiler: used to load line profile extension
    -   %lprun: Run the line profiler
    -   -f is to specify which function's specify lines to inspect
    -   after -f write the execution for the function

    Example:    %lprun -f estimate_pi estimate_pi(10000)

11) 