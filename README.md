# GPT-LLM-Based-Impression-Prediction-from-Radiology-Reports

This research paper presents a novel large language model specifically fine-tuned on radiology reports. The model has been designed to generate accurate impressions by leveraging patients' medical findings and background information. The primary objective of this model is to assist physicians in optimizing their documentation process, ultimately reducing the time required for generating comprehensive reports. By employing this technology, physicians can potentially alleviate the risk of burnout associated with extensive and repetitive documentation tasks.

## Data
The data for this project was obtained from the University of Chicago Medicine, consisting of 789,280 de-identified radiology reports. 

## Current Progress
We have already tried two models Alpaca-7b (code in Capstone_Code.ipynb) and Medalpaca7b (code in medalpaca-7b.ipynb) on Sono Types (6577 records in total). More detail about our methodology, result and analysis could be found in our proposal. In general, from the ROUGE score and our user interface demo, the model is capable of generating appropriate impression text, but there are still limitations that need to be addressed and few areas of improvement to consider.

## Next Steps:
- Also include the clinical historical information as one part of the input.
- Consider the order of the impression, which means that in addition to generating accurate impressions, we need to ensure that the order or sequence of the impressions is meaningful and coherent.
- Try Other Models: 4 models will be deployed in total and the best one among the one will be selected.
- Run the model on other modalities (CT, X-ray, Ultrasound … etc).
- Build and Refine Output API.
