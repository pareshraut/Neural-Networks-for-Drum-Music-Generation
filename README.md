# Neural-Networks-for-Drum-Music-Generation

presentation deck : https://gamma.app/public/Using-Neural-Networks-for-Drum-Music-Generation-ffrjj4t57judp7q

This project focuses on generating drum music using a Long Short-Term Memory (LSTM) neural network. The LSTM model is trained on a dataset of MIDI files containing rock-style drum performances. The goal is to create a model that can generate realistic and expressive drum sequences.

### Dataset
The dataset used for training the LSTM model is the Groove MIDI Dataset (GMD). It consists of approximately 13.6 hours of drumming, comprising 1,150 MIDI files and over 22,000 measures of drum performances. Each drum performance in the dataset is played along with a metronome set at a specific tempo by the drummer.

It's important to note that the MIDI files in the dataset were recorded using a Roland TD-11 electronic drum kit, which has some pitch value discrepancies compared to the General MIDI (GM) Specifications. These discrepancies are accounted for during playback and training by using a mapping that aligns the Roland pitch values with the GM pitch values.

For this project, a subset of 128 MIDI files from the rock genre was selected to train the model. This narrower focus allows the model to specialize in generating drum music specifically in the rock style.

### Methodology
The project follows the following steps:

**Data Collection**: The MIDI files from the rock genre are collected and preprocessed to extract the drum notes.

**Exploratory Data Analysis (EDA)**: A comprehensive analysis is performed on the dataset, including measures of drumming, tempo variations, and pitch mappings between Roland and GM specifications. This analysis provides insights into the characteristics of the drum performances and helps in understanding the data better.

**Feature Engineering and Transformations**: The drum notes extracted from the MIDI files are further processed to create input sequences for the LSTM model. The pitch names are mapped to integers, and the sequences are prepared by sliding a window of a fixed length over the notes.

### Model Architecture and Training:
An LSTM neural network is designed and trained on the prepared input sequences. The model consists of multiple LSTM layers with dropout and batch normalization for regularization. The training process involves optimizing the model using the Adam optimizer and minimizing the categorical cross-entropy loss.

### Results and Learnings: 
The trained LSTM model generates drum music sequences based on the provided dataset. However, due to the limitations of the dataset size and computational resources, the generated drum music may exhibit repetitive patterns and similarities. The project provides insights into the impact of these limitations and highlights the need for a broader and more diverse dataset for improved drum music generation.

### Future Work
To enhance the drum music generation process, the following areas can be explored:

Dataset Expansion: Incorporating MIDI files from various drumming styles and genres, in addition to rock, would increase the diversity and genre-specificity of the generated drum sequences.

Computational Resources: Scaling up the computational resources, such as using more powerful hardware or leveraging cloud-based services, would allow for training more complex and expressive LSTM models.

Data Augmentation: Applying data augmentation techniques, such as tempo variations, pitch shifts, and dynamic adjustments, can introduce further diversity and realism in the generated drum music.

Transfer Learning: Leveraging pre-trained models or using transfer learning techniques from related music generation tasks could help improve the performance of the LSTM model in generating drum music.

By addressing these aspects, we can overcome the limitations of the current implementation and achieve more diverse and expressive drum music generation using the LSTM model.

Usage
To use the code in this project, follow these steps:

Install the necessary dependencies 

Run the lstm.py script to start the training process for the LSTM model. Adjust the hyperparameters,

To directly predict new tracks just run predict.py 



