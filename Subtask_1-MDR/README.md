# Subtask 1 - Multi-Drug Resistant Detection

Weights of LSTM model for Task 1 found [here](https://www.dropbox.com/s/plu542ns1fgr3yx/Resnet50_T1_sgd_LSTM_v7_epoch_5?dl=0)

### Below is the code to define the LSTM model in Keras
```python
from keras.models import Sequential
from keras.layers import Dense, Dropout, Embedding, Bidirectional, Activation, LSTM, SimpleRNN

model = None
batch_size = 50
seq_length = 75
input_feat = 2048

feature_layers = [
    LSTM(2048, return_sequences=True, input_shape=(seq_length, input_feat)),
    LSTM(1250, return_sequences=True),
    LSTM(750),
    Dropout(0.3),
    Dense(500, activation='linear'),
    Dropout(0.1)
]

classification_layers = [
    Dense(250, activation='linear'),
    Dense(1),
    Activation("sigmoid")
]
model = Sequential(feature_layers + classification_layers)
model.compile(optimizer="sgd", loss="mean_squared_error")
```

