# GPT-LLM-Based-Impression-Prediction-from-Radiology-Reports
Our project aims to utilize large language models to generate accurate words for the Impression section of medical reports by leveraging patients' medical findings and background information. The primary objective is to assist physicians in optimizing their documentation process, ultimately reducing the time required for generating comprehensive reports. 

## Data
The data for this project was obtained from the University of Chicago Medicine, consisting of 789,280 de-identified radiology reports. 

## Methodology
Several large language models are experimented including Alpaca- 7b, Medalpaca-7b, Llama 2.0-7b, Llama 2.0-13b and Mistral-7b.

## Model Evaluation
To comprehensively assess the performance of the models in generating precise impressions from patients' medical findings and background information, ROUGE scores have been selected as the primary evaluation metrics. The baseline results for comparison are derived from the paper titled 'Customized Impression Prediction from Radiology Reports Using BERT and LSTMs'.[1]

Here is the result:
<p align="center">
  <img width="750" alt="Screen Shot 2023-11-18 at 11 54 11 PM" src="https://github.com/EllieZhangy/GPT-LLM-Based-Impression-Prediction-from-Radiology-Reports/assets/133906690/6053f853-f396-4fee-bff2-4941bc4659b7">
</p>

## Demo
Here's an example of output of Mistral-7b model provided by Hugging Face:
<p align="center">
  <img width="1000" alt="image" src="https://github.com/EllieZhangy/GPT-LLM-Based-Impression-Prediction-from-Radiology-Reports/assets/133906690/0c1a0b94-8e58-4087-af1d-a43db61e641e">
</p>


## Reference
[1] Gundogdu, B., Pamuksuz, U., Chung, J. H., Telleria, J. M., Liu, P., Khan, F., & Chang, P. J. (2021). Customized impression prediction from radiology reports using BERT and LSTMs. IEEE Transactions on Artificial Intelligence.

