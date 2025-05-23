# Soft Detection Notebook

This notebook provides functionality for detecting and analyzing soft plaques in coronary images. It includes image processing techniques such as thresholding, masking, and contour detection to highlight plaque regions within medical scans.

## Features
- **Detect coronary regions** using grayscale masking techniques.
- **Detect plaque regions** by thresholding specific pixel intensity ranges.
- **Outline detected plaques** to highlight their contours.
- **Average images** for smoother outputs.
- **Threshold images** to extract relevant features.
- **Identify key pixel locations** in each row of an image.

## Dependencies
Ensure the following Python libraries are installed before running the notebook:

```bash
pip install numpy opencv-python matplotlib
```

## Usage
1. Load coronary scan images and masks.
2. Use the `detect_coronary_and_draw_mask()` function to identify normal coronary regions.
3. Apply `detect_plaques_and_draw_mask()` to highlight potential plaque areas.
4. Use `detect_out_and_draw_mask()` to outline detected plaques.
5. Visualize results using OpenCV and Matplotlib.

## Example
```python
import cv2
import numpy as np

image = cv2.imread("coronary_scan.jpg")
mask = cv2.imread("mask.jpg", cv2.IMREAD_GRAYSCALE)

highlighted_image, binary_mask = detect_plaques_and_draw_mask(image, mask)
cv2.imshow("Highlighted Plaque", highlighted_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Notes
- Ensure that images and masks have the same dimensions before processing.
- Adjust pixel intensity ranges in the detection functions to fine-tune results.

## Author
This notebook was created for research in coronary plaque detection and medical image analysis.
