# RNN-Stock-Closing-Price-Prediction

In the folder 'RNN_models', two notebooks contain RNN models set to the same architecture and parameters with the only difference being the feautres on which to base predictions; while one monitors the preceding closing prices, the other monitors the fear and greed index.

Below is a sampling of the fear and greed index (fng_value) to closing prices:

![](https://github.com/Femi-0/RNN-Stock-Closing-Price-Prediction/blob/main/Resources/Screen%20Shot%202022-06-06%20at%2011.07.43%20AM.png)

Both features showed some tracking of the closing prices. However, while the FNG based model only tracked price direction, the closing price based model performed a better job of tracking the change in both price direction and magnitude. As shown in the graphs below:

#### FNG based LSTM model
---
![](https://github.com/Femi-0/RNN-Stock-Closing-Price-Prediction/blob/main/Resources/Screen%20Shot%202022-06-06%20at%2011.36.24%20AM.png)

#### Closing price based LSTM model
---
![](https://github.com/Femi-0/RNN-Stock-Closing-Price-Prediction/blob/main/Resources/Screen%20Shot%202022-06-06%20at%2011.08.50%20AM.png)

## Model performance evaluation
---

#### Loss
---
FNG based LSTM model | Closing price based LSTM model
---|---
0.1024 | 0.0124

#### Better Values Tracking
---
Closing price based LSTM model track values better.

#### Window Selection
---

Some windows trialed, and their corresponding losses are presented for both models below:

##### FNG based LSTM model
---
Window | Batch Size | Loss
---|---|---
2|8|0.1113
2|64|0.1914
6|32|0.1218
8|32|0.1174
10|32|0.1024


##### Closing price based LSTM model
---
Window | Batch Size | Loss
---|---|---
4|32|0.0466
6|32|0.0110
6|64|0.0540
8|64|0.0301
10|32|0.0124

