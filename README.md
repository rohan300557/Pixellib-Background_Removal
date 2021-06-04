# PixelLib Background Removal

Image segmentation involves converting an image into a collection of regions of pixels that are represented by a mask or a labeled image. or It is used when we have to classify each pixel of the classes.

Eg:- Which pixel belongs to which object by masking in the picture

PixelLib is a library for performing segmentation of objects in images and videos.
I used Deeplabv3+ framework to perform semantic segmentation. Xception model trained on pascalvoc dataset is used for semantic segmentation.

You can change the background of any image through image segmentation using PixelLib feature called as image tuning.
Image Segmentation Process:
* Remove the objects segmented from the image by masking in the image.
* Place the new background.
* Combine segmented object with the modified background.
* Install PixelLib:
 > ### Requirements:
> * [ ] Install PixelLib on CMD using:- `pip install pixellib`
 >* [ ] Model: deeplabv3_xception_tf_dim_ordering_tf_kernels.h5
*You can Download form [here](https://github.com/ayoolaolafenwa/PixelLib/releases/download/1.1/deeplabv3_xception_tf_dim_ordering_tf_kernels.h5).*





>### Input Image: 
>**This image will be used to change the background.**
>
> <img src="https://raw.githubusercontent.com/rohan300557/Pixellib-Background_Removal/main/Input%20image/joker.jpg?token=AOPFY3YC2LPORMVR4LC72P3AYO546" data-canonical-src="https://raw.githubusercontent.com/rohan300557/Pixellib-Background_Removal/main/Input%20image/joker.jpg?token=AOPFY3YC2LPORMVR4LC72P3AYO546" width="400" height="300" />

>### Output Image: 
>
>> #### Masked
>```python: 
>segment_image = semantic_segmentation()
>segment_image.load_pascalvoc_model("Model/deeplabv3_xception_tf_dim_ordering_tf_kernels.h5")
>segment_image.segmentAsPascalvoc("Input image/joker.jpg", output_image_name = "Output Image/mask_joker.jpg")
>````
>  <img src="https://raw.githubusercontent.com/rohan300557/Pixellib-Background_Removal/main/Output%20Image/mask_joker.jpg?token=AOPFY37PHG5M76HUHTK355DAYO2CC" data-canonical-src="https://raw.githubusercontent.com/rohan300557/Pixellib-Background_Removal/main/Output%20Image/mask_joker.jpg?token=AOPFY37PHG5M76HUHTK355DAYO2CC" width="400" height="300" />
>  
>> #### Background color changed to white 
>```python:
>change_bg = alter_bg()
>change_bg.load_pascalvoc_model("Model/deeplabv3_xception_tf_dim_ordering_tf_kernels.h5")
>output = change_bg.color_bg("Input image/joker.jpg", colors =  (255, 255, 255))
>cv2.imwrite("Output Image/change_bgcolor_joker.jpg", output)
>```
>
> <img src="https://raw.githubusercontent.com/rohan300557/Pixellib-Background_Removal/main/Output%20Image/change_bgcolor_joker.jpg?token=AOPFY33TRD4EMQHMWV7DIH3AYO2ME" data-canonical-src="https://raw.githubusercontent.com/rohan300557/Pixellib-Background_Removal/main/Output%20Image/change_bgcolor_joker.jpg?token=AOPFY33TRD4EMQHMWV7DIH3AYO2ME" width="400" height="300" />

## For Reference 
 * Change the Background of Any Image: [towardsdatascience](https://towardsdatascience.com/change-the-background-of-any-image-with-5-lines-of-code-23a0ef10ce9a)
 
