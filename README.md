# Image Transformation
Image transformation refers to the process of systematically altering or adjusting digital images to achieve specific effects or prepare the data for machine learning. Such transformations can include geometric changes such as flipping, rotating, cropping, or colour adjustments such as brightness, contrast, saturation, and hue.

These techniques have several advantages:

They enable data augmentation, making models more robust against variations in images.

They help increase visual diversity in datasets without having to capture new images.

They offer the possibility to normalise and optimise images for specific applications or training scenarios.

This project demonstrates image transformations in a simple and visually comprehensible way. Each transformation applied is displayed directly on the image, so you can immediately see which operations have been performed.

## Technologies Used:
Tool: Python

Skills: TensorFlow, NumPy, Matplotlib

## Example of an image transformation:
```
fig, axes = plt.subplots(1, 2, figsize=(12,6))

# Original
axes[0].imshow(img)
axes[0].set_title("Original")
axes[0].axis("off")

# Transformed
transformed_img, transforms = transform_image(img)
axes[1].imshow(transformed_img)
axes[1].set_title("Transformed")
axes[1].axis("off")
draw_transformations(axes[1], transforms)

plt.show()
```
Result:
<img width="867" height="499" alt="Screenshot 2025-12-03 090401" src="https://github.com/user-attachments/assets/6ffad127-f5af-457e-8f35-7bd800be4533" />

## For several examples:
```
fig, axes = plt.subplots(2, 3, figsize=(15,10))
axes = axes.flatten()
n = 6
for i in range(n):
    t_img, transforms = transform_image(img)
    axes[i].imshow(t_img)
    axes[i].set_title(f"Transformed {i+1}")
    axes[i].axis("off")
    draw_transformations(axes[i], transforms)

plt.tight_layout()
plt.show()
```
Result:
<img width="1294" height="978" alt="Screenshot 2025-12-03 091000" src="https://github.com/user-attachments/assets/3df78b81-baf8-4bc5-9608-08d6bd3be79b" />

