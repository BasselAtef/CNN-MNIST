# DecodeLabs-Project4-CNN-MNIST

# Fashion-MNIST Classification using CNN (Keras)

This repository contains a complete Jupyter Notebook that builds, trains, and evaluates a Convolutional Neural Network (CNN) to classify clothing items from the Fashion-MNIST dataset using Keras/TensorFlow. It also includes a pipeline for running inference on custom local images.

## 🚀 Features
* **Dataset:** Uses Fashion-MNIST (60,000 training images, 10,000 test images).
* **Architecture:** Sequential CNN with two `Conv2D` layers, `MaxPooling2D`, and `Dense` layers.
* **Optimization:** Trained using the Adam optimizer with `categorical_crossentropy` loss.
* **Inference:** Includes a ready-to-use prediction script to test custom external images on the trained model.

## 📂 Project Structure
* `CNN_MNIST_FASHION.ipynb` - The main Jupyter Notebook containing model training and inference.
* `mnist_cnn_model.keras` - The trained model saved in the native Keras format.

## 📊 Model Performance
After training for 12 epochs, the model achieves:
* **Training Accuracy:** ~99.2%
* **Test Accuracy:** ~92.1%
* **Test Loss:** 0.4697

## 🛠️ Requirements & Installation

You can run this project on colab.research.google.com, preferably with the T4 GPU setting on for training the model.
To run this project locally, ensure you have Python 3.x installed along with the required dependencies:

```bash
pip install tensorflow numpy pillow jupyter
```

## 💻 How to Use

### 1. Train the Model

Open the notebook in Jupyter or Google Colab and execute the cells sequentially to load the dataset, preprocess the data, and train the CNN.

### 2. Predict Custom Images

To classify your own clothing images, use the prediction block at the bottom of the notebook:

1. Place a grayscale image (ideally a 28x28 pixel image with a dark background and white foreground, similar to Fashion-MNIST format) in your directory.
2. Update the filename path in the notebook:
```python
img = load_img('your_custom_image.png', color_mode='grayscale', target_size=(28, 28))

```


3. Run the prediction cell to output the class label (e.g., *Pullover*, *T-shirt/Top*, *Sneaker*).

## 🏷️ Supported Classes

The model classifies images into one of the following 10 categories:
`T-shirt/Top`, `Trousers`, `Pullover`, `Dress`, `Coat`, `Sandal`, `Shirt`, `Sneaker`, `Bag`, `Ankleboot`.

## NOTE: I have added 3 sample grayscale images to test the project if it's functioning as intended.
```

```
