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

##### Program:
### Developed By: K. N A G U L
### Register Number: 212222230089


## Output:

### i) Read and display the image

```py
    import cv2
    image=cv2.imread('Dog.jpg',1)   
    image=cv2.resize(image,(400,300))
    cv2.imshow('N A G U L',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-02-15 223223](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/8ad47d8a-6b7c-4d42-9528-bdb153fecafc)

### ii)Write the image
```
    import cv2
    image=cv2.imread('Dog.jpg',0)
    cv2.imwrite('White Dog.jpg',image)
```
## Output:
![image](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/22d7ae02-9d57-47d8-97c8-beebca453676)

### iii)Shape of the Image
```
    import cv2
    image=cv2.imread('Dog.jpg',1)
    print(image.shape)
```
## Output:
![image](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/340c5a3c-fcc6-42e0-83de-c2534156a023)


### iv)Access rows and columns
```
    import random
    import cv2
    image=cv2.imread('Dog.jpg',1)
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
## Output:
![Screenshot 2024-02-15 223341](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/82d35846-4270-4547-971f-fd2796c6673a)


### v)Cut and paste portion of image
```
   import cv2
   image=cv2.imread('Dog.jpg',1)
   image=cv2.resize(image,(400,400))
   tag =image[130:200,110:190]
   image[110:180,120:200] = tag
   cv2.imshow('partimage1',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-02-15 223422](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/5c360329-1251-4404-91c6-cd0bdf16e736)


### vi) BGR and RGB to HSV and GRAY
```
import cv2
img = cv2.imread('Dog.jpg',1)
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
## Output:
![Screenshot 2024-02-15 223513](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/15b9a41b-4b4b-4893-8454-73e0ed80f3fb)
![Screenshot 2024-02-15 223520](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/ab88d9e0-8d65-41ee-ac7f-08f95967973d)
![Screenshot 2024-02-15 223542](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/eea6487e-235b-4b0a-8f09-fe26948f397f)
![Screenshot 2024-02-15 223534](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/0f4fbfe5-ac5e-433e-9240-19d363feca37)
![Screenshot 2024-02-15 223527](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/312a4457-4b3f-42da-8e0b-5b7866fc14e9)


### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('Dog.jpg')
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
## Output:
![Screenshot 2024-02-15 223625](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/646eace9-d6a3-4cbc-a6d7-c592280cedb3)
![Screenshot 2024-02-15 223639](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/9fcd6d3e-5137-4768-b9f7-dbe94b7c74de)
![Screenshot 2024-02-15 223632](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/cecff5c6-30aa-4cda-aaa7-612a9264ebcd)



### viii) RGB and BGR to YCrCb
```
import cv2
img = cv2.imread('Dog.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-02-15 223805](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/f6430691-a215-4d0a-b3dd-6095756771f8)
![Screenshot 2024-02-15 223820](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/529d2633-3041-4e36-b544-a5eaea2de6db)
![Screenshot 2024-02-15 223813](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/466eb010-9d44-4344-ab7d-5718dc2545be)

### ix) Split and merge RGB Image
```
import cv2
img = cv2.imread('Dog.jpg',1)
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
## Output:
![Screenshot 2024-02-15 223907](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/3673e041-7d23-45cf-8fb6-8701177d3115)
![Screenshot 2024-02-15 223940](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/f6c643af-90f6-42e8-809a-dec503bc1654)
![Screenshot 2024-02-15 223932](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/7d0b5b1e-6dd7-49af-96a3-afc382feface)
![Screenshot 2024-02-15 223917](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/4af97389-bce3-47f8-9d5c-1219d7e5f317)


### x) Split and merge HSV Image
```
import cv2
img = cv2.imread("Dog.jpg",1)
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
## Output:
![Screenshot 2024-02-15 224020](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/ebe3a6d7-21c2-4119-8517-5eda06be194d)
![Screenshot 2024-02-15 224036](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/0908dbe0-1eb7-41a7-91e2-ad026b40e2de)
![Screenshot 2024-02-15 224029](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/0a4d43b4-f362-4b86-998f-0ab94cff69ca)
![Screenshot 2024-02-15 224012](https://github.com/Nagul71/COLOR_CONVERSIONS_OF-IMAGE/assets/118661118/e761c2b3-c3fc-4f20-833b-459d2c63080f)




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







