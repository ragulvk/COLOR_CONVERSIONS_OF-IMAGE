# EX-01 COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
 #### Step1: Choose an image and save it as a filename.jpg ,
 #### Step2: Use imread(filename, flags) to read the file.
 #### Step3: Use imshow(window_name, image) to display the image.
 #### Step4: Use imwrite(filename, image) to write the image.
 #### Step5: End the program and close the output image windows.
 #### Step6: Convert BGR and RGB to HSV and GRAY
 #### Step7: Convert HSV to RGB and BGR
 #### Step8: Convert RGB and BGR to YCrCb
 #### Step9: Split and Merge RGB Image
 #### Step10: Split and merge HSV Image

### Program:

### Developed By:ONTEDDU SIRISHA
### Register Number: 212222230103
<table>
  <tr>
    <td width=50%>

### i) Read and display the image
```Python
   import cv2
    image=cv2.imread('peacock.jpg')
    cv2.imshow('SIRISHA',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:
![image](https://github.com/22003264/COLOR_CONVERSIONS_OF-IMAGE/assets/119389139/b8b9a69b-9946-48b0-a046-3d0643480cdd)


  </td>
  </tr>

   <tr>
    <td width=50%>

### ii)Write the image
```Python
    import cv2
    image=cv2.imread('peacock.jpg',0)
    cv2.imwrite('demos.jpg',image)
```
  </td>
  <td>

### OUTPUT:
![O2](https://github.com/JananiSoundararajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119477549/ec5c8983-f3d4-44de-9c37-be087c0f7a4d)


  </td>
  </tr>
  <tr>
    <td width=50%>

### iii)Shape of the Image
```Python
   import cv2
    image=cv2.imread('peacock.jpg',1)
    print(image.shape)
```
  </td>
  <td>

### OUTPUT:
![O3](https://github.com/JananiSoundararajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119477549/e212692e-0645-471a-851c-ffdb77b95494)

  </td>
  </tr>
  <tr>
    <td>
      
### iv)Access rows and columns
```Python
   import random
    import cv2
    image=cv2.imread('peacock.jpg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
  </td>
  <td width="50%">

### OUTPUT:
![O4](https://github.com/JananiSoundararajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119477549/0d190152-ff66-4efe-9295-98978bd09fc5)

  </td>
  </tr>
  <tr>
    <td width=50%>
      
### v)Cut and paste portion of image

 ```Python
   import cv2
   image=cv2.imread('peacock.jpg',1)
   image=cv2.resize(image,(400,400))
   tag =image[150:200,110:160]
   image[110:160,150:200] = tag
   cv2.imshow('partimage1',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()
```
  </td>
  <td>
    
### OUTPUT:
![O5](https://github.com/JananiSoundararajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119477549/1dbf0024-e307-4698-ad76-3434995956f1)

  </td>
  </tr>
</table>

### vi) BGR and RGB to HSV and GRAY
```Python
import cv2
img = cv2.imread('peacock.jpg',1)
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

### OUTPUT:
![O6](https://github.com/JananiSoundararajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119477549/39d5394c-bde6-459a-bbcf-378c305bffc5)

### vii) HSV to RGB and BGR
```Python
import cv2
img = cv2.imread('peacock.jpg')
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

### OUTPUT:
![O7](https://github.com/JananiSoundararajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119477549/3875f6ec-f3d9-4d08-ad0f-1d6ea9a70b47)



### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('peacock.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![O8](https://github.com/JananiSoundararajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119477549/4693bba5-570d-4d42-b98c-bc148d60560a)



### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread('peacock.jpg',1)
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

### OUTPUT:
![O9](https://github.com/JananiSoundararajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119477549/47f359ae-a89d-4ff7-a3be-ba58d0b16e27)



### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread("peacock.jpg",1)
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

### OUTPUT:
![O10](https://github.com/JananiSoundararajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119477549/8143fe85-9354-45f0-9b63-1bc68df9c40c)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.
