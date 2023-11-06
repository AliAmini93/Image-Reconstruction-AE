# Image Reconstruction Using AutoEncoders(AEs)
## Task 1: Autoencoder for TinyImageNet Dataset
### Description
A four-layer autoencoder was developed for the TinyImageNet dataset to process 600x600 color images. This Jupyter Notebook (Task_1.ipynb) underwent preprocessing, including class selection, resizing, and normalization. The model was trained for 10 epochs with the Adam optimizer, using mean squared error for loss evaluation. The model's effectiveness was validated by the loss metrics and visual comparison of original and reconstructed test images, demonstrating its capability in image reconstruction and feature extraction.
### Dataset Preparation

#### Selection of Classes
- **Dataset**: TinyImageNet, containing natural color images.
- **Classes Selected**: A subset of classes with 500 training and 50 validation samples each.
- **Specific Classes**: 'mashed potato', 'bell pepper', 'alp', 'sewing machine', 'lemon', 'banana', 'umbrella', 'volleyball', 'torch', 'mushroom'.
- **Allocation**: 400 samples for training (40 from each class) and 100 samples for testing (10 from each class).

#### Data Preprocessing
- **Approach**: Generator-based for efficient memory usage.
- **Image Resizing**: Adjusted to 600x600 pixels for the autoencoder.
- **Normalization**: Pixel values scaled to the [0, 1] range.

### Model Architecture

#### Encoder
- **Layers**: Four convolutional layers with 'relu' activation.
- **Filters**: Sizes increase from 32, 64, 128, to 256.
- **Pooling**: Max-pooling layers follow each convolutional layer.

#### Decoder
- **Design**: Mirrors the encoder with convolutional and upsampling layers.
- **Activation**: 'sigmoid' function in the final layer for image reconstruction.

### Compilation and Training
- **Optimizer**: Adam.
- **Loss Function**: Mean squared error.
- **Epochs**: 10.
- **Batch Size**: 32.
- **Validation**: Used to monitor performance during training.

### Performance Evaluation
- **Loss Visualization**: Plots of training and validation loss.
    ![image](https://github.com/AliAmini93/Image-Reconstruction-AE/assets/96921261/8e748cae-cc9c-4bfa-a9eb-df369d8f13b0)

- **Reconstruction Quality**: Visual comparison of original vs. reconstructed images from the test set.
   ![image](https://github.com/AliAmini93/Image-Reconstruction-AE/assets/96921261/4959095f-1066-4b20-8465-7cc3b1e23cb0)
