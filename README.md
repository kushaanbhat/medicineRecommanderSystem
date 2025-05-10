# Medical Diagnosis and Recommendation System Documentation

## Academic Report

### Abstract

This report documents the development of a medical diagnosis and recommendation system implemented using Flask, Pandas, NumPy, and a pre-trained Support Vector Classifier (SVC) model. The system takes a list of symptoms as input and predicts the most likely disease. Based on the predicted disease, it provides a detailed description of the disease, precautions to take, recommended medications, dietary suggestions, and workout recommendations.  This project aims to provide a user-friendly interface for preliminary self-diagnosis and health management advice. This is not intended to replace consultation with a medical professional.

### Introduction

The increasing demand for accessible and convenient healthcare solutions has led to the development of various online medical diagnosis tools. This project addresses this need by creating a web application that allows users to input their symptoms and receive a potential diagnosis along with relevant health recommendations. The system leverages a pre-trained Support Vector Classifier (SVC) model to predict the disease based on the provided symptoms.  Further, the system integrates information from various datasets to offer comprehensive advice on managing the identified condition. The Flask framework facilitates the creation of a user-friendly web interface, while Pandas and NumPy enable efficient data handling and processing.

### Methodology

The development of this system involved the following key steps:

1.  **Data Collection and Preprocessing:** Several datasets were compiled and preprocessed:

    *   `symtoms_df.csv`: Contains symptoms associated with various diseases.
    *   `precautions_df.csv`: Provides precautions to be taken for specific diseases.
    *   `workout_df.csv`: Suggests workout routines for different conditions.
    *   `description.csv`: Offers detailed descriptions of each disease.
    *   `medications.csv`: Lists recommended medications for each disease.
    *   `diets.csv`: Provides dietary recommendations for each disease.

    These datasets were cleaned and organized using Pandas to ensure data consistency and accuracy.

2.  **Model Training:** A Support Vector Classifier (SVC) model was trained using a labeled dataset of symptoms and corresponding diseases.  The model was trained offline, and the trained model (`svc.pkl`) was loaded into the application. Details on the training process are outside the scope of this documentation as the model was pre-trained.

3.  **Web Application Development:** The Flask framework was used to create a web application with the following functionalities:

    *   A home page where users can input their symptoms.
    *   A prediction endpoint that processes the user's input, predicts the disease, and retrieves relevant information.
    *   An "about" page providing information about the system.

4.  **User Interface Design:** The user interface was designed to be intuitive and user-friendly, allowing users to easily input their symptoms and view the prediction results and recommendations. HTML and CSS were used for the front-end development.

5.  **Integration and Testing:**  The different components of the system were integrated, and thorough testing was conducted to ensure accurate predictions and proper functionality.

### Proposed System

The proposed system is a web-based application that provides a medical diagnosis and recommendation service based on user-provided symptoms.  The system architecture can be visualized as follows:

**Components:**

*   **User Interface:** A web page implemented using HTML templates where users can input their symptoms.
*   **Flask Application:** A Python application using the Flask framework to handle user requests, interact with the prediction model, and render the output.
*   **SVC Model:** A pre-trained Support Vector Classifier model (`svc.pkl`) used for disease prediction based on symptoms.
*   **Data Storage:** CSV files containing information about symptoms, diseases, precautions, medications, diets, and workouts.
*   **Helper Functions:** Python functions to retrieve and format the relevant information based on the predicted disease.

**Workflow:**

1.  The user enters their symptoms through the web interface.
2.  The Flask application receives the symptoms via a POST request.
3.  The application preprocesses the symptoms and converts them into a numerical input vector.
4.  The SVC model predicts the disease based on the input vector.
5.  The application retrieves the disease description, precautions, medications, dietary suggestions, and workout recommendations from the data storage using helper functions.
6.  The application renders the prediction results and recommendations on the web page.

### Expected Results

The system is expected to provide accurate disease predictions based on the user-provided symptoms. Additionally, it should offer helpful and relevant recommendations for managing the predicted condition, including precautions, medications, dietary suggestions, and workout routines.  The user interface is expected to be intuitive and user-friendly, allowing users to easily access and understand the information.

Specifically, the system should achieve the following:

*   **Accuracy:** Provide disease predictions that align with the user's symptoms with reasonable accuracy, given the limitations of self-diagnosis tools.  The accuracy is dependent on the training data used for the SVC model.
*   **Relevance:** Offer recommendations (precautions, medications, diets, workouts) that are directly related to the predicted disease and are helpful for managing the condition.
*   **Usability:**  Provide a user-friendly interface that is easy to navigate and understand, even for users with limited technical skills.
*   **Comprehensive Information:** Display the disease description, precautions, medications, diet, and workout plans clearly and concisely.

**Example Scenario:**

A user enters the following symptoms: "itching, skin\_rash, nodal\_skin\_eruptions".  The system should predict "Fungal infection" and display the corresponding disease description, precautions, medications, dietary recommendations, and workout suggestions from the respective datasets.

### Conclusion

This project presents a medical diagnosis and recommendation system that aims to provide users with preliminary insights into their health conditions and offer relevant recommendations for managing them. The system leverages a pre-trained SVC model, the Flask framework, and various datasets to deliver a user-friendly and informative experience.  While this system is not a substitute for professional medical advice, it can serve as a valuable tool for self-assessment and health management. Future work could involve improving the accuracy of the prediction model, expanding the dataset to include a wider range of diseases and symptoms, and incorporating more personalized recommendations based on user demographics and medical history. Furthermore, the system could be extended to incorporate other functionalities such as appointment scheduling with healthcare professionals.
