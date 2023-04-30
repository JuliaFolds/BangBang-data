# Benchmark result

* Pull request commit: [`4a9ee5a389b7e6770d37ef19a4f80f69712ba319`](https://github.com/JuliaFolds/BangBang.jl/commit/4a9ee5a389b7e6770d37ef19a4f80f69712ba319)
* Pull request: <https://github.com/JuliaFolds/BangBang.jl/pull/202> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmarks:
    - Target: 30 Apr 2023 - 01:24
    - Baseline: 30 Apr 2023 - 01:26
* Package commits:
    - Target: a2f0bd
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
| `["dataframes", "Categorical"]`                             | 0.78 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["dataframes", "Missing-String"]`                          | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1036-azure #43-Ubuntu SMP Wed Mar 29 16:11:05 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       8620 s          0 s       1598 s      43735 s          0 s
       #2  2593 MHz      32926 s          3 s       2200 s      18707 s          0 s
       
  Memory: 6.781208038330078 GB (3147.39453125 MB free)
  Uptime: 546.0 sec
  Load Avg:  1.080078125  0.87451171875  0.46240234375
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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1036-azure #43-Ubuntu SMP Wed Mar 29 16:11:05 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      20280 s          0 s       2066 s      45574 s          0 s
       #2  2593 MHz      35095 s          3 s       2428 s      30229 s          0 s
       
  Memory: 6.781208038330078 GB (3136.71875 MB free)
  Uptime: 685.0 sec
  Load Avg:  1.0751953125  0.96435546875  0.5556640625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmark: 30 Apr 2023 - 1:24
* Package commit: a2f0bd
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
| `["append", "append!!(::SVector, ::SingletonVector)"]`                                      |  11.712 ns (5%) |           |                 |             |
| `["append", "append!!(::Vector, ::SingletonVector)"]`                                       | 502.709 μs (5%) |           |                 |             |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]`                                 |  11.712 ns (5%) |           |                 |             |
| `["collectors", :(:comp => "filter"), :(:impl => "base")]`                                  |  39.201 μs (5%) |           | 128.66 KiB (1%) |          14 |
| `["collectors", :(:comp => "filter"), :(:impl => "coll")]`                                  |  48.901 μs (5%) |           | 284.81 KiB (1%) |        5012 |
| `["collectors", :(:comp => "filter"), :(:impl => "nonexpanding")]`                          |  46.901 μs (5%) |           | 312.75 KiB (1%) |        5005 |
| `["collectors", :(:comp => "filter"), :(:impl => "vec")]`                                   |  39.001 μs (5%) |           | 128.59 KiB (1%) |          13 |
| `["collectors", :(:comp => "map"), :(:impl => "coll")]`                                     |   8.800 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "man")]`                                      |   9.300 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "safe_coll")]`                                |  12.401 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "vec")]`                                      |  73.101 μs (5%) |           | 256.64 KiB (1%) |          14 |
| `["dataframes", "Categorical"]`                                                             | 518.452 ms (5%) | 73.731 ms | 804.14 MiB (1%) |     4024332 |
| `["dataframes", "Int-Int"]`                                                                 |   1.121 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-Int"]`                                                             |   1.533 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-String"]`                                                          |   1.464 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["dataframes", "String-String"]`                                                           |   1.444 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :empty)]`     |  43.601 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :equal)]`     |  23.800 μs (5%) |           |                 |             |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :half)]`      |  39.201 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", :(:combine => :+), :(:desttype => :widen), :(:destkeys => :empty)]`          |  39.800 μs (5%) |           |  92.31 KiB (1%) |          18 |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :empty)]` |  41.301 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :equal)]` |  20.500 μs (5%) |           |                 |             |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :half)]`  |  38.101 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", :(:combine => :right), :(:desttype => :widen), :(:destkeys => :empty)]`      |  37.000 μs (5%) |           |  92.31 KiB (1%) |          18 |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1036-azure #43-Ubuntu SMP Wed Mar 29 16:11:05 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       8620 s          0 s       1598 s      43735 s          0 s
       #2  2593 MHz      32926 s          3 s       2200 s      18707 s          0 s
       
  Memory: 6.781208038330078 GB (3147.39453125 MB free)
  Uptime: 546.0 sec
  Load Avg:  1.080078125  0.87451171875  0.46240234375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmark: 30 Apr 2023 - 1:26
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

