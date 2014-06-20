
[![Build Status](https://travis-ci.org/toggl/toggldesktop.png)](https://travis-ci.org/toggl/toggldesktop)

Build instructions
------------------

OSX and Linux
=============
First, build dependencies:
```
make deps
```
then the app itself:
```
make
```

To build, then run the app:
```
make run
```

Run unit tets with
```
make test
```

Linux 
=====
You need to install xorg-dev and qtcreator packages.

Windows
=======
We're building the Windows app using [Visual Studio Express 2013 for Windows Desktop](http://www.microsoft.com/en-us/download/details.aspx?id=40787) 

First, [build OpenSSL for Visual Studio](http://developer.covenanteyes.com/building-openssl-for-visual-studio/). From Visual Studio Tools, open up a Developer Command Prompt. cd to the project folder, then

```
cd third_party\openssl
perl Configure VC-WIN32
ms\do_ms
nmake -f ms\ntdll.mak clean
nmake -f ms\ntdll.mak 
```

Then open the solution in Visual Studio. Next, you'll need to install the net-bugsnag package: from the Tools menu select NuGet Package Manager, then Package Manager Console. Into the console, type:

```
Install-Package Bugsnag.Library
```

From the same console, install Oauth2 related packages:

```
Install-Package Google.Apis.Auth;
Install-Package Google.Apis.Oauth2.v2;
```

Downloads
---------

OSX
===
Toggl built and signed app for OSX is [available for download](https://www.toggl.com/api/v8/installer?platform=darwin&app=td&channel=stable). You need at least OSX 10.8.

Windows
=======
Toggl built and signed app for Windows is *beta* and is [availabe for download](https://www.toggl.com/api/v8/installer?platform=windows&app=td&channel=beta). App has been tested on Windows 7, 8 and 8.1

