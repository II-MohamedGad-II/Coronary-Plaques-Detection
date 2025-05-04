# Coronary Plaque Segmentation Notebook

This notebook provides functionality for segmenting coronary plaques in medical images. It leverages deep learning models and image processing techniques to classify and segment different plaque types.

## Features
- **Load and preprocess medical images** from multiple categories (calcified, normal, mixed, soft).
- **Train a UNET model** using TensorFlow and Keras for coronary segmentation.
- **Apply early stopping** to optimize model performance.
- **Visualize segmentation results** using Matplotlib.

## Dependencies
Ensure the following Python libraries are installed before running the notebook:

```bash
pip install tensorflow numpy opencv-python matplotlib scikit-learn glob2
```

## Usage
1. **Prepare Dataset**: Place images into appropriate folders (`calcified`, `normal`, `mixed`, `soft`).
2. **Load Images**: The script automatically loads images using `glob`.
3. **Train the Model**: Run the training cells to segment plaques.
4. **Evaluate & Visualize**: Use Matplotlib to analyze segmentation results.

## Example
```python
import cv2
import numpy as np

image = cv2.imread("sample_image.jpg")
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Process the image with a segmentation model
segmented_output = model.predict(np.expand_dims(gray_image, axis=0))

plt.imshow(segmented_output[0], cmap="gray")
plt.show()
```

## Notes
- Adjust dataset paths as needed before training.
- Experiment with hyperparameters to improve segmentation accuracy.
- Ensure GPU acceleration is enabled for faster training (if available).

## Author
This notebook was created for research in coronary plaque segmentation using deep learning.
