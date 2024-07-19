## Project Overview

This project is part of the Udacity Data Scientist Nanodegree program, in collaboration with IBM. The goal of the project is to build a recommendation system for the IBM Watson Studio platform. We leverage various recommendation techniques, including collaborative filtering and matrix factorization, to suggest articles to users based on their interaction history.

## Project Structure

- **Recommendations_with_IBM.ipynb**: The Jupyter notebook containing all the code and analysis for building and evaluating the recommendation system.
- **data/**: Directory containing the datasets used in the project.
  - `user-item-interactions.csv`
  - `articles_community.csv`
- **Project_tests.py**: Test functions
- **README.md**: This readme file.
- **LICENCE**: MIT Licence
- **Pickel files**: Matrix dataset and test data

## Datasets

The datasets used in this project include:
- **user-item-interactions.csv**: Contains user interactions with articles.
- **articles_community.csv**: Contains details about the articles.
- **user_item_matrix.p**: Pickled user-item interaction matrix for matrix factorization.

## Project Steps

### Part I: Exploratory Data Analysis

We start by exploring the datasets to understand the structure and key statistics, such as the distribution of user interactions and the number of unique users and articles.

### Part II: Rank-Based Recommendations

In this section, we build a recommendation system based on the most popular articles. This method is straightforward and serves as a baseline for comparison with more advanced techniques.

### Part III: User-User Based Collaborative Filtering

Here, we implement collaborative filtering to recommend articles based on the similarity between users. We compute user similarity using the dot product of user-article interaction vectors and recommend articles liked by similar users.

### Part IV: Matrix Factorization

Using Singular Value Decomposition (SVD), we factorize the user-item interaction matrix to capture latent features that explain user-article interactions. This approach helps in handling sparsity and making more personalized recommendations.

### Part V: Evaluation and Improvement

We evaluate the performance of the recommendation systems using metrics such as accuracy. Additionally, we explore the impact of different numbers of latent features on the accuracy of the SVD-based recommendations.

## Installation and Usage

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/Recommendations_with_IBM.git
    cd Recommendations_with_IBM
    ```

2. **Install required libraries**:
    Ensure you have `pandas`, `numpy`, `matplotlib`, and `scikit-learn` installed. You can install them using:
    ```bash
    pip install pandas numpy matplotlib scikit-learn
    ```

3. **Run the Jupyter Notebook**:
    ```bash
    jupyter notebook Recommendations_with_IBM.ipynb
    ```

4. **Convert Notebook to PDF** (optional):
    Ensure `pandoc` is installed, then run:
    ```python
    from subprocess import call
    call(['python', '-m', 'nbconvert', '--to', 'pdf', 'Recommendations_with_IBM.ipynb'])
    ```

## Acknowledgments

This project is part of the Udacity Data Scientist Nanodegree program in collaboration with IBM. Special thanks to the Udacity and IBM teams for providing the datasets and guidance for this project.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
