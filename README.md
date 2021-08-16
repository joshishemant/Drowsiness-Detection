# Drowsiness-Detection
A real time drowsiness detection system using neural networks
.

In Drowsiness Detection System, it is difficult to tell from a single frame if the person is blinking or falling asleep. In order to overcome this problem, the chosen approach uses CNN-LSTM, which comprises of two sub- models: the convolutional neural network model (CNN) for feature extraction and LSTM for interpreting the features across consecutive frames. The procedure for drowsiness detection is thus as follows: First, we extract significant CNN features from the video frames.
Then features representing the sequence of the action (Alert or a Drowsy Driver) for a certain time interval (fixed number of frames) are fed to the LSTM as an input. Finally, a softmax layer is used to predict drowsiness/alertness of the entire video sequence.

The model was tried and tested with various parameters. Inception-v3 retrained on the given dataset of eye patches obtained an approximate training accuracy of: 95.5%. Testing accuracy was 87.5% for 30 epochs for the LSTM model. The model was able to classify the drowsy driver with 93% confidence and alert driver was detected with the confidence of 95.5% in most of the trails.

 The hyper parameters, accuracy and loss functions obtained for 30 epochs were stored in log and recorded as shown in the graph below.	
 
 ![lstm_graph](https://user-images.githubusercontent.com/67290562/129606193-4f42aedc-b2f6-488f-a587-ee0ca4161334.PNG)
 
Future Scope:

The proposed model can be improvised by learning to detect faces and eyes in varied lighting conditions, such as at night with infrared lights. In addition to this, the model should also be able to recognize drowsy eyes with sunglasses.
With some modification this system can be used in combination with real time cameras to provide alert a driver while he is driving. This will however require exhaustive testing on a larger dataset.
