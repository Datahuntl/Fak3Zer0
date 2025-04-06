# Fak3Zer0
DeepFake detector, utilizing Machine learning algorithm(s)

## Selecting an Architectural Model
### CNNs (Convolutional Neural Networks)
Excellent for learning spatial features in images. Popular architectures include ResNet, EfficientNet, VGG, and MobileNet. You can adapt these pre-trained models using transfer learning, which can significantly speed up training and improve performance, especially with limited data.   
### RNNs (Recurrent Neural Networks)
Especially LSTMs (Long Short-Term Memory) or GRUs (Gated Recurrent Units): Useful for processing sequential data like video frames to capture temporal dependencies and inconsistencies in motion.   
### Transformers
Increasingly being used for video analysis and can capture long-range dependencies in sequences of frames.   
### Hybrid Architectures
Combining CNNs for spatial feature extraction with RNNs or Transformers for temporal analysis

## Relevant research material
### Youtube videos:
[MesoNet: a Compact Facial Video Forgery Detection Network](https://www.youtube.com/watch?app=desktop&v=kYeLBZMTLjk&t=13s) <br>
[Deepfake detection using Deep Learning (ResNext and LSTM)](https://www.youtube.com/watch?app=desktop&v=O3_MypgLuvc) <br>
### Github Projects:
[Exploring Deepfake Detection with MesoNet](https://github.com/kiteco/python-youtube-code/tree/master/Deepfake-detection) <br>
[Deepfake detection using Deep Learning (ResNext and LSTM)](https://github.com/abhijithjadhav/Deepfake_detection_using_deep_learning?tab=readme-ov-file) <br>
### Research papers:
MesoNet: a Compact Facial Video Forgery Detection Network <br>
