# 🎯 Customer Support Case Type Classification

A machine learning solution that automatically classifies customer support cases into billing, technical, or general queries.

## 📋 Overview

This project provides a streamlined text classification system built in Python using Google Colab. It takes customer support messages and categorizes them to help customer service teams prioritize and route inquiries more efficiently.


## ✨ Features

- 🤖 Automatic classification of support tickets into three categories:
  - 💰 Billing issues
  - 🔧 Technical problems
  - ❓ General inquiries
- 🧹 Text preprocessing to clean and standardize customer messages
- 🧠 Model training with two different algorithms (Naive Bayes and Logistic Regression)
- 📊 Performance evaluation with detailed metrics
- 📈 Visualization of results with confusion matrix
- 🔍 Feature importance analysis to understand classification decisions
- 🚀 Ready-to-use function for classifying new support cases

## 🔧 Requirements

- Python 3.6+
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn

## 💻 Installation

1. Clone this repository:
```
git clone https://github.com/aryan7905/09_Customer_Support_Case_Type_Classification_202401100300069.git
cd 09_Customer_Support_Case_Type_Classification_202401100300069
```

2. Upload the notebook to Google Colab or run it locally

3. Ensure your dataset is in the correct location (`/content/support_cases.csv` for Colab)

## 📚 Dataset

The model expects a CSV file with at least two columns:
- A text column containing the customer support messages
- A category column with labels (billing, technical, general)

Example format:
```
case_type,category
"I was charged twice this month",billing
"The app keeps crashing when I open it",technical
"How do I change my email address?",general
```

![Sample Dataset](/sample_images/dataset_preview.png)

## 🚀 Usage

### Quick Start

1. Run the notebook cells sequentially in Google Colab
2. Modify the `text_column` and `target_column` variables in Cell 2 to match your dataset's column names
3. Use the `classify_support_case()` function from Cell 5 to classify new support cases

### Classification Function

```python
result = classify_support_case("The application is not responding when I click submit")
print(f"Category: {result['category']}")
print(f"Confidence: {result['confidence']}")
```

## ⚙️ How It Works

1. **Data Preprocessing:** 🧹 Cleans text by removing special characters, converting to lowercase, and normalizing spaces
2. **Feature Extraction:** 📝 Transforms text into TF-IDF feature vectors
3. **Model Training:** 🏋️‍♀️ Trains classification models on the processed data
4. **Evaluation:** ✅ Compares model performance using accuracy, precision, recall, and F1-score
5. **Feature Analysis:** 🔍 Identifies the most important words for each category
6. **Classification:** 🎯 Uses the best model to predict categories for new support cases

![Workflow Diagram](/sample_images/workflow.png)

## 📊 Results

The models typically achieve accuracy between 80-95% depending on the dataset quality and class distribution. Logistic Regression usually outperforms Naive Bayes for this task.
![{8C47DA57-E0DA-44D5-8F3A-815E29E7C28A}](https://github.com/user-attachments/assets/d94a190c-4546-47d6-a0ca-886137f51a39)
![{69A44666-3158-474B-9656-F555538B3062}](https://github.com/user-attachments/assets/2bddf2ef-a469-4d4f-b404-8b6d4b9d0d40)


![Performance Chart](/sample_images/performance_metrics.png)

## 🔧 Customization

- Adjust the `max_features` parameter in the TF-IDF vectorizer to include more or fewer words
- Try different classification algorithms by importing from scikit-learn
- Add more preprocessing steps like stemming or lemmatization for potentially better results

## 📜 License

MIT

## 📬 Contact

Aryan - [GitHub Profile](https://github.com/aryan7905)

Project Link: https://github.com/aryan7905/09_Customer_Support_Case_Type_Classification_202401100300069

---

## 📚 Additional Resources

- [Scikit-learn Documentation](https://scikit-learn.org/stable/documentation.html)
- [Text Classification Guide](https://scikit-learn.org/stable/tutorial/text_analytics/working_with_text_data.html)
- [TF-IDF Explained](https://en.wikipedia.org/wiki/Tf%E2%80%93idf)

## 🙏 Acknowledgements

- [Google Colab](https://colab.research.google.com/) for providing a free environment to run machine learning models
- [Scikit-learn](https://scikit-learn.org/) for their excellent machine learning library
- [Pandas](https://pandas.pydata.org/) for data manipulation capabilities
