# part_dimensions_project
This is repository documents the progress and the code for the reserach project titled 'Automated Measurement of Additive Manufactured Parts through Computer Vision and Deep Learning'. This project is being done under the 
MIRAGE Lab[https://mirage.umd.edu/?utm_source=umd&utm_medium=organic&utm_campaign=network] at UMD lead by PRof. Davis J. Mcgregor[https://www.davismcgregor.com/]. The project leverages semantic segmentation models to seperate 
out regions of interest from the images of additively manufactured parts and further uses algorithms to carry out measurements

# Dataset Development
The dataset development for the project consisted of using contour extraction algorithms from CV2 to extract the contours of the pieces under study, rotate them and paste them on a black background. 100 such rotations for the piece
and its specific label was carried out. 


<img src="https://github.com/user-attachments/assets/c8f96ef9-d476-41d1-b54b-ebcd739d3cf6" title="example_image_1" width="200" height="150"/>                   <img src="https://github.com/user-attachments/assets/76748c25-7702-47af-9d81-450a5a6f8f0c" title="example_label_1" width="200" height="150"/>

<img src="https://github.com/user-attachments/assets/b4861c34-ecf0-4e5d-a2da-50772eb8d5fc" title="example_image_2" width="200" height="150"/>           <img src="https://github.com/user-attachments/assets/c849666a-6f1c-43d8-abf5-fb6bb11f8062" alt="shuffled_label_48" title="example_label_2" width="200" height="150"/>


Images to the left are of the pieces and to the right are of the corresponding labels. There were 100 images of the each piece with hundred different orientations. Only the above two pieces were used for fine-tuning the YOLOV8 model.

# YOLOV8 Fine-Tuning and Inference Results
Using the images and respective labels YOLOV8 model was fine tuned. For fine tuning the labels were used to create appropriate text files. 
Following are the inference results on two seperate test images. It can be observed that the predicted masks closely encode the parallel regions in the image. This can be use to further carry out measurements. 

<img src="https://github.com/user-attachments/assets/368d277e-4d1f-44d0-b5fd-a5d45845f4d4" title="Part Image 191" width="200" height="150"/>


<img src="https://github.com/user-attachments/assets/24c9668a-056f-4946-99c1-de6524a698d9" alt="part_image_194" title="Part Image 194" width="200" height="150"/>

Please note that these results were picked up directly as they were returned by the YOLOV8 API.


# SegFormer Fine-Tuning and Inference Results
The same data was used for training the SegFormer model proposed in the paper titled "SegFormer: Simple and Efficient Design for Semantic Segmentation with Transformers"[https://arxiv.org/abs/2105.15203]. 
Following were the inference results on one of the pieces.

<img width="200" height="150" alt="segformer_image" src="https://github.com/user-attachments/assets/7c4f8d59-92af-4858-a5c9-feaf033d126d">    <img width="200" height = "150" alt="segformer_inference" src="https://github.com/user-attachments/assets/447ecd8b-210e-4f13-b118-8779f987daec">



















































