# Coronary Plaque Detection Project

This project focuses on detecting coronary plaques in medical images. The workflow involves preprocessing images, analyzing pixel data, and developing detection algorithms for both soft and calcified plaques.

## Project Workflow

### 1. Coronary Segmentation
The first step involves segmenting the coronary arteries from primary medical images. This reduces noise and allows the algorithm to focus solely on the coronary regions, improving accuracy.

### 2. Image Data Extraction
After extracting and cutting the coronary images, a data file is generated containing key pixel information, including:
- Number of pixels within different intensity ranges (e.g., 100–130, 130–170, 170–200, etc.).
- Sum of pixel values exceeding specific thresholds (e.g., >200, >150, etc.).

This data is crucial for understanding the distribution of pixel intensities and identifying patterns related to plaques.

### 3. Data Analysis
To develop an effective detection algorithm, exploratory data analysis (EDA) is performed to gain insights into plaque characteristics. This phase helps:
- Identify intensity thresholds that distinguish healthy and plaque-affected regions.
- Establish relationships between pixel distributions and plaque types.
- Optimize the segmentation and detection process.

### 4. Plaque Detection Algorithm
Based on the analysis, detection algorithms are built for:
- **Soft Plaques**: These require specific intensity thresholds and texture analysis.
- **Calcified Plaques**: Characterized by high-intensity values, making them distinguishable through thresholding and contour detection techniques.

The developed models are capable of segmenting, analyzing, and detecting coronary plaques with improved accuracy.

## Dependencies
Ensure the following Python libraries are installed before running the scripts:

```bash
pip install numpy opencv-python matplotlib pandas tensorflow scikit-learn glob2
```

## Usage
1. **Segment Coronary Arteries** using the segmentation algorithm.
2. **Extract Image Statistics** and generate the data file.
3. **Perform Data Analysis** to refine detection thresholds.
4. **Run Plaque Detection Algorithms** for both soft and calcified plaques.

## Notes
- Image quality and preprocessing significantly impact detection accuracy.
- Threshold values may need adjustment based on dataset characteristics.
- GPU acceleration is recommended for faster processing.

## Author
This project was developed for research in coronary plaque detection and medical image analysis.
