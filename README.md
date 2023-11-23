# GPT-LLM-Based-Impression-Prediction-from-Radiology-Reports
Our project aims to utilize large language models to generate accurate words for the Impression section of medical reports by leveraging patients' medical findings and background information. The primary objective is to assist physicians in optimizing their documentation process, ultimately reducing the time required for generating comprehensive reports. 

## Data
The data for this project was obtained from the University of Chicago Medicine, consisting of 789,280 de-identified radiology reports. 
<p align="center">
  <img width="450" alt="image" src="https://github.com/EllieZhangy/GPT-LLM-Based-Impression-Prediction-from-Radiology-Reports/assets/133906690/2e8ae0fe-3a99-4b86-8398-7791a774b8e3">
</p>

Our data is textual, well-organized, and covers multiple modalities. We chose MRI for modeling considering the data size.


## Methodology
Here is the workflow of our project:
<p align="center">
  <img width="800" alt="Screen Shot 2023-11-19 at 12 04 07 AM" src="https://github.com/EllieZhangy/GPT-LLM-Based-Impression-Prediction-from-Radiology-Reports/assets/133906690/5ae86f3f-5f74-42e2-a49e-4b0a827930ea">
</p>

Several large language base models are experimented including **Alpaca- 7b, Medalpaca-7b, Llama 2.0-7b, Llama 2.0-13b and Mistral-7b**:
<p align="center">
  <img width="800" alt="Screen Shot 2023-11-19 at 12 05 09 AM" src="https://github.com/EllieZhangy/GPT-LLM-Based-Impression-Prediction-from-Radiology-Reports/assets/133906690/d2fd1258-b23b-4fc8-8e9c-b12783b690aa">
</p>

The selection of the model is based on:
- Open-Source Availability
- Manageable Model Size
- Proven Performance
- Use Case

## Model Evaluation
To comprehensively assess the performance of the models in generating precise impressions from patients' medical findings and background information, **ROUGE scores** have been selected as the primary evaluation metrics. The baseline results for comparison are derived from the paper titled 'Customized Impression Prediction from Radiology Reports Using BERT and LSTMs'.[1]

Here is the result:
<p align="center">
<img width="750" alt="Screen Shot 2023-11-23 at 5 24 48 PM" src="https://github.com/EllieZhangy/GPT-LLM-Based-Impression-Prediction-from-Radiology-Reports/assets/133906690/c3e9270d-ac09-4689-a7ff-570c31cd47e8">
</p>

## Demo
Below is an example demonstrating our user-friendly interface, developed with Gradio, utilizing the fine-tuned Mistral-7b model:
<p align="center">
  <img width="1000" alt="image" src="https://github.com/EllieZhangy/GPT-LLM-Based-Impression-Prediction-from-Radiology-Reports/assets/133906690/0c1a0b94-8e58-4087-af1d-a43db61e641e">
</p>


## Reference
[1] Gundogdu, B., Pamuksuz, U., Chung, J. H., Telleria, J. M., Liu, P., Khan, F., & Chang, P. J. (2021). Customized impression prediction from radiology reports using BERT and LSTMs. IEEE Transactions on Artificial Intelligence.

