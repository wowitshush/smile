# smile
**smile** is a lightweight operating system inspired by RSX11, VMS, and other historical operating systems, written in pure assembly. it currently targets the Z80 and Z180 processors running on rc2014 (or compatible) hardware, but is planned to be ported to the PDP11.

## inspiration
having explored the world of retrocomputing for a few years now, i've had the pleasure of learning quite a bit about the operating systems that came and went long before my time. i am particularly drawn to RSX11 and VMS, and the overall design of **smile** will ultimately reflect that. i feel that while we have learned many lessons through decades of hard work and skilled research, there are many that we have forgotten. some features that i have found to be indispensable in historic operating systems that i use are sorely missing when i return to my typical x86 or ARM machine. the thesis of this project is to show that looking back on things we once wrote off as archaic or silly, some can find a place in the modern computing landscape.

## a word of warning
this is a hobbyist project, and should not be seen as anything more than that. things will break, so if you value your data keep good backups. i am neither an expert in systems programming nor assembly, so expect less-than-production-quality code. i'll do my best.

## features
* unix-like, to an extent
  * unix is generally more user-friendly than RSX11 or VMS, so we attempt to behave similarly
* flexible, configurable hierarchical versioning filesystem
  * with the exception of certain files such as databases, new versions of files will be created with `;n+1` appended to their filename where `n` is the previous version of that same file
* system device and resource tailoring
  * `SYSGEN` allows a user to add or remove devices or adjust resource allocations at will, allowing for highly tailored, efficient systems
* native security facilities
  * see [here](http://www0.mi.infn.it/~calcolo/OpenVMS/ssb71/6346/6346ptoc.htm) for a better understanding of my thought process. not necessary in a hobbyist OS, sure, but why not? :)
* smart command line interpreter
  * many features (the ability to input abbreviated commands (`HEL` instead of `HELLO`, for instance) will be cribbed from DCL (the RSX11/VMS CLI) to provide a powerful, yet easy to use CLI

## project ideology
* be light - the executive and system services must leave as much room as possible for users
* be flexible - users must be able to tailor their system to their hardware to further conserve resources
* be kind - while RSX11 and VMS are clear inspirations, aim to be more friendly and approachable to novice users
* be open - **smile** will be friendly and responsive to community contributions, and will embrace any forks
* be reliable - uptime and stability are the key focuses

## long-term goals
* compilers and interpreters for C, F77, BASIC, etc
* APIs for interacting with rc2014 modules
* 
