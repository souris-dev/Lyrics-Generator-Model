# Lyrics Generator Model
A lyrics generation model using stacked LSTMs (CuDNNLSTMs), implemented using Keras.

Currently, only Taylor Swift's style is available here, as the dataset for her songs was easily available [here](https://www.kaggle.com/PromptCloudHQ/taylor-swift-song-lyrics-from-all-the-albums) at Kaggle.

Soon, support for poem generation and lyrics of other artists will also be added.


## Model Architecture:

Currently, the lyrics are tokenized by word, and the architecture of the model is as follows:

1. Embedding (100 values for each token)
2. LSTM (actually, CuDNNLSTM)
3. LSTM (this layer can receive state info from the previous LSTM layer)
4. Dropout
5. Dense (fully-connected layer)

__Note__: This notebook was made to run in Google Colab and needs to mount Google Drive at a point. That line may have to be changed to run it locally. Also, as the model uses CuDNNLSTM that work only on GPUs, this notebook needs to be run on a GPU-equipped machine to enable successful training of the model. CuDNNLSTM is effectively a faster version of LSTMs for use on GPUs.
