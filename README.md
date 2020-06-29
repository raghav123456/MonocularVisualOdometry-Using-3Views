## Odometry using MOIL LIBRARY genrating 3 View 

We used approach designed in MOIL-Lab ,  “MOIL SDK- MCUT Omnidirectional Imaging Lab” to extricate the fisheye picture into 6 diverse view as: Front, Left, Right, Down, Lower left, Lower right separately. By utilizing this technique, we made a direction of 6 view by  the arrangement of fisheye pictures as a source document for odometry.​

 It means we use source fisheye images and integrate that with MOIL Library and generate 6-view odometry.

**Calibration Parameter T265 CAMERA:** 

```
Focal Length:  618.8560
Center or Principle point: (427, 394)
```
**MOIL LIBRARY PARAMETERS**

```
	md->Config("car", 3, 3,
			427,394, 1, //center
			848, 800, 1.68, // resolution
			0, 0, -24.964, 38.2, -16.956, 183.42 //calibration
	);
```
## HOW TO RUN ON TERMINAL

Step 1.Open Terminal 

Step 2.
```
git clone https://github.com/Shivani1796/MonocularVisualOdometry-Using-3Views.git
```

Step 3.Compile command
 ```
     cd MonocularVisualOdometry-Using-3Views
     mkdir build 
     cd build 
     cmake .. 
     make 
 ```
Step 4.Run command
```
	./vo /home/shivani/Documents/mydataset/D5_17-04/poses/D5.txt /home/shivani/Documents/fisheye-test-images/D5/%d.png 3.4 0,0 -10,0 10,0
	
```
**DESCRIPTION:**

Argument 1: Ground Truth Data (/home/shivani/Documents/mydataset/D5_17-04/poses/D5.txt)
Argument 2: Image sequence  (/home/shivani/Documents/fisheye-test-images/D5/%d.png)
Argument 3: Zoom Factor (3.4)
Argument 4: Front View angle 
Argument 5: Left View angle
Argument 6: Right View angle

 **NOTE**
- Change img_path and pose_path to correct image sequences and pose file paths according to your system.
- Ensure focal length and principal point information is correct .
---------------------------------------------------------------------------------------------------------------------------

## HOW TO RUN ON ECLIPSE

Please follow the below url to understand how to clone poject on Eclipse

https://bit.ly/31ph49X

---------------------------------------------------------------------------------------------------------------------------

## Odometry using Round Path

<p align="center">
  <img src="https://github.com/Shivani1796/FinalCode-MVO-/blob/master/img/result1%20.png">
</p>



## Odometry using long path
<p align="center">
  <img src="https://github.com/Shivani1796/FinalCode-MVO-/blob/master/img/result2.png">
</p>



## Odometry using Straight Path
<p align="center">
  <img src="https://github.com/Shivani1796/FinalCode-MVO-/blob/master/img/result3.png">
</p>
