
# RainbowProbe project #

## 1) Description ##

Nutek RainbowProbe cancer scanner on Arm MX8M platform

### 1.2) Profile ###

Company description: [Nutek](https://nutekmedtech.com/ "Nutek")

![Alt text](doc/screenshots/NutekBig.png?raw=true "Nutek")

### 1.3) Location ###

We are hosted at technological center ZWT in Graz, Austria [ZWT](https://www.zwt-graz.at/ "ZWT") 

![Alt text](doc/screenshots/ZWT.png?raw=true "ZWT")

Managed by team: [ZWT](https://www.humantechnology.at/team/ "ZWT-team") 


## 2) Concept ##

The main goal is to get high-tech (and look&feel) product at lowest runtime retail price.

The concept is proven “factory automation” way (Soft PLC), where the solution consists of two main components:

### 2.1) Scanner ###

![Alt text](doc/screenshots/VideoProcessingRealtime.png?raw=true "Scanner")

Realtime Data acquisition and digital analysis :
 * Linux on MX8M board 
 * Realtime service C++ process processing image data, dedicated to 1 core
 * Internal threads taking care about capturing image frames, storing, sorting
 * Each incoming frame gets assigned one thread to make pre-analysis
 * Integration thread tries to make whole picture by merging incoming frames

[MX8M](https://www.variscite.com/product/system-on-module-som/cortex-a53-krait/dart-mx8m-nxp-imx-8m/ "MX8M")
 
![Alt text](doc/screenshots/CaptureMx8mini.png?raw=true "MX8M")

 
### 2.2) Panel ###

![Alt text](doc/screenshots/VideoProcessingNodeJs.png?raw=true "Panel")

Basically , it should be possible to capture the FrameBuffer on MX8 mini and send it to Bluetooth Screen.
As cheap solution is also classic solution of “any” tablet (starting at 75eur), connected over Bluetooth or WiFi.
This could also be any laptop or standalone PC.
Main goal should be spreading the CPU/GPU load over more tasks (cores, chips) in order to get balanced
system , which wouldn’t produce too much concentrated heat and be able to cool it very simply
At the end comes GUI implemented by JavaScript module, offering wide range of stylistic platforms

#### 2.2.1) WebExplorer (node.js) #### 

Independent GUI Presentation on Touchpanel (bluetooth raw GUI or blutooth WebBrowser)
 * Node.js web engine with C++ AddOn extensions for dedicated Image handling
 * JavaScript UI for dynamic modern user interface
 * Direct FrameBuffer output or standalone WebBrowser

![Alt text](doc/screenshots/CaptureAmazon7.png?raw=true "Tablet")

![Alt text](doc/screenshots/NodeJs.png?raw=true "NodeJs")

![Alt text](doc/screenshots/NodeJsAddOnCpp.png?raw=true "NodeJsC++")

#### 2.2.2) JavaScript GUI Interface  ####

![Alt text](doc/screenshots/UI-JS.png?raw=true "UI-JS")

![Alt text](doc/screenshots/UI-JS2.png?raw=true "UI-JS")

![Alt text](doc/screenshots/UI-JS9.png?raw=true "UI-JS")

## 3) Software Development ##

Repositories are kept in private space and accesible over  [Github PAT](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token "Github PAT")
They are accesible over private Git-path: 

git clone https://ghp_XXXXXXXXX---PAT---XXXXXXXXXX@github.com/nutek-rainbow/scanner.git

### 3.1) scanner ###

Is being developed in private repository, which contains cmake based C++ code,
Compile batch scipt produces installation packages at compile time.  
Instructions are available to each joined developer.

start build.bat or build.sh (depending on operating system)

There is also licensing mechanism , based on OTP Serial-Number: [OTP](https://www.digi.com/resources/documentation/digidocs/embedded/dey/3.0/cc8mnano/bsp_r_otp_8m "OTP")


https://github.com/nutek-rainbow/scanner.git

### 3.2) panel ###

Is being developed in private repository, which contains cmake based JavaScript and node.js code,
Compile batch scipt produces installation packages at compile time. 
Instructions are available to each joined developer.

https://github.com/nutek-rainbow/panel.git


## 4) Development Prerequisits  ##
To build platform, following tools have to be pre-installed:

### 4.1) Visual Studio Community 2022 ###

https://visualstudio.microsoft.com/vs/community/
 
If you have multiple Visual Studio versions or MSVC versions installed, you must go to vcpkg/triplets/x64-windows and set(VCPKG_PLATFORM_TOOLSET v142)

see: [Triplets](https://www.python.org/downloads/release/python-3105/ "Triplets")

otherwise your latest installed compiler will be used which is not guaranteed to work when you intend to mix compiler-versions.
Optionaly you cann install also msbuild: Build Tools for Visual Studio 2022 

### 4.2) Notepad++ ###
  https://notepad-plus-plus.org/downloads/

### 4.3) GIT ###
  https://git-scm.com/download/win
  https://kbroman.org/github_tutorial/pages/first_time.html

### 4.4) 7z zip tool ###
  https://www.7-zip.org/download.html

### 4.5) python ###
  in same partition with all options:  
  https://www.python.org/downloads/release/python-3105/ 
   
### 4.6) CMAKE: ###
  https://cmake.org/download/

### 4.7) powershell ###
  https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.2#msi
  and start it ALWAYS in "administrator" mode !!!
  
## 5) ARTIFACT (Installation packages) ##
  On succesfull build, operating system depending installation package is created, which is being installed as any usual

### 5.1) RainbowScanner.deb ###
  Operation system depending installation package is created To be installed on handheld platform

### 5.2) RainbowPanel.deb ###
  To be installed on GUI device, probably same MX8M

## 6) Document editing ##

[Editor rules](https://github.com/tchapi/markdown-cheatsheet "editor")



