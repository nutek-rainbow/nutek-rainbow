
# RainbowProbe repository #

## *) Description ##

Nutek RainbowProbe development, using C++, cmake on Arm MX8M.


git clone https://github.com/nutek-rainbow/RainbowProbe.git

Nutek platform is explained on web page:
[Nutek](https://nutekmedtech.com/ "Nutek")

[MX8M](https://www.variscite.com/product/system-on-module-som/cortex-a53-krait/dart-mx8m-nxp-imx-8m/ "MX8M")

## 1) Prerequisits  ##
To build platform, following tools have to be pre-installed:

### 1.1) Visual Studio Community 2022 ###

[Community 2022](https://visualstudio.microsoft.com/vs/community/ "Community 2022")
 
If you have multiple Visual Studio versions or MSVC versions installed, you must go to vcpkg/triplets/x64-windows and set(VCPKG_PLATFORM_TOOLSET v142)

see: [Triplets](https://www.python.org/downloads/release/python-3105/ "Triplets")

otherwise your latest installed compiler will be used which is not guaranteed to work when you intend to mix compiler-versions.
Optionaly you cann install also msbuild: Build Tools for Visual Studio 2022 

Build script was also successfully tested to work with VS 2022 installation, which should be 
automatically detected

### 1.2) Notepad++ ###
  https://notepad-plus-plus.org/downloads/

### 1.3) GIT ###
  https://git-scm.com/download/win

### 1.4) 7z zip tool ###
  https://www.7-zip.org/download.html

### 1.5) python ###
  in same partition with all options:
    
  [Python310](https://www.python.org/downloads/release/python-3105/ "Python310")
   
### 1.6) CMAKE: ###
  https://cmake.org/download/

### 1.7) powershell ###
  [Powershell](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.2#msi "Powershell")
  
  and start it ALWAYS in "administrator" mode !!!


## 2) ARTIFACT (TARGET) ##
  On succesfull build, following is created:
  
### 2.1) RainbowScanner.deb ###
  To be installed on handheld platform

### 2.2) RainbowPanel.deb ###
  To be installed on GUI device, probably same MX8M

### 2.3) install ###

## 2.4) usage in project ##
  start build.bat or build.sh (depending on operating system)


## 3) Modifying VCPKG package&port list ##


### 3.1) own port list ###

### 3.2) port files ###
  When changing anything on port files, like wibu: (C:\vcpkg-registry\versions\w-\wibu.json),
  then you have to take its commit SHA ( by calling "git rev-parse HEAD:ports/wibu")
  and set the SHA in the version reference (C:\vcpkg-registry\versions\w-\wibu.json) 
  "git-tree": "b07897ca8ba07f7ef5532e6fed01c19b8260e55c"

### 3.3) checking in ###
  After that or when changing vcpkg.json or vcpkg-configuration.json, or ANYTHING in repo,
	

## 4) Caution saveats ##

### 4.1) concept ###
  Reason and meaning of this repository is explained here:
  


### 4.3) Github PAT token ###
  In August 2021 GutHub has changed their security policy and old User/Pass concept doesn't work anymore.
  You have to use Personal Access Token, as described here:
   
  [Github PAT](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token "Github PAT")

### 4.4) git clone ###
  If GitHub connection doesn't work, you have to check the PAT used in Jenkins Job scripts and renew it with fresh ones.
  New git call should like like this:
  
  git clone https://ghp_XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX@github.com/CADstarGmbH/scanner.git


## 5) Concept ##
 

### 5.1) MX8M ###

![Alt text](doc/screenshots/CaptureMx8mini.png?raw=true "MX8M") 

### 9.7) list of covering pages  ###


## 10) Document editing ##

[Editor rules](https://github.com/tchapi/markdown-cheatsheet "editor")



