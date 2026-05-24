# Image-Handling-and-Pixel-Transformations-Using-OpenCV 

## AIM:
Write a Python program using OpenCV that performs the following tasks:

1) Read and Display an Image.  
2) Adjust the brightness of an image.  
3) Modify the image contrast.  
4) Generate a third image using bitwise operations.

## Software Required:
- Anaconda - Python 3.7
- Jupyter Notebook (for interactive development and execution)

## Algorithm:
### Step 1:
Load an image from your local directory and display it.

### Step 2:
o Draw a line from the top-left to the bottom-right of the image.
o Draw a circle at the center of the image. 
o Draw a rectangle around a specific region of interest in the image. 
o Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step 3:
o Convert the image from RGB to HSV and display it.
o Convert the image from RGB to GRAY and display it. 
o Convert the image from RGB to YCrCb and display it.  
o Convert the HSV image back to RGB and display it.

### Step 4:
o Access and print the value of the pixel at coordinates (100, 100). 
o Modify the color of the pixel at (200, 200) to white.

### Step 5:
o Resize the original image to half its size and display it.

### Step6:
o Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.

### Step7:
o Flip the original image horizontally and display it. 
o Flip the original image vertically and display it.

### Step8:
o Save the final modified image to your local directory.

## Program Developed By:
- **Name:** NANDIKA S 
- **Register Number:** 212224230175

## Ex. No. 01

### Import neccessary libraries
        import cv2
        import matplotlib.pyplot as plt
### Read the image using OpenCV
    img = cv2.imread('Qno. 1.jpg', cv2.IMREAD_COLOR)
### Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
    img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
### Display the image using Matplotlib
    plt.imshow(img_rgb, cmap='viridis')  # You can change 'viridis' to another cmap or use None for RGB images
    plt.title("Original Image")
    plt.axis('off')  # Removes axis ticks and labels
    plt.show()
### Load the image
    image = cv2.imread('Qno. 1.jpg') 
### Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
    img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
    img_rgb.shape
### Draw a line from top-left to bottom-right
    line_img = cv2.line(img_rgb, (0, 0), (768, 600), (255, 0, 0), 2) # cv2.line(image, start_point, end_point, color, thickness)
    plt.imshow(line_img, cmap='viridis')  
    plt.title("Image with Line")
    plt.axis('off')  
    plt.show()
### Load the image
    image = cv2.imread('Qno. 1.jpg') 
### Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
    img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
    img_rgb.shape
    circle_img = cv2.circle(img_rgb,(400,300),150,(255,0,0),10) # cv2.circle(image, center, radius, color, thickness)
    plt.imshow(circle_img, cmap='viridis')  
    plt.title("Image with Circle")
    plt.axis('off')  
    plt.show()
### Load the image
    image = cv2.imread('Qno. 1.jpg') 
### Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
    img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
    img.shape
### Draw a rectangle around the Whole image
    rectangle_img = cv2.rectangle(img_rgb, (0, 0), (768, 600), (0, 0, 255), 10)  # cv2.rectangle(image, start_point, end_point, color, thickness)
    plt.imshow(rectangle_img, cmap='viridis')  
    plt.title("Image with Rectangle")
    plt.axis('off')  
    plt.show()
### Load the image
    image = cv2.imread('Qno. 1.jpg') 
### Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
    img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
### Add text to the image
    text_img = cv2.putText(img_rgb, "OpenCV Drawing", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10)  ## cv2.putText(image, text, position, font, font_scale, color, thickness)
    plt.imshow(text_img, cmap='viridis')  
    plt.title("Image with Text")
    plt.axis('off')  
    plt.show()
### Load the image
    image = cv2.imread('Qno. 1.jpg') 
    image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
### Original RGB Image
        plt.imshow(image_rgb)
        plt.title("Original RGB Image")
        plt.axis("off")
### Convert RGB to HSV
        image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)
### HSV Image
    plt.imshow(image_hsv)
    plt.title("HSV Image")
    plt.axis("off")
### Convert RGB to GRAY
    image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)
### Grayscale Image
    plt.imshow(image_gray, cmap='gray')
    plt.title("Grayscale Image")
    plt.axis("off")
### Convert RGB to YCrCb
    image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)
### YCrCb Image
    plt.imshow(image_ycrcb)
    plt.title("YCrCb Image")
    plt.axis("off")
### Convert HSV back to RGB
    image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
    plt.imshow(image_hsv_to_rgb)
    plt.title("HSV to RGB Image")
    plt.axis("off")
### Modify a block of pixels (300x300) to white, starting from (200, 200)
    image[200:500, 200:500] = [255, 255, 255]  # Rows: 200-499, Columns: 200-499
### Display the modified image
    plt.imshow(image_rgb)
    plt.title("Image with 300x300 White Block")
    plt.axis("off")
    plt.show()
