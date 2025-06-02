# GuesturePaint-Hand-Drawing
This project is a fun and practical implementation of computer vision using OpenCV, where I built a virtual "Air Canvas" that allows users to draw in the air by waving a colored object, like a fingertip marker, in front of a webcam.

The main idea was to track the motion of a colored object in real-time and use that motion to draw on a virtual canvas. I used the HSV color space for color detection because it is more robust to lighting changes than RGB. A trackbar interface was added to dynamically adjust HSV ranges for different markers.

After detecting the colored object in the frame, I applied **morphological operations** like erosion and dilation to clean up the mask and remove noise. Then, using **contour detection**, I identified the largest contour in the mask, which represents the marker. I extracted its center position and stored these coordinates to draw continuous lines on the canvas.

To make the tool more interactive, I added ink color selection buttons on the screen. When the marker touches those areas, the ink color changes accordingly.

This project helped me strengthen my understanding of real-time image processing, color segmentation, contour analysis, and OpenCV operations. It also showed how computer vision can be used to build intuitive and touch-free user interfaces.

# Algorithm

1. Start reading the frames and convert the captured frames to HSV colour space.(Easy for colour detection)
2. Prepare the canvas frame and put the respective ink buttons on it.
3.. Adjust the trackbar values for finding the mask of coloured marker.
4. Preprocess the mask with morphological operations.(Erotion and dilation)
5. Detect the contours, find the center coordinates of largest contour and keep storing them in the array for successive frames .(Arrays for drawing points on canvas)
6. Finally draw the points stored in array on the frames and canvas .

Requirements: python3 , numpy , opencv installed on your system.

# Video

https://github.com/user-attachments/assets/3b41343f-e085-4612-a1ee-87f0093d40d9

