# Removing Noise from Signals with the help of RNN/ LSTM

**Removing Noise from Signals with the help of RNN/ LSTM**

In this project, we deal with noise reduction of different signals with recurrent networks.

## **Dataset**

With the help of commands in python, we generate sine, triangular and sawtooth signals. The following defaults are considered for these signals.

* We consider ten periods for each signal.

* We consider the periodicity of each signal as 200 seconds. That is, the total time is 2000 seconds.

* We consider the sampling frequency 1000, so we have 2000,000 samples for each signal.

The figure below shows these three signals.

 ![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/Original-signals.png)

* Then, out of these ten periods, we keep 7 for train data (i.e., 1400 seconds), assign one period to validation data (i.e., 200 seconds), and give 2 for test data.

* We generate Gaussian noise with a variance of one and a mean of zero and add it to the signals.

## **Network**

We designed the RNN and LSTM Networks with the below features. 
 ![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/LSTM.png)

 ![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/LSTM-Output.png)

 ![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/RNN.png)


 ![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/RNN-Output.png)

## **Comparison**

* **Comparing RNN and LSTM**

In this part, LSTM gives us a better result. LSTM is faster, and the LSTM network produces 99% accuracy on the test data, while the similar RNN network gives us 97% accuracy.
Also, the SNR value of the LSTM network output is almost two times the SNR of the RNN network output signal.
On the other hand, RNN converges to a higher accuracy value faster 
In the following, we have compared the process of changes in Accuracy and Loss on train and validation data for these two networks.

 ![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/Comparing-LSTM-RNN.png)

* **The effect of Learning Rate**

The learning rate controls the speed at which the model adapts to the problem. Lower learning rates require more training sessions due to more minor weight changes per update, while more significant learning rates lead to faster changes and fewer training sessions.
Too high a learning rate can cause the model to converge too quickly to a suboptimal solution, while too small a learning rate can cause the process to stall.

 ![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/Learning-Rate-LSTM.png)

 ![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/Learning-Rate-RNN.png)


* **The effect of Batch size**

As you can see above, the smaller batch size (16) gives us higher accuracy. With the help of the LSTM network and batch size of 16, we reached 99% accuracy, but the training time increased because more learning occurred. On the other hand, the learning speed increases, and we achieve more accuracy and less loss. However, the larger batch size causes less learning and lower accuracy than the larger batch size, but the training time is shorter.

 ![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/Batch-Size-LSTM.png)

 ![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/Batch-Size-LSTM-Compare.png)

 ![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/Batch-Size-RNN.png)

 ![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/Batch-Size-RNN-Compare.png)

* **The Effect of the Number of Epochs**
 ![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/Epochs-LSTM.png)

 ![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/Epochs-LSTM-Compare.png)

 ![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/Epochs-RNN.png)

 ![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/Epochs-RNN-Compare.png)


* **The Effect of Changing Noise Variance**

![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/Variance.png)

![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/Variance-Output.png)


## **Adding non-stationary noise**

To add noise whose variance and mean are time-varying, we divide the signals into two parts and add noise with a variance of 1 and a mean of zero to the first part and noise with a variance of 15 and a mean of 5 to the second part. The signals after adding noise are shown in the below figure.

![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/Original-signals.png)

![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/Noisy-Signals.png)

![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/Non.stationary.noise.LSTM.png)

![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/Non.stationary.noise.LSTM.Result.png)

![](https://github.com/Fateme-Azizabadi/Removing-Noise-from-Signals-with-the-help-of-RNN-LSTM/blob/main/Images/Non.stationary.noise.Output.png)


 
 
