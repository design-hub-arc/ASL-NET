# ASL-NET

Neural Network for recognizing ASL alphabet.

&nbsp;

**Training Mode:**

Train a model with the asl_dataset, the batch size and where you would like the model stored.

Dataset Link: http://www.mediafire.com/file/4nrm2dszm654j8r/asl-alphabet-resized.zip/file

Note: If you are not using the asl_alphabet_resized dataset, you may need to make modifications for the network to train on your data.
```
python asl_net.py /path/to/dataset_dir batch_size /path/to/model.h5
```

&nbsp;

**Test Mode (Fast Forward):**

Use a trained model to make predictions on a folder of images. Difference here is that the first argument is now just a folder of images rather than a folder with a train, val, and test directory for training. Another difference here is the extra argument, which is a path to a pdf (existing or not) for saving the outputted prediction report.
```
python asl_net.py /path/to/images_dir bacth_size /path/to/model.h5 /path/to/PDF_output.pdf
```

&nbsp;

**Project Setup:**

ASL PROJECT SETUP INSTRUCTIONS ON Windows/Linux/Mac (Note that some basic commands may be Operating system dependent):
THIS SETUP IS INTENDED TO SETUP THE ENVIRONMENT AND HAVE EVERYTHONG NEEDED. THIS IS NOT A TUTORIAL ON
TRAINING OR TESTING A NETWORK
SHARED DRIVE: https://drive.google.com/drive/u/1/folders/0AIqeXvvVgJDvUk9PVA


* Install Python3 with PIP, and GIT if not already installed.
  - https://www.python.org/downloads/
  - https://git-scm.com/downloads

* Now lets make a directory for all of our work, models, and datasets to be stored. And go to it.
  - mkdir ASLProject
  - cd ASLProject

* Clone the ASL-Net repository.. (you will need git installed for this)
  - git clone https://github.com/designhubarc/ASL-NET.git

* Next lets get our dataset and move it to our ASLProject directory after the download is complete.
  - https://drive.google.com/file/d/1xy36uS2Qci2ea3nb2d4pXxpgTIfho7S7/view?usp=sharing

* Unzip the dataset in the ASLProject/ directory. You will notice that it makes a folder within a folder.
  So we have ASLProject/asl-alphabet-resized/asl-alphabet-resized/... Lets bring the inner folder back one directory such
  that we have ASLProject/asl-alphabet-resized/... directly followed by the train,test, and val folders
  Make sure you are in the ASLProject directory and run:
  - mv .\asl-alphabet-resized\asl-alphabet-resized\* .\asl-alphabet-resized\
  - rm -r .\asl-alphabet-resized\asl-alphabet-resized\

* Lastly we need our Python dependencies installed with PIP
  The command is 'pip install ...'
  - pip intall numpy, matplotlib, tensorflow or tensorflow-gpu, tqdm
					 
		
		
		
NOTE: If using a GPU, I believe you will need the CUDA toolkit.. This part is much more complicated to setup, but here is the official what you need. https://www.tensorflow.org/install/gpu
