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

## Task 2: CIFAR-10 Image Pair Reconstruction from Averages Using Parallel Autoencoders
### Description
This task involves the unique challenge of reconstructing two distinct images from their average. A parallel autoencoder architecture was implemented to independently train for each output image. The model was trained using the CIFAR-10 dataset, where 2000 images were selected for training and 800 for testing, creating 1000 and 400 pairs respectively. The input to the model was the average of these image pairs. The model's performance was evaluated using the Structural Similarity Index (SSIM) as the loss function over 40 epochs.

### Dataset Preparation
- **Dataset**: CIFAR-10.
- **Training Images**: 2000 images from the training set to create 1000 pairs.
- **Testing Images**: 800 images from the test set to create 400 pairs.
- **Input Generation**: Averaging each pair of images to serve as the model input.

### Model Architecture
- **Encoder**: Consists of convolutional layers with 'relu' activation, followed by max-pooling.
- **Decoder**: Includes convolutional layers with 'relu' activation, followed by upsampling, and a final 'sigmoid' activation layer for output.

### Compilation and Training
- **Optimizers**: Two Adam optimizers for the parallel autoencoder.
- **Loss Function**: Structural Similarity Index (SSIM) for loss calculation.
- **Epochs**: 40.

### Performance Evaluation
- **Loss Metrics**: SSIM-based loss for both training and validation sets.
- **Visualization**: Loss curves plotted for both outputs and visual comparison of input averages, target, and predicted images.
    ![image](https://github.com/AliAmini93/Image-Reconstruction-AE/assets/96921261/0eac5577-45b1-4faa-ad15-97a2cd44b486)
### Additional Notes
- The model demonstrates the ability to independently reconstruct two images from their average, showcasing the effectiveness of parallel autoencoders in dual image reconstruction tasks.
  ![image](https://github.com/AliAmini93/Image-Reconstruction-AE/assets/96921261/6be72d23-6822-4b9d-993d-cbc8752fafb6)
  ![image](https://github.com/AliAmini93/Image-Reconstruction-AE/assets/96921261/db5d8ac0-1a88-4bf9-8c2c-b8a086a7653c)
  ![image](https://github.com/AliAmini93/Image-Reconstruction-AE/assets/96921261/a0da88ea-fedc-4099-a5f3-bcf03878b4f8)
  ![image](https://github.com/AliAmini93/Image-Reconstruction-AE/assets/96921261/baea9b47-2cfd-4b6c-b4bb-7ee4feec99e1)
  ![Uploading image.png…]()
  






