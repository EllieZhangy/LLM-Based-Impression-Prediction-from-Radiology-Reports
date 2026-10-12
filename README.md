# LLM-Based Impression Prediction from Radiology Reports

**Can an open large language model turn radiology findings and patient context into a concise report impression?**

`Clinical NLP` · `Large Language Models` · `Fine-tuning` · `ROUGE Evaluation` · `Gradio`

This capstone research project compares several open language models for generating the **Impression** section of radiology reports from structured clinical context and report findings. The goal is to study whether domain-adapted LLMs can support documentation workflows—not to replace radiologists or provide autonomous diagnosis.

> **Research-only project:** the models and demo are not validated medical devices and must not be used for clinical decisions, patient care, or medical advice.

## Project highlights

| | |
| --- | --- |
| **Research task** | Generate a radiology impression from findings and available patient context |
| **Source corpus** | 789,280 de-identified radiology reports from University of Chicago Medicine |
| **Primary modeling focus** | MRI reports; selected notebooks also explore ultrasound |
| **Models compared** | Alpaca-7B, Medalpaca-7B, Llama 2 7B/13B, and Mistral-7B |
| **Evaluation** | ROUGE-based comparison with a published BERT/LSTM baseline |
| **Prototype** | Gradio interface using a fine-tuned Mistral-7B workflow |
| **Artifacts** | Experiment notebooks, capstone paper, presentation, figures, and demo screenshot |

## Research question

Radiology reports usually contain a detailed **Findings** section followed by a shorter **Impression** that summarizes the most clinically important observations. This project asks whether open LLMs can learn that transformation while producing language that is concise, relevant, and consistent with the source report.

The intended workflow is assistive:

```text
Patient context + radiology findings
                 ↓
      preprocessing and prompt format
                 ↓
      open LLM fine-tuning / inference
                 ↓
        generated impression draft
                 ↓
       clinician review and correction
```

## Data

The original corpus contains **789,280 de-identified radiology reports** spanning multiple imaging modalities. MRI was selected as the primary modeling subset based on project scope and data availability.

<p align="center">
  <img width="520" alt="Overview of the de-identified radiology report dataset" src="https://github.com/EllieZhangy/GPT-LLM-Based-Impression-Prediction-from-Radiology-Reports/assets/133906690/2e8ae0fe-3a99-4b86-8398-7791a774b8e3" />
</p>

The clinical dataset is **not included in this public repository**. The repository contains the research notebooks and presentation materials needed to understand the experiments, but reproducing training requires separately authorized access to appropriate de-identified data and institutional safeguards.

## Methodology

<p align="center">
  <img width="900" alt="Radiology impression prediction research workflow" src="https://github.com/EllieZhangy/GPT-LLM-Based-Impression-Prediction-from-Radiology-Reports/assets/133906690/5ae86f3f-5f74-42e2-a49e-4b0a827930ea" />
</p>

The study compares multiple open base and medically oriented models:

- **Alpaca-7B**
- **Medalpaca-7B**
- **Llama 2 7B**
- **Llama 2 13B**
- **Mistral-7B**

<p align="center">
  <img width="900" alt="Open language models evaluated in the project" src="https://github.com/EllieZhangy/GPT-LLM-Based-Impression-Prediction-from-Radiology-Reports/assets/133906690/d2fd1258-b23b-4fc8-8e9c-b12783b690aa" />
</p>

Models were selected based on open availability, manageable size, prior language-model performance, and relevance to the clinical text-generation task.

## Evaluation

The experiments use **ROUGE scores** to compare generated impressions with reference impressions. The published baseline comes from:

> Gundogdu, B., Pamuksuz, U., Chung, J. H., Telleria, J. M., Liu, P., Khan, F., & Chang, P. J. (2021). *Customized impression prediction from radiology reports using BERT and LSTMs*. IEEE Transactions on Artificial Intelligence.

<p align="center">
  <img width="820" alt="ROUGE evaluation results for the compared models" src="https://github.com/EllieZhangy/GPT-LLM-Based-Impression-Prediction-from-Radiology-Reports/assets/133906690/96478e65-07a8-4a48-bc7a-acc5b7054b2e" />
</p>

ROUGE is useful for lexical overlap, but it does not establish factual clinical correctness, safety, calibration, or diagnostic value. A clinical-grade evaluation would also require expert review, factual consistency checks, subgroup analysis, error taxonomy, and prospective validation.

## Demo

A Gradio prototype was created around the fine-tuned **Mistral-7B** workflow to demonstrate how findings could be entered and returned as a draft impression.

<p align="center">
  <img width="1100" alt="Gradio demo for radiology impression generation" src="https://github.com/EllieZhangy/GPT-LLM-Based-Impression-Prediction-from-Radiology-Reports/assets/133906690/0c1a0b94-8e58-4087-af1d-a43db61e641e" />
</p>

The screenshot is a research interface, not a currently hosted clinical application.

## Repository guide

### Experiment notebooks

- [`Alpaca-7b.ipynb`](Alpaca-7b.ipynb)
- [`Medalpaca_7b_mri.ipynb`](Medalpaca_7b_mri.ipynb)
- [`Medalpaca_7b_ultrasound.ipynb`](Medalpaca_7b_ultrasound.ipynb)
- [`Llama2_7b_mri.ipynb`](Llama2_7b_mri.ipynb)
- [`Llama2_13b_mri.ipynb`](Llama2_13b_mri.ipynb)
- [`Llama2_13b_ultrasound.ipynb`](Llama2_13b_ultrasound.ipynb)
- [`Mistral_7b_mri.ipynb`](Mistral_7b_mri.ipynb)

### Research materials

- [`Capstone Project Final Paper.pdf`](Capstone%20Project%20Final%20Paper.pdf)
- [`Final Capstone II Presentation.pptx`](Final%20Capstone%20II%20Presentation.pptx)

Notebook environments and external model dependencies may have changed since the original experiments. Treat the repository as a documented research artifact rather than a guaranteed one-command reproduction package.

## Responsible-use notes

- Generated impressions can omit findings, introduce unsupported claims, or use clinically inappropriate wording.
- Outputs require review by qualified clinicians and should never be inserted into a medical record automatically.
- De-identification reduces but does not eliminate privacy risk; clinical text must be handled under the relevant institutional and legal requirements.
- Performance on one institution's report style may not generalize to other hospitals, modalities, patient populations, or reporting conventions.
- Automated text-overlap metrics are not a substitute for radiologist evaluation or patient-safety testing.

## Selected work

- [AI Driving School](https://elliezhangy.github.io/ai-driving-school/) — a voice- and text-controlled Chinese parking game.
- [Daily Mood Screen](https://github.com/EllieZhangy/Daily-Mood-Screen) — a personalized macOS wallpaper pipeline using weather, photos, and mood.
- [Memory Studio](https://github.com/EllieZhangy/my-ai-poster-skills) — a photo-to-poster web app with reusable visual styles.
