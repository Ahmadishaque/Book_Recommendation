Book Recommendation System
Overview
This project is a collaborative filtering-based book recommendation system built on a dataset of approximately 270,000 books and 105,000 users. The system efficiently suggests personalized book recommendations using advanced similarity computation and recommendation algorithms.

Key Features
Optimized Similarity Computation: Implements a custom cosine similarity function using vectorized operations for scalability, addressing memory constraints in handling large datasets.
Sparse Data Handling: Transforms and processes a large sparse user-book matrix efficiently, avoiding memory overloads typical of dense matrix operations.
Personalized Recommendations: Generates top-5 book suggestions for each user by leveraging user preferences and collaborative filtering techniques.
Scalable and Efficient: Designed to handle high-dimensional data with a focus on computational efficiency and memory management.
Highlights
Performance Optimization:

Replaced scikit-learn’s cosine similarity function with a custom implementation to optimize memory usage and computation speed.
Focused on non-zero indices to reduce unnecessary calculations for zero entries in the user-book matrix.
Recommendation Algorithm:

Identifies top-K similar users for each target user.
Calculates weighted average ratings for potential recommendations, considering user similarity scores.
Suggests top-5 books based on estimated ratings for unread books.
Technology Stack:

Languages: Python (Pandas, NumPy)
Libraries: Custom cosine similarity implementation, data handling with Pandas, and matrix operations with NumPy.
Dataset: Extensive book and user data, including ratings, sourced from a real-world library dataset.
Installation and Usage
Prerequisites
Python 3.8+
Libraries: Pandas, NumPy, scikit-learn
Setup Instructions
Clone the repository:
bash
Copy
Edit
git clone https://github.com/YourGitHubUsername/Book-Recommendation-System.git
cd Book-Recommendation-System
Install dependencies:
bash
Copy
Edit
pip install -r requirements.txt
Run the main script:
bash
Copy
Edit
python recommend_books.py
Input Files
UserBookMatrix.libsvm: The sparse user-book matrix file in SVMLight format.
Books.csv: Metadata of books, including ISBN and title.
Output
Book_Recommendations.csv: The final file containing user-specific book recommendations with titles and scores.
How It Works
Preprocessing:

Converts the sparse matrix into a dense format for relevant operations.
Maps user and book IDs for easy lookup during recommendations.
Similarity Computation:

Computes similarity scores only for non-zero indices to minimize computation overhead.
Handles edge cases (e.g., division by zero) using robust error handling.
Recommendation Generation:

Identifies books rated by similar users but unread by the target user.
Calculates estimated ratings for each candidate book using a weighted average formula.
Output Generation:

Saves top-5 recommendations per user in a CSV format, including book titles and recommendation scores.
Results
Efficiently generated personalized recommendations for over 105,000 users.
Solved scalability and memory issues typical of large recommendation systems.
Future Improvements
Extend the system to support dynamic updates (e.g., new ratings or books).
Incorporate advanced algorithms like matrix factorization or deep learning-based recommenders for enhanced accuracy.
Build a web-based user interface for live interaction with the system.
License
This project is open-source and available under the MIT License.

Contact
If you have any questions or suggestions, feel free to reach out:

Email: aikarimi@asu.edu
GitHub: [YourGitHubProfile](https://github.com/Ahmadishaque)
Pro Tip for Recruiters: This project demonstrates my ability to handle big data challenges, optimize machine learning workflows, and deliver scalable solutions for real-world recommendation systems.


