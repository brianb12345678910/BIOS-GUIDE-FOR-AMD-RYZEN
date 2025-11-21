# BIOS GUIDE FOR AMD RYZEN

List of relevant BIOS settings aiming for performance on Ryzen systems.

## Introduction 

- Every setting is detailed with my personnal recommendation for each settings based on my researchs, commun sense and testing.																
- Those settings must not be applied simultaneously, test the impact of each settings on your performances and temps if you want to get the most out of this guide					
- Make your own researchs									
- Most options are likely to be hidden in your BIOS, there are several ways to access them but it's not the purpose of this guide		

 ## Processor core settings 
 
 **SMT Control**
 
 - Auto 
 - Enable
 - **Disable***
 
SMT Control (Simultaneous Multithreading or Hyperthreading) allows the CPU to execute multiple threads concurrently, each physical core appears as two logical cores to the operating system, and each logical core can execute its own thread. Using multiple execution threads per core requires resource sharing and is a possible source of inconsistent system response.

Some demanding games, optimized for multi-core usage will do better with SMT enabled but most competitve games don't benefit from SMT as it comes with a latency penalty so disable it if you have 6+ cores. Note that disabling SMT will give you lower power consumption and temperatures which gives you more headroom to OC and will allow your CPU to achieve higher boost clocks (cf. `

**PSS Support**

- Auto
- **Enable***
- Disable

PSS support, allows the operating system to use PSS (Performance Supported States) and related ACPI objects to control the power and performance of the processor.

PSS Support should give you better performances if you are using *Core Performance *. If you have a manual static OC it might not be the case.

**Core Performance Boost** 

- **Auto***
- Disable

Core Performance Boost allows the processor to boost to higher clock speeds under certain conditions. When enabled, the processor can boost to higher clock speeds when it is operating below certain temperature and power limits, in order to improve performance.

Basically it allows your CPU to go beyond his base clock, some sort of an auto OC.
It should be on Auto if you don't have a static OC. I personnaly don't recommend doing a static OC on Ryzen.

**Global C-state Control**

- Auto
- **Enable***
- Disable 

The Global C-States Control controls IO based C-state generation and DF Cstates, including core processor C-States.
Disabling this feature means that the CPU cores can only be in C0 (active) or C1 state because the C1 state cannot be disabled. A CPU core will be in C1 state if the core is halted by the OS. If you have a low latency or extremely low jitter use case, then consider disabling DF C-states as described in this guide. AMD strongly recommends not disabling Global C-states except for debugging.

If you are using *Core Performance Boost*, disabling this option comes with a performance penalty. You might want to disable this feature if you are using a static OC. This setting alone can have an important impact on the system's performance, make your own tests and conclusions.
