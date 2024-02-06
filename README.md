# Genre Classification & Recognition : A Comparative Study

## Major Project - Under Graduation Final 

- Computer Science & Engineering - SRM Institute of Science and Technology

## Music Information Retrieval (MIR) Analysis

* Convert Analog signals to mini frames of digital signals based on sampling rate (slicing of audio wave into data points)
* Frames are based on frame size and hop length that provide amplitude data
* Fourier transform is applied on these sinals to extract important parts (on-set detection)
* FFT converts time-domain signal to frequency based

## Genre Classification training and analysis

* Create dataset using MIR analysis and extrack 6 sets of data points (Zero-crossing rate, spectral centroid/contrast/bandwidth/rolloff. Mean and standard deviation of each, 13 pairs of MFCC of the same
* Split data into training and testing (to compare and study accuracy)
* Perform 4 algorithms in test data (K-Nearest Neighbor, Random Forest, Support Vector Machine, Simple Neural Network)
* Identify algorithm with best accuracy (in our case SVM) - `70%`
* Extract SVM model into pickle file
* Run cached pickle model to test data on the fly

### Architecture

* `TesFiles/` and `TrainFiles/` directories with relevant data
* GTZAN Dataset of musical (.wav) files (from Kaggle - [GTZAN Dataset Music Genre Classification](https://www.kaggle.com/datasets/andradaolteanu/gtzan-dataset-music-genre-classification) for `TrainFiles/`
* Test `.mp3` or `.wav` files in `TestFiles/` directory
* Config file with environment variables
* Static resources in `resources/` directory
* Analysis Theory consists of Music Information Retrieval (MIR) concept Theory
* `data_set.csv/` file recreated by running Create Dataset file
* `model.pkl` created by running Create Model file
* Runner file for training and running recogizer
* Recognizer requires `TestFiles/` directory to be non-empty
