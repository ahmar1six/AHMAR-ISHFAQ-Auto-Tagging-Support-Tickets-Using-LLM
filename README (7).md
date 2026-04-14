# 🏷️ Auto Tagging Support Tickets Using LLM

> Automatically tag customer support tickets into categories using Groq's Llama 3.3 70B with Zero-Shot and Few-Shot prompt engineering techniques.

---

## 📌 Objective

Build an intelligent system that:
- Automatically assigns **top 3 most relevant tags** to each support ticket
- Compares **Zero-Shot vs Few-Shot** prompt engineering performance
- Uses **Large Language Models (LLM)** for text classification
- Demonstrates real-world **prompt engineering** techniques

---

## 🏗️ Methodology / Approach

### 1. 📊 Dataset
- Used real **Customer Support Ticket Dataset** from Kaggle
- **8,469 total tickets** with 5 types and 16 subjects
- Selected **50 sample tickets** for LLM tagging

### 2. 🤖 Zero-Shot Tagging
- No examples given to the LLM
- Only task description and available tags provided
- LLM predicts top 3 tags purely from its training knowledge

### 3. 🎯 Few-Shot Tagging
- **5 labeled examples** provided to the LLM
- Examples show correct tagging patterns
- LLM learns from examples and applies similar logic

### 4. 📈 Evaluation
- **Full Match** — predicted tag exactly matches actual type/subject
- **Partial Match** — partial word overlap between predicted and actual
- Compared both approaches side by side

---

## 🛠️ Tech Stack

| Component | Technology |
|---|---|
| 🧠 LLM | Groq — Llama 3.3 70B |
| 📊 Data Processing | Pandas |
| 📈 Visualization | Matplotlib |
| 💬 Prompt Engineering | Zero-Shot & Few-Shot |
| 💻 Platform | Kaggle Notebooks |

---

## 📊 Key Results

| Method | Full Match | Partial Match |
|---|---|---|
| 🎯 Zero-Shot | 36.0% | 44.0% |
| 🚀 Few-Shot | 32.0% | 46.0% |
| 📈 Improvement | -4.0% | +2.0% |

---

## 💡 Key Insights

1. **Few-Shot improves partial match** by 2% over Zero-Shot
2. **Dataset quality matters** — `{product_purchased}` placeholders in descriptions reduced accuracy
3. **LLM bias** — model leaned towards "Technical issue" tag due to vague descriptions
4. **With clean data**, Few-Shot would significantly outperform Zero-Shot
5. **Top 3 tags** successfully generated for every ticket

---

## 🧪 Sample Output

| Ticket | Zero-Shot Tags | Few-Shot Tags |
|---|---|---|
| "Charged twice for order" | Technical issue, Software bug, Medium | Refund request, Payment issue, High |
| "App keeps crashing" | Technical issue, Software bug, Medium | Technical issue, Display issue, Medium |
| "Cannot login to account" | Technical issue, Account access, High | Technical issue, Account access, High |

---

## 🚀 How to Run

### 1. Clone the Repository
```bash
git clone https://github.com/Dev-ZishanKhan/Auto-Tagging-Support-Tickets-LLM
cd Auto-Tagging-Support-Tickets-LLM

### 2. Install Dependencies
```bash
pip install groq pandas scikit-learn matplotlib
```

### 3. Set Your Groq API Key
```bash
export GROQ_API_KEY="your_groq_api_key_here"
```

### 4. Run the Notebook
Open `auto_tagging_tickets.ipynb` in Kaggle or Jupyter

---

## 📁 Project Structure

```
Auto-Tagging-Support-Tickets-LLM/
│
├── auto_tagging_tickets.ipynb     # Main Jupyter Notebook
├── customer_support_tickets.csv   # Dataset path 
└── README.md                      # Project documentation
```

---

## 📝 License

This project is part of the **DevelopersHub Corporation AI/ML Engineering Internship** — Advanced Task 5.

---

## 👨‍💻 Author

**Your Name**
- 🌐 GitHub: [@Dev-ZishanKhan](https://github.com/Dev-ZishanKhan)
- 💼 LinkedIn: [zishan-coderx](https://www.linkedin.com/in/zishan-coderx-048483370/)
