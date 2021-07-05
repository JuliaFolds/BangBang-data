# Benchmark result

* Pull request commit: [`b482825d608a3b1aa43ec1372df1cd893c25a06d`](https://github.com/JuliaFolds/BangBang.jl/commit/b482825d608a3b1aa43ec1372df1cd893c25a06d)
* Pull request: <https://github.com/JuliaFolds/BangBang.jl/pull/202> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmarks:
    - Target: 5 Jul 2021 - 00:59
    - Baseline: 5 Jul 2021 - 01:02
* Package commits:
    - Target: 2a2baa
    - Baseline: a10491
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
| `["append", "append!!(::SVector, ::SingletonVector)"]`                                   | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collectors", ":comp => \"map\"", ":impl => \"coll\""]`                                | 0.76 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collectors", ":comp => \"map\"", ":impl => \"safe_coll\""]`                           | 0.84 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collectors", ":comp => \"map\"", ":impl => \"vec\""]`                                 | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["dataframes", "Categorical"]`                                                          | 0.82 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["dataframes", "Int-Int"]`                                                              |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :empty"]`     |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :half"]`      |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :empty"]` |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :equal"]` | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mergewith", ":combine => :right", ":desttype => :widen", ":destkeys => :empty"]`      | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |

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
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1036-azure #38~20.04.1-Ubuntu SMP Thu Jun 17 14:14:18 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       9128 s         14 s       1445 s      53322 s          0 s
       #2  2294 MHz      29912 s          4 s       1719 s      32385 s          0 s
       
  Memory: 6.790924072265625 GB (3270.1328125 MB free)
  Uptime: 645.0 sec
  Load Avg:  1.0751953125  0.82080078125  0.4267578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1036-azure #38~20.04.1-Ubuntu SMP Thu Jun 17 14:14:18 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      11231 s         14 s       1685 s      66061 s          0 s
       #2  2294 MHz      42485 s          4 s       2113 s      34532 s          0 s
       
  Memory: 6.790924072265625 GB (3277.5 MB free)
  Uptime: 796.0 sec
  Load Avg:  1.0771484375  0.9267578125  0.53271484375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmark: 5 Jul 2021 - 0:59
