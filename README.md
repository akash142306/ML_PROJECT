# ML_PROJECT
 Image Caption Generator Project: Create an innovative Image Caption Generator using machine learning. This project employs advanced neural network architectures to analyze images and generate descriptive captions automatically. Enhancing accessibility and understanding, the model undergoes rigorous training and evaluation to ensure relevant output


# Image Caption Generator

This project aims to create an image caption generator using deep learning techniques. The model is based on a combination of Convolutional Neural Network (CNN) and Long Short-Term Memory (LSTM) networks.

## Requirements
- Python (>=3.6)
- TensorFlow (>=2.0)
- Keras
- Numpy
- PIL
- Matplotlib
- tqdm

## Setup

### Install Dependencies

```bash
pip install tensorflow keras numpy Pillow matplotlib tqdm
```

### Dataset

1. Download the [Flickr8k dataset](https://forms.illinois.edu/sec/1713398).
2. Extract the dataset and organize it with images in one folder (`Flicker8k_Dataset`) and text data in another (`txt`).
3. Ensure that the text data contains a file named `Flickr8k.token.txt` with image captions.

### Pre-trained Model

Download the pre-trained Xception model from Keras:

```python
from keras.applications.xception import Xception
model = Xception(weights='imagenet')
model.save('xception_model.h5')
```

### Data Cleaning and Pre-processing

1. Run the provided data cleaning script to clean and preprocess the text data:

```bash
python data_cleaning.py
```

2. Save the descriptions in a single file:

```bash
python data_cleaning.py
```

### Extract Image Features

1. Extract features from images using the pre-trained Xception model:

```bash
python extract_features.py
```

2. Save the features in a pickle file (`features.p`):

```bash
python extract_features.py
```

### Training the Model

1. Run the training script to train the image caption generator model:

```bash
python train_model.py
```

2. The model will be saved in the `models` directory.

## Testing the Model

1. Provide a sample image path for testing:

```bash
python test_model.py --image <path_to_sample_image>
```

2. The model will generate and display a caption for the provided image.

## Contributors

- Akash Chandrashekharan
- Islauddin 
- Savan Sutariya
- Tejal Mate
- Utkarsha Kale
- Agastya Bhardwaj
- Rushikesh Bhise
- Devendra Pardhi

## Acknowledgments

https://www.analyticsvidhya.com

Feel free to customize this README file based on your specific project details, contributors, and acknowledgments.
