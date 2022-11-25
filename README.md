# Visual Cryptography of Biometric Data



## Description
This was my final project for my Data Privacy and Security class. One of the cryptographic techniques that we studied was Shamir's Secret Sharing Scheme. The (t,n) sharing scheme splits a secret into n unique pieces/"shares" that contain information to "reconstruct" the secret. The secret can only be reconstructed if information from at least t shares are combined. In this application, pixels from an image are encrypted using the (t,n) sharing scheme, resulting in n new images. By combining t of these n images, the original image can be restored.  


## Installation
This program runs on python 3 and requires the installation of the following libraries:

OpenCV and OpenCV-Contrib </br>
Numpy </br>
PyFingerprint (for part 3)</br>
pyserial3 (for part 3)</br>



## Usage

### To run the program
****
From the SRC folder, type the following:

python project.py

****************************************

#### There are three parts to the project:
1. Image Encryption technique
2. Fingerprint encryption/decryption from dataset


#### For part 1:
_________________________________________________________
##### Encryption:
You will be prompted to enter a filename for an image.  These images should be placed in the DATA/pictures folder.
Once you've directed the program to a valid image file, the program will prompt you to enter values for t and n.
As it stands, the program currently works best when t=3.  When t=4, it sometimes works but not always.
Anything greater than 4 will result in the program terminating. </br>

The program will then display the image in grayscale and prompt you to press enter.
The program will encrypt the images and save them in the DATA/pictures folder.

##### Decryption:

You will then be prompted to enter the exact filename of one of the shares and then its corresponding share value.  The shar value will
be the share value will correspond to the naming scheme, i.e. if the file was saved as "cat1.png", the share value will be 1.  
Enter these until you have entered at least t shares.
Press 'r' and the picture will be restored (in grayscale).

#### For part 2:
_____________________________________________________________
Part 2 will choose an image from the dataset at random and display it's feature points.  This dataset can be found in /DATA/DB1_B.
The program will create a text file of the locations of the keypoints (titled "answerkey.txt") and .tsv files that contain the share values of the keypoints.
By pressing enter (after the first 3 images appear), the program will randomly decrypt 3 "shares" files and create a text file of the decrypted shares.  You can then compare the decrypted text file with the answerkey to confirm the points were successfully restored.


.
