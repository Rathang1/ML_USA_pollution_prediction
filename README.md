# ML_USA_pollution_prediction
LSTM (RNN) on Time Series data without using standard libraries (from scratch).

Link available for dataset in working as of now. Incase it doesn't work then refer to https://www.kaggle.com/datasets/sogun3/uspollution for the dataset

We take into account the average concentrations of four primary pollutants: nitrogen dioxide, sulfur dioxide, carbon monoxide, and ozone, throughout the day. This report outlines how to forecast mean value utilizing US air pollution data between the years 2000 - 2016 using a Recurrent Neural Network (RNN) with Long-Short-Term-Memory Networks (LSTM) approach. LSTM resolves long-term dependency issues and assists in determining the mean in time series due to its distinctive storage unit structure. Root Mean Squared Error (RMSE) and Mean Absolute Percentage Error (MAPE) have been used to calculate the accuracy of the model after it has been trained with various parameter combinations. Furthermore, the model performance has been visualized using graphs in results folder for various combinations of hyper-parameters.

Recurrent Neural Networks: 
A Recurrent Neural Network (RNN) is a type of Artificial Neural Network that is made for chronological data where instances of data are dependent on instances of data that appeared before them in the chronological order or in general any dataset where the current instance in consideration is dependent on some previous instance. LSTM is the best suited for our scenario because of its memory persistence feature.

![image](https://user-images.githubusercontent.com/95063504/177926184-ed62e622-f711-4e15-ab99-0a0b43faf015.png)


Long – Short - Term - Memory Architecture:
The LSTM model works as one of the best choices due to the way it utilizes its memory element. Just like what its name suggests – LSTM tries to maintain its history of cell states for the variability of long-length or short length and this memory remembered is further exploited for the mature performance of the cells. 

![image](https://user-images.githubusercontent.com/95063504/177926204-40e5f5a9-c900-4581-94a2-18dbcebc1713.png)

It is an improvised version of RNN. for countering the gradient issues (exploding and vanishing) because RNN with these flaws cannot be used for the analysis of the dataset in practical scenarios if the memory element gets compromised. The cell state recurs a fixed number of times and for each such iteration, it changes its form as well as the weights that monitor the value of gradient inclination of the model. These are then handed over to the next iterations for designated computations. LSTMs deal with both Long Term Memory (LTM) and Short-Term Memory (STM) and for making the calculations simple and effective. It uses the concept of gates.
The recursive calling of its cell state to update its three most important results which are termed as gates are – in-out-forget trio (input-output–memory).
1. In element – It takes up the previous cell state results and forms a paired vector with the current sequence input which is utilized on the activation function to initialize the memory element.
2. Memory element – The forget gate or more like a memory gate for preserving the historic memory of results. It performs computations to get a processed vector that can decide on the fraction of history to be remembered. It makes use of two different functions such that they are constituted together which in turn proceeds to merge with the initialized input.
3. Out element – Now this has the responsibility to produce the final cell state output such that it comprises activated in-state vectors along with the memory processed vectors applied on tanh.

![image](https://user-images.githubusercontent.com/95063504/177926150-7e0ed9dd-5c8f-4877-9bde-71da554adb1a.png)

Conclusion and Future Work:
As a result of this experiment, we were able to uncover a consistent pattern in the mean concentration levels of air pollutants, despite the fact that the mean concentration levels of air pollutants are clearly erratic. It is also obvious from past data that mean levels of air pollutants can consistently jump or fall, thus we anticipate that by adding as many impacting elements as possible along with the spatial data, we would be capable of achieving better results in the near future.
Since there are several other models, including auto-regressor, ARIMA, and moving average, have indeed been demonstrated to be effective at diagnosing time series difficulties accompanying RNNs and LSTMs. We would try to work on these model versions as well. Furthermore, since each of such algorithms will have its own set of benefits and costs, an ensemble classifier can be designed to mitigate drawbacks simultaneously stacking the benefits and obtaining significant outcomes.

References:

[1] Understanding LSTMs <https://colah.github.io/posts/2015-08-Understanding-LSTMs/>

[2] Fabiana Martins Clemente, Aleš Popovič, Sara Silva, and Leonardo Vanneschi, "A Machine Learning Approach to Predict Air Quality in California”, 04 Aug 2020, IEEE

[3] Yun-Chia Liang, Yona Maimury, Angela Hsiang-Ling Chen, and Josue Rodolfo Cuevas Juarez, “Machine Learning-Based Prediction of Air Quality”, 21 December 2020, MDPI

[4] Deriving Back Propagation Equations for an LSTM < https://christinakouridi.blog/2019/06/19/backpropagation-lstm/>

[5] Everything you need to know about Min-Max normalization: A Python tutorial < https://towardsdatascience.com/everything-you-need-to-know-about-min-max-normalization-in-python-b79592732b79>
