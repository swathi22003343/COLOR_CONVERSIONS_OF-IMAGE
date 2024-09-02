# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

### Program:
### Developed By:SWATHI D
### Register Number:212222230154
i) Read and display the image
```
import cv2
image=cv2.imread('swathi.jpg',1)
image = cv2.resize(image, (400, 300))
cv2.imshow('swathi d',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


## Output:

### i) Read and display the image
![Screenshot 2024-09-02 101907](https://github.com/user-attachments/assets/512900c8-90a4-4e2d-b491-cbcef3fc151b)


<br>
<br>

### ii)Write the image
```
 cv2.imwrite('b.jpg',image)
```
## OUTPUT:
![Screenshot 2024-09-02 105646](https://github.com/user-attachments/assets/c639b8ac-a799-4c77-a2af-01d5b55af39b)

<br>
<br>

### iii)Shape of the Image
```
print(image.shape)
```
## OUTPUT:
![Screenshot 2024-09-02 102345](https://github.com/user-attachments/assets/80fd3d83-7e30-44d0-b9a4-5c48ff10e57c)

<br>
<br>

### iv)Access rows and columns
```
import random
image=cv2.resize(image,(400,400))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),
                     random.randint(0,255),
                     random.randint(0,255)] 
cv2.imshow('swathi-1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT:
![Screenshot 2024-09-02 102512](https://github.com/user-attachments/assets/048477fc-fb1a-4ed3-9a4c-9185fe523073)

<br>
<br>

### v)Cut and paste portion of image
```
image=cv2.imread('swathi.jpg',1)
image=cv2.resize(image,(400,400))
tag =image[130:200,110:190]
image[110:180,120:200] = tag
cv2.imshow('swathi-2',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/1179bf36-06a3-442a-8b4d-5cdf324d1ac2)

<br>
<br>

### vi) BGR and RGB to HSV and GRAY
```
img = cv2.imread('swathi.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)

hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)

hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)

gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)

gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT:
![Screenshot 2024-09-02 102818](https://github.com/user-attachments/assets/5d7a8c4f-fef0-42eb-bd63-6d24b325e67d)
![image](https://github.com/user-attachments/assets/cbe6cd32-c768-422a-8286-147ee832894e)

![Screenshot 2024-09-02 102832](https://github.com/user-attachments/assets/f139acd6-13ca-422b-a41a-a3167f2445ee)
![Screenshot 2024-09-02 102913](https://github.com/user-attachments/assets/695c418c-ec84-4a3a-9eee-25d078fd18d4)
![Screenshot 2024-09-02 102955](https://github.com/user-attachments/assets/a01b4d6e-7e9b-4249-9425-ae4dcd14439f)




<br>
<br>

### vii) HSV to RGB and BGR
```
img = cv2.imread('swathi.jpg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT:
![Screenshot 2024-09-02 103122](https://github.com/user-attachments/assets/3735410a-5ae0-4589-9f74-540dbfb343ee)
![Screenshot 2024-09-02 103111](https://github.com/user-attachments/assets/d81f571e-70c1-4b52-b4dd-0cd5e6a1cd26)
![Screenshot 2024-09-02 103101](https://github.com/user-attachments/assets/91b1c4ed-3f5f-40fd-ae66-386977e79584)




<br>
<br>

### viii) RGB and BGR to YCrCb
```
img = cv2.imread('swathi.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT:
![Screenshot 2024-09-02 103205](https://github.com/user-attachments/assets/d1ca0bf9-ead4-49b9-8aa5-9b83b458a19c)
![Screenshot 2024-09-02 103245](https://github.com/user-attachments/assets/291f776b-95d2-44a9-83d9-d71b5417fbbb)
![Screenshot 2024-09-02 103232](https://github.com/user-attachments/assets/c2332a6e-f40c-4f12-96e0-cfd77f350a40)



<br>
<br>

### ix) Split and merge RGB Image
```
img = cv2.imread('swathi.jpg',1)
img = cv2.resize(img,(300,200))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]
cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)
merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT:
![Screenshot 2024-09-02 103517](https://github.com/user-attachments/assets/5604bb2a-ab46-40ae-acfa-b5b0fd24dccd)
![Screenshot 2024-09-02 103337](https://github.com/user-attachments/assets/37c70041-71c9-4ac5-92e4-3781883088b1)
![Screenshot 2024-09-02 103454](https://github.com/user-attachments/assets/d764a91b-d888-4daf-85c2-e1956553861b)
![Screenshot 2024-09-02 103504](https://github.com/user-attachments/assets/4e31b2e5-df89-446c-a6be-4f613993575d)


<br>
<br>

### x) Split and merge HSV Image
```
img = cv2.imread("swathi.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
H,S,V=cv2.split(img)
cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)
merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT:

![Screenshot 2024-09-02 125447](https://github.com/user-attachments/assets/751e0f31-60a4-4077-8f5f-4d11ef377b3e)


![Screenshot 2024-09-02 124907](https://github.com/user-attachments/assets/14fb73d3-1a0b-4192-8504-0d720be2ed93)

![Screenshot 2024-09-02 124943](https://github.com/user-attachments/assets/33643ac1-3941-4b41-9f79-201497683e2a)

![Screenshot 2024-09-02 125003](https://github.com/user-attachments/assets/4af3a2f9-e6b9-4e77-abed-397d41857c9e)




<br>
<br>




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







