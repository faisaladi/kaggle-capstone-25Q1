# Prompt Optimization Tool (Kaggle Capstone 2025 Q1)

> **Project Status**: 🎓 `Capstone / ML & GenAI Research`  
> **Domain**: LLM Prompt Engineering, Automated Evaluation & Cost Optimization  
> **Tech Stack**: Python, Jupyter, Google GenAI SDK (Gemini), Kaggle Secrets API, Pandas, NumPy

An automated Prompt Optimization and Evaluation Tool developed for the Kaggle 2025 Q1 Capstone. The project formulates prompt engineering as a multi-objective optimization problem, balancing model response quality, token efficiency, structural fidelity, and API cost.

---

## 🎯 Overview & Objectives

In production LLM applications, prompt verbosity directly drives API latency and inference costs. This project provides an automated pipeline that takes candidate system and user prompts, iteratively optimizes their instruction structure, and benchmarks the outputs across quantitative evaluation criteria:

1. **Token Efficiency**: Measures token compression ratios while retaining essential semantic instructions.
2. **Cost Calculation**: Models token costs per 1K tokens across varying frontier model pricing tiers.
3. **Structured Scoring**: Automatically weights evaluation criteria according to production constraints (e.g., latency-first edge deployments vs. accuracy-first reasoning tasks).
4. **Automated Benchmark Reporting**: Renders markdown tables comparing baseline prompts against optimized variants.

---

## 📂 Repository Contents

| Notebook | Description |
| :--- | :--- |
| **`prompt-optimization-tool.ipynb`** | Core implementation notebook containing prompt mutation logic, evaluation scorers, cost estimation models, and visualization components. |
| **`kaggle-submission.ipynb`** | Final submission notebook formatted for automated Kaggle leaderboard evaluation. |
| **`kaggle-capstone-25Q1.ipynb`** | Baseline experimentation and metric validation notebook. |

---

## 🔒 Security & Best Practices

- **Zero Hardcoded Secrets**: Fully adheres to security best practices by utilizing Kaggle's `UserSecretsClient` (`user_secrets.get_secret("GOOGLE_API_KEY")`) to handle API credentials dynamically without storing secrets in version control or output cells.

---

## 🚀 Running the Notebooks

### Option A: On Kaggle
1. Upload the notebook to [Kaggle Notebooks](https://www.kaggle.com/code).
2. Go to **Add-ons** > **Secrets** and add your `GOOGLE_API_KEY`.
3. Select Python 3 GPU/CPU accelerator and click **Run All**.

### Option B: Local Environment
```bash
# Clone the repository
git clone https://github.com/faisaladi/kaggle-capstone-25Q1.git
cd kaggle-capstone-25Q1

# Create virtual environment and install dependencies
python3 -m venv venv
source venv/bin/activate
pip install google-genai jupyter pandas numpy

# Export API key and start Jupyter
export GOOGLE_API_KEY="your_gemini_api_key"
jupyter notebook
```

---

## 📜 License

MIT License - see [LICENSE](LICENSE) for details.
