# Project: Web Scraping and Natural Language Processing for Film Reviews

---

## Introduction:
This project comprises two primary tasks: Web Scraping utilizing Beautifulsoup4 and Natural Language Processing (NLP) leveraging Machine Learning algorithms. The web scraping component involves extracting data from user reviews of the iconic film "Forrest Gump" from the IMDB platform (accessible via this link: [IMDB Forrest Gump Reviews](https://www.imdb.com/title/tt0109830/reviews)). It's crucial to note that I am still relatively novice in web development and HTML, hence there might be instances where my language or terminology usage deviates from standardized conventions.

## Motivation:
The rationale behind conducting this analysis is primarily as an exercise to practice web scraping and NLP techniques on my favorite movie.

## Repository Structure:
- **Dataset Folder:**
  - **Splited_Dataset Subfolder:**
    - **data.csv**
    - **data_val.csv**
  - **ForrestGump_reviews.csv**
  - **ForrestGump_reviews1.csv**
- **Scraping Folder:**
  - **IMDB Forrest Gump.ipynb**
  - **Simple 1st data.ipynb**
  - **Split_dataset.ipynb**
- **Analisis_Review.ipynb**
- **Other Files:**
  - **README.md**

## Analysis Method:
The data scraping results are stored in CSV files and further split to ensure the utilization of clean datasets without missing values. The dataset is then divided into training and testing sets with a ratio of 0.2 for training. Prior to training, the star ratings are mapped into three categories: 0-3 for negative, 4-7 for neutral, and 8-10 for positive. Additionally, stop words are removed.

## Parameters:
- **vocab_size**: 10000
- **max_length**: 100
- **embedding_dim**: 200
- **trunc_type**: 'post'
- **oov_tok**: "<OOV>"

## Considerations:
Parameter selection, particularly the max length and vocab size, is crucial due to the substantial content of the dataset, necessitating large matrices.

## Model Configuration:
- **Loss Function**: 'sparse_categorical_crossentropy' for multiclass classification.
- **Final Training Results (Epoch 10/10):**
  - Loss: 0.0335
  - Sparse Categorical Accuracy: 0.9907
  - Validation Loss: 0.5276
  - Validation Sparse Categorical Accuracy: 0.8721

## Word Embeddings Visualization:
The final step involves visualizing word embeddings using the following link: [TensorFlow Projector](https://projector.tensorflow.org/). You can download the files from the following link for visualization: [TSV File](https://drive.google.com/drive/folders/1oyENkkB3_0_Nw-F_T1KxcgacQ6e8oyWo?usp=sharing).

https://github.com/Alanjamlu34/Web-Scraping-IMDB-Movie-Reviews/assets/142156489/8353cd60-ee9d-4b2e-8b0e-c12bda5e5501

> [!CAUTION]
> When running on your local machine, you might encounter some error on building model. To avoid this, I reccomend to use Python 3.11.
