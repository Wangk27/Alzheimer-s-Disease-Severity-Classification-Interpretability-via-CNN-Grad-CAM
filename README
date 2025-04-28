Alzheimer’s Disease Severity Classification & Interpretability via CNN + Grad-CAM

○ Goal: Develop a convolutional neural network to automatically classify T1-weighted brain MRI slices into four Alzheimer’s severity levels—Non Demented, Very Mild Dementia, Mild Dementia, and Moderate Dementia—with state-of-the-art accuracy, and generate interpretable Grad-CAM heatmaps to highlight discriminative brain regions.
○ Data: Leveraging the OASIS-1 archive, which provides 86 437 MRI slices evenly distributed across the four diagnostic categories, we split the data into 69 150 training and 17 287 validation images for model development and evaluation ​

○ Methods:

  • Model Architecture: A custom CNN built in TensorFlow/Keras featuring an input Rescaling layer, four Conv2D + BatchNorm + ReLU + MaxPool blocks, followed by a penultimate convolution for higher-resolution feature maps, and two fully connected layers with dropout before a softmax output.
  • Training Strategy: Data augmentation (random horizontal flips and small rotations), Adam optimizer (1 × 10⁻⁴), sparse categorical cross-entropy loss, and callbacks for ReduceLROnPlateau, EarlyStopping, and ModelCheckpoint ensure robust convergence and prevent overfitting ​
  • Evaluation: Monitor accuracy and loss curves during training; compute multiclass ROC curves and AUC on the validation set to assess discriminative power across all four classes.
  • Interpretability: Implement Grad-CAM by tapping into penultimate and final convolutional activations, computing class-specific gradients, and generating upsampled heatmaps masked by a brain-extraction routine. Contour-based ROI extraction then overlays green bounding boxes on regions driving each prediction.

○ Expected Outcomes: A high-accuracy classifier (> 80 % validation accuracy) coupled with transparent visual explanations, enabling both automated screening support and insight into neuroanatomical patterns associated with dementia progression.
