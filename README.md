# Phishing URL Detection using NLP and Sequence Models
Darshan Raju
# Overview
This repository contains the Phishing URL Detection System using NLP and Sequence Models, which was created as part of the research project "Phishing URL Detection using NLP and Sequence Models: A Comparative Study of Character-Level CNN-GRU and Transformer Approaches.

The system investigates how sequence learning architectures applied to raw URL strings can improve phishing detection accuracy while being transparent and interpretable using attention mechanisms and explainable AI methodologies.

Traditional phishing classifiers frequently achieve high accuracy, but provide no insight into why a specific URL is identified. This study addresses that gap by combining deep sequence models, specifically CharCNN-GRU with Attention and DistilBERT transformers, to provide human-interpretable insights into model decision-making via character-level attention visualization.

# Research Goal
To design and evaluate a deep learning-based phishing URL detection system capable of:

-Detecting phishing URLs using character-level sequence patterns 

-Explaining classification outcomes for human analysts and security teams through attention maps

-Balancing performance, interpretability, and practical deployment in real-world security operations
# Key Contribution 
-Hybrid Sequence Architecture: Designed and implemented a CharCNN-GRU model with an attention mechanism that catches both local character motifs (suspicious TLDs, delimiter patterns) and long-range sequential dependencies in URL strings, achieving 93.9% accuracy in multi-class phishing detection.

-Interpretability-Based Evaluation: Integrated attention visualization to reveal character-level decision variables, allowing security analysts to comprehend which URL substrings (brand tokens, security terms, path segments) drive dangerous classifications.
# Dataset 
Dataset sourced from Kaggle:https://www.kaggle.com/datasets/sid321axn/malicious-urls-dataset
# key Insights
Experimental investigation revealed that sequence-aware models outperform standard feature-engineered techniques for URL-based phishing detection. More crucially, attention mechanisms reveal how specific structural patterns, such as brand token placement in subdomains, hyphen-separated security phrases, and path-based login prompts, correlate with malicious intent, providing actionable insights for cybersecurity experts.

The CharCNN-GRU hybrid strikes the best compromise between local pattern identification and sequential context modeling, whilst the DistilBERT transformer delivers higher precision in the low false positive domain required for industrial deployment. Together, these models build a complementary cascade that maintains high detection rates while balancing computational and analyst burden restrictions.
# Key Findings
CharCNN-GRU-Attention achieved 93.9% accuracy and 0.990 ROC-AUC, beating all traditional baselines.
Attention maps revealed interpretable patterns: phishing URLs focus on brand tokens in subdomains and hyphenated security phrases, whereas benign URLs exhibit balanced attention across short, clean domains.

Multi-class detection revealed asymmetric confusion between phishing and benign classes , but malware and defacement had near-perfect separation .
