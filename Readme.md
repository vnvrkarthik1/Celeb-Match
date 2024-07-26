
```markdown
# celebMatch Project

Welcome to the `celebMatch` project! This project is designed to compare and find matching faces between a sample image and a set of images using the DeepFace library. It includes functionalities to find the closest match among known faces for a given image.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Functions](#functions)
- [Requirements](#requirements)
- [License](#license)

## Installation

To use this project, you need to install the required Python packages. You can do this using `pip`. 

```bash
pip install deepface
pip install tqdm
```

## Usage

This project includes two main functionalities:
1. **Comparing a Sample Image with Images in a Folder**
2. **Finding the Best Match for an Unknown Face Among Known Faces**

### Comparing a Sample Image

1. **Set Up Paths**

   Modify the `sample_image_path` and `images_folder_path` variables to point to your sample image and the folder containing images to compare against.

2. **Run the Comparison**

   Run the script to compare the sample image with all images in the specified folder. It will output the image with the smallest distance and display both the sample image and the closest match.

### Finding the Best Match

1. **Set Up Known Faces Directory**

   Modify the `known_faces_dir` variable to point to the directory containing images of known faces.

2. **Set Up the Unknown Image**

   Modify the `unknown_image_path` variable to point to the image you want to find a match for.

3. **Run the Matching**

   Execute the script to find the best match for the unknown image among the known faces. It will print out the name of the closest match and the distance.

## Functions

### `compare_images(sample_image_path, images_folder_path)`

Compares a sample image with all images in the specified folder using the DeepFace library. Displays the most similar image and the comparison results.

**Parameters:**
- `sample_image_path` (str): Path to the sample image.
- `images_folder_path` (str): Path to the folder containing images for comparison.

### `find_best_match(known_faces, unknown_face_path, model_name='VGG-Face', distance_metric='cosine')`

Finds the best match for an unknown face among the known faces.

**Parameters:**
- `known_faces` (dict): Dictionary where keys are celebrity names and values are paths to their images.
- `unknown_face_path` (str): Path to the unknown face image.
- `model_name` (str): The model to use for comparison, default is `'VGG-Face'`.
- `distance_metric` (str): Metric for distance measurement, default is `'cosine'`.

**Returns:**
- `best_match` (str): Name of the best matching celebrity.
- `min_distance` (float): Distance between the unknown face and the best match.

## Requirements

- Python 3.x
- `deepface` library
- `tqdm` library

Make sure all dependencies are installed before running the scripts.

Happy face matching!
