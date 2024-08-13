# Movie Reviews Classification

This project is focused on classifying movie reviews as positive or negative. The classification is based on a score ranging between 0 and 1, where the closer the score is to 1, the more positive the review is, and the closer it is to 0, the more negative the review is. The model's performance is evaluated using Accuracy and F1 Score metrics.

## Table of Contents
- [Project Overview](#project-overview)
- [Model](#model)
- [Data Preprocessing](#data-preprocessing)
- [Performance Metrics](#performance-metrics)
- [How to Use](#how-to-use)
- [Dependencies](#dependencies)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
The goal of this project is to classify movie reviews into positive or negative sentiment. The sentiment is determined by a score between 0 and 1:
- **0 to 0.5:** Negative sentiment
- **0.5 to 1:** Positive sentiment

The project is implemented in Python using TensorFlow, with BERT as the underlying model architecture. The BERT model is fetched from TensorFlow Hub and is applied in two scenarios:
1. On processed data.
2. On raw (unprocessed) data.

## Model
The model used in this project is based on BERT (Bidirectional Encoder Representations from Transformers). BERT is a pre-trained model provided by TensorFlow Hub.

- **Preprocessing Layer:**  
  `bert_preprocess = hub.KerasLayer("https://tfhub.dev/tensorflow/bert_en_uncased_preprocess/3")`

- **Encoder Layer:**  
  `bert_encoder = hub.KerasLayer("https://tfhub.dev/tensorflow/bert_en_uncased_L-12_H-768_A-12/4")`

## Data Preprocessing
The data preprocessing includes:
- Tokenization
- Padding/Truncating sequences to a uniform length
- Applying the BERT preprocessing layer

The model is trained once on processed data and once without any preprocessing to compare the impact of preprocessing on model performance.

## Performance Metrics
The model's performance is evaluated using the following metrics:
- **Accuracy Score:** Measures the percentage of correctly classified reviews.
- **F1 Score:** A weighted average of precision and recall, especially useful for imbalanced datasets.

## How to Use
1. **Download the `.ipynb` files** from this repository.

2. **Upload the files to Google Colab or Jupyter Notebook**.

3. **Run the notebooks** in Colab or Jupyter to train the model and predict sentiments.

## Dependencies
The dependencies are managed within the Colab or Jupyter Notebook environment, so no additional installation steps are needed.

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## License
This project is licensed under the MIT License.
