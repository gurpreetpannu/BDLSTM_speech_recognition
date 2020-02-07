# BDLSTM_speech_recognition
The original dataset had over 100K recordings of 35 words spoken in different tones and pitches. I tried to build a multiclass classification model using Neural network.

The audio was in `.wav` formats. I used the librosa library to extract the mfcc, mfcc-delta and mfcc-delta-delta features to get a numerical representation of the audio files. I tried the model I developed on mel features alone and the above mfcc and mel features appended together, however the novel mfcc features seem to work the best with the highest accuracy.

Overall I achieved a 93% accuracy on test set. I had achieved accuracy of upwards of 95% on a more complicated model which had 5 neural network models stacked on one another. However such a model is not feasible when used in production because of the sheer size of which was atleast 50 times larger than the final model I developed. 

The preprocessing after extracting the mfcc features were limited to balancing the classes. I did toy around with normalising the data, however I dropped it later as it resulted in lower accuracy. 

A novel library which helped tremendously in this project is `kapre`. This library had function called **Normalisation2D** which helped in Normalisation of the mfcc feature before feeding it in the model.
