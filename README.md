# face_emotion_detection

this project is based on deep learning 
Emotion recognition is the process of identifying human emotion. People vary widely in their accuracy at recognizing the emotions of others. Use of technology to help people with emotion recognition is a relatively nascent research area. Generally, the technology works best if it uses multiple modalities in context. To date, the most work has been conducted on automating the recognition of facial expressions from video, spoken expressions from audio, written expressions from text, and physiology as measured by wearables.

Facial expressions are a form of nonverbal communication. Various studies have been done for the classification of these facial expressions. There is strong evidence for the universal facial expressions of seven emotions which include: neutral happy, sadness, anger, disgust, fear, and surprise. So it is very important to detect these emotions on the face as it has wide applications in the field of Computer Vision and Artificial Intelligence. These fields are researching on the facial emotions to get the sentiments of the humans automatically. Problem Statement

The Indian education landscape has been undergoing rapid changes for the past 10 years owing to the advancement of web-based learning services, specifically, eLearning platforms. Global E-learning is estimated to witness an 8X over the next 5 years to reach USD 2B in 2021. India is expected to grow with a CAGR of 44% crossing the 10M users mark in 2021. Although the market is growing on a rapid scale, there are major challenges associated with digital learning when compared with brick and mortar classrooms. One of many challenges is how to ensure quality learning for students. Digital platforms might overpower physical classrooms in terms of content quality but when it comes to understanding whether students are able to grasp the content in a live class scenario is yet an open-end challenge. In a physical classroom during a lecturing teacher can see the faces and assess the emotion of the class and tune their lecture accordingly, whether he is going fast or slow. He can identify students who need special attention. Digital classrooms are conducted via video telephony software program (ex- Zoom) where it’s not possible for medium scale class (25-50) to see all students and access the mood. Because of this drawback, students are not focusing on content due to a lack of surveillance. While digital platforms have limitations in terms of physical surveillance but it comes with the power of data and machines which can work for you. It provides data in the form of video, audio, and texts which can be analyzed using deep learning algorithms. Deep learning backed system not only solves the surveillance issue, but it also removes the human bias from the system, and all information is no longer in the teacher’s brain rather translated in numbers that can be analyzed and tracked. We will solve the above-mentioned challenge by applying deep learning algorithms to live video data.The solution to this problem is by recognizing facial emotions.

Dataset Information

The data comes from the past Kaggle competition “Challenges in Representation Learning: Facial Expression Recognition Challenge”: we have defined the image size to 48 so each image will be reduced to a size of 48x48.The faces have been automatically registered so that the face is more or less centered and occupies about the same amount of space in each image. Each image corresponds to a facial expression in one of seven categories (0=Angry, 1=Disgust, 2=Fear, 3=Happy, 4=Sad, 5=Surprise, 6=Neutral). The dataset contains approximately 36K images. Dataset link - https://www.kaggle.com/msambare/fer2013

Emotion detection Recognition using deep learning(CNN MODEL)

CNN with the following global architecture:

4 convolutional layers
2 fully connected layers
Basic CNN architecture details:

Input layer - Input layer in CNN should contain image data.
convolutional layer - convolutional layer is sometimes called feature extractor layer because features of the image are get extracted within this layer
Pooling layer - Pooling is used to reduce the dimensionality of each features while retaining the most important information. It is used between two convolution layer
Fully CL - Fully connected layer involves weights, biases, and neurons. It connects neurons in one layer to neurons in another layer. It is used to classify images between different category by training and placed before the output layer
Output Layer - Output layer contains the label which is in the form of one-hot encoded
Classic NNs are usually composed of several fully connected layers. This means that every node of one layer is connected to all the nodes of the next layer. Convolutional Neural Networks also have Convolutional layers that apply sliding functions to groups of pixels that are next to each other. There are two main parts to a CNN architecture- A convolution tool that separates and identifies the various features of the image for analysis in a process called as Feature Extraction A fully connected layer that utilizes the output from the convolution process and predicts the class of the image based on the features extracted in previous stages. This was the model structure. In the output layer there were 7 nodes. Dependencies

Python 3 Tensorflow-CPU Keras Opencv Streamlit Streamlit-Webrtc

Front-end using Streamlit We have created front-end using Streamlit for webapp and used streamlit-webrtc which helped to deal with real-time video streams. Image captured from the webcam is sent to VideoTransformer function to detect the emotion. Then this model was deployed on heroku platform with the help of buildpack-apt which is necessary to deploy opencv model on heroku. But heroku platform only allows model size as 500 mb. And tensorflow 2.0 itself takes 420 mb so we replaced it with tensorflow-cpu. All the other packages used and their version can be found in requirements.txt Our final model was of 496.6 mb and it was successfully deployed but the live stream itself takes 250-300 mb while loading live-stream or opening the webcam. And hence the webcam was not loading or opening and our model was not giving expected output. Due to size concern we use less size model which was stopped early nearly at 23-25 epochs and gives us the accuracy of 60-65%. And the model is performing well.

Deployment

