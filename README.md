[![View detectOS on File Exchange](https://www.mathworks.com/matlabcentral/images/matlab-file-exchange.svg)](https://www.mathworks.com/matlabcentral/fileexchange/59695-detectos)

# detectOS

**detectOS** returns the name and version number of the operating system.

## Purpose

For the development of cross-platform apps in MATLAB, it is useful to know the operating system (OS) on which MATLAB is running, e.g. to select native fonts and font sizes (see **[getOSfont](https://www.mathworks.com/matlabcentral/fileexchange/60710-getosfont)**) or to fine-tune the layout and design of graphical user interface elements. **detectOS** returns the name and version number of the underlying OS for a wide range of platforms and OS versions. 

## Usage 

`OS = detectOS` returns the name of the operating system as a lowercase character vector, such as `'windows'`, `'macos'` (which includes OS X), `'solaris'`, `'aix'`, `'ubuntu'`, `'centos'`, and many other Unix/Linux distributions. It is thus much more fine-grained than MATLAB's built-in `ispc` / `ismac` / `isunix` and `computer` functions. If the OS cannot be determined, an error is thrown.

`[OS, OSVersion] = detectOS` also returns the OS version number as a numeric row vector. For example, Windows 7 SP1 (version 6.1.7601) is reported as `OS = 'windows'` and `OSVersion = [6, 1, 7601]`. If the OS version cannot be determined, a warning is issued and the empty numeric array is returned.

For a list of Windows releases, see https://en.wikipedia.org/wiki/Ver_(command).

For a list of macOS releases, see https://support.apple.com/en-us/HT201260.

## Requirements

**detectOS** requires MATLAB R2016b or above (version 1.0 runs on R2013a or above). It was tested on the following operating systems (64-bit, unless otherwise stated) and should run on a wide variety of other Unix/Linux distributions without modification:

* Windows 10 (10.0.10586)
* Windows 8.1 Update 1 (6.3.9600)
* Windows 7 (6.1.7601)
* Windows 7 (6.1.7601), 32-bit
* Windows XP Pro SP3 (5.1.2600),32-bit
* macOS Big Sur (11.2.3)
* macOS Catalina (10.15.7)
* macOS Sierra (10.12.1)
* OS X El Capitan (10.11.6)
* Ubuntu 16.04 LTS
* Ubuntu 15.10
* Ubuntu 14.04 LTS
* CentOS 7
* CentOS 6.8 (Final)

## Motivation

Another great tool returning information about the CPU and operating system is **[CPU Info](https://www.mathworks.com/matlabcentral/fileexchange/33155-cpu-info)**. Unfortunately, **CPU Info** does not differentiate between Unix/Linux distributions, and does not return sensible information about the OS version in these cases. Adding this capability was the main motivation for developing **detectOS**.

## Feedback

Please let me know if you have tested **detectOS** on other operating systems. Any feedback or suggestions for improvement are welcome!
