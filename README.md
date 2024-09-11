
# Automated Essay Scoring 
Deep Learning for AI course (Instructor: Professor Ilyoup Kwak) 
 
## Overview
- Motivated by the need to improve essay scoring algorithms for students in underserved communities who lack proper guidance from educators. Implemented algorithms utilizing BERT-based models such as Albert, Electra, and DeBERTa to predict scores.
- Fine-tuned the models as a multi-class classification problem, as the dependent variable "score" in the essay dataset is a categorical variable on a scale from 1 to 6. Set num_labels parameter to 6, applied cross entropy as the loss function, and configured dropout_prob at 0.5.
- Checked that QWK (quadratic weighted kappa), the evaluation metric, did not perform well in classification models. Converted the problem into a regression task, and fine-tuned the models with num_labels set to 1, using MSE as the loss function and no dropout.
- Achieved a QWK score ranging from 0.50 to 0.73 when building classification models using BERT algorithms (Albert, Electra, DeBERTa). Improved QWK scores to a range of 0.78 to 0.81 after reconstructing the models as regression tasks. Identified DeBERTa as the top-performing model in terms of predictive performance.
- Encountered a data imbalance issue among dependent variable classes, where classes 1, 5, and 6 were significantly underrepresented compared to other classes.
- Applied EDA (easy data augmentation) techniques to address the imbalance but faced issues where syntactically or contextually incorrect sentences negatively impacted scoring. Switched to text augmentation techniques using WordNet-based synonym augmentation and round-trip translation, expanding the underrepresented classes by threefold.
- Increased QWK from 0.81 to 0.91 in the DeBERTa regression model after applying data augmentation.
- Skills: Python, Deep Learning, pandas, NumPy, Matplotlib, Seaborn, Pytorch, Tranformers, Hugging Face, Scikit-Learn, Google Colab, Natural Language Processing (NLP), Data augmentation, Torch optimizers and schedulers, file handling and data extraction
