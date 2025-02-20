**Skin Cancer Classification Using CNN**

Overview
This project implements a Convolutional Neural Network (CNN) to classify images of skin lesions into seven different categories of skin cancer. The dataset used is the HAM10000 dataset, which contains labeled dermatoscopic images.

Dataset

The dataset includes images of skin lesions categorized into the following seven classes:

- Melanocytic nevi (nv)
- Melanoma (mel)
- Benign keratosis-like lesions (bkl)
- Basal cell carcinoma (bcc)
- Actinic keratoses (akiec)
- Vascular lesions (vas)
- Dermatofibroma (df)

The metadata for these images is provided in HAM10000_metadata.csv.

Project Structure

HAM10000_metadata.csv: Metadata containing lesion types, patient details, and image IDs.

data/HAM10000/: Directory containing all skin lesion images.

skin_cancer_classification.py: The main script that processes data, trains the CNN model, and evaluates its performance.

Steps in the Pipeline

1. Data Preprocessing

Load metadata (HAM10000_metadata.csv).

Encode lesion types into numerical labels.

Visualize class distribution, patient demographics, and lesion localization.

Balance the dataset by resampling to ensure equal representation of each class.

Map image IDs to their file paths and resize images to 32x32 pixels.

2. Train-Test Split

Split the dataset into training (75%) and testing (25%) sets.

Normalize pixel values to the range [0,1].

Convert labels to categorical format for multi-class classification.

3. CNN Model Architecture

Three convolutional layers (256, 128, 64 filters) with ReLU activation.

Max pooling and dropout layers for feature extraction and regularization.

Fully connected layers and softmax activation for multi-class classification.

4. Training

Compile the model using Adam optimizer and categorical cross-entropy loss.

Train the model for 50 epochs with a batch size of 16.

Monitor training and validation accuracy/loss.

5. Model Evaluation

Compute accuracy on the test set.

Plot training/validation accuracy and loss over epochs.

Generate a confusion matrix to analyze classification performance.

Plot fraction of incorrect classifications per class.

Running the Project

To execute the project, run the following command:

python skin_cancer_classification.py

Results and Insights

The trained CNN model achieves a test accuracy of approximately X% (varies based on training).

The model performs well on some classes but may misclassify similar-looking lesions.

Data augmentation and transfer learning (e.g., using MobileNet or VGG16) could further improve performance.

Acknowledgment

The HAM10000 dataset is provided by Tschandl et al. and is widely used for research in dermatological image classification.

