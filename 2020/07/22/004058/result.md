# Benchmark result

* Pull request commit: [`c0341bf7684a70720eea328b44a83c0ef8fc3d42`](https://github.com/JuliaFolds/BangBang.jl/commit/c0341bf7684a70720eea328b44a83c0ef8fc3d42)
* Pull request: <https://github.com/JuliaFolds/BangBang.jl/pull/135> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmarks:
    - Target: 22 Jul 2020 - 00:37
    - Baseline: 22 Jul 2020 - 00:40
* Package commits:
    - Target: b041ca
    - Baseline: 27399e
* Julia commits:
    - Target: 44fa15
    - Baseline: 44fa15
* Julia command flags:
    - Target: None
    - Baseline: None
* Environment variables:
    - Target: None
    - Baseline: None

## Results
A ratio greater than `1.0` denotes a possible regression (marked with :x:), while a ratio less
than `1.0` denotes a possible improvement (marked with :white_check_mark:). Only significant results - results
that indicate possible regressions or improvements - are shown below (thus, an empty table means that all
benchmark results remained invariant between builds).

| ID                                                                                       | time ratio                   | memory ratio                 |
|------------------------------------------------------------------------------------------|------------------------------|------------------------------|
| `["collectors", ":comp => \"filter\"", ":impl => \"nonexpanding\""]`                     | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collectors", ":comp => \"filter\"", ":impl => \"vec\""]`                              | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collectors", ":comp => \"map\"", ":impl => \"coll\""]`                                | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collectors", ":comp => \"map\"", ":impl => \"man\""]`                                 |                1.21 (5%) :x: |                   1.00 (1%)  |
| `["collectors", ":comp => \"map\"", ":impl => \"safe_coll\""]`                           | 0.74 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["dataframes", "Categorical"]`                                                          | 0.74 (5%) :white_check_mark: | 0.92 (1%) :white_check_mark: |
| `["dataframes", "String-String"]`                                                        |                1.20 (5%) :x: |                   1.00 (1%)  |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :empty"]`     | 0.85 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :equal"]`     |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :half"]`      |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["mergewith", ":combine => :+", ":desttype => :widen", ":destkeys => :empty"]`          |                1.22 (5%) :x: |                   1.00 (1%)  |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :empty"]` | 0.82 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :equal"]` | 0.74 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :half"]`  | 0.69 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mergewith", ":combine => :right", ":desttype => :widen", ":destkeys => :empty"]`      | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append"]`
- `["collectors", ":comp => \"filter\""]`
- `["collectors", ":comp => \"map\""]`
- `["dataframes"]`
- `["mergewith", ":combine => :+", ":desttype => :compatible"]`
- `["mergewith", ":combine => :+", ":desttype => :widen"]`
- `["mergewith", ":combine => :right", ":desttype => :compatible"]`
- `["mergewith", ":combine => :right", ":desttype => :widen"]`

## Julia versioninfo

### Target
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      10830 s          0 s       1179 s      36360 s          0 s
       #2  2095 MHz      22388 s          0 s       2060 s      24042 s          0 s
       
  Memory: 6.764884948730469 GB (2910.84765625 MB free)
  Uptime: 500.0 sec
  Load Avg:  1.04443359375  0.8701171875  0.4443359375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

### Baseline
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      15582 s          0 s       1492 s      47176 s          0 s
       #2  2095 MHz      33212 s          0 s       2322 s      28826 s          0 s
       
  Memory: 6.764884948730469 GB (2991.25 MB free)
  Uptime: 660.0 sec
  Load Avg:  1.07958984375  0.9697265625  0.55419921875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmark: 22 Jul 2020 - 0:37
* Package commit: b041ca
* Julia commit: 44fa15
* Julia command flags: None
* Environment variables: None

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                                                       | time            | GC time   | memory          | allocations |
|------------------------------------------------------------------------------------------|----------------:|----------:|----------------:|------------:|
| `["append", "append!!(::SVector, ::SingletonVector)"]`                                   |   9.409 ns (5%) |           |                 |             |
| `["append", "append!!(::Vector, ::SingletonVector)"]`                                    | 418.912 μs (5%) |           |                 |             |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]`                              |  11.011 ns (5%) |           |                 |             |
| `["collectors", ":comp => \"filter\"", ":impl => \"base\""]`                             |  37.601 μs (5%) |           | 128.66 KiB (1%) |          14 |
| `["collectors", ":comp => \"filter\"", ":impl => \"coll\""]`                             |  44.801 μs (5%) |           | 284.81 KiB (1%) |        5012 |
| `["collectors", ":comp => \"filter\"", ":impl => \"nonexpanding\""]`                     |  34.301 μs (5%) |           | 312.75 KiB (1%) |        5005 |
| `["collectors", ":comp => \"filter\"", ":impl => \"vec\""]`                              |  34.901 μs (5%) |           | 128.59 KiB (1%) |          13 |
| `["collectors", ":comp => \"map\"", ":impl => \"coll\""]`                                |   5.800 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"man\""]`                                 |   6.400 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"safe_coll\""]`                           |  10.000 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"vec\""]`                                 |  63.002 μs (5%) |           | 256.64 KiB (1%) |          14 |
| `["dataframes", "Categorical"]`                                                          | 624.777 ms (5%) | 75.031 ms | 909.14 MiB (1%) |     5335052 |
| `["dataframes", "Int-Int"]`                                                              | 986.308 μs (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-Int"]`                                                          |   1.571 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-String"]`                                                       |   1.308 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["dataframes", "String-String"]`                                                        |   1.467 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :empty"]`     |  34.401 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :equal"]`     |  20.600 μs (5%) |           |                 |             |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :half"]`      |  30.101 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", ":combine => :+", ":desttype => :widen", ":destkeys => :empty"]`          |  37.601 μs (5%) |           |  92.31 KiB (1%) |          18 |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :empty"]` |  30.101 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :equal"]` |  16.101 μs (5%) |           |                 |             |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :half"]`  |  27.401 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", ":combine => :right", ":desttype => :widen", ":destkeys => :empty"]`      |  34.701 μs (5%) |           |  92.31 KiB (1%) |          18 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append"]`
- `["collectors", ":comp => \"filter\""]`
- `["collectors", ":comp => \"map\""]`
- `["dataframes"]`
- `["mergewith", ":combine => :+", ":desttype => :compatible"]`
- `["mergewith", ":combine => :+", ":desttype => :widen"]`
- `["mergewith", ":combine => :right", ":desttype => :compatible"]`
- `["mergewith", ":combine => :right", ":desttype => :widen"]`

