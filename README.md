# detectOS

**detectOS** returns the name and version number of the operating system.

## Purpose

For many cross-platform applications, it is useful to know the operating system (OS) on which MATLAB code is running, *e.g.* to select native fonts and font sizes or to fine-tune the layout and design of graphical user interface elements. **detectOS** returns the name and version number of the underlying OS for a wide range of platforms and OS versions. 

## Usage 

`OS = detectOS` returns the name of the operating system as one of the following, lowercase strings: `'macos'`, `'windows'`, `'solaris'`, `'aix'` or another Unix/Linux distribution (`'ubuntu'`, `'centos'`, etc.). If the OS cannot be determined, an error is thrown.

`[OS, OSVersion] = detectOS` also returns the OS version number as a numeric row vector. For example, Windows 7 SP1 (Windows version 6.1.7600) is identified as `OS = 'windows'` and `OSVersion = [6, 1, 7601]`. If the OS version cannot be determined, a warning is issued and the empty numeric vector is returned.

For a list of Windows releases, see https://en.wikipedia.org/wiki/Ver_(command).

For a list of Mac releases, see https://support.apple.com/en-us/HT201260.

## Systems Tested

All tested operating systems are 64-bit unless otherwise stated.

* OS X El Capitan (10.11.6) with R2013a, R2014b, R2015a, R2015b, R2016a, R2016b
* Windows XP Pro SP3 (5.1.2600) with R2014b, R2015a (32-bit)
* Windows 7 (6.1.7601) with R2014b, R2015b (32-bit)
* Windows 7 (6.1.7601) with R2015b, R2016a, R2016b
* Windows 8.1 Update 1 (6.3.9600) with R2015b, R2016a, R2016b
* Windows 10 (10.0.10586) with R2015b, R2016a, R2016b
* Ubuntu 14.04 LTS with R2014b, R2015b, R2016a, R2016b
* Ubuntu 15.10 with R2014b, R2015b, R2016a, R2016b
* Ubuntu 16.04 LTS with R2015b, R2016a, R2016b
* CentOS 6.8 (Final) with R2015b, R2016a, R2016b
* CentOS 7 with R2015b, R2016a, R2016b

**detectOS** should also run on a wide variety of other Unix/Linux distributions without modification.

## Requirements

Requires MATLAB R2013a or later.

## Feedback

Please let me know if you have tested **detectOS** on other operating systems.

Any help in improving the code is greatly appreciated!
