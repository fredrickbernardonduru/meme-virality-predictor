# Meme Virality Predictor

![Python](https://img.shields.io/badge/Python-3.8+-blue)
![PySpark](https://img.shields.io/badge/PySpark-3.5-orange)

## Overview
This project develops a regression model in PySpark to predict the viral potential of social media memes, measured as an Engagement Score derived from likes, shares, and comments. The model leverages features such as Image Complexity, Text Length, Posting Hour, Follower Count, Meme Category, and Platform, processed using one-hot encoding, feature scaling with StandardScaler, and Linear Regression within a PySpark pipeline. The dataset, sourced from platforms like Reddit, Instagram, X, and others, contains 89,978 records cleaned by removing rows with missing values. The goal is to empower content creators and marketers with predictive insights to optimize meme performance before posting.

## Repository Structure
- **`codes/`**: Contains the Jupyter Notebook (`meme_virality_project.ipynb`) with the complete PySpark pipeline for data preprocessing, model training, and evaluation.
- **`data/`**: Available in the folder Data, it is named (`meme_dataset.csv`) from Data/meme_datase.csv.
- **`README.md`**: This file, providing project overview, setup instructions, and usage details.

## Setup Instructions
1. **Prerequisites**:
   - Python 3.8 or higher
   - PySpark (`pip install pyspark`)
   - Jupyter Notebook (`pip install jupyter`)
2. **Installation**:
   - Clone the repository:
     ```bash
     git clone https://github.com/yourusername/meme-virality-predictor.git
     ```
   - Navigate to the `codes/` folder:
     ```bash
     cd meme-virality-predictor/codes
     ```
   - Install dependencies:
     ```bash
     pip install pyspark jupyter
     ```
3. **Dataset**:
   - Download `meme_dataset.csv` from [insert your dataset link here].
   - Place it in a `Data/` folder or update the file path in the notebook (`../Data/meme_dataset.csv`).
4. **Run the Notebook**:
   - Launch Jupyter Notebook:
     ```bash
     jupyter notebook meme_virality_project.ipynb
     ```
   - Execute the cells to preprocess data, train the model, and evaluate results.

## Results
The Linear Regression model achieved an RMSE of 19.516 and an R² score of -0.0000657, indicating poor performance compared to a baseline mean prediction. This suggests the model fails to capture complex patterns in the data. Recommended improvements include:
- Switching to a non-linear model like RandomForestRegressor.
- Adding features such as caption sentiment or image-based attributes (e.g., text or face detection).
- Collecting more data to improve generalization.

## Usage
Run the `meme_virality_project.ipynb` notebook in the `codes/` folder to:
1. Load and preprocess the dataset (handling missing values, encoding categorical variables).
2. Train the regression model using the PySpark pipeline.
3. Evaluate predictions using RMSE and R² metrics.
Experiment with alternative algorithms (e.g., RandomForestRegressor) or new features to enhance model accuracy.

## Future Improvements
- Implement RandomForestRegressor or GradientBoostedTreeRegressor for better handling of non-linear relationships.
- Incorporate advanced features like sentiment analysis of captions or image-based features using APIs (e.g., Google Vision).
- Perform hyperparameter tuning with CrossValidator to optimize model performance.
- Expand the dataset with additional meme data from platforms like X (see [X API](https://x.ai/api)).

## Contributing
Contributions are welcome! Please:
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/your-feature`).
3. Commit changes (`git commit -m "Add your feature"`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.

## License
[MIT License](LICENSE)

## Contact
For questions or suggestions, open an issue or contact fredrichbernard4126@gmail.com.
