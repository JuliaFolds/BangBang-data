# Benchmark result

* Pull request commit: [`604c9b4162b1a399956a11800697ec611b97de9a`](https://github.com/JuliaFolds/BangBang.jl/commit/604c9b4162b1a399956a11800697ec611b97de9a)
* Pull request: <https://github.com/JuliaFolds/BangBang.jl/pull/202> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmarks:
    - Target: 23 Nov 2023 - 01:11
    - Baseline: 23 Nov 2023 - 01:13
* Package commits:
    - Target: 996c6a
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
| `["dataframes", "Categorical"]`                             | 0.75 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |

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
  uname: Linux 6.2.0-1016-azure #16~22.04.1-Ubuntu SMP Tue Oct 10 17:11:51 UTC 2023 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3243 MHz       4693 s          0 s       1451 s      39402 s          0 s
       #2  3245 MHz      14068 s          0 s       1816 s      29676 s          0 s
       #3  2445 MHz       9457 s          2 s       1192 s      34797 s          0 s
       #4  2596 MHz       5686 s          0 s       1271 s      38437 s          0 s
       
  Memory: 15.60689926147461 GB (12065.21875 MB free)
  Uptime: 459.0 sec
  Load Avg:  1.0  0.7177734375  0.3359375
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
  uname: Linux 6.2.0-1016-azure #16~22.04.1-Ubuntu SMP Tue Oct 10 17:11:51 UTC 2023 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3242 MHz       9381 s          0 s       1792 s      45190 s          0 s
       #2  2445 MHz      17440 s          0 s       2318 s      36614 s          0 s
       #3  3057 MHz      10428 s          2 s       1482 s      44341 s          0 s
       #4  2660 MHz       7193 s          0 s       1570 s      47448 s          0 s
       
  Memory: 15.60689926147461 GB (12081.10546875 MB free)
  Uptime: 567.0 sec
  Load Avg:  1.0615234375  0.84716796875  0.43017578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, generic)
