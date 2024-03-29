# Build instructions for Gentoo Linux

Updated 2024-03-29

---

> [!WARNING]
> Please note that we do not give support for compiling the viewer on your own. However, there is a self-compilers group in Second Life that can be joined to ask questions related to compiling the viewer: [Firestorm Self Compilers](https://tinyurl.com/firestorm-self-compilers)

This procedure is based on discussions with the Firestorm Linux development team and is the only one recommended for Firestorm for Linux. System requirements are:
- Gentoo Linux (x86_64)
- GNOME or KDE Desktop Profile (Hardened profile is not available)
- 16GB or more RAM ([Low Memory Caution](#common-issuesbugsglitches-and-solutions))
- 64GB hard drive space 
- 4 or more core CPU (you could get by with 2 cores, but the process will take much longer)
- GCC 13.2 compiler (which is the default version on Gentoo Linux)

> [!WARNING]
> A system with a glibc version of at least 2.37 is required (Gentoo Linux meets this requirement) 
> Building on a system with a glibc version older than 2.37 will likely result in linker errors.

> [!IMPORTANT]
> Only 64 bit builds (multilib and no-multilib profile) are possible - 32 bit (x86 profile) support was dropped quite some time ago.

## Establish your programming environment

This only needs to be done once.

### Create your source tree

Typically, Linux source code is stored in a src directory in your home directory. So: `mkdir ~/src`

### Install required packages

A few packages must be installed on the build system. Some may already be installed: