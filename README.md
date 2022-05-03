# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the necessary modules


### Step2
For performing smoothing operation on a image.

Average filter:
```python

avg_kernel=np.ones((13,13),np.float32)/169
average_filter_image=cv2.filter2D(image,-1,avg_kernel)
```
Weighted average filter :
```python
wt_avg_kernel=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
wt_average_filter_image=cv2.filter2D(image,-1,wt_avg_kernel)
```
Gaussian Blur:
```python
gaussian_blur=cv2.GaussianBlur(image,(31,31),0,0)
```
Median filter:
```python
median_blur=cv2.medianBlur(image,11)
```


### Step3
For performing sharpening on a image.

Laplacian Kernel:
```python
lap_kernel=np.array([[-1,-1,-1],[-1,8,-1],[-1,-1,-1]])
lap_image=cv2.filter2D(image,-1,lap_kernel)
```
Laplacian Operator:
```python
Lap_sharp=cv2.Laplacian(image,cv2.CV_64F)
```




### Step4
Display all the images with their respective filters.



## Program:
### Developed By   : BALAJI N
### Register Number: 212220230006


### 1. Smoothing Filters

i) Using Averaging Filter
```Python
avg_kernel=np.ones((13,13),np.float32)/169
average_filter_image=cv2.filter2D(image,-1,avg_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Average Filter image')
plt.imshow(average_filter_image)
plt.show()







```
ii) Using Weighted Averaging Filter
```Python
weight_average_kernel=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weight_average_filter_image=cv2.filter2D(image,-1,weight_average_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image[30:200,50:200])
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Weighted average Filter image')
plt.imshow(weight_average_filter_image[30:200,50:200])
plt.show()









```
iii) Using Gaussian Filter
```Python

gaussian_blur=cv2.GaussianBlur(image,(31,31),0,0)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Gaussian Filter image')
plt.imshow(gaussian_blur)
plt.show()








```

iv) Using Median Filter
```Python
median_blur=cv2.medianBlur(image,11)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Median Filter image')
plt.imshow(median_blur)
plt.show()







```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
laplacian_kernel=np.array([[-1,-1,-1],[-1,8,-1],[-1,-1,-1]])
laplacian_image=cv2.filter2D(image,-1,laplacian_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Laplacian Kernel Filter image')
plt.imshow(laplacian_image)
plt.show()





```
ii) Using Laplacian Operator
```Python
Laplacian_sharp=cv2.Laplacian(image,cv2.CV_64F)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Laplacian Operator Filter image')
plt.imshow(Laplacian_sharp)
plt.show()














```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
![Screenshot (123)](https://user-images.githubusercontent.com/75234946/166441265-3975e4f3-3e88-4fb0-b646-84ce14e24a41.png)


ii) Using Weighted Averaging Filter
![Screenshot (125)](https://user-images.githubusercontent.com/75234946/166441409-20df41e8-1d9a-47d4-b2b4-0076b490aa3b.png)


iii) Using Weighted Averaging Filter
![Screenshot (127)](https://user-images.githubusercontent.com/75234946/166441527-e779f65f-7fc3-46d5-a4ad-72bc119fb3a8.png)


iv) Using Median Filter
![image](https://user-images.githubusercontent.com/75234946/166441626-e3c6c766-876b-41be-a107-cc9ed78aef2f.png)


### 2. Sharpening Filters



i) Using Laplacian Kernal
![image](https://user-images.githubusercontent.com/75234946/166441817-f942e1fd-b0a5-4bab-9e38-5c73692d760f.png)


ii) Using Laplacian Operator
![image](https://user-images.githubusercontent.com/75234946/166441917-56f3e4b3-a09c-409e-b872-600f5e3535e5.png)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