STREAMLIT CLOUD : Introduction
Emotion recognition is the process of identifying human emotion. People vary widely in their accuracy at recognizing the emotions of others. Use of technology to help people with emotion recognition is a relatively nascent research area. Generally, the technology works best if it uses multiple modalities in context. To date, the most work has been conducted on automating the recognition of facial expressions from video, spoken expressions from audio, written expressions from text, and physiology as measured by wearables.

Facial expressions are a form of nonverbal communication. Various studies have been done for the classification of these facial expressions. There is strong evidence for the universal facial expressions of seven emotions which include: neutral happy, sadness, anger, disgust, fear, and surprise. So it is very important to detect these emotions on the face as it has wide applications in the field of Computer Vision and Artificial Intelligence. These fields are researching on the facial emotions to get the sentiments of the humans automatically. Problem Statement

The Indian education landscape has been undergoing rapid changes for the past 10 years owing to the advancement of web-based learning services, specifically, eLearning platforms. Global E-learning is estimated to witness an 8X over the next 5 years to reach USD 2B in 2021. India is expected to grow with a CAGR of 44% crossing the 10M users mark in 2021. Although the market is growing on a rapid scale, there are major challenges associated with digital learning when compared with brick and mortar classrooms. One of many challenges is how to ensure quality learning for students. Digital platforms might overpower physical classrooms in terms of content quality but when it comes to understanding whether students are able to grasp the content in a live class scenario is yet an open-end challenge. In a physical classroom during a lecturing teacher can see the faces and assess the emotion of the class and tune their lecture accordingly, whether he is going fast or slow. He can identify students who need special attention. Digital classrooms are conducted via video telephony software program (ex- Zoom) where it’s not possible for medium scale class (25-50) to see all students and access the mood. Because of this drawback, students are not focusing on content due to a lack of surveillance. While digital platforms have limitations in terms of physical surveillance but it comes with the power of data and machines which can work for you. It provides data in the form of video, audio, and texts which can be analyzed using deep learning algorithms. Deep learning backed system not only solves the surveillance issue, but it also removes the human bias from the system, and all information is no longer in the teacher’s brain rather translated in numbers that can be analyzed and tracked. We will solve the above-mentioned challenge by applying deep learning algorithms to live video data.The solution to this problem is by recognizing facial emotions.

Dataset Information

The data comes from the past Kaggle competition “Challenges in Representation Learning: Facial Expression Recognition Challenge”: we have defined the image size to 48 so each image will be reduced to a size of 48x48.The faces have been automatically registered so that the face is more or less centered and occupies about the same amount of space in each image. Each image corresponds to a facial expression in one of seven categories (0=Angry, 1=Disgust, 2=Fear, 3=Happy, 4=Sad, 5=Surprise, 6=Neutral). The dataset contains approximately 36K images. Dataset link - https://www.kaggle.com/msambare/fer2013

Emotion detection Recognition using deep learning(CNN MODEL)

CNN with the following global architecture:

4 convolutional layers
2 fully connected layers
Basic CNN architecture details:

Input layer - Input layer in CNN should contain image data.
convolutional layer - convolutional layer is sometimes called feature extractor layer because features of the image are get extracted within this layer
Pooling layer - Pooling is used to reduce the dimensionality of each features while retaining the most important information. It is used between two convolution layer
Fully CL - Fully connected layer involves weights, biases, and neurons. It connects neurons in one layer to neurons in another layer. It is used to classify images between different category by training and placed before the output layer
Output Layer - Output layer contains the label which is in the form of one-hot encoded
Classic NNs are usually composed of several fully connected layers. This means that every node of one layer is connected to all the nodes of the next layer. Convolutional Neural Networks also have Convolutional layers that apply sliding functions to groups of pixels that are next to each other. There are two main parts to a CNN architecture- A convolution tool that separates and identifies the various features of the image for analysis in a process called as Feature Extraction A fully connected layer that utilizes the output from the convolution process and predicts the class of the image based on the features extracted in previous stages. This was the model structure. In the output layer there were 7 nodes. Dependencies

Python 3 Tensorflow-CPU Keras Opencv Streamlit Streamlit-Webrtc

Front-end using Streamlit We have created front-end using Streamlit for webapp and used streamlit-webrtc which helped to deal with real-time video streams. Image captured from the webcam is sent to VideoTransformer function to detect the emotion. Then this model was deployed on heroku platform with the help of buildpack-apt which is necessary to deploy opencv model on heroku. But heroku platform only allows model size as 500 mb. And tensorflow 2.0 itself takes 420 mb so we replaced it with tensorflow-cpu. All the other packages used and their version can be found in requirements.txt Our final model was of 496.6 mb and it was successfully deployed but the live stream itself takes 250-300 mb while loading live-stream or opening the webcam. And hence the webcam was not loading or opening and our model was not giving expected output. Due to size concern we use less size model which was stopped early nearly at 23-25 epochs and gives us the accuracy of 60-65%. And the model is performing well.

Deployment

CONCLUSION

Model is giving an accuracy of 68% and validation accuracy of 64% .It is robust in that it works well even in a dim light environment.
The application is able to detect face location and predict the right expression while checking it on a local webcam.
The front-end of the model was made using streamlit for webapp and running well on local webapp link.
Successfully deployed the Streamlit WebApp on Heroku and Streamlit Cloud , that runs on a web server.
