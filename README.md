# NLP-Based Product Recommender System in Django

This is a Django-based Product Recommendation System that suggests similar products when a user clicks on a particular product. The system utilizes Natural Language Processing (NLP) techniques to analyze product descriptions and recommend similar items.

It follows a content-based filtering approach, where product similarity is computed based on text embeddings. However, this implementation requires precomputing similarity scores, making it not scalable for large datasets.

---

## Technologies Used
- Django (for backend and API)
- NLP (TF-IDF or Word Embeddings) (to compute similarity)
- Pandas & NumPy (for data processing)
- SQLite (as the default database)

---

## Features
✅ **Product Listing Page** - Displays all available products.

✅ **Recommendation System** - Suggests similar products based on text similarity.

✅ **API for Recommendations** - Provides product recommendations through an API endpoint.

✅ **Simple UI** - Users can browse and get recommendations visually.

---

## Screenshots
### 1. **All Products Page**:
   ![All Products](https://github.com/PrathameshPC77/django_nlp_recommender/blob/main/all_products.png)

### 2. **Recommended Products Page**:
   ![Recommended Products](https://github.com/PrathameshPC77/django_nlp_recommender/blob/main/similar_products.png)

---

## How It Works
1. **Dataset**: The system uses a dataset of products with attributes like name, description, and category.
2. **NLP Algorithm**: The product descriptions are processed using NLP techniques (e.g., TF-IDF, cosine similarity) to find similar products.
3. **Django Models**: The products and their relationships are stored in Django models.
4. **API**: An API endpoint is created to fetch recommendations for a given product.
5. **UI**: A simple frontend displays the products and their recommendations.

---

## Installation & Setup
#### 1. Clone the repository
    git clone https://github.com/yourusername/repo-name.git  
    cd repo-name  

#### 2. Create virtual environment (Skip if already created)
    python -m venv venv  
    source venv/bin/activate  # On Windows use: venv\Scripts\activate  

#### 3. Install dependencies  
    pip install -r requirements.txt  

#### 4. Run migrations  
    python manage.py migrate  

#### 5. Start the server  
    python manage.py runserver  

---

## How the Recommendation Works
1. **Preprocessing:** Product descriptions are vectorized using NLP techniques like TF-IDF.
2. **Similarity Computation:** Each product is compared with others using cosine similarity.
3. **Precomputed Storage:** Similar product scores are stored in the database to speed up recommendations.
4. **Recommendation API:** When a user clicks a product, the system fetches similar products using the precomputed scores.

---

## Limitations & Scalability Issues
⚠ **Not Scalable** – Currently, similarity scores are precomputed, meaning if new products are added, all values must be recalculated.

⚠ **Cold Start Problem** – New products have no recommendations until scores are updated.

⚠ **Database Load** – Storing all similarity scores increases storage usage.

---

## Future Improvements
🔹 Implement real-time similarity calculations instead of precomputing.

🔹 Use vector databases (e.g., FAISS or Annoy) for faster recommendations.

🔹 Improve database efficiency with better indexing techniques.

---

## Future Improvements
- Implement a more scalable algorithm (e.g., matrix factorization or deep learning-based recommendations).
- Use a distributed system (e.g., Apache Spark) for handling large datasets.
- Add user authentication and personalized recommendations.

---

## References
- [Kaggle](https://www.kaggle.com/datasets/PromptCloudHQ/flipkart-products)
- [YouTube Video](https://www.youtube.com/watch?v=eGHN3XvBBv8)

---

## Contributing
Feel free to contribute! Fork the repo and submit a PR.

---

## License
This project is licensed under the MIT License. See the LICENSE file for details.
