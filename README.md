# Natural-Language-Processing-and-Topic-Modelling-on-User-Review-of-Watch

This project aims to analyze customer reviews of watch products using machine learning and natural language processing techniques. By understanding customer sentiments and identifying key themes, the analysis assists in enhancing product features, improving customer satisfaction, and guiding targeted marketing strategies.

---
## **Table of Contents**
- [Project Overview](#project-overview)
- [Dataset](#dataset)
  - [Technologies Used](#technologies-used)
- [Project Workflow](#project-workflow)
- [Key Results](#key-results)
- [Insights](#insights)
- [Recommendations](#recommendations)
- [How to Run](#how-to-run)
- [Future Enhancements](#future-enhancements)

---

## **Project Overview**
Customer reviews provide invaluable insights into product performance, customer satisfaction, and areas needing improvement. This project leverages data preprocessing, text analysis, and machine learning models to uncover patterns and themes within watch product reviews. Techniques such as TF-IDF vectorization, K-Means clustering, and Latent Dirichlet Allocation (LDA) are employed to extract and visualize meaningful information from textual data.

---

## **Dataset**
The dataset used in this project includes the following columns:
- `marketplace`
- `customer_id`
- `review_id`
- `product_id`
- `product_parent`
- `product_title`
- `product_category`
- `star_rating`
- `helpful_votes`
- `total_votes`
- `vine`
- `verified_purchase`
- `review_headline`
- `review_body`
- `review_date`

The dataset contains **960,045** entries, focusing primarily on the `review_body` for textual analysis. A random sample of 1,000 reviews was selected for detailed analysis to ensure computational efficiency while maintaining data diversity.

---

## **Technologies Used**
- **Programming Language:** Python
- **Libraries:**
  - **Data Analysis & Preprocessing:** Pandas, NumPy
  - **Natural Language Processing:** NLTK, SnowballStemmer
  - **Data Visualization:** Matplotlib, Seaborn, WordCloud
  - **Machine Learning:** scikit-learn
- **Jupyter Notebook:** For interactive development and analysis

---

## **Project Workflow**
1. **Data Loading and Cleaning:**
   - Imported necessary libraries.
   - Loaded the dataset into a Pandas DataFrame.
   - Removed entries with missing `review_body`.
   - Selected a random sample of 1,000 reviews for analysis.

2. **Tokenizing and Stemming:**
   - Loaded and extended English stopwords.
   - Utilized NLTK's `SnowballStemmer` to reduce words to their root forms.
   - Tokenized, filtered, and stemmed the review texts.
   - Generated a word cloud to visualize the most frequent terms.
   - Sentimental Analysis: Percentage of Positive Words

3. **TF-IDF Vectorization:**
   - Converted the processed text data into a TF-IDF matrix.
   - Configured the vectorizer to filter out extremely common and rare terms, limit vocabulary size, and use custom tokenization.
   - Produced a sparse matrix representing the importance of terms in each review.

4. **K-Means Clustering:**
   - Applied the Elbow Method to determine the optimal number of clusters, selecting K=15.
   - Clustered the reviews based on their TF-IDF representations.
   - Analyzed the distribution of reviews across clusters and identified dominant themes.

5. **Topic Modeling with LDA:**
   - Employed Latent Dirichlet Allocation to uncover latent topics within the reviews.
   - Configured LDA with 15 topics to align with K-Means clustering.
   - Identified dominant topics for each review and extracted top keywords for interpretation.

---
### **Visualizations**
- **Word Cloud:**
  - Highlighted frequently mentioned terms such as "time," "look," "love," "band," and "great," signifying appreciation for design and functionality.
  - Some negative terms like "problem," "return," and "broke" indicated concerns about durability.

- **Ratings Distribution:**
  - A bar chart showed a majority of **5-star ratings**, suggesting high customer satisfaction.
  - Fewer reviews were observed as ratings decreased, with very few **1-star** to **3-star** reviews.

- **PCA Scatter Plot:**
  - Reduced TF-IDF dimensions to 2D to visualize cluster separations.
  - Clearly marked centroids highlighted distinct groupings within the data.

---

## **Key Results**

### **Model Performance**
- **K-Means Clustering:**
  - Determined **15 clusters** as optimal based on the Elbow Method.
  - **Cluster 14** emerged as the dominant cluster, containing **879 reviews**, indicating prevalent common themes.
  - Smaller clusters captured niche topics such as gifting, quality, and specific product features.

- **LDA Topic Modeling:**
  - Identified **15 distinct topics** reflecting various aspects of watch reviews.
  - Topics encompassed themes like design, gifting occasions, affordability, usability, repair services, and durability

---

## **Insights**
- **Positive Sentiments:**
  - Customers frequently praised the design, functionality, and overall quality of the watches.
  - High satisfaction is evident from the prevalence of positive keywords and high star ratings.

- **Areas for Improvement:**
  - Durability concerns were noted, with some reviews mentioning issues like scratches and mechanical problems.
  - Affordability and value for money were recurring themes, indicating sensitivity to pricing.

- **Gifting Trends:**
  - A significant number of reviews focused on watches as gifts, particularly for occasions like birthdays and Christmas.
  - This highlights the importance of marketing watches as thoughtful and stylish gift options.

- **Customer Engagement:**
  - Active members and customers with multiple products showed lower churn rates, emphasizing the effectiveness of engagement strategies.

---

## **Recommendations**

### **Product Development**
- **Enhance Durability:**
  - Address common durability issues by improving materials and manufacturing processes.
  - Offer extended warranties or repair services to build customer trust.

- **Design Innovations:**
  - Continue to innovate in design to maintain customer interest and satisfaction.
  - Incorporate customer feedback to refine aesthetic and functional features.

### **Marketing Strategies**
- **Targeted Gifting Campaigns:**
  - Develop marketing campaigns focused on gifting occasions, highlighting watches as ideal presents.
  - Offer special promotions or bundles during peak gifting seasons.

- **Value Proposition:**
  - Clearly communicate the value for money, emphasizing quality and unique features to justify pricing.
  - Introduce tiered product lines to cater to different budget segments.

### **Customer Engagement**
- **Loyalty Programs:**
  - Implement loyalty programs to reward repeat customers and encourage multi-product purchases.
  - Offer exclusive benefits or discounts to active members to reduce churn rates.

- **Personalized Services:**
  - Provide personalized recommendations and services based on customer preferences and purchase history.
  - Engage with customers through follow-up communications and feedback requests.

### **Operational Improvements**
- **Responsive Customer Service:**
  - Enhance customer service responsiveness to address issues promptly and effectively.
  - Use feedback from negative reviews to inform service improvements.

- **Localized Strategies:**
  - Investigate region-specific factors contributing to higher churn rates and tailor strategies accordingly.
  - Offer region-specific products or services to better meet local customer needs.

---

## **How to Run**
To replicate this project, follow these steps:

1. **Clone the Repository:**
    ```bash
    git clone https://github.com/YizhouWang0316/NLP-and-Topic-Modelling-on-User-Review-of-Watch.git
    ```

2. **Navigate to the Project Directory:**
    ```bash
    cd NLP-and-Topic-Modelling-on-User-Review-of-Watch
    ```
3. **Run the Jupyter Notebook:**
    Open `watch_reviews_analysis.ipynb` in Jupyter Notebook and execute the cells sequentially.

---

## **Future Enhancements**

- **Interactive Dashboards:**
  - Develop interactive dashboards using tools like Streamlit or Tableau to enable dynamic data exploration and visualization for stakeholders.

- **Scalability:**
  - Expand the analysis to include larger datasets or real-time review data to enhance the robustness and applicability of the findings.

- **Model Optimization:**
  - Experiment with different machine learning algorithms and hyperparameter tuning to improve clustering accuracy and topic coherence.

- **Multilingual Support:**
  - Incorporate reviews in multiple languages to broaden the analysis scope and cater to a more diverse customer base.

---
