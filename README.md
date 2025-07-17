# -RECOMMENDATION-SYSTEM
COMPANY: CODTECH IT SOLUTIONS
NAME: MADANIKA PITTAM
INTERN ID: CT04DG1969
DOMAIN: MACHINE LEARNING
DURATION: 4 WEEKS
MENTOR: NEELA SANTOSH
1. Introduction
Recommendation systems have become an essential part of the digital ecosystem. From e-commerce platforms like Amazon to streaming services such as Netflix, recommendation systems personalize user experience by suggesting products or content aligned with user preferences. This project focuses on building a movie recommendation system using the MovieLens dataset. It applies collaborative filtering techniques, specifically Singular Value Decomposition (SVD), to predict and recommend movies to users based on their past ratings.

The task was completed as part of an internship project to develop hands-on expertise with real-world datasets and machine learning algorithms tailored for recommender systems.

2. Objective
The main objectives of the project were:

To understand and prepare the MovieLens dataset for collaborative filtering.

To apply matrix factorization using SVD for rating prediction.

To evaluate the model's performance using standard metrics such as RMSE and MAE.

To generate personalized movie recommendations for a given user.

3. Dataset Description
The project uses the MovieLens dataset, a widely used benchmark dataset for recommendation system research. The dataset consists of two primary CSV files:

ratings.csv: Contains user ID, movie ID, rating, and timestamp.

movies.csv: Includes movie ID and movie titles.

Each entry in the ratings file represents a user's rating for a specific movie, with values ranging from 0.5 to 5.0. The dataset enables the exploration of user-movie interactions essential for collaborative filtering.

4. Methodology
a. Environment Setup
The project was implemented in Google Colab using Python. Key libraries included:

pandas and numpy for data manipulation.

scikit-surprise (also known as surprise) for building and evaluating recommendation models.

matplotlib for any optional visualizations (though not used heavily in this version).

b. Data Loading and Preprocessing
The datasets ratings.csv and movies.csv were uploaded using Google Colab’s file upload utility.

The ratings data was transformed into the format required by the surprise library using a Reader object.

Only the necessary columns (userId, movieId, rating) were extracted for model training.

c. Train-Test Split
Using surprise.model_selection, the dataset was split into training (80%) and testing (20%) sets. This step ensured that model evaluation was done on unseen data, reflecting real-world performance more accurately.

d. Model Building – SVD (Singular Value Decomposition)
The SVD algorithm is a widely adopted technique in collaborative filtering, especially for sparse user-item interaction matrices. The model attempts to discover latent features for both users and movies that best explain observed ratings.

The model was trained on the training set using model.fit().

After training, predictions were made on the test set to compare predicted ratings with actual ratings.

e. Model Evaluation
Two commonly used metrics were used to evaluate performance:

RMSE (Root Mean Square Error): Measures the square root of the average squared difference between predicted and actual ratings.

MAE (Mean Absolute Error): Measures the average magnitude of errors in predictions.

Lower values for both metrics indicate better performance. These metrics provide a quantitative measure of how well the model is predicting user preferences.

5. Personalized Recommendations
To demonstrate real-world use, the system was used to generate top-5 movie recommendations for a specific user:

All movies already rated by the user were filtered out.

The system predicted ratings for unseen movies.

The top 5 movies with the highest predicted ratings were extracted.

These were then matched with titles from movies.csv to make the output user-friendly.

This personalized list serves as a practical example of the model in action.

6. Tools and Technologies Used
Python: Programming language

Google Colab: Development environment

Pandas, NumPy: Data manipulation

Surprise Library: Model training and evaluation

MovieLens Dataset: Publicly available dataset used for recommender systems

7. Results and Discussion
The SVD-based model produced reliable predictions with RMSE and MAE values typically below 1. This indicates that the model captured user preferences quite well for a simple baseline.

Although the model’s accuracy could be improved with hyperparameter tuning and more sophisticated methods (e.g., hybrid systems or deep learning), it still performed admirably on the provided dataset and was able to produce meaningful recommendations.

8. Conclusion
This project successfully implemented a collaborative filtering-based recommendation system using the MovieLens dataset. The use of the SVD algorithm enabled the model to learn latent factors from sparse user-movie interaction data, leading to accurate predictions. The results proved the practicality of matrix factorization in real-world applications.

Through this hands-on task, key concepts such as data preprocessing, model evaluation, and collaborative filtering were reinforced. The project also showcased the importance of understanding user behavior for building intelligent systems.