## Julia versioninfo
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      10830 s          0 s       1179 s      36360 s          0 s
       #2  2095 MHz      22388 s          0 s       2060 s      24042 s          0 s
       
  Memory: 6.764884948730469 GB (2910.84765625 MB free)
  Uptime: 500.0 sec
  Load Avg:  1.04443359375  0.8701171875  0.4443359375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmark: 22 Jul 2020 - 0:40
* Package commit: 27399e
* Julia commit: 44fa15
* Julia command flags: None
* Environment variables: None

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                                                       | time            | GC time    | memory          | allocations |
|------------------------------------------------------------------------------------------|----------------:|-----------:|----------------:|------------:|
| `["append", "append!!(::SVector, ::SingletonVector)"]`                                   |   9.710 ns (5%) |            |                 |             |
| `["append", "append!!(::Vector, ::SingletonVector)"]`                                    | 420.406 μs (5%) |            |                 |             |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]`                              |  11.311 ns (5%) |            |                 |             |
| `["collectors", ":comp => \"filter\"", ":impl => \"base\""]`                             |  39.400 μs (5%) |            | 128.66 KiB (1%) |          14 |
| `["collectors", ":comp => \"filter\"", ":impl => \"coll\""]`                             |  46.201 μs (5%) |            | 284.81 KiB (1%) |        5012 |
| `["collectors", ":comp => \"filter\"", ":impl => \"nonexpanding\""]`                     |  38.901 μs (5%) |            | 312.75 KiB (1%) |        5005 |
| `["collectors", ":comp => \"filter\"", ":impl => \"vec\""]`                              |  39.301 μs (5%) |            | 128.59 KiB (1%) |          13 |
| `["collectors", ":comp => \"map\"", ":impl => \"coll\""]`                                |   6.500 μs (5%) |            |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"man\""]`                                 |   5.300 μs (5%) |            |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"safe_coll\""]`                           |  13.600 μs (5%) |            |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"vec\""]`                                 |  64.501 μs (5%) |            | 256.64 KiB (1%) |          14 |
| `["dataframes", "Categorical"]`                                                          | 849.149 ms (5%) | 102.549 ms | 992.89 MiB (1%) |     6318092 |
| `["dataframes", "Int-Int"]`                                                              | 990.116 μs (5%) |            | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-Int"]`                                                          |   1.599 ms (5%) |            | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-String"]`                                                       |   1.285 ms (5%) |            | 160.27 KiB (1%) |       10252 |
| `["dataframes", "String-String"]`                                                        |   1.219 ms (5%) |            | 160.27 KiB (1%) |       10252 |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :empty"]`     |  40.501 μs (5%) |            |  91.72 KiB (1%) |          14 |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :equal"]`     |  19.500 μs (5%) |            |                 |             |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :half"]`      |  28.101 μs (5%) |            |  68.34 KiB (1%) |           5 |
| `["mergewith", ":combine => :+", ":desttype => :widen", ":destkeys => :empty"]`          |  30.900 μs (5%) |            |  92.31 KiB (1%) |          18 |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :empty"]` |  36.900 μs (5%) |            |  91.72 KiB (1%) |          14 |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :equal"]` |  21.800 μs (5%) |            |                 |             |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :half"]`  |  39.801 μs (5%) |            |  68.34 KiB (1%) |           5 |
| `["mergewith", ":combine => :right", ":desttype => :widen", ":destkeys => :empty"]`      |  39.600 μs (5%) |            |  92.31 KiB (1%) |          18 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append"]`
- `["collectors", ":comp => \"filter\""]`
- `["collectors", ":comp => \"map\""]`
- `["dataframes"]`
- `["mergewith", ":combine => :+", ":desttype => :compatible"]`
- `["mergewith", ":combine => :+", ":desttype => :widen"]`
- `["mergewith", ":combine => :right", ":desttype => :compatible"]`
- `["mergewith", ":combine => :right", ":desttype => :widen"]`

## Julia versioninfo
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      15582 s          0 s       1492 s      47176 s          0 s
       #2  2095 MHz      33212 s          0 s       2322 s      28826 s          0 s
       
  Memory: 6.764884948730469 GB (2991.25 MB free)
  Uptime: 660.0 sec
  Load Avg:  1.07958984375  0.9697265625  0.55419921875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 2 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 2 |

`lscpu` output:

    Architecture:        x86_64
    CPU op-mode(s):      32-bit, 64-bit
    Byte Order:          Little Endian
    CPU(s):              2
    On-line CPU(s) list: 0,1
    Thread(s) per core:  1
    Core(s) per socket:  2
    Socket(s):           1
    NUMA node(s):        1
    Vendor ID:           GenuineIntel
    CPU family:          6
    Model:               85
    Model name:          Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    Stepping:            4
    CPU MHz:             2095.076
    BogoMIPS:            4190.15
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            1024K
    L3 cache:            36608K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x04, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 44 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

