• Data Acquisition & Merging:

Loaded movie metadata and credits from online CSV files using Pandas.
Merged the two datasets on the common movie identifiers to create a unified DataFrame for further analysis.
• Exploratory Data Analysis (EDA):

Inspected dataset structures, data types, and checked for missing or extreme values in both movies and credits datasets.
• Feature Encoding:

Parsed JSON strings in columns such as cast, keywords, and genres to extract relevant names.
Employed both loop-based and lambda-based methods for encoding, demonstrating the benefits of concise lambda functions over explicit loops.
• Feature Engineering:

Created a new combined_features column by concatenating the processed genres, keywords, cast, and overview fields to build a comprehensive textual representation for each movie.
• Text Vectorization:

Utilized the TfidfVectorizer from Scikit-learn to transform the combined textual features into a TF-IDF feature matrix, effectively converting text data into numerical vectors.
• Model Training & Recommendation Engine:

Trained a K-Nearest Neighbors (KNN) model using cosine similarity on the TF-IDF feature matrix to identify movies with similar content.
Developed a recommendation function that takes a movie title (e.g., "The Dark Knight") and returns the top similar movies along with their similarity distances.
• Demonstration of Recommendations:

Generated and displayed movie recommendations (e.g., "The Dark Knight Rises", "Batman Returns") along with the corresponding cosine distance scores to showcase the recommender system's effectiveness.
• Model Serialization & Deployment:

Saved the trained KNN model, the TF-IDF feature matrix, and the processed dataset using pickle for future use.
Created necessary directories to store these artifacts and demonstrated loading them back into the environment, ensuring reproducibility and ease of deployment.
