# Benchmark result

* Pull request commit: [`0d5b311e2ce99f745cb347eff20da4695987d62c`](https://github.com/JuliaFolds/BangBang.jl/commit/0d5b311e2ce99f745cb347eff20da4695987d62c)
* Pull request: <https://github.com/JuliaFolds/BangBang.jl/pull/202> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmarks:
    - Target: 29 Dec 2023 - 01:00
    - Baseline: 29 Dec 2023 - 01:02
* Package commits:
    - Target: 6f5b62
    - Baseline: d70a19
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

| ID                                                          | time ratio                   | memory ratio                 |
|-------------------------------------------------------------|------------------------------|------------------------------|
| `["append", "append!!(::SVector, ::SingletonVector)"]`      | 0.60 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]` | 0.60 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["dataframes", "Categorical"]`                             | 0.87 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append"]`
- `["dataframes"]`

## Julia versioninfo

### Target
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.3 LTS
  uname: Linux 6.2.0-1018-azure #18~22.04.1-Ubuntu SMP Tue Nov 21 19:25:02 UTC 2023 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2911 MHz       4164 s          0 s       1287 s      45390 s          0 s
       #2  2632 MHz       3712 s          1 s       1295 s      45835 s          0 s
       #3  3243 MHz      17506 s          0 s       1602 s      31760 s          0 s
       #4  2445 MHz       8508 s          0 s       1295 s      41024 s          0 s
       
  Memory: 15.606903076171875 GB (12042.50390625 MB free)
  Uptime: 511.0 sec
  Load Avg:  1.00048828125  0.73974609375  0.35302734375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, generic)
```

### Baseline
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.3 LTS
  uname: Linux 6.2.0-1018-azure #18~22.04.1-Ubuntu SMP Tue Nov 21 19:25:02 UTC 2023 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2445 MHz       7514 s          0 s       1712 s      52723 s          0 s
       #2  3242 MHz       8183 s          1 s       1608 s      52161 s          0 s
       #3  2610 MHz      19124 s          0 s       1864 s      40983 s          0 s
       #4  2554 MHz       9852 s          0 s       1829 s      50254 s          0 s
       
  Memory: 15.606903076171875 GB (12054.3671875 MB free)
  Uptime: 622.0 sec
  Load Avg:  1.0615234375  0.86279296875  0.44580078125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, generic)
```

---
# Target result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmark: 29 Dec 2023 - 1:0
* Package commit: 6f5b62
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

| ID                                                                                          | time            | GC time   | memory          | allocations |
|---------------------------------------------------------------------------------------------|----------------:|----------:|----------------:|------------:|
| `["append", "append!!(::SVector, ::SingletonVector)"]`                                      |  10.489 ns (5%) |           |                 |             |
| `["append", "append!!(::Vector, ::SingletonVector)"]`                                       | 401.658 μs (5%) |           |                 |             |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]`                                 |  10.489 ns (5%) |           |                 |             |
| `["collectors", :(:comp => "filter"), :(:impl => "base")]`                                  |  27.191 μs (5%) |           | 128.66 KiB (1%) |          14 |
| `["collectors", :(:comp => "filter"), :(:impl => "coll")]`                                  |  28.032 μs (5%) |           | 284.81 KiB (1%) |        5012 |
| `["collectors", :(:comp => "filter"), :(:impl => "nonexpanding")]`                          |  25.327 μs (5%) |           | 312.75 KiB (1%) |        5005 |
| `["collectors", :(:comp => "filter"), :(:impl => "vec")]`                                   |  27.140 μs (5%) |           | 128.59 KiB (1%) |          13 |
| `["collectors", :(:comp => "map"), :(:impl => "coll")]`                                     |   2.754 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "man")]`                                      |   2.038 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "safe_coll")]`                                |   6.514 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "vec")]`                                      |  49.382 μs (5%) |           | 256.64 KiB (1%) |          14 |
| `["dataframes", "Categorical"]`                                                             | 319.896 ms (5%) | 35.142 ms | 804.14 MiB (1%) |     4024332 |
| `["dataframes", "Int-Int"]`                                                                 | 823.824 μs (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-Int"]`                                                             |   1.140 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-String"]`                                                          |   1.030 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["dataframes", "String-String"]`                                                           |   1.017 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :empty)]`     |  17.904 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :equal)]`     |  10.139 μs (5%) |           |                 |             |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :half)]`      |  15.068 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", :(:combine => :+), :(:desttype => :widen), :(:destkeys => :empty)]`          |  18.114 μs (5%) |           |  92.31 KiB (1%) |          18 |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :empty)]` |  12.152 μs (5%) |           |  30.57 KiB (1%) |           4 |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :equal)]` |   8.946 μs (5%) |           |                 |             |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :half)]`  |  10.880 μs (5%) |           |  22.78 KiB (1%) |           1 |
| `["mergewith", :(:combine => :right), :(:desttype => :widen), :(:destkeys => :empty)]`      |  18.435 μs (5%) |           |  92.31 KiB (1%) |          18 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append"]`
- `["collectors", :(:comp => "filter")]`
- `["collectors", :(:comp => "map")]`
- `["dataframes"]`
- `["mergewith", :(:combine => :+), :(:desttype => :compatible)]`
- `["mergewith", :(:combine => :+), :(:desttype => :widen)]`
- `["mergewith", :(:combine => :right), :(:desttype => :compatible)]`
- `["mergewith", :(:combine => :right), :(:desttype => :widen)]`

