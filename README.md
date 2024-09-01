

# Million Songs Dataset - Recommendation Engine

## Overview

This project involves building a music recommendation engine using the **Million Songs Dataset**. The goal is to develop a system that can recommend songs to users based on their listening history, leveraging collaborative filtering techniques and content-based filtering methods.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Data Preprocessing](#data-preprocessing)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Dataset

The **Million Songs Dataset** is a freely available collection of audio features and metadata for a million contemporary popular music tracks. The dataset does not include any audio, but instead provides metadata and features extracted from the music.

The dataset includes the following types of data:

- **Song Metadata:** Information about the songs including title, artist, year, and duration.
- **User Data:** Information about user interactions with songs, such as play counts and user IDs.
- **Audio Features:** Numerical data representing various audio features like tempo, key, loudness, etc.

You can download the dataset and access it via the [official website](http://millionsongdataset.com/) or by using the preprocessed datasets available in the repository.

## Project Structure

```bash
├── data
│   ├── million_songs.csv                 # Main dataset file
├── notebooks
│   ├── Data_Preprocessing.ipynb          # Jupyter notebook for data preprocessing
│   ├── Recommendation_Modeling.ipynb     # Jupyter notebook for model development
├── models
│   ├── recommendation_model.pkl          # Saved trained recommendation model
├── README.md                             # Project README file
└── requirements.txt                      # Python packages required
```

## Installation

To run this project locally, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/million-songs-recommendation-engine.git
   cd million-songs-recommendation-engine
   ```

2. Create and activate a virtual environment (optional but recommended):

   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows use `venv\Scripts\activate`
   ```

3. Install the required Python packages:

   ```bash
   pip install -r requirements.txt
   ```

4. Download the Million Songs Dataset and place it in the `data/` directory if it's not already included.

## Data Preprocessing

Data preprocessing is a key step in building the recommendation engine. It involves:

- **Handling Missing Values:** Checking for and addressing any missing values in the dataset.
- **Feature Engineering:** Creating additional features from the raw data that can be useful for the recommendation engine.
- **Normalization:** Scaling the data to ensure that features contribute equally to the model.
- **Splitting Data:** Dividing the dataset into training and testing sets for model evaluation.

## Modeling

The project explores multiple approaches to build the recommendation engine:

1. **Collaborative Filtering:** 
   - **User-User Collaborative Filtering:** Recommends songs to users based on the preferences of similar users.
   - **Item-Item Collaborative Filtering:** Recommends songs similar to the ones a user has already liked.

2. **Content-Based Filtering:** 
   - Recommends songs based on the content of the songs (e.g., genre, artist, tempo) and the user's previous interactions.

3. **Matrix Factorization:** 
   - Techniques like Singular Value Decomposition (SVD) to reduce dimensionality and capture latent factors for better recommendations.

4. **Hybrid Models:** 
   - Combines collaborative filtering and content-based methods to improve the recommendation quality.

## Evaluation

The models are evaluated using metrics specific to recommendation systems:

- **Precision@K:** Measures the proportion of recommended songs in the top K that are relevant.
- **Recall@K:** Measures the proportion of relevant songs recommended out of all relevant songs available.
- **Mean Average Precision (MAP):** A measure that considers the precision at every position in the ranked list of recommendations.
- **Root Mean Squared Error (RMSE):** For models that predict user ratings.

## Results

- The best-performing model achieved a precision of **X%** and recall of **Y%** at K=10.
- Hybrid models generally performed better than individual approaches, combining the strengths of collaborative filtering and content-based filtering.

*Note: Replace **X%** and **Y%** with the actual results from your model.*

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please feel free to create a pull request or open an issue.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

