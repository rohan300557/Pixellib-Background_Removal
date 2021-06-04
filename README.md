# PixelLib Background Removal

Image segmentation involves converting an image into a collection of regions of pixels that are represented by a mask or a labeled image. or It is used when we have to classify each pixel of the classes.

Eg:- Which pixel belongs to which object by masking in the picture

PixelLib is a library for performing segmentation of objects in images and videos.
I used Deeplabv3+ framework to perform semantic segmentation. Xception model trained on pascalvoc dataset is used for semantic segmentation.
Name of the Model: deeplabv3_xception_tf_dim_ordering_tf_kernels.h5
*You can Download for [here](https://github.com/ayoolaolafenwa/PixelLib/releases/download/1.1/deeplabv3_xception_tf_dim_ordering_tf_kernels.h5).*
You can change the background of any image through image segmentation using PixelLib feature called as image tuning.
Image Segmentation Process:
* Remove the objects segmented from the image by masking in the image.
* Place the new background.
* Combine segmented object with the modified background.

### Input Image: This image will be used to change the background.


Install PixelLib:
On CMD:- `pip install pixellib`