* Package commit: 2a2baa
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
| `["append", "append!!(::SVector, ::SingletonVector)"]`                                   |  12.012 ns (5%) |           |                 |             |
| `["append", "append!!(::Vector, ::SingletonVector)"]`                                    | 407.602 μs (5%) |           |                 |             |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]`                              |  12.100 ns (5%) |           |                 |             |
| `["collectors", ":comp => \"filter\"", ":impl => \"base\""]`                             |  34.300 μs (5%) |           | 128.66 KiB (1%) |          14 |
| `["collectors", ":comp => \"filter\"", ":impl => \"coll\""]`                             |  38.200 μs (5%) |           | 284.81 KiB (1%) |        5012 |
| `["collectors", ":comp => \"filter\"", ":impl => \"nonexpanding\""]`                     |  33.400 μs (5%) |           | 312.75 KiB (1%) |        5005 |
| `["collectors", ":comp => \"filter\"", ":impl => \"vec\""]`                              |  34.600 μs (5%) |           | 128.59 KiB (1%) |          13 |
| `["collectors", ":comp => \"map\"", ":impl => \"coll\""]`                                |   4.117 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"man\""]`                                 |   4.740 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"safe_coll\""]`                           |   8.700 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"vec\""]`                                 |  58.800 μs (5%) |           | 256.64 KiB (1%) |          14 |
| `["dataframes", "Categorical"]`                                                          | 569.740 ms (5%) | 75.211 ms | 889.14 MiB (1%) |     4925452 |
| `["dataframes", "Int-Int"]`                                                              | 972.610 μs (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-Int"]`                                                          |   1.291 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-String"]`                                                       |   1.339 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["dataframes", "String-String"]`                                                        |   1.272 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :empty"]`     |  37.500 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :equal"]`     |  18.700 μs (5%) |           |                 |             |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :half"]`      |  32.501 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", ":combine => :+", ":desttype => :widen", ":destkeys => :empty"]`          |  39.101 μs (5%) |           |  92.31 KiB (1%) |          18 |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :empty"]` |  37.300 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :equal"]` |  16.200 μs (5%) |           |                 |             |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :half"]`  |  29.601 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", ":combine => :right", ":desttype => :widen", ":destkeys => :empty"]`      |  38.801 μs (5%) |           |  92.31 KiB (1%) |          18 |

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
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1036-azure #38~20.04.1-Ubuntu SMP Thu Jun 17 14:14:18 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       9128 s         14 s       1445 s      53322 s          0 s
       #2  2294 MHz      29912 s          4 s       1719 s      32385 s          0 s
       
  Memory: 6.790924072265625 GB (3270.1328125 MB free)
  Uptime: 645.0 sec
  Load Avg:  1.0751953125  0.82080078125  0.4267578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmark: 5 Jul 2021 - 1:2
* Package commit: a10491
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
| `["append", "append!!(::SVector, ::SingletonVector)"]`                                   |  13.213 ns (5%) |           |                 |             |
| `["append", "append!!(::Vector, ::SingletonVector)"]`                                    | 413.004 μs (5%) |           |                 |             |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]`                              |  12.400 ns (5%) |           |                 |             |
| `["collectors", ":comp => \"filter\"", ":impl => \"base\""]`                             |  34.500 μs (5%) |           | 128.66 KiB (1%) |          14 |
| `["collectors", ":comp => \"filter\"", ":impl => \"coll\""]`                             |  39.500 μs (5%) |           | 284.81 KiB (1%) |        5012 |
| `["collectors", ":comp => \"filter\"", ":impl => \"nonexpanding\""]`                     |  34.100 μs (5%) |           | 312.75 KiB (1%) |        5005 |
| `["collectors", ":comp => \"filter\"", ":impl => \"vec\""]`                              |  36.100 μs (5%) |           | 128.59 KiB (1%) |          13 |
| `["collectors", ":comp => \"map\"", ":impl => \"coll\""]`                                |   5.400 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"man\""]`                                 |   4.900 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"safe_coll\""]`                           |  10.399 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"vec\""]`                                 |  62.800 μs (5%) |           | 256.64 KiB (1%) |          14 |
| `["dataframes", "Categorical"]`                                                          | 693.459 ms (5%) | 80.883 ms | 909.14 MiB (1%) |     5335052 |
| `["dataframes", "Int-Int"]`                                                              | 918.804 μs (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-Int"]`                                                          |   1.287 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-String"]`                                                       |   1.320 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["dataframes", "String-String"]`                                                        |   1.270 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :empty"]`     |  35.200 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :equal"]`     |  18.300 μs (5%) |           |                 |             |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :half"]`      |  29.600 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", ":combine => :+", ":desttype => :widen", ":destkeys => :empty"]`          |  39.500 μs (5%) |           |  92.31 KiB (1%) |          18 |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :empty"]` |  35.501 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :equal"]` |  17.500 μs (5%) |           |                 |             |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :half"]`  |  31.101 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", ":combine => :right", ":desttype => :widen", ":destkeys => :empty"]`      |  41.801 μs (5%) |           |  92.31 KiB (1%) |          18 |

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
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1036-azure #38~20.04.1-Ubuntu SMP Thu Jun 17 14:14:18 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      11231 s         14 s       1685 s      66061 s          0 s
       #2  2294 MHz      42485 s          4 s       2113 s      34532 s          0 s
       
  Memory: 6.790924072265625 GB (3277.5 MB free)
  Uptime: 796.0 sec
  Load Avg:  1.0771484375  0.9267578125  0.53271484375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 2 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 2 |

`lscpu` output:

    Architecture:                    x86_64
    CPU op-mode(s):                  32-bit, 64-bit
    Byte Order:                      Little Endian
    Address sizes:                   46 bits physical, 48 bits virtual
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    NUMA node(s):                    1
    Vendor ID:                       GenuineIntel
    CPU family:                      6
    Model:                           79
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    Stepping:                        1
    CPU MHz:                         2294.683
    BogoMIPS:                        4589.36
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        50 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Full generic retpoline, STIBP disabled, RSB filling
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Broadwell                                              |
| Model              | Family: 0x06, Model: 0x4f, Stepping: 0x01, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 51200) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

