# 🧠 Balancing Rigor and Utility: Mitigating Cognitive Biases in Large Language Models for Multiple-Choice Questions

Welcome to the official repository for the paper:

**_Balancing Rigor and Utility: Mitigating Cognitive Biases in Large Language Models for Multiple-Choice Questions_**

This repository hosts the experimental results and supporting materials from our study on how cognitive biases manifest in large language models (LLMs) during multiple-choice question answering. We examine the trade-off between accuracy and reasoning consistency, and explore strategies to mitigate undesirable biases.

---

## 📂 Repository Contents

This repository includes:

- 📄 **Experiment Results (CSV format)**: Model responses and correctness labels  
- 📊 **Evaluation Comparisons**: Across GPT-4, Gemini 1.0 Pro, and LLaMA3-70B  
- 🔍 **Question Data**: The full text of the multiple-choice questions used in evaluation  
- 📁 **Supplemental Examples**: Referenced in the paper’s appendix and available on the project website

---

## 🤖 Evaluated Models

We evaluated the following models:

- **GPT-4**  
- **Gemini 1.0 Pro**  
- **LLaMA3-70B**

Each model was prompted using a consistent format and evaluated on the same set of questions to ensure fair comparison.

---

## 📊 CSV Format Description

The core data files are in CSV format. Each row corresponds to a single question, and each model’s response is recorded alongside its correctness.

### **Response CSV Columns without reject in Response_result folder**

| Column Name         | Description                                      |
|---------------------|--------------------------------------------------|
| `question-ID`       | Unique question identifier                       |
| `question`          | Full question text with answer options           |
| `GT`                | Ground truth answer                              |
| `GPT_resp`          | GPT-4’s generated response                       |
| `Inference results`       | Whether GPT-4 have a correct inference |
| `Final result`       | Whether GPT-4's response matches the ground truth |
| `Gemini_resp`       | Gemini 1.0 Pro’s response                        |
| `Inference results`       | Whether Gemini have a correct inference |
| `Final result`       | Whether Gemini's response matches the ground truth |
| `llama3_resp`       | LLaMA3-70B’s response                            |
| `Inference results`       | Whether LLaMA3-70B have a correct inference |
| `Final result`       | Whether LLaMA3-70B's response matches the ground truth |

### **Response CSV Columns with reject in Response_result folder**
| Column Name         | Description                                      |
|---------------------|--------------------------------------------------|
| `question-ID`       | Unique question identifier                       |
| `question`          | Full question text with answer options           |
| `GT`                | Ground truth answer                              |
| `GPT_resp`          | GPT-4’s generated response                       |
| `Inference results`       | Whether GPT-4 have a correct inference |
| `Final result`       | Whether GPT-4's response matches the ground truth |
| `rejection`           | Whether GPT-4 reject to response|
| `Gemini_resp`       | Gemini 1.0 Pro’s response                        |
| `Inference results`       | Whether Gemini have a correct inference |
| `Final result`       | Whether Gemini's response matches the ground truth |
| `rejection`           | Whether Gemini reject to response|
| `llama3_resp`       | LLaMA3-70B’s response                            |
| `Inference results`       | Whether LLaMA3-70B have a correct inference |
| `Final result`       | Whether LLaMA3-70B's response matches the ground truth |
| `rejection`           | Whether LLaMA3-70B reject to response|

### **Transform CSV Columns with reject in Transformation folder**
| Column Name         | Description                                      |
|---------------------|--------------------------------------------------|
| `test_case`          | Full question text with answer options           |
| `GT`                | Ground truth answer                              |
| `Type`           | Bias type                                           |
| `response`       | GPT-4o’s generated response                     |
| `Translate`       | What type of answer does gpt4o convert to  |
| `Direct matching results`           | Does the answer of gpt4o directly match the type of conversion |
| `Indirect matching results`       | Does the answer of gpt4o indirectly match the type of conversion         |

> 📌 Note: The first row in each CSV file is the header.

---

## 📚 Example Questions

You can find example questions and model responses in the **Appendix** of the paper. Additional examples and interactive demos may also be provided on our [project website](https://hanyangzhong.github.io/BRU-website/) *(link to be added)*.

---
## 🧾 Citation
If you use this repository or our findings in your work, please consider citing our paper:

bibtex
```
@misc{wang2024balancingrigorutilitymitigating,
      title={Balancing Rigor and Utility: Mitigating Cognitive Biases in Large Language Models for Multiple-Choice Questions}, 
      author={Liman Wang and Hanyang Zhong and Wenting Cao and Zeyuan Sun},
      year={2024},
      eprint={2406.10999},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2406.10999}, 
}
```
---
## 🤝 Contact
For questions, suggestions, or collaboration inquiries, feel free to open an issue on GitHub or contact the authors via the paper.


