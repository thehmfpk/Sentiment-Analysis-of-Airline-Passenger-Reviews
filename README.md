# ✈️ Sentiment Analysis of Airline Passenger Reviews

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![NLP](https://img.shields.io/badge/NLP-Sentiment%20Analysis-green.svg)](https://www.nltk.org/)
[![Machine Learning](https://img.shields.io/badge/ML-Classification-orange.svg)](https://scikit-learn.org/)

##  Business Context
Customer feedback is the backbone of service improvement in the airline industry. This project takes raw, unstructured passenger reviews and transforms them into actionable insights. We focus on British Airways data to determine what makes a flight "recommended" versus "non-recommended".

## Technical Workflow

### 1. Data Processing & EDA
* **Dataset**: 3,701 unique flight reviews including ratings for Seat Comfort, Staff Service, and Ground Service.
* **Cleaning**: Handled missing values in critical columns like `ReviewBody` and removed duplicate entries to ensure data integrity.
* **Feature Engineering**: Extracted sentiment polarity using two distinct methodologies:
    * **TextBlob**: For general linguistic polarity.
    * **VADER (Valence Aware Dictionary and sEntiment Reasoner)**: Specifically tuned for social media and review-style sentiments.

### 2. Machine Learning Pipeline
We converted text data into numerical vectors using **TF-IDF Vectorization** and trained the following models to predict sentiment:
* **Logistic Regression**: A baseline statistical model for high-dimensional text data.
* **K-Nearest Neighbors (KNN)**: A distance-based approach to find similarities between review patterns.

### 3. Visual Insights
The project includes deep-dive visualizations:
* **Sentiment Distribution**: Comparison of VADER vs. TextBlob classification.
* **Service Metrics**: Analysis of how "Value for Money" correlates with the final recommendation.
* **Word Clouds**: Automated generation of top positive and negative keywords (e.g., "friendly staff" vs. "delayed flight").

##  Key Features
* **Dual-Sentiment Analysis**: Provides a more robust view of sentiment by comparing two different NLP libraries.
* **Text Preprocessing**: Includes tokenization and removal of noise from raw passenger feedback.
* **Predictive Power**: Models built to automatically classify future reviews based on historical patterns.

##  Analysis: Pros & Cons
### Pros
* **Granular Detail**: Not just "Positive/Negative," but analyzes specific service aspects like Wifi, Food, and Entertainment.
* **Modular Code**: The pipeline can be easily adapted for other airlines (Ryanair, Qatar Airways, etc.).

### Cons
* **Class Imbalance**: The dataset reflects real-world trends where extreme reviews (1/10 or 10/10) are more common than neutral ones.
* **Hardware Constraints**: Large-scale TF-IDF matrices can be memory-intensive for local machines.

##  Potential Use Cases
1. **Real-time Feedback Monitoring**: Integrate with Twitter/X or TripAdvisor APIs to track brand health.
2. **Competitive Benchmarking**: Compare British Airways' service scores against competitors in the same routes.
3. **Operational Prioritization**: Identify if "Ground Service" or "Seat Comfort" is the primary driver of negative reviews to allocate budgets effectively.

## Repository Structure
* `Sentiment_Analysis.ipynb`: The main Jupyter Notebook containing all code and visualizations.
* `Flight_experience_N3700.csv`: The raw dataset of 3,700 reviews.
* `LICENSE`: Usage terms for this project.
* `README`: INFO for this project.
