# DIP-APOLLO
# Basic Image manupulation
```python
#import cv2
import matplotlib.pyplot as plt
image = cv2.imread('rocket.jpg')
height=720
width=1280
print(f"Width: {width}, Height: {height}")
plt.figure(figsize=(10, 10))
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.show()
cv2.imwrite('rocket-11-Launch.png', image)
```
# output
![Screenshot 2024-10-29 115556](https://github.com/user-attachments/assets/303ed01e-cc09-41bd-9dd8-21b59fd78e8d)

```python
import cv2
import matplotlib.pyplot as plt

image = cv2.imread('rocket.jpg')

text = 'Apollo 11 Saturn V Launch, July 16, 1969 ushh'
font_face = cv2.FONT_HERSHEY_PLAIN
font_scale = 3
font_thickness = 3
text_color = (255, 255, 255)  

text_size, _ = cv2.getTextSize(text, font_face, font_scale, font_thickness)
text_x = (image.shape[1] - text_size[0]) // 2  
text_y = image.shape[0] - 50  

cv2.putText(image, text, (text_x, text_y), font_face, font_scale, text_color, font_thickness)

magenta = (255, 0, 255)  
image_rectangle = cv2.rectangle(image, (700, 60), (500, 630), magenta, thickness=3, lineType=cv2.LINE_8)

plt.figure(figsize=[12, 12])
plt.imshow(cv2.cvtColor(image_rectangle, cv2.COLOR_BGR2RGB))
plt.axis('on')
plt.show()
```
# output
![Screenshot 2024-10-29 115832](https://github.com/user-attachments/assets/35b9e5a9-e8ef-4367-8bb1-7ff20b55765d)

```python
img = cv2.imread('moulake.jpg', cv2.IMREAD_COLOR)
print(img.shape)
plt.figure(figsize=[3, 3])
plt.imshow(img[:, :, ::-1])
plt.title("Original Image")
plt.axis('off')
plt.show()
```
# output
![Screenshot 2024-10-29 120019](https://github.com/user-attachments/assets/f5fe4fb1-5689-4929-98ca-9da30d871fed)

```python
x, y, a, b = 250, 250, 250, 250
cropped_img = img[y:y+b, x:x+a]
resized_img = cv2.resize(cropped_img,None, fx=2, fy=2)
flipped_img = cv2.flip(resized_img, 1)
plt.figure(figsize=[5, 5])
plt.imshow(flipped_img[:, :, ::-1])
plt.axis('off')
plt.title("Cropped, Resized, and Flipped Image")
plt.show()
```
# output
![image](https://github.com/user-attachments/assets/e25c86aa-37f7-45f3-98f6-93e962f248a4)

```python
gray_image = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
print("Grayscale Image Shape:", gray_image.shape)
plt.figure(figsize=(10, 10))
plt.imshow(gray_image)
plt.axis('off')
plt.title("Grayscale Image")
plt.show()
```
# output
![image](https://github.com/user-attachments/assets/f7ac93ee-7c82-49b3-8148-8a09a4cdb37a)

```python
img = cv2.imread('ship.jpg', cv2.IMREAD_COLOR)
print(img.shape)
plt.figure(figsize=[3, 3])
plt.imshow(img[:, :, ::-1])
plt.title("Original Image")
plt.axis('off')
plt.show()
```
# output
![image](https://github.com/user-attachments/assets/cc9a81d9-5d98-4522-bfb1-1787775c6e87)

```python
import cv2
import matplotlib.pyplot as plt

image = cv2.imread('ship.jpg')

text = 'Ship gushhhhh'
font_face = cv2.FONT_HERSHEY_PLAIN
font_scale = 3
font_thickness = 3
text_color = (255, 255, 255)  

text_size, _ = cv2.getTextSize(text, font_face, font_scale, font_thickness)
text_x = (image.shape[1] - text_size[0]) // 2  
text_y = image.shape[0] - 50  

cv2.putText(image, text, (text_x, text_y), font_face, font_scale, text_color, font_thickness)

magenta = (255, 0, 255)  
image_rectangle = cv2.rectangle(image, (400, 200), (300, 280), magenta, thickness=3, lineType=cv2.LINE_8)

plt.figure(figsize=[12, 12])
plt.imshow(cv2.cvtColor(image_rectangle, cv2.COLOR_BGR2RGB))
plt.axis('on')
plt.show()
```
# output
![image](https://github.com/user-attachments/assets/2f42ce04-c2f5-4fdf-a6fc-282ae218e7d3)


