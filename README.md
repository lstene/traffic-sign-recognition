# **Project Overview**

### **Objective**

In this study, I aim to develop convolutional neural network (CNN) models tailored to accurately classify traffic signs in Ecuador. By focusing on region-specific training data, my goal is to enhance the precision and robustness of traffic sign recognition systems under diverse conditions. This research could significantly contribute to the safety and efficiency of autonomous and assisted driving technologies in Ecuador, fostering their wider adoption in the local market. My models will be trained to recognize traffic signs in various scenarios, including different weather patterns and potential alterations caused by environmental factors or human interference.
This project develops deep learning models for traffic sign recognition in Ecuador. Using CNNs, it improves recognition of ‘Stop,’ ‘Yield,’ traffic lights, and speed limits. A dataset of 5322 images was created, and a regularized CNN achieved 91% accuracy on validation data, highlighting the value of robust datasets and regularization.

### **Tools and Methodologies**

Data analysis was conducted using Python for statistical computations and for visualizations. TensorFlow and Keras libraries were used along with Python for developing and training the CNN models. The methodologies included neural networks, CNNs with and without regularization. To guide the study CRISP-DM was used as reference.

# **The Approach and Process**

### **Data Collection**

The first step was gathering quantitative images on traffic-signs of Stop, Yield, speed limits and traffic lights. As this kind of images were limited in Ecuador it was decided to use traffic signs from other countries that have similar shapes that the one in Ecuador. The datasets was formed from [Kaggle](https://www.kaggle.com/datasets/andrewmvd/road-sign-detection/code) and [RoboFlow](https://universe.roboflow.com/tesis-lhuim/trafficsignalsmobilenetv2/browse?queryText=&pageSize=50&startingIndex=0&browseQuery=true). Also there were images taken locally from Google Maps and web scrapped from Google Images

### **Exploratory Analysis**

The images were reviewed individually in order to determine which one fitted the study. The left images were uploaded to Python as  training and test datasets. 

### Data preparation

The exploratory analysis left the final dataset in a total of 5722 images. From this 5322 were used for training and validation. 400 served as testing. All the training-validation images were modified with data augmentation techniques for better training of the models.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ffd29d6c-74da-4c04-b4b4-a11f5a89a3a9/0c2af46c-a0c2-4d9b-9e48-582fb31880c3/Untitled.png)

## Modeling

### CNN with regularization

This last model outperforms the other two. It includes dropout and regularization layers that help the model prevent overfit. This one achieves a 0.91 precision

### **Challenges and Solutions**

One significant challenge was the lack of images available in Ecuador, specially for Stop and Yield. For that, there were used images from other countries similar to train the model and then test it with local signs. Also overfitting was a problem for the model in its first training. For that data augmentation play a key role giving more variety to the dataset. 

### Evaluation and predictions

Here are a few predictions made by the model and the metrics it had after evaluation

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ffd29d6c-74da-4c04-b4b4-a11f5a89a3a9/e6a560f9-7ba5-4ea6-85f0-bbbd9a7fb677/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ffd29d6c-74da-4c04-b4b4-a11f5a89a3a9/a6a21922-9477-49ce-ba80-ebe0ac82d57c/Untitled.png)

# **End Results and Recommendations**

### **Reflections**

After analyzing the cycle iteration, we found that the training time for the regularized convolutional model was significant, taking approximately twelve hours. For future iterations, utilizing different hardware configurations may prove beneficial. While the TPU outperformed the standard graphics cards available on Google Colab, evaluating the performance of other GPUs, such as the NVIDIA A1000, could offer further improvements. Additionally, the data-loading process was notably time-consuming. A more efficient approach would involve loading the image dataset into Google Drive, storing it there, and accessing it directly from the cloud. This method would mitigate the issues associated with the volatile execution environment and potentially reduce data loading times.

### **Next Steps**

Based on the previous results, several considerations should be considered.

- First, more images are needed across all classes to provide the model with more data to learn from. This increase in data will enhance the model's ability to generalize and improve its performance.
- The current parameters yielded positive results, suggesting that these settings are adequate. Therefore, no modifications to these parameters are necessary for the next iteration.
- Finally, given the model's growth trend, extending the training to more epochs could help it reach its maximum potential. This additional training time will allow the model to refine its learning further and improve accuracy.

Implementing these considerations optimizes the model's performance, leading to more robust results in future iterations.

### **Conclusion**

This study has successfully demonstrated the development and evaluation of deep learning models, specifically convolutional neural networks (CNNs), for traffic sign recognition tailored to the unique characteristics of Ecuadorian traffic signs. The models were trained and validated on a diverse dataset, including public and manually collected images, resulting in a comprehensive database. Our regularized CNN model achieved a commendable precision of 91% on validation data and 81% on test data, highlighting its robustness and generalizability.
The findings underscore the importance of using region-specific data and advanced data augmentation techniques to enhance model performance and mitigate overfitting. Additionally, our study highlights the critical role of regularization in preventing overfitting and improving model reliability.
Despite the positive results, the study faced limitations, such as the narrow scope of traffic sign categories and the small dataset size. Future research should focus on expanding the dataset to include a wider variety of traffic signs and collecting more data to improve model generalization. Optimizing training and evaluation using advanced hardware configurations and exploring advanced deep learning techniques, such as transfer learning, are also recommended.
Testing the models in real-world driving conditions is essential to assess their practical usability and effectiveness. By addressing these areas, future research can further realize the full potential of AI-driven traffic sign recognition systems, enhancing the safety and reliability of autonomous and assisted driving technologies in Ecuador and beyond.

For a deeper dive into the methodologies and data, the project's GitHub repository is available at [GitHub Repository](https://github.com/lstene/traffic-sign-recognition).
