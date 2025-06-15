# 🚀 HireSignal  
**Turn job posts into new clients — automatically.**  
HireSignal helps AI & software consulting companies discover potential leads by scanning job postings (e.g., from LinkedIn) and crafting personalized, portfolio-backed cold emails.

---

## 🧠 What It Does

When companies post new job openings, they’re signaling real business needs. **HireSignal taps into those signals** and turns them into an opportunity for you to pitch your services — intelligently and at scale.

With the help of a local LLM and vector-based portfolio matching, HireSignal:

1. Scrapes job descriptions from a given URL
2. Extracts structured information (role, skills, experience, etc.)
3. Matches the job to your company’s previous work (via tech stack)
4. Generates a tailored cold email to pitch your services

---

## 💼 Who It's For

- AI & Software Consultants  
- Freelancers and Dev Shops  
- Business Development Executives  
- Anyone who wants smarter cold outreach based on real hiring signals

---

## 🛠️ Features

- 🧹 Cleans messy job descriptions into structured data
- 🧠 Uses a local LLM (`llama3.2` via Ollama) to extract roles, skills, and needs
- 🔗 Matches job skills with your portfolio (powered by ChromaDB)
- 📨 Crafts personalized cold emails based on real hiring intent
- 🌐 Easy-to-use UI with Streamlit

---

## 📂 Project Structure

```
├── chains.py           # LLM chains for job extraction and email writing
├── portfolio.py        # Loads and queries your past work via vector search
├── utils.py            # Cleans up raw web content
├── main.py             # Streamlit front-end
├── resource/
│   └── my_portfolio.csv  # Your techstack + project links
├── vectorstore/        # ChromaDB persistent storage
├── .env                # For environment variables like USER_AGENT
```

---

## 🧪 Example Use Case

You're a consultant offering data automation services. A company posts a job looking for a "Python automation engineer" on LinkedIn.

You paste the job URL into HireSignal.  
It extracts the job’s key skills, matches it to your work with Pandas and Airflow, and creates a cold email like:

```markdown
Hi [Hiring Manager],

I'm Brian, BDE at Brian&CO — an AI & software consulting firm specializing in workflow automation. I noticed your team is looking for a Python automation engineer, and we’ve helped several companies streamline similar processes...

[Includes relevant case study links]
```

---

## 📋 Setup

### 1. Clone the repo

```bash
git clone https://github.com/brian-fez/HireSignal.git
cd HireSignal
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Set up `.env`

Create a `.env` file in the root:

```
USER_AGENT=MyLangchainApp/1.0
```

### 4. Prepare your portfolio

Edit `resource/my_portfolio.csv` with:

| Techstack          | Links                           |
|--------------------|----------------------------------|
| Python, Pandas     | https://yourcompany.com/case1    |
| React, FastAPI     | https://yourcompany.com/case2    |

### 5. Run the app

```bash
streamlit run main.py
```

---

## 📦 Requirements

- Python 3.10+
- Ollama (with `llama3.2` model installed)
- Packages:
  - `streamlit`
  - `langchain`
  - `langchain-community`
  - `chromadb`
  - `pandas`
  - `python-dotenv`

---

## 🧠 Powered By

- [LangChain](https://www.langchain.com/)
- [Ollama](https://ollama.com/)
- [ChromaDB](https://www.trychroma.com/)
- [Streamlit](https://streamlit.io/)

---

## 📈 Roadmap Ideas

- [ ] Support uploading job PDFs or text
- [ ] Add resume/cover letter generation
- [ ] Save lead + email history to file or DB
- [ ] Auto-detect company and contact details

---

## ⚡ License

MIT License
