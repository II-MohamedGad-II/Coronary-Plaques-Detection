# Calcified Plaque Detection Notebook

This notebook provides functionality for detecting calcified plaques in coronary images. It includes image processing techniques to identify and analyze calcified regions in medical scans.

## Features
- **Load and preprocess medical images** from a dataset of calcified plaque scans.
- **Apply OpenCV-based image processing** for analysis.
- **Perform segmentation and detection** of calcified plaques.

## Dependencies
Ensure the following Python libraries are installed before running the notebook:

```bash
pip install numpy opencv-python matplotlib pandas glob2
```

## Usage
1. **Prepare Dataset**: Place calcified plaque images into a folder.
2. **Load Images**: The script automatically loads images using `glob`.
3. **Process Images**: Use OpenCV to analyze plaque regions.
4. **Visualize Results**: Use Matplotlib to display detection outputs.

## Example
```python
import cv2
import numpy as np

image = cv2.imread("calcified_sample.jpg", cv2.IMREAD_GRAYSCALE)
blurred = cv2.GaussianBlur(image, (5, 5), 0)
edges = cv2.Canny(blurred, 50, 150)

plt.imshow(edges, cmap="gray")
plt.show()
```

## Notes
- Adjust preprocessing parameters to refine detection accuracy.
- Ensure images are in the correct format before loading.
- Modify detection thresholds based on image contrast levels.

## Author
This notebook was created for research in calcified plaque detection using image processing techniques.
