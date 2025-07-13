# Job Relevance Rating System

# 🔍 Job Relevance Rating System (AI-Powered)

This project is an **AI-based job rating engine** built using `sentence-transformers` in **Google Colab**. It helps evaluate how relevant a job is to a user based on their prompt (interests, background, skills, or experience) and the job's description/title.

---

## 🌟 Features

- ✅ Accepts **natural language prompts** from users
- 🧠 Uses `all-MiniLM-L6-v2` sentence transformer for **semantic similarity**
- ✨ Optional use of **Gemini API** to extract structured skills from user prompt
- 📈 Calculates a **job relevance score** scaled to 5
- 🔄 Easily integratable into job portals, recommenders, or career apps

---

## 🧪 Example Input

```json
{
  "user_prompt": "I'm a CS graduate interested in statistics and machine learning. I've built projects like fraud detection and used car price prediction.",
  "job_name": "Data Scientist",
  "job_description": "Looking for someone with strong math/stats skills, data analysis, and experience with real-world ML projects."
}

Relevance Score: 4.1 / 5
```
# 📁 How It Works
 ## Input

User provides a career prompt

Job name and description are collected (manually or from web scraping)

## Processing

Prompt and job info are embedded using sentence-transformers

Cosine similarity is used to compute semantic closeness

Optional: Gemini API enhances the prompt by extracting structured skills

## Output

A single float value indicating how relevant the job is to the user

# 🧱 Stack

🐍 Python

🤗 SentenceTransformers

🧠 Gemini API (optional)

📓 Google Colab (for development and testing)

# 💡 Use Cases

Job match scoring engine

Career recommender system

Resume alignment tools

LLM-to-job search integration

# 🚀 Getting Started

1. Open in Colab

2. Install dependencies
pip install sentence-transformers
pip install google-generativeai  # Optional for Gemini support

3. Run the notebook and modify the rate_job() function with your input.

   
📌 Optional: Gemini Prompt Structuring
To improve rating accuracy, you can structure vague user prompts using Google's Gemini API:


 Example
"The following is the user prompt. Please extract 5–10 key skills for job matching: {user_prompt}"


# 🤖 Future Ideas
Connect with real-time job listings (e.g., web scraping from Indeed)

Add FastAPI or Flask API endpoint

Build frontend (e.g., Streamlit or React) for users to upload and get scores

📝 License
Open-source for research and educational use. Please credit this repository if reused.

🙌 Contributing
Got ideas to improve this? Want to integrate it into your app? PRs and feedback are welcome!

📬 Contact
Feel free to reach out if you're building something cool with this!