## Julia versioninfo
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.3 LTS
  uname: Linux 6.2.0-1018-azure #18~22.04.1-Ubuntu SMP Tue Nov 21 19:25:02 UTC 2023 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2911 MHz       4164 s          0 s       1287 s      45390 s          0 s
       #2  2632 MHz       3712 s          1 s       1295 s      45835 s          0 s
       #3  3243 MHz      17506 s          0 s       1602 s      31760 s          0 s
       #4  2445 MHz       8508 s          0 s       1295 s      41024 s          0 s
       
  Memory: 15.606903076171875 GB (12042.50390625 MB free)
  Uptime: 511.0 sec
  Load Avg:  1.00048828125  0.73974609375  0.35302734375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, generic)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmark: 29 Dec 2023 - 1:2
* Package commit: d70a19
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

| ID                                                                                          | time            | GC time   | memory          | allocations |
|---------------------------------------------------------------------------------------------|----------------:|----------:|----------------:|------------:|
| `["append", "append!!(::SVector, ::SingletonVector)"]`                                      |  17.570 ns (5%) |           |                 |             |
| `["append", "append!!(::Vector, ::SingletonVector)"]`                                       | 401.638 μs (5%) |           |                 |             |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]`                                 |  17.580 ns (5%) |           |                 |             |
| `["collectors", :(:comp => "filter"), :(:impl => "base")]`                                  |  27.130 μs (5%) |           | 128.66 KiB (1%) |          14 |
| `["collectors", :(:comp => "filter"), :(:impl => "coll")]`                                  |  29.084 μs (5%) |           | 284.81 KiB (1%) |        5012 |
| `["collectors", :(:comp => "filter"), :(:impl => "nonexpanding")]`                          |  24.546 μs (5%) |           | 312.75 KiB (1%) |        5005 |
| `["collectors", :(:comp => "filter"), :(:impl => "vec")]`                                   |  26.679 μs (5%) |           | 128.59 KiB (1%) |          13 |
| `["collectors", :(:comp => "map"), :(:impl => "coll")]`                                     |   2.525 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "man")]`                                      |   2.846 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "safe_coll")]`                                |   6.371 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "vec")]`                                      |  47.388 μs (5%) |           | 256.64 KiB (1%) |          14 |
| `["dataframes", "Categorical"]`                                                             | 368.208 ms (5%) | 43.918 ms | 909.14 MiB (1%) |     5335052 |
| `["dataframes", "Int-Int"]`                                                                 | 818.945 μs (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-Int"]`                                                             |   1.134 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-String"]`                                                          |   1.050 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["dataframes", "String-String"]`                                                           |   1.017 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :empty)]`     |  18.585 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :equal)]`     |  10.590 μs (5%) |           |                 |             |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :half)]`      |  15.800 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", :(:combine => :+), :(:desttype => :widen), :(:destkeys => :empty)]`          |  19.036 μs (5%) |           |  92.31 KiB (1%) |          18 |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :empty)]` |  18.855 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :equal)]` |   9.066 μs (5%) |           |                 |             |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :half)]`  |  15.248 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", :(:combine => :right), :(:desttype => :widen), :(:destkeys => :empty)]`      |  19.115 μs (5%) |           |  92.31 KiB (1%) |          18 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append"]`
- `["collectors", :(:comp => "filter")]`
- `["collectors", :(:comp => "map")]`
- `["dataframes"]`
- `["mergewith", :(:combine => :+), :(:desttype => :compatible)]`
- `["mergewith", :(:combine => :+), :(:desttype => :widen)]`
- `["mergewith", :(:combine => :right), :(:desttype => :compatible)]`
- `["mergewith", :(:combine => :right), :(:desttype => :widen)]`

