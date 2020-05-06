# Lyrics Generator Model
A lyrics generation model using an RNN with stacked LSTMs (CuDNNLSTMs), implemented using Keras.

Currently, only Taylor Swift's style is available here, as the dataset for her songs was easily available [here](https://www.kaggle.com/PromptCloudHQ/taylor-swift-song-lyrics-from-all-the-albums) at Kaggle.

Soon, support for poem generation and lyrics of other artists will also be added.


# Model Architecture:

Currently, the lyrics are tokenized by word, and the architecture of the model is as follows:

1. Embedding (100 values for each token)
2. LSTM (acutally, CuDNNLSTM)
3. LSTM (this layer can receive state info from the previous LSTM layer)
4. Dropout
5. Dense (fully-connected layer)
