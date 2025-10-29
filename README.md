# 🖼️ Real-Time Image Brightness Controller using OpenCV & Python

## 📌 Project Overview
This project demonstrates how to **dynamically control image brightness and darkness** using **OpenCV** trackbars in Python.  
It allows independent adjustment of brightness and darkness levels in real time, showcasing the fundamentals of **image processing, pixel manipulation, and GUI control** with OpenCV.

## 🚀 Features
- 🎚️ Real-time brightness & darkness control  
- 💡 Independent adjustment using trackbars  
- 🧠 Demonstrates image arithmetic operations  
- 🧩 Simple and modular Python code  
- 🖥️ Beginner-friendly OpenCV application  

## 🧰 Technologies Used
- **Python**
- **OpenCV**
- **NumPy**

## 🧑‍💻 How It Works
1. Load an image using OpenCV.  
2. Create interactive trackbars for brightness and darkness control.  
3. Update image display dynamically as trackbar values change.  
4. Press **‘Q’** or **‘q’** to exit the application.

## 🧾 Code Example
```python
import cv2
import numpy as np

# Read the image
img = cv2.imread("Nature.jpeg")
cv2.namedWindow('Brightness Control', cv2.WINDOW_FREERATIO)

def nothing(x):
    pass

# Create trackbars
cv2.createTrackbar('Brightness', 'Brightness Control', 0, 255, nothing)
cv2.createTrackbar('Darkness', 'Brightness Control', 0, 255, nothing)

br = dr = 0
cv2.imshow('Brightness Control', img)

while True:
    br2 = br
    dr2 = dr
    br = cv2.getTrackbarPos('Brightness', 'Brightness Control')
    dr = cv2.getTrackbarPos('Darkness', 'Brightness Control')

    if br != br2:
        cv2.imshow('Brightness Control', cv2.add(img, br))
    elif dr != dr2:
        cv2.imshow('Brightness Control', cv2.add(img, -dr))

    if cv2.waitKey(1) in [ord('q'), ord('Q')]:
        break

cv2.destroyAllWindows()
````
# Interface 
<img width="1920" height="1028" alt="Brightness Control Interface" src="https://github.com/user-attachments/assets/21be63a9-ada0-4eaf-8ef7-2f11cc5c6940" />


## 📂 How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/OpenCV-Image-Brightness-Controller.git
   ```
2. Navigate to the project folder:

   ```bash
   cd OpenCV-Image-Brightness-Controller
   ```
3. Install dependencies:

   ```bash
   pip install opencv-python numpy
   ```
4. Run the script:

   ```bash
   python brightness_control.py
   ```

## Demo Video:
[Video](https://youtu.be/uF-vbQYgE2c)

### 📎 Connect With Me

💼 [LinkedIn](www.linkedin.com/in/shamanthula-bhavana-7343bb331)

---

### 🏷️ Tags

#OpenCV #Python #ComputerVision #ImageProcessing #AI #MachineLearning #Coding #ProjectShowcase

```