## Julia versioninfo
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.3 LTS
  uname: Linux 6.2.0-1018-azure #18~22.04.1-Ubuntu SMP Tue Nov 21 19:25:02 UTC 2023 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2445 MHz       7514 s          0 s       1712 s      52723 s          0 s
       #2  3242 MHz       8183 s          1 s       1608 s      52161 s          0 s
       #3  2610 MHz      19124 s          0 s       1864 s      40983 s          0 s
       #4  2554 MHz       9852 s          0 s       1829 s      50254 s          0 s
       
  Memory: 15.606903076171875 GB (12054.3671875 MB free)
  Uptime: 622.0 sec
  Load Avg:  1.0615234375  0.86279296875  0.44580078125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, generic)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 4 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 4 |

`lscpu` output:

    Architecture:                       x86_64
    CPU op-mode(s):                     32-bit, 64-bit
    Address sizes:                      48 bits physical, 48 bits virtual
    Byte Order:                         Little Endian
    CPU(s):                             4
    On-line CPU(s) list:                0-3
    Vendor ID:                          AuthenticAMD
    Model name:                         AMD EPYC 7763 64-Core Processor
    CPU family:                         25
    Model:                              1
    Thread(s) per core:                 2
    Core(s) per socket:                 2
    Socket(s):                          1
    Stepping:                           1
    BogoMIPS:                           4890.84
    Flags:                              fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext invpcid_single vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
    Virtualization:                     AMD-V
    Hypervisor vendor:                  Microsoft
    Virtualization type:                full
    L1d cache:                          64 KiB (2 instances)
    L1i cache:                          64 KiB (2 instances)
    L2 cache:                           1 MiB (2 instances)
    L3 cache:                           32 MiB (1 instance)
    NUMA node(s):                       1
    NUMA node0 CPU(s):                  0-3
    Vulnerability Gather data sampling: Not affected
    Vulnerability Itlb multihit:        Not affected
    Vulnerability L1tf:                 Not affected
    Vulnerability Mds:                  Not affected
    Vulnerability Meltdown:             Not affected
    Vulnerability Mmio stale data:      Not affected
    Vulnerability Retbleed:             Not affected
    Vulnerability Spec rstack overflow: Mitigation; safe RET, no microcode
    Vulnerability Spec store bypass:    Vulnerable
    Vulnerability Spectre v1:           Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:           Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:                Not affected
    Vulnerability Tsx async abort:      Not affected
    

| Cpu Property       | Value                                                      |
|:------------------ |:---------------------------------------------------------- |
| Brand              | AMD EPYC 7763 64-Core Processor                            |
| Vendor             | :AMD                                                       |
| Architecture       | :Unknown                                                   |
| Model              | Family: 0xaf, Model: 0x01, Stepping: 0x01, Type: 0x00      |
| Cores              | 16 physical cores, 16 logical cores (on executing CPU)     |
|                    | No Hyperthreading hardware capability detected             |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (32, 512, 32768) kbytes                        |
|                    | 64 byte cache line size                                    |
| Address Size       | 48 bits virtual, 48 bits physical                          |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported    |
| Hypervisor         | Yes, Microsoft                                             |

