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
Choose an image and save it as a filename.jpg.
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
```
Developed By:Yogabharathi S
Register Number:212222230179
```
### i) Read and display the image
```
    import cv2
    image=cv2.imread('dog.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('212222230179 Yogabharathi,image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
### ii)Write the image
```
    import cv2
    image=cv2.imread('dog.jpg',0)
    cv2.imwrite('demos.jpg',image)
```

### iii)Shape of the Image
```
    import cv2
    image=cv2.imread('dog.jpg',1)
    print(image.shape)
```
### iv)Access rows and columns
```
    import random
    import cv2
    image=cv2.imread('dog.jpg',1)
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

### v)Cut and paste portion of image
```
   import cv2
   image=cv2.imread('dog.jpg',1)
   image=cv2.resize(image,(400,400))
   tag =image[150:200,110:160]
   image[110:160,150:200] = tag
   cv2.imshow('partimage1',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()
```
### vi) BGR and RGB to HSV and GRAY
```
import cv2
img = cv2.imread('dog.jpg',1)
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
### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('dog.jpg')
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
### viii) RGB and BGR to YCrCb
```
import cv2
img = cv2.imread('dog.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### ix) Split and merge RGB Image
```
import cv2
img = cv2.imread('dog.jpg',1)
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

### x) Split and merge HSV Image
```
import cv2
img = cv2.imread("dog.jpg",1)
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

### i) Read and display the image

![WhatsApp Image 2024-02-15 at 7 50 52 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/2f4a5018-7941-49c7-9d7c-6ac0d78ae970)

### ii)Write the image

![WhatsApp Image 2024-02-15 at 9 29 55 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/e04e506a-edeb-4b4e-bf94-4a89ffce8631)


### iii)Shape of the Image

![Screenshot from 2024-02-15 19-36-02](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/b2923dbe-6bf7-4e6a-aa85-15eb357d5b7f)

### iv)Access rows and columns
![WhatsApp Image 2024-02-15 at 7 51 26 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/04628da1-304e-497d-a263-4efd2d6c0c97)

### v)Cut and paste portion of image

![WhatsApp Image 2024-02-15 at 7 51 38 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/5965b3d7-9fa4-4f97-94e5-2dd44c1e272b)

### vi) BGR and RGB to HSV and GRAY

![WhatsApp Image 2024-02-15 at 9 12 37 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/6efe871d-1dd9-4d66-aa26-9b5d8e29a0ff)
![WhatsApp Image 2024-02-15 at 9 13 05 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/4eb5962f-b02e-4770-b880-bace0fc5e6f2)
![WhatsApp Image 2024-02-15 at 9 12 32 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/0d3a1f30-328a-4573-831d-3bcf5d98ba37)
![WhatsApp Image 2024-02-15 at 9 13 25 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/bbbbd49b-c98a-4293-a256-2551ef827b55)
![WhatsApp Image 2024-02-15 at 9 13 14 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/b0290096-f523-4e83-a523-5f8dde6236d6)

### vii) HSV to RGB and BGR
![WhatsApp Image 2024-02-15 at 9 15 34 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/7063c25f-0ba7-4d34-8d06-8a8ebda6461b)
![WhatsApp Image 2024-02-15 at 9 15 27 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/7214c0d1-81d8-45c1-89d9-de1553d378c3)
![WhatsApp Image 2024-02-15 at 9 15 16 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/bbb79f34-a836-44f2-b051-21fd60e9291c)


### viii) RGB and BGR to YCrCb
![WhatsApp Image 2024-02-15 at 9 17 20 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/971e5326-c953-4e74-b04e-babcc6ffe8c5)
![WhatsApp Image 2024-02-15 at 9 17 30 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/e83c7624-6ff3-4308-923a-574fdd98ea06)
![WhatsApp Image 2024-02-15 at 9 17 43 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/431d2f48-b86d-4126-8ed9-1119c2ba1732)

### ix) Split and merge RGB Image
![WhatsApp Image 2024-02-15 at 9 19 18 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/ab2a34fe-87ad-4e5f-abd9-a9524b998491)
![WhatsApp Image 2024-02-15 at 9 19 44 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/670656e0-f12c-49e0-9658-303dc2078bea)
![WhatsApp Image 2024-02-15 at 9 19 36 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/75f5d20e-c1fe-457e-891c-10bd715141a4)
![WhatsApp Image 2024-02-15 at 9 20 01 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/a4acf06b-0f08-4a5e-b737-77675e5abfd7)

### x) Split and merge HSV Image
![WhatsApp Image 2024-02-15 at 9 21 18 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/2e69b65f-f6c2-4869-a6f2-4dc9e43ddc1b)
![WhatsApp Image 2024-02-15 at 9 21 29 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/0d261e25-338c-4842-b8bd-722c4c06da24)
![WhatsApp Image 2024-02-15 at 9 21 38 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/9e547f82-70aa-49d4-b014-58c51a009383)
![WhatsApp Image 2024-02-15 at 9 21 49 PM](https://github.com/Yogabharathi3/COLOR_CONVERSIONS_OF-IMAGE/assets/118899387/91514a75-abc5-46b0-925c-a12ec4f89522)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.
