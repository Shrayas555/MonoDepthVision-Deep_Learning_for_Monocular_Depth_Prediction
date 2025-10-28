# MonoDepthNet — Monocular Depth Estimation with UNet

MonoDepthNet is a deep learning project for monocular depth estimation, where the goal is to predict pixel-wise depth maps from single RGB images.  
This model uses a UNet-based convolutional architecture with skip connections to learn dense depth representations efficiently.

The project is implemented in PyTorch and trained on the NYU Depth V2 dataset.  
It leverages a scale-invariant loss function and AdamW optimizer to achieve high accuracy and stable convergence.

### Key Features
- UNet-based encoder–decoder network for depth prediction  
- Scale-invariant loss for robust geometric consistency  
- AdamW optimization with adaptive learning rate scheduling  
- Early stopping and checkpoint saving for efficient training  
- Visualization of RGB, ground truth, and predicted depth maps  

### Results
The model achieved strong convergence with low training and validation losses, demonstrating effective generalization across unseen indoor scenes.  
Loss curves show consistent improvement, and predicted depth maps align closely with ground truth distributions.

### Future Work
- Integrate ResNet or transformer backbones for improved feature extraction  
- Explore SSIM or perceptual loss for sharper depth boundaries  
- Extend the model to real-time inference for computational photography applications  

### Author
Shrayas Raju  
Clemson University  

