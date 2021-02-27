# ASL-NET

Neural Network for recognizing ASL alphabet.

&nbsp;

**Training Mode:**

Train a model with the asl_dataset, the batch size and where you would like the model stored.

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
