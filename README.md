# Image Reconstruction Using AutoEncoders(AEs)
# Task 1: Autoencoder for TinyImageNet Dataset

## Dataset Preparation

### Selection of Classes
- **Dataset**: TinyImageNet, containing natural color images.
- **Classes Selected**: A subset of classes with 500 training and 50 validation samples each.
- **Specific Classes**: 'mashed potato', 'bell pepper', 'alp', 'sewing machine', 'lemon', 'banana', 'umbrella', 'volleyball', 'torch', 'mushroom'.
- **Allocation**: 400 samples for training (40 from each class) and 100 samples for testing (10 from each class).

### Data Preprocessing
- **Approach**: Generator-based for efficient memory usage.
- **Image Resizing**: Adjusted to 600x600 pixels for the autoencoder.
- **Normalization**: Pixel values scaled to the [0, 1] range.

## Model Architecture

### Encoder
- **Layers**: Four convolutional layers with 'relu' activation.
- **Filters**: Sizes increase from 32, 64, 128, to 256.
- **Pooling**: Max-pooling layers follow each convolutional layer.

### Decoder
- **Design**: Mirrors the encoder with convolutional and upsampling layers.
- **Activation**: 'sigmoid' function in the final layer for image reconstruction.

## Compilation and Training
- **Optimizer**: Adam.
- **Loss Function**: Mean squared error.
- **Epochs**: 10.
- **Batch Size**: 32.
- **Validation**: Used to monitor performance during training.

## Performance Evaluation
- **Loss Visualization**: Plots of training and validation loss.
- **Reconstruction Quality**: Visual comparison of original vs. reconstructed images from the test set.

## Additional Notes
- **Documentation**: Comments within the notebook explain each step and function.
- **Performance Metrics**: Quantitative loss during training and qualitative image reconstruction assessment.