```

---
# Target result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmark: 23 Nov 2023 - 1:11
* Package commit: 996c6a
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
| `["append", "append!!(::Vector, ::SingletonVector)"]`                                       | 401.593 μs (5%) |           |                 |             |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]`                                 |  10.489 ns (5%) |           |                 |             |
| `["collectors", :(:comp => "filter"), :(:impl => "base")]`                                  |  27.170 μs (5%) |           | 128.66 KiB (1%) |          14 |
| `["collectors", :(:comp => "filter"), :(:impl => "coll")]`                                  |  29.474 μs (5%) |           | 284.81 KiB (1%) |        5012 |
| `["collectors", :(:comp => "filter"), :(:impl => "nonexpanding")]`                          |  25.617 μs (5%) |           | 312.75 KiB (1%) |        5005 |
| `["collectors", :(:comp => "filter"), :(:impl => "vec")]`                                   |  27.101 μs (5%) |           | 128.59 KiB (1%) |          13 |
| `["collectors", :(:comp => "map"), :(:impl => "coll")]`                                     |   2.723 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "man")]`                                      |   2.845 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "safe_coll")]`                                |   6.490 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "vec")]`                                      |  47.067 μs (5%) |           | 256.64 KiB (1%) |          14 |
| `["dataframes", "Categorical"]`                                                             | 337.617 ms (5%) | 39.032 ms | 804.14 MiB (1%) |     4024332 |
| `["dataframes", "Int-Int"]`                                                                 | 820.549 μs (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-Int"]`                                                             |   1.136 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-String"]`                                                          |   1.053 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["dataframes", "String-String"]`                                                           |   1.026 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :empty)]`     |  18.634 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :equal)]`     |  10.530 μs (5%) |           |                 |             |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :half)]`      |  15.819 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", :(:combine => :+), :(:desttype => :widen), :(:destkeys => :empty)]`          |  18.935 μs (5%) |           |  92.31 KiB (1%) |          18 |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :empty)]` |  18.755 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :equal)]` |   8.887 μs (5%) |           |                 |             |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :half)]`  |  15.068 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", :(:combine => :right), :(:desttype => :widen), :(:destkeys => :empty)]`      |  19.055 μs (5%) |           |  92.31 KiB (1%) |          18 |

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
  uname: Linux 6.2.0-1016-azure #16~22.04.1-Ubuntu SMP Tue Oct 10 17:11:51 UTC 2023 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3243 MHz       4693 s          0 s       1451 s      39402 s          0 s
       #2  3245 MHz      14068 s          0 s       1816 s      29676 s          0 s
       #3  2445 MHz       9457 s          2 s       1192 s      34797 s          0 s
       #4  2596 MHz       5686 s          0 s       1271 s      38437 s          0 s
       
  Memory: 15.60689926147461 GB (12065.21875 MB free)
  Uptime: 459.0 sec
  Load Avg:  1.0  0.7177734375  0.3359375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, generic)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmark: 23 Nov 2023 - 1:13
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
| `["append", "append!!(::SVector, ::SingletonVector)"]`                                      |  10.521 ns (5%) |           |                 |             |
| `["append", "append!!(::Vector, ::SingletonVector)"]`                                       | 401.593 μs (5%) |           |                 |             |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]`                                 |  10.531 ns (5%) |           |                 |             |
| `["collectors", :(:comp => "filter"), :(:impl => "base")]`                                  |  26.218 μs (5%) |           | 128.66 KiB (1%) |          14 |
| `["collectors", :(:comp => "filter"), :(:impl => "coll")]`                                  |  29.144 μs (5%) |           | 284.81 KiB (1%) |        5012 |
| `["collectors", :(:comp => "filter"), :(:impl => "nonexpanding")]`                          |  25.517 μs (5%) |           | 312.75 KiB (1%) |        5005 |
| `["collectors", :(:comp => "filter"), :(:impl => "vec")]`                                   |  27.331 μs (5%) |           | 128.59 KiB (1%) |          13 |
| `["collectors", :(:comp => "map"), :(:impl => "coll")]`                                     |   2.705 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "man")]`                                      |   2.965 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "safe_coll")]`                                |   6.372 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "vec")]`                                      |  47.127 μs (5%) |           | 256.64 KiB (1%) |          14 |
| `["dataframes", "Categorical"]`                                                             | 447.697 ms (5%) | 52.765 ms | 909.14 MiB (1%) |     5335052 |
| `["dataframes", "Int-Int"]`                                                                 | 814.618 μs (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-Int"]`                                                             |   1.134 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-String"]`                                                          |   1.033 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["dataframes", "String-String"]`                                                           |   1.055 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :empty)]`     |  18.494 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :equal)]`     |  10.509 μs (5%) |           |                 |             |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :half)]`      |  15.479 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", :(:combine => :+), :(:desttype => :widen), :(:destkeys => :empty)]`          |  18.364 μs (5%) |           |  92.31 KiB (1%) |          18 |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :empty)]` |  18.374 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :equal)]` |   9.007 μs (5%) |           |                 |             |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :half)]`  |  14.668 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", :(:combine => :right), :(:desttype => :widen), :(:destkeys => :empty)]`      |  18.214 μs (5%) |           |  92.31 KiB (1%) |          18 |

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
  uname: Linux 6.2.0-1016-azure #16~22.04.1-Ubuntu SMP Tue Oct 10 17:11:51 UTC 2023 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3242 MHz       9381 s          0 s       1792 s      45190 s          0 s
       #2  2445 MHz      17440 s          0 s       2318 s      36614 s          0 s
       #3  3057 MHz      10428 s          2 s       1482 s      44341 s          0 s
       #4  2660 MHz       7193 s          0 s       1570 s      47448 s          0 s
       
  Memory: 15.60689926147461 GB (12081.10546875 MB free)
  Uptime: 567.0 sec
  Load Avg:  1.0615234375  0.84716796875  0.43017578125
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
    BogoMIPS:                           4890.86
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

