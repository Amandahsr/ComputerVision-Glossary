# Overview of computer vision techniques/models
A list of common and useful computational techniques and models I have come across when working on image processing applications.

## Classicial CV techniques
- Vignetting: Techniques for creating darker edges in images, also known as vignetting.
- Flat-field correction: Techniques for correcting darker edges (or vignette effects) in images to smooth out image intensities.
- Morphological operations: Binary mask processing operations to improve the quality of generated masks for object detection in images.
- Low-pass filters: Filters that remove high-frequency noises while allowing low-frequency signals to pass through, useful for providing smoothing and blurring effects in images.
- High-pass filters: Filters that remove low-frequency noises while allowing high-frequency signals to pass through, useful for sharpening effects and detecting sharp edges in images.
- Otsu Thresholding: A simple method for generating a binary mask of objects in images, useful for object detections.
- Image denoising: Technique to reduce graininess and decolorization in images to improve image quality.
- Feature Extraction: Methods used to convert objects of interest in an image into vector representation, useful for object recognition and object matching tasks.

## Open-source deep-learning models/libraries
- [Deepspot](https://github.com/cbib/DeepSpot): Deep-learning method for enhancement of fluorescent spots in microscopy images.
- [Cellpose](https://github.com/MouseLand/cellpose): A neural network based method trained specifically for cell segmentation in images.
- [Segment Anything Model (SAM)](https://github.com/facebookresearch/segment-anything): An AI model from MetaAI that takes in user-specified prompts to segment objects in images.
- [BigFISH](https://github.com/fish-quant/big-fish) spot detection in microscopy images: Detects fluorescent spots in microscopy images.
- [trackpy](https://github.com/soft-matter/trackpy) spot detection in microscopy images: Detects fluorescent spots in microscopy images.
- [Watershed](https://www.geeksforgeeks.org/computer-vision/image-segmentation-with-watershed-algorithm-opencv-python): An opencv algorithm that involves creating basins based on pixel intensities, and expanding them to segment objects in images.

## ML architectural performance add-ons
- [Convolutional Block Attention Module (CBAM)](https://openaccess.thecvf.com/content_ECCV_2018/papers/Sanghyun_Woo_Convolutional_Block_Attention_ECCV_2018_paper.pdf): Lightweight attention module that can be easily integrated to different types of model architecture to improve performance. Shown to have negligible computational/memory overhead but provides significant performance when used.

## ML architectural performance considerations
- Gradient descent algorithms: Methods utilized by neural network models to shift weights in a way that improve performance, where performance is quantified by a loss/utility function.
- Loss functions: Statistical functions used by machine learning models to calculate error between predictions and target values. Used in neural networks during gradient descent to shift weights such that error is minimized.
- Utility functions: Statistical functions used by machine learning models to calculate how close predictions are to target values. Used in neural networks during gradient ascent to shift weights such that likelihood is maximized.
- Overfitting: Refers to when models are trained to fit too well to training/observed data, such that they no longer generalize and perform well to testing/unobserved data. Can be identified by comparing how the loss curve looks between training and validation data.
- Underfitting: Refers to when models are not sufficiently trained to perform well even on training/observed data, so they don't perform well to testing/unobserved data as well. Can be identified by a loss curve that continues to improve during model training.
