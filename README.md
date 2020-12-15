# Lane-detection-for-autonomous-vehicles
Lane detection of autonomous vehicles

# Installation required -
sudo apt-get install python3-pip<br/>
pip3 install opencv-python<br/>
pip3 install scipy

# How to run -
python3 lane_detection.py --input_image <image_path><br/>
Also one find other arguments using -<br>
python3 lane_detection.py --help

# Steps involved -
Read image

![Result 1](/images/lane.jpg)
Canny edge detection : -

![Result 2](/images/canny.jpg)

Image mask: -<br/>
If first mask don't work then i am using 2nd mask and so on. In worst case, i will use four mask.<br/>
![Mask 1](/images/mask1.jpg)
![Mask 2](/images/mask2.jpg)
![Mask 3](/images/mask3.jpg)
![Mask 4](/images/mask4.jpg)

Find ROI using image mask: -<br/>
![Mask canny](/images/Masked_canny.jpg)

Detecting, classifying and averaging left and right lines with the help of hough transform: -<br/>
![lines](/images/lines.jpg)

Cropping and giving final result: -<br/>
![output](/images/output.jpg)

# Other Results -

![Result 1](/images/output4.jpg)

![Result 2](/images/output2.jpg)

![Result 3](/images/output3.jpg)

![Result 4](/images/output1.jpg)


# Conclusion -
I implimented lane using image processing techniques. Further improvement in this project may be find distance of nearest vehicle in the lane detected, so that accidents can be avoided.

# Refrences -
[Lane Detection for Autonomous Vehicles using OpenCV Library](https://www.irjet.net/archives/V6/i1/IRJET-V6I1245.pdf)
