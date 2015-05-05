Simple background removal and ROI estimation 
============================================

Contributors: Petri Kainiemi, Ilkka Salento

While developing with Kinect and especially when Kinect's low-level depth stream
is involved it is often required to get environment seen in depth frame layered
using depth values and unneeded data removed. That unneeded data is often considered 
as a background data. In addition bounds of the object which later enters the scene may
need to be identified. 

This repository represents a simple method to remove the background and find the bounds 

**Background removal algorithm**

Background removal algorithm calculates average depth values of first 10 sequential depth 
Some of the pixels in the depth frames may have zero value due to how distance is calculated with 
 
Resulting averaged depth frame is subtracted pixel by pixel from the input depth frame and if 
needs to be specifically set case by case depending on object�s distance from background and noise. 
 
**Region Of Interest (ROI) estimation**
 
Boundaries of the object can be identified by finding out the minimum and maximum coordinates from 
coordinates from foreground kernels. 
