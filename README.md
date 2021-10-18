# Data-Augmentation
How to use Deep Learning when you have Limited Data 


Here You can add the image path that you want to Augment. 

* `img = load_img('') ` 

Add how many images you wanna to generate from your selected image, in this case it's 200

* `i += 1
   if i > 200: 
       break  # otherwise the generator would loop indefinitely`

Popular Augmentation Techniques

**Flip**
You can flip images horizontally and vertically. Some frameworks do not provide function for vertical flips. But, a vertical flip is equivalent to rotating an image by 180 degrees and then performing a horizontal flip. 

![image](https://user-images.githubusercontent.com/56305868/137679113-6bcb85d7-e761-45b6-ad7c-3caa17c07628.png)

 **Rotation**
 One key thing to note about this operation is that image dimensions may not be preserved after rotation. If your image is a square, rotating it at right angles will preserve the image size. If it’s a rectangle, rotating it by 180 degrees would preserve the size. Rotating the image by finer angles will also change the final image size.
 
 ![image](https://user-images.githubusercontent.com/56305868/137679428-8b9118a2-d88c-4082-8f1c-84201e0d1e83.png)

**Scale**
The image can be scaled outward or inward. While scaling outward, the final image size will be larger than the original image size. Most image frameworks cut out a section from the new image, with size equal to the original image.

![image](https://user-images.githubusercontent.com/56305868/137679464-1e2377ef-d607-43b3-b6a1-46014a3f9a65.png)

**Crop**
Unlike scaling, we just randomly sample a section from the original image. We then resize this section to the original image size. This method is popularly known as random cropping

![image](https://user-images.githubusercontent.com/56305868/137679572-4ac57d32-f94d-4f4c-8956-ef9f26f5c9f7.png)

**Translation**
Translation just involves moving the image along the X or Y direction (or both). This method of augmentation is very useful as most objects can be located at almost anywhere in the image. This forces your convolutional neural network to look everywhere.

![image](https://user-images.githubusercontent.com/56305868/137679710-4e364c68-92f3-4b8b-b0f3-0e2b1b955b08.png)

**Gaussian Noise**
Over-fitting usually happens when your neural network tries to learn high frequency features (patterns that occur a lot) that may not be useful. Gaussian noise, which has zero mean, essentially has data points in all frequencies, effectively distorting the high frequency features. This also means that lower frequency components (usually, your intended data) are also distorted, but your neural network can learn to look past that. Adding just the right amount of noise can enhance the learning capability.

![image](https://user-images.githubusercontent.com/56305868/137679934-024cd4c8-4b4b-4f91-a255-b4863148105b.png)