| ID                                                                                          | time            | GC time    | memory          | allocations |
|---------------------------------------------------------------------------------------------|----------------:|-----------:|----------------:|------------:|
| `["append", "append!!(::SVector, ::SingletonVector)"]`                                      |  11.712 ns (5%) |            |                 |             |
| `["append", "append!!(::Vector, ::SingletonVector)"]`                                       | 502.509 μs (5%) |            |                 |             |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]`                                 |  11.712 ns (5%) |            |                 |             |
| `["collectors", :(:comp => "filter"), :(:impl => "base")]`                                  |  38.301 μs (5%) |            | 128.66 KiB (1%) |          14 |
| `["collectors", :(:comp => "filter"), :(:impl => "coll")]`                                  |  49.101 μs (5%) |            | 284.81 KiB (1%) |        5012 |
| `["collectors", :(:comp => "filter"), :(:impl => "nonexpanding")]`                          |  46.600 μs (5%) |            | 312.75 KiB (1%) |        5005 |
| `["collectors", :(:comp => "filter"), :(:impl => "vec")]`                                   |  38.801 μs (5%) |            | 128.59 KiB (1%) |          13 |
| `["collectors", :(:comp => "map"), :(:impl => "coll")]`                                     |   8.900 μs (5%) |            |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "man")]`                                      |   8.800 μs (5%) |            |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "safe_coll")]`                                |  12.000 μs (5%) |            |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "vec")]`                                      |  70.702 μs (5%) |            | 256.64 KiB (1%) |          14 |
| `["dataframes", "Categorical"]`                                                             | 662.700 ms (5%) | 103.165 ms | 909.14 MiB (1%) |     5335052 |
| `["dataframes", "Int-Int"]`                                                                 |   1.132 ms (5%) |            | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-Int"]`                                                             |   1.513 ms (5%) |            | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-String"]`                                                          |   1.547 ms (5%) |            | 160.27 KiB (1%) |       10252 |
| `["dataframes", "String-String"]`                                                           |   1.510 ms (5%) |            | 160.27 KiB (1%) |       10252 |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :empty)]`     |  37.301 μs (5%) |            |  91.72 KiB (1%) |          14 |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :equal)]`     |  21.500 μs (5%) |            |                 |             |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :half)]`      |  35.500 μs (5%) |            |  68.34 KiB (1%) |           5 |
| `["mergewith", :(:combine => :+), :(:desttype => :widen), :(:destkeys => :empty)]`          |  41.501 μs (5%) |            |  92.31 KiB (1%) |          18 |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :empty)]` |  35.701 μs (5%) |            |  91.72 KiB (1%) |          14 |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :equal)]` |  18.300 μs (5%) |            |                 |             |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :half)]`  |  32.800 μs (5%) |            |  68.34 KiB (1%) |           5 |
| `["mergewith", :(:combine => :right), :(:desttype => :widen), :(:destkeys => :empty)]`      |  36.201 μs (5%) |            |  92.31 KiB (1%) |          18 |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1036-azure #43-Ubuntu SMP Wed Mar 29 16:11:05 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      20280 s          0 s       2066 s      45574 s          0 s
       #2  2593 MHz      35095 s          3 s       2428 s      30229 s          0 s
       
  Memory: 6.781208038330078 GB (3136.71875 MB free)
  Uptime: 685.0 sec
  Load Avg:  1.0751953125  0.96435546875  0.5556640625
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

    Architecture:                    x86_64
    CPU op-mode(s):                  32-bit, 64-bit
    Address sizes:                   46 bits physical, 48 bits virtual
    Byte Order:                      Little Endian
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Vendor ID:                       GenuineIntel
    Model name:                      Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz
    CPU family:                      6
    Model:                           85
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        7
    BogoMIPS:                        5187.81
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        2 MiB (2 instances)
    L3 cache:                        35.8 MiB (1 instance)
    NUMA node(s):                    1
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Vulnerable
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz          |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x07, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

