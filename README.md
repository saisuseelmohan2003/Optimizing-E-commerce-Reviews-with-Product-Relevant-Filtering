# Optimizing E-commerce Reviews with Product-Relevant Filtering 🛒✨

## Overview 🚀

This project focuses on **automating the filtering of e-commerce reviews** to ensure that reviews are correctly aligned with the respective products. By using natural language processing (NLP) and an advanced model through LangChain’s framework, this project can distinguish relevant reviews from irrelevant or mismatched ones with a high degree of accuracy.

## Features 💡

- **Automated Review Filtering**: Classifies reviews as "relevant" or "irrelevant" based on alignment with the correct product. 🛍️
- **Product-Specific Validation**: Rejects reviews that refer to different products, are generic, or contain mismatched brand references. ❌
- **Context-Aware Analysis**: Accepts reviews with valid product-related issues, even without explicit product names, as long as they are related to the product context. ✅
- **Efficient Data Processing**: Uses Python and Pandas for seamless data handling and analysis. 📊

## How It Works 🛠️

1. **Data Ingestion** 📥:
   - The system reads reviews from an input file, with each review associated with a product name and URL.
   
2. **Review Evaluation** 📝:
   - Reviews are evaluated based on a defined prompt template, leveraging LangChain and the `gemma2` model to classify each review as "accept" or "reject."
   - Each review decision is based on whether the review content aligns with the product or not.

3. **Decision Logic** 🧠:
   - **Reject**: Reviews are rejected if they mention a completely different product, use a generic category or brand to describe another item, or contain irrelevant content.
   - **Accept**: Reviews are accepted if they contain complaints, service-related issues, or any valid product-related feedback—even if specific product names are missing.

4. **Accuracy Validation** ✅:
   - The model’s output is compared with manually labeled data to calculate accuracy, ensuring reliable review filtering performance.

## Technologies Used 🛠️

- **Python**: For scripting, automation, and data processing.
- **Pandas**: For efficient data manipulation and analysis.
- **LangChain**: For NLP model integration and prompt handling.
- **gemma2 model**: For context-aware review classification.

## How To Run 🧑‍💻

1. **Prepare Input Data**:
    - Ensure the input data includes columns for `product URL`, `product name`, `review`, and a manual validation label if using for accuracy testing.

2. **Install Dependencies**:
   - Install necessary packages like `langchain`, `pandas`, and `sklearn`.

3. **Run the Script**:
   - Execute the main script to process the dataset and classify reviews.
   - An output file will be generated with columns for model prediction and reasons for classification decisions.

4. **Review the Output**:
   - The output file provides a complete list of reviews with their classification ("accept" or "reject") and reasons for the decision, useful for quality assurance.

## Usage 📚

- **E-commerce Platforms**: Streamlines review management by filtering irrelevant or mismatched reviews.
- **Product Review Analysis**: Enhances product-specific sentiment analysis by ensuring reviews match their respective products.
- **Customer Feedback Processing**: Improves customer insights by focusing only on relevant product-related feedback.

*Happy Filtering!* ✨🔍