### Load the image
    image = cv2.imread('Qno. 1.jpg') 
    image.shape
### Resize the image to half its size
    resized_image = cv2.resize(image, (768 // 2, 600 // 2))  # (new_width, new_height)
### Convert BGR to RGB for displaying with Matplotlib
    resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)
    resized_image_rgb.shape
### Display the resized image
    plt.imshow(resized_image_rgb)
    plt.title("Resized Image (Half Size)")
    plt.axis("off")
    plt.show()
### Load the image
    image = cv2.imread('Qno. 1.jpg') 
    image.shape
### Crop a 300x300 region starting from (50, 50)
    roi = image[50:350, 50:350]  # Rows: 50-349, Columns: 50-349
### Convert BGR to RGB for displaying with Matplotlib
    roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)
### Display the cropped region (ROI)
    plt.imshow(roi_rgb)
    plt.title("Cropped Region of Interest (ROI)")
    plt.axis("off")
    plt.show()
### Load the image
    image = cv2.imread('Qno. 1.jpg') 
### Flip the image horizontally (left-right)
    flipped_horizontally = cv2.flip(image, 1)
### Convert BGR to RGB for displaying with Matplotlib
    flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)
### Horizontal flip
    plt.imshow(flipped_horizontally_rgb)
    plt.title("Flipped Horizontally")
    plt.axis("off")
### Flip the image vertically (up-down)
    flipped_vertically = cv2.flip(image, 0)
### Convert BGR to RGB for displaying with Matplotlib
    flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)
### Vertical flip
    plt.imshow(flipped_vertically_rgb)
    plt.title("Flipped Vertically")
    plt.axis("off")


## Output:
1. ORIGINAL IMAGE
   <Figure size 640x480 with 1 Axes><img width="493" height="409" alt="image" src="https://github.com/user-attachments/assets/944b272d-c49c-4888-8808-84ed82b43a2e" />

2. IMAGE WITH LINE
   <img width="632" height="493" alt="image" src="https://github.com/user-attachments/assets/5ff6b8d1-09be-42f0-adb7-772af9137f9c" />

3. IMAGE WITH CIRCLE
<img width="634" height="494" alt="image" src="https://github.com/user-attachments/assets/12599706-6501-4e41-aaef-1551ac2e8f52" />

4, IMAGE WITH RECTANGLE 
<img width="634" height="493" alt="image" src="https://github.com/user-attachments/assets/92bd86ff-9a3c-4516-b8d4-04a739334f83" />

5. IMAGE WITH TEXT
<img width="632" height="497" alt="image" src="https://github.com/user-attachments/assets/a1d9feac-893c-4bd3-967a-08986880f3c7" />

6. ORIGINAL RGB IMAGE
<img width="634" height="497" alt="image" src="https://github.com/user-attachments/assets/45ee6209-642b-46e6-8e2c-fa12a7be6eea" />

7. HSV IMAGE
<img width="631" height="489" alt="image" src="https://github.com/user-attachments/assets/176a1ec1-2279-423d-b10a-3bef5afb4cbf" />

8.GRAYSCALE IMAGE
<img width="634" height="494" alt="image" src="https://github.com/user-attachments/assets/4def687a-5329-4f44-be84-4b60a9b12afb" />

9. YCRCB IMAGE
<img width="636" height="490" alt="image" src="https://github.com/user-attachments/assets/4b6d4de6-6fa5-45f9-a162-e126a8cba078" />

10. HSV TO RGB IMAGE
<img width="632" height="491" alt="image" src="https://github.com/user-attachments/assets/f074f745-e4cc-46c4-a2ef-78f6e2965ec3" />

11. IMAGE WITH 300X300 WHITE BLOCK
<img width="634" height="497" alt="image" src="https://github.com/user-attachments/assets/3bd8be6f-2777-45b0-a666-5c2fddfb611f" />

12. RESIZED IMAGE (HALF SIZE)
<img width="634" height="496" alt="image" src="https://github.com/user-attachments/assets/74e7f23d-a3b5-45cc-9cd5-ff2b809abe74" />

13. CROPPED REGION OF INTEREST (ROI)
<img width="493" height="493" alt="image" src="https://github.com/user-attachments/assets/8e0158e5-243a-40b6-9639-5c5053c568ae" />

14. FLIPPED HORIZONTALLY
<img width="630" height="493" alt="image" src="https://github.com/user-attachments/assets/7f3d2a83-a503-4789-94f6-39f414e35a27" />

15. FLIPPED VERTICALLY
<img width="629" height="488" alt="image" src="https://github.com/user-attachments/assets/3661e6af-e140-426e-a863-22070ab520a2" />

## Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.

