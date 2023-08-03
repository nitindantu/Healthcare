# Introduction
Diabetic retinopathy (DR) is one of the leading causes of vision loss. According to a recent study from International Diabetes Federation, the global prevalence of DR among the individuals with diabetes for the period from 2015 to 2019 was at more than 25%. According to the World Health Organization, more than 300 million people worldwide have diabetes, and the disease prevalence has been rising rapidly in developing countries.

     Early detection and treatment are crucial steps towards preventing DR. Currently, detecting DR is a time-consuming process. The screening procedure requires a trained clinical expert to examine the fundus photographs of the patient’s retina. This creates delays in diagnosis and treatment of the disease. Automated evaluation of retina photographs can speed up the efficiency and coverage of the DR screening programs. This is especially relevant for developing countries, which often lack qualified medical stuff to perform the diagnosis.

# Description 
The project aims at developing a deep learning model for predicting the severity of DR disease based on the patient’s retina photograph. Previous research has explored the usage of deep learning for detecting DR and concluded that convolutional neural networks (CNNs) have high potential in this task. 

# Preprocessing
- Reducing lighting-condition effects: Images come with many different lighting conditions, some images are very dark and difficult to visualize. We can try to convert the image to gray scale, and visualize better. Alternatively, there is a better approach. We can try the method of Ben Graham.
- Cropping uninformative area
## Comparing unprocessed vs preprocessed 
![image](https://github.com/nitindantu/Healthcare/assets/41870240/5bba5567-45f7-48ba-83a5-8df88387b15b)

![image](https://github.com/nitindantu/Healthcare/assets/41870240/ec9110e3-acdd-4359-ac73-ca0f0d84b1e4)


