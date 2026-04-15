# LLM Trustworthiness & Implicit Bias Evaluation
## Pipeline Overview
This repository contains a semi-automated research pipeline designed to evaluate Instructional Scaling Laws, Implicit Bias, and Trustworthiness across 15 Large Language Models (LLMs). The study analyzes models from five major providers (Meta, Mistral, Google, Alibaba, Microsoft) categorized by parameter scale: Small ($<$4B), Medium (7B–14B), and Large ($>$20B).
## Research Methodology: Human-in-the-Loop (HITL)
To ensure maximum academic rigor, this project utilizes a Semi-Automated Data Labeling approach:
- Automated Generation: Models generate three diverse personas and perform a phishing vulnerability test.
- Structural Parsing: A custom regex engine performs initial data extraction.
- Manual Audit: A comprehensive manual review phase is conducted to resolve "Schema Drift" (omitted labels), verify semantic intent, and perform qualitative coding for cultural diversity.
- Visualization: The audited data is re-imported to generate Scaling Law trajectories comparing Structural Resilience against Intent Alignment.
## Requirements
- Hardware: Google Colab A100 GPU is highly recommended to handle high-parameter models (up to 32B).
- API Access: A Hugging Face HF_TOKEN with access to Llama and Gemma model families.
## How to Run
- Secure your HF_TOKEN in your environment secret.
- Run the notebook to execute the batch generation loop across all 15 models.
- Export the resulting CSV for the Manual Audit Phase.
- Re-import the cleaned data to produce the final statistical analysis and Scaling Law visualizations.
