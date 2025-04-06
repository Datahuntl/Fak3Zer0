# Fak3Zer0
DeepFake detector, utilizing Machine learning algorithm(s)

## Datasets
[Kaggle Deepfake Detection Challenge](https://www.kaggle.com/competitions/deepfake-detection-challenge/data)
[Kaggle Celeb DF (v2)](https://www.kaggle.com/datasets/reubensuju/celeb-df-v2)
[WildDeepfake: A Challenging Real-World Dataset for Deepfake Detection](https://github.com/OpenTAI/wild-deepfake)

## Selecting an Architectural Model
### 3D Convolutional Neural Networks (3D CNNs)
Unlike 2D CNNs that operate on individual frames, 3D CNNs apply 3D convolutional filters that can learn spatiotemporal features directly from a sequence of video frames. The filters move across the spatial dimensions (height and width) and the temporal dimension (number of frames).
#### Common Architectures:
- **C3D (Convolutional 3D Network):** One of the pioneering 3D CNN architectures.
- **I3D (Inflated 3D ConvNet):** Starts with pre-trained 2D CNN filters (like Inception) and inflates them into 3D, often leading to better performance due to strong initialization.
- **R(2+1)D:** Decomposes the 3D convolution into separate 2D spatial convolutions and 1D temporal convolutions, which can be more parameter-efficient and easier to train.
### Recurrent Neural Networks (RNNs) and their variants (LSTMs and GRUs)
RNNs are designed to process sequential data. For video, you can extract spatial features from each frame using a 2D CNN (as a feature extractor) and then feed these frame-level features into an RNN to model the temporal relationships between frames.
#### Common Architectures:
- **CNN + LSTM:** A very popular approach where a CNN (e.g., ResNet, EfficientNet) extracts features per frame, and an LSTM processes the sequence of these feature vectors.
- **CNN + GRU:** Similar to CNN + LSTM but uses Gated Recurrent Units, which are often faster to train and can perform comparably in many tasks.
- **Bi-directional LSTMs/GRUs:** Processing the temporal sequence in both forward and backward directions can provide more context.
### Hybrid
Combining the strengths of different architectures can often lead to improved performance.
#### Examples:
- **CNN + RNN (as mentioned above):** Leveraging CNNs for spatial feature extraction and RNNs for temporal modeling.
- **CNN + Transformer:** Using CNNs for efficient feature extraction and Transformers for powerful temporal modeling.
- **3D CNN + RNN/Transformer:** Using a 3D CNN to extract initial spatiotemporal features and then feeding these into an RNN or Transformer for further temporal reasoning.
### Graph Neural Networks (GNNs)
GNNs are designed to operate on graph-structured data. In the context of video, you could represent facial landmarks or other key points as nodes in a graph, and the relationships between them (e.g., distances, angles) as edges. The temporal evolution of these graphs can then be analyzed using GNNs.
#### Common Architectures:
- **Spatial-Temporal Graph Convolutional Networks (ST-GCN):** While primarily used for action recognition, the concept of modeling spatiotemporal relationships using graph convolutions could be adapted for analyzing facial movements in deepfakes.

## Relevant research material
### Youtube videos:
[MesoNet: a Compact Facial Video Forgery Detection Network](https://www.youtube.com/watch?app=desktop&v=kYeLBZMTLjk&t=13s) <br>
[Deepfake detection using Deep Learning (ResNext and LSTM)](https://www.youtube.com/watch?app=desktop&v=O3_MypgLuvc) <br>
### Github Projects:
[Exploring Deepfake Detection with MesoNet](https://github.com/kiteco/python-youtube-code/tree/master/Deepfake-detection) <br>
[Deepfake detection using Deep Learning (ResNext and LSTM)](https://github.com/abhijithjadhav/Deepfake_detection_using_deep_learning?tab=readme-ov-file) <br>
### Research papers:
MesoNet: a Compact Facial Video Forgery Detection Network <br>
