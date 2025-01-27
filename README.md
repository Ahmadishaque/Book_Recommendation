# Scalable Book Recommendation System: Optimized Cosine Similarity Computation for Large Sparse Datasets

## Overview
This project demonstrates the implementation of a highly efficient and scalable book recommendation system. It leverages an optimized cosine similarity computation for processing large sparse datasets, addressing memory constraints and computational bottlenecks encountered in traditional methods.

The recommendation system is designed to analyze a user-book ratings dataset with over **100,000 users** and **270,000 books**, providing personalized book recommendations based on user similarity. The project is implemented in Python with vectorized operations to handle sparse matrices efficiently.

---

## Key Features

- **Optimized Cosine Similarity Computation:**
  - Reimplemented cosine similarity computation using vectorized operations to reduce memory usage and improve scalability.
  - Limited calculations to non-zero indices of user vectors, significantly reducing unnecessary computations.

- **Personalized Recommendations:**
  - Identifies the top-K similar users for each target user.
  - Suggests the top-rated books by similar users that the target user has not yet read.

- **Efficient Sparse Data Processing:**
  - Processes large user-book matrices stored in sparse formats to optimize memory consumption.
  - Converts sparse data to dense formats only for relevant computations.

- **Scalability:**
  - Capable of processing datasets containing millions of user-book interactions.
  - Designed for future integration with distributed systems or cloud platforms for even larger-scale operations.

---

## Dataset

The project uses two main datasets:

1. **User-Book Ratings Matrix:**
   - Stored in sparse format (e.g., LIBSVM format).
   - Contains user ratings for various books.

2. **Books Metadata:**
   - CSV file containing book details, such as ISBN, title, and author.

Example of book data:

| ISBN           | Title                      | Author           |
|----------------|----------------------------|------------------|
| 9781234567890  | Example Book Title 1       | Author Name 1    |
| 9780987654321  | Example Book Title 2       | Author Name 2    |

---

## Project Structure

```
.
├── notebooks
│   └── ProjectGroup17_IFT511.ipynb   # Jupyter Notebook with implementation
├── data
│   ├── UserBookMatrix.libsvm         # Sparse matrix in LIBSVM format
│   └── Books.csv                     # Metadata for books
├── output
│   └── Book_Recommendations.csv      # Final recommendations
├── README.md                         # Project documentation
└── LICENSE                           # License information
```

---

## Installation and Requirements

### Prerequisites
Ensure you have the following installed:

- Python 3.8+
- Required Python libraries:
  - `pandas`
  - `numpy`
  - `scikit-learn`

### Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/your_username/scalable-book-rec-system.git
   cd scalable-book-rec-system
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Place the `UserBookMatrix.libsvm` and `Books.csv` files in the `data/` directory.

4. Run the Jupyter notebook for the implementation:
   ```bash
   jupyter notebook notebooks/ProjectGroup17_IFT511.ipynb
   ```

---

## Methodology

1. **Data Preprocessing:**
   - Convert the sparse user-book matrix to a dense format only for relevant computations.
   - Reverse mappings for users and books for readability.

2. **Optimized Similarity Calculation:**
   - Compute cosine similarity only for non-zero indices of the target user's vector.
   - Use vectorized operations for faster computation.

3. **Recommendation Generation:**
   - Identify the top-K similar users for each target user based on cosine similarity.
   - Suggest books with the highest weighted average ratings from these similar users.

4. **Output:**
   - Save the recommendations as a CSV file (`output/Book_Recommendations.csv`).

---

## Results
The system efficiently handles large datasets, generating personalized recommendations while avoiding memory crashes. The optimized similarity computation reduces RAM usage and improves processing speed.

---

## Future Work

- **Integration with Distributed Systems:**
  - Adapt the implementation for distributed frameworks like Apache Spark for handling even larger datasets.

- **Enhanced Recommendation Models:**
  - Experiment with hybrid recommendation systems by incorporating content-based filtering and deep learning models.

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

## Author
**[Your Name]**  
Master's Student, Arizona State University  
Feel free to connect via [LinkedIn](https://linkedin.com/in/your-profile) or explore more projects on [GitHub](https://github.com/your_username).
