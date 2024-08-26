# part_dimensions_project
This is repository documents the progress and the code for the reserach project titled 'Automated Measurement of Additive Manufactured Parts through Computer Vision and Deep Learning'. This project is being done under the 
MIRAGE Lab[https://mirage.umd.edu/?utm_source=umd&utm_medium=organic&utm_campaign=network] at UMD lead by PRof. Davis J. Mcgregor[https://www.davismcgregor.com/]. The project leverages semantic segmentation models to seperate 
out regions of interest from the images of additively manufactured parts and further uses algorithms to carry out measurements

# Dataset Development
The dataset development for the project consisted of using contour extraction algorithms from CV2 to extract the contours of the pieces under study, rotate them and paste them on a black background. 100 such rotations for the piece
and its specific label was carried out. 


<img src="https://github.com/user-attachments/assets/c8f96ef9-d476-41d1-b54b-ebcd739d3cf6" alt="shuffled_image_1" title="Piece Image" width="200" height="100"/> <img src="https://github.com/user-attachments/assets/76748c25-7702-47af-9d81-450a5a6f8f0c" alt="shuffled_label_1" width="200" height="150"/>
