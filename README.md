# Overview of computer vision glossary
A list of common and useful computational techniques/models I have come across when working on computer vision applications. Some of them are illustrated using visual examples in this repository.

## Classical CV techniques
- Vignetting: Techniques for creating darker edges in images, also known as vignetting.
- Flat-field correction: Techniques for correcting darker edges (or vignette effects) in images to smooth out image intensities.
- Chromatic aberration correction: Methods for correcting chromatic abberations in images (e.g. color fringing, image blur), through calculating and applying offsets and scale factors. 
- Morphological operations: Binary mask processing operations to improve the quality of generated masks for object detection in images.
- Low-pass filters: Filters that remove high-frequency noises while allowing low-frequency signals to pass through, useful for providing smoothing and blurring effects in images.
- High-pass filters: Filters that remove low-frequency noises while allowing high-frequency signals to pass through, useful for sharpening effects and detecting sharp edges in images.
- Otsu Thresholding: A simple method for generating a binary mask of objects in images, useful for object detections.
- Image denoising: Technique to reduce graininess and decolorization in images to improve image quality.
- Feature Extraction: Methods used to convert objects of interest in an image into vector representation, useful for object recognition and object matching tasks.
- Voxelization: Methods used to turn a set of 3D xyz coordinates into an organized grid of 3D voxel (volumetric pixels), useful as a preprocessing step for 3D construction tasks.

## Open-source deep-learning models/libraries
- [Deepspot](https://github.com/cbib/DeepSpot): Deep-learning CNN model for enhancement of fluorescent spots in microscopy images.
- [Cellpose](https://github.com/MouseLand/cellpose): A U-Net model trained specifically for cell segmentation in images. Offers segmentation on specific cell features, such as cell boundaries or nucleus segmentation.
- [BigFISH](https://github.com/fish-quant/big-fish) spot detection in microscopy images: Detects fluorescent spots in microscopy images by enhancing spots using a Laplacian of Gaussian (LoG) filter, followed by pixel intensity thresholding to detect RNA spots.
- [trackpy](https://github.com/soft-matter/trackpy) spot detection in microscopy images: Detects fluorescent spots in microscopy images by leveraging on the Crocker-Grier algorithm (detect feature then track movement).
- [Watershed](https://www.geeksforgeeks.org/computer-vision/image-segmentation-with-watershed-algorithm-opencv-python): An opencv algorithm that involves creating basins based on pixel intensities, and expanding them to segment objects in images.
- [Segment Anything Model (SAM)](https://github.com/facebookresearch/segment-anything): A vision-transformer (ViT) model from MetaAI that takes in user-specified prompts to segment objects in images. Offers both a GUI and an API for better customization of segmentation.
- [CLIP](https://arxiv.org/pdf/2103.00020): A vision language model from OpenAI that connects images to texts and vice versa. Useful for zero-shot image classification or semantic embedding tasks. 

## ML performance improvement techniques
- Quantization: Methods used to reduce model precision (e.g. weights/activation outputs), used to reduce model memory or improve inference speed. Most useful for models required to run on edge devices that have memory or computational constraints.
- Hyperparameter tuning techniques: Methods used to tune the hyperparameters of a model to optimize for performance. Depending on model complexity and how many hyperparameters need to be tuned, these techniques are usually time-consuming and costly to carry out.
- [Squeeze-and-Excitation Networks (SE)](https://arxiv.org/pdf/1709.01507): Lightweight attention module that can be easily integrated to different types of model architecture to improve performance.
- [Convolutional Block Attention Module (CBAM)](https://openaccess.thecvf.com/content_ECCV_2018/papers/Sanghyun_Woo_Convolutional_Block_Attention_ECCV_2018_paper.pdf): Lightweight attention module that can be easily integrated to different types of model architecture to improve performance. Shown to have negligible computational/memory overhead but provides significant performance when used.

## ML architectural components
- Gradient descent algorithms: Methods utilized by optimizers in neural network models to shift weights in a way that improve performance, where performance is quantified by a loss/utility function.
- Loss functions: Statistical functions used by machine learning models to calculate error between predictions and target values. Used in neural networks during gradient descent to shift weights such that error is minimized.
- Utility functions: Statistical functions used by machine learning models to calculate how close predictions are to target values. Used in neural networks during gradient ascent to shift weights such that likelihood is maximized.
- Overfitting: Refers to when models are trained to fit too well to training/observed data, such that they no longer generalize and perform well to testing/unobserved data. Can be identified by comparing how the loss curve looks between training and validation data.
- Underfitting: Refers to when models are not sufficiently trained to perform well even on training/observed data, so they don't perform well to testing/unobserved data as well. Can be identified by a loss curve that continues to improve during model training.
- Activation functions: Functions applied to a neuron's output values to introduce non-linearity to models, since neurons inherently calculate output based on a linear function. We can best think of activation functions as transforming model output to a set range of values suitable for the prediction task at hand.
- Pooling layers: Applies a function for simultaneous downsampling and feature extraction, also help models learn features that are spatially invariant (i.e. Translation Invariance).
- Strides: Parameter that determines how much a convolutional filter is moved when extracting features in the input data. Typically used as an alternative to pooling layers for simulataneous downsampling and feature extraction, since they are computationally cheaper and does not rely on a fixed pooling function.

## Other good-to-know metrics/theories
- Signal-to-Noise ratio: The ratio of signal to noise, or information from the object of interest vs from non-object of interest. For images, it is defined as the mean pixel intensity / standard deviation of noise. Useful to measure variability for image quality purposes.
- Signal-to-Background ratio: The ratio of signal to background, or intensity of a target vs the background of an image. It is defined as the mean pixel intensity of target / mean intensity of background intensity. Useful to measure contrast between target and background for image quality purposes.
- Pinhole camera model: The mathematical relationship used for actual depth estimation tasks, between the position of a camera lens and the size of an object on a 2D image. Given the focal length of a camera (distance between camera lens and object) and the physical/digital dimensions of an object, you can solve for the actual depth of the object. 
