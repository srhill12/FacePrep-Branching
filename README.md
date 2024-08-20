

# Preparing Faces for Branching

This project involves the preparation of a dataset of face images, which are processed and augmented for subsequent training tasks. The primary goal is to preprocess the images, apply augmentations, and save the processed data for use in training machine learning models.

## Table of Contents
- [Project Overview](#project-overview)
- [Requirements](#requirements)
- [Installation](#installation)
- [Dataset Preparation](#dataset-preparation)
  - [1. Preprocessing](#1-preprocessing)
  - [2. Data Augmentation](#2-data-augmentation)
  - [3. Saving the Processed Data](#3-saving-the-processed-data)
- [Running the Notebook](#running-the-notebook)
- [Results](#results)
- [License](#license)

## Project Overview

This project focuses on preparing a dataset of face images for branching tasks. The notebook `preparing_faces_for_branching.ipynb` contains steps to preprocess the dataset, apply various augmentations to increase the diversity of the data, and save the resulting processed images for later use.

## Requirements

The project requires the following Python libraries:

- `numpy`
- `pandas`
- `matplotlib`
- `PIL` (Python Imaging Library)
- `cv2` (OpenCV)
- `albumentations`
- `os` (standard Python library for file handling)

You can install these libraries using pip:

```bash
pip install numpy pandas matplotlib pillow opencv-python-headless albumentations
```

## Installation

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/srhill12/prep-faces.git
   cd prep-faces
   ```

2. **Set Up the Environment:**

   Create a virtual environment and activate it:

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. **Install Dependencies:**

   Install the required Python libraries:

   ```bash
   pip install -r requirements.txt
   ```

## Dataset Preparation

The preparation of the dataset involves several steps, including preprocessing, augmentation, and saving the processed images. Below is a breakdown of each step:

### 1. Preprocessing

The preprocessing step involves resizing, normalizing, and cleaning the images to ensure they are in a consistent format suitable for training models. 

- **Resizing:** All images are resized to a standard size (e.g., 128x128 pixels) to maintain uniformity across the dataset.
- **Normalization:** The pixel values of the images are normalized to a range of [0, 1].
- **Cleaning:** Images with anomalies or artifacts are identified and removed to ensure the quality of the dataset.

### 2. Data Augmentation

To increase the diversity and robustness of the dataset, various augmentation techniques are applied:

- **Random Rotation:** Images are rotated randomly within a specified range.
- **Horizontal Flipping:** Images are flipped horizontally to introduce mirror images.
- **Zooming:** Random zoom operations are applied to introduce variations in scale.
- **Brightness/Contrast Adjustments:** The brightness and contrast of the images are randomly adjusted to simulate different lighting conditions.
- **Blurring:** Gaussian blur is applied to simulate out-of-focus images.

These augmentations are implemented using the `albumentations` library, which provides a wide range of image transformation techniques.

### 3. Saving the Processed Data

After preprocessing and augmentation, the processed images are saved in a designated directory for later use. The images are stored in subdirectories based on their augmentation type to allow easy retrieval during model training.

- **Saving Format:** The images are saved in `.jpg` format with filenames indicating the type of augmentation applied.
- **Directory Structure:** A structured directory format is used to organize the images, making it easy to manage and retrieve specific datasets.

## Running the Notebook

To run the notebook and execute the preprocessing and augmentation steps:

1. **Open the Jupyter Notebook:**

   ```bash
   jupyter notebook preparing_faces_for_branching.ipynb
   ```

2. **Execute Cells:**

   Follow the instructions within the notebook, executing the cells in order. This will preprocess the dataset, apply augmentations, and save the processed images.

## Results

The processed images are saved in the specified output directory, with each type of augmentation stored in its corresponding subdirectory. The resulting dataset is well-prepared for training machine learning models, with increased diversity and robustness due to the applied augmentations.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

This README should cover the main aspects of the project. If there are any additional details or specific instructions you'd like to include, feel free to modify it accordingly!
