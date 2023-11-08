# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>
Import the required


### Step2:
<br>
Convert the input image to gray, to get more details and for the laplacian operator, we have to convert the input image to BGR format

### Step3:
<br>
Apply smoothing to reduce noise, here we are using Gaussian blur

### Step4:
<br>
Perform the edge detector operation

### Step5:
<br>
Show to detected image

 
## Program:



# Import the packages
```
import cv2

```


# Load the image, Convert to grayscale and remove noise
```
i=cv2.imread('flower.jpg',-1)
gray=cv2.cvtColor(i,cv2.COLOR_BGR2GRAY)
img = cv2.GaussianBlur(gray,(3,3),0)

```

# SOBEL EDGE DETECTOR
```
sobel_x=cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
cv2.imshow('sobel_x',sobel_x)
cv2.waitKey(0)
cv2.destroyAllWindows()
sobel_y=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
cv2.imshow('sobel_y',sobel_y)
cv2.waitKey(0)
cv2.destroyAllWindows()
sobel_xy=cv2.Sobel(img,cv2.CV_64F,1,1,ksize=5)
cv2.imshow('sobel_xy',sobel_xy)
cv2.waitKey(0)
cv2.destroyAllWindows()
```




# LAPLACIAN EDGE DETECTOR
```
rgb_image = cv2.cvtColor(i,cv2.COLOR_BGR2RGB)
laplacian_operator = cv2.Laplacian(rgb_image,cv2.CV_64F)
cv2.imshow('laplacian_operator',laplacian_operator)
cv2.waitKey(0)
cv2.destroyAllWindows()
```



# CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(img, 120, 150)
cv2.imshow('canny',canny_edges)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### SOBEL EDGE DETECTOR
<br>
<img width="450" alt="image" src="https://github.com/Jeswanth21001768/EDGEDETECTION/assets/94155480/406091c8-f46b-4c74-909e-389073415b1c">

<br>
<img width="453" alt="image" src="https://github.com/Jeswanth21001768/EDGEDETECTION/assets/94155480/cae7e713-e614-4559-bdd5-3b0a23b093af">

<br>
<img width="450" alt="image" src="https://github.com/Jeswanth21001768/EDGEDETECTION/assets/94155480/8f911550-0cc6-48da-9b70-844f19a90126">

<br>




<br>


### LAPLACIAN EDGE DETECTOR
<br>
<br>
<img width="453" alt="image" src="https://github.com/Jeswanth21001768/EDGEDETECTION/assets/94155480/2a2b7a11-7d5b-40b6-b995-acb0175257f0">
<br>
<br>
<img width="458" alt="image" src="https://github.com/Jeswanth21001768/EDGEDETECTION/assets/94155480/1e269f73-462d-4a2e-aa93-66126508a051">

<br>
<br>


### CANNY EDGE DETECTOR
<br>
<img width="450" alt="image" src="https://github.com/Jeswanth21001768/EDGEDETECTION/assets/94155480/46d0a019-0423-435b-9b20-ba6f98473768">

<br>

<br>
<br>
<br>
<br>

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
