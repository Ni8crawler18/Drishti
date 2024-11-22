# Drishti - NLP Model for Complaint Categorization

Drishti is an NLP-based model designed to categorize user complaints written in Hinglish and English into **3 main categories** and further classify them into **62 subcategories**. This pipeline employs **TF-IDF vectorization** and **LightGBM** to provide efficient and transparent predictions without relying on pre-trained models.

## Project Structure

```
.
├── LICENSE                 # Licensing information
├── model                   # Contains the core Jupyter notebooks
│   ├── 1_map.ipynb        # Maps existing categories to new ones
│   ├── 2_preprocessing.ipynb  # Preprocesses the complaint text
│   ├── 3_model.ipynb      # Trains the LightGBM model and evaluates performance
│   └── datasets           # Contains the dataset files
│       ├── test.csv       # Test dataset (replace with validation.csv for model testing)
│       └── train.csv      # Training dataset
├── public                  # Public resources and documentation
│   ├── Draft+IndiaAI+CyberGuard+AI+Hackathon_+Dataset+Usage+Guidelines.pdf
│   └── schema-indiaai-cyberguard-ai-hackathon.pdf
└── README.md              # Documentation for the repository
```

## Getting Started

### Dataset Preparation

1. Place your **train.csv** and **validation.csv** files inside the `datasets` directory
2. Rename `validation.csv` to `test.csv` if needed to match the existing workflow

### Running the Model

Follow these steps to execute the model pipeline:

1. **Mapping Categories**
   * Open and run **1_map.ipynb** to map the original dataset's categories and subcategories to the new format

2. **Preprocessing**
   * Open and run **2_preprocessing.ipynb** to clean and preprocess the complaint text (Hinglish-to-English conversion, tokenization, stopword removal, etc.)

3. **Model Training and Evaluation**
   * Open and run **3_model.ipynb** to:
     * Vectorize the preprocessed text using TF-IDF
     * Train the LightGBM model on the 3 main categories and 62 subcategories
     * Evaluate the model's performance

> **Note**: The evaluation metrics, including accuracy, F1 score, log loss, and confusion matrix, are displayed within the cells of `3_model.ipynb`.

## Key Features

* **Multiclass Classification**: Categorizes complaints into **3 main categories**
* **Multilabel Classification**: Maps complaints into **62 subcategories**
* **Custom Preprocessing Pipeline**: Handles Hinglish-to-English conversion and comprehensive text cleaning
* **Fully Transparent Pipeline**: Avoids reliance on pre-trained models, ensuring a custom and explainable solution

## Evaluation

* **Main Category Classification**: Achieves **87% accuracy** and an **86.5% F1 score** across 3 main categories
* **Subcategory Classification**: Achieves **56% accuracy** for 62 subcategories

## License

This project is distributed under the MIT License. See `LICENSE` for details.

## Acknowledgments

The dataset and problem statement were provided as part of the **IndiaAI CyberGuard AI Hackathon**.