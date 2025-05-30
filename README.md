# ECG_classifier_2d_CCN
ECG classifier modified from 'Deep residual 2D convolutional neural network for cardiovascular disease classification' Elyamani et. al.

Elyamani, H.A., Salem, M.A., Melgani, F. et al. Deep residual 2D convolutional neural network for cardiovascular disease classification. Sci Rep 14, 22040 (2024). https://doi.org/10.1038/s41598-024-72382-3

Creative Commons licence

Original code base found here: https://github.com/HaneenElyamani/ECG-classification

The original model was trained on PTB-XL data set: https://physionet.org/content/ptb-xl/1.0.1/

The output has been modified to output seven classes: ['1dAVb', 'AFIB', 'AFLT', 'LBBB', 'NORM', 'OTHER', 'RBBB']

There is also code to shape the dataset found here: https://physionet.org/content/ecg-arrhythmia/1.0.0/ to the same format for further fine-tuning or testing.

There is options for fine-tuning with frozen weights or not, I found better results when full weights were retrained.

To use the original code base data prep, use 'Data-different-leads.ipynb'
'Task3_Data_Prep.ipynb' will prep for the seven classes for the fine-tuned model.
'Classification_Model_Finetune.ipynb' can be used for fine-tuning or training the model.
'Main.ipynb' contains code for benchmarking the model as well as code for analysing single instances of ECGs with explanation. It assumes that the ECG has been converted to numpy array already.
