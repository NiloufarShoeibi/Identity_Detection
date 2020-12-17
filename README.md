# Identity Detection 👩👨
In this project, the face_recognition pre-trained model has been used to identify the identity of the faces in the images using the database of the identities that will be given to the model as an input.


🧙🏻‍♂️ **The Model** 
The model consists of some steps to follow, each step is explained below. I used the face recognition pre-trained model which has been built using dlib’s state-of-the-art face recognition and built with deep learning. The model has an accuracy of 99.38% on the Labeled Faces in the Wild benchmark.


🔥 **Architecture**

The following image shows the details of the model and each necessary step to follow for identifying the identity of an unknown person using the database of known people with their identities.

<p align="center">
  <img src="https://github.com/NiloufarShoeibi/Identity_Detection/blob/main/Identity%20Detection%20Diagram.jpg" width="750" title="The Model's Architecture">
 
</p>

- **The inputs** are the path to the training dataset which is the folder of existed identities and the following pictures of each person.
The training dataset has been gathered from the BISITE Website with related identities.
- **The outputs** are the images we are going to predict their identities.
The predicted images have been gathered randomly by selecting some of the photos of the colleagues and random people.

- **extract_paths(img_folder)** Extracts the path of each image inside the main folder
- **Load_images (paths)** This loads images by transforming them into ndnumpy arrays.
- **Face_location (images)** Detects the location of the eyes, the eyebrows, the nose, and the mouth. 
- **Extract_labels(folder)** assigns the identity of the people to their images.
- **Find_Faces(images)** will find faces that existed in the image (there can be 0 or multiple faces in an image) and crop them and save them in the new folder.  
- **Face_encoding (images)** builds the encoding of the faces for the further calculations
- **Face_Matching(img_folder, faces_folder)** does the face comparison and save the path of the images and regarding identity as the output and also, shows the image within the predicted identity.
