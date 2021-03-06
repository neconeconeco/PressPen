# PressPen
A stylus supporting painting in the 3D space by pressure measurement

## Introduction
PressPen is a 3D input stylus combining pressure measurement and computer vision pose tracking algorithm. With the development and commercialization of AR/VR technology, various companies have distributed a variety of 3D input devices while developers have developed a large amount of interactive applications for them. However, there are two defects of present 3D input devices: 1. Complexity in setting up a working space; 2. Unclearness in expressing the intensity of user intension. From the perspective of those disadvantages, the work proposed PressPen, which use single web camera to track the position and rotation of the stylus, which allow users set up working space easily, and is embedded with a Bluetooth pressure sensor, which allows user intension determination.

To be more specific, to track the pose of the pen, a combination of approximate pose estimation (APE) and inter-frame corner tracking (ICT) is used in the tracking algorithm. Then the C++ algorithm is exported to be used in C# (Unity3d). As for pressure measurement, Unity3d use Bluetooth interface to obtain the pressure data transmitted from pen, which measures pressure by pressure sensor and broadcast it with Bluetooth module. Integrating both pose tracking and pressure measurement, PressPen library provides developers APIs to obtain pose and pressure value information of every frame. What’s more, the work contains two interactive applications to demonstrate the functionality of PressPen.

## Submodules
The project mainly contains three parts: 1. Realization of tracking algorithm, 2. Design and assemble hardware, 3. Development of interactive applications.  

|id|dictionary name|introduction|  
|-|-|-|  
|1|[Interactive Application](Interactive%20Application)|Contains PressPen library for Unity3d with two interactive application developed by Unity3d: 1. 3D paiting application, 2. 3D sandbox application|  
|2|[Pen Tracking Algorithm](Pen%20Tracking%20Algorithm)|Partial realization of *DodecaPen* by C++ and interface for C#. ARTest is the first version while Markermapper is the final version which is more clean and extendible|  
|3|[Pressure Measurement](Pressure%20Measurement)|Design and result of the hardware and some Arduino code for it|  

## Demo Video
A Chinese demo video could be found on [Youtube](https://youtu.be/TBKHy2FkBvc). 
 
