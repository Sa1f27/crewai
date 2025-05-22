# 🧠 AI-Powered Technical Interviewer with CrewAI & LangChain

This project simulates a real-time technical interview using [CrewAI](https://docs.crewai.com/) and [LangChain](https://www.langchain.com/) with GPT-based agents. It features two collaborative agents — an **Interviewer** and an **Evaluator** — who dynamically generate questions and assess user responses interactively.

## 📁 Project Structure

```
.
├── agents/
│   ├── interviewer.py        # Defines the Interviewer agent
│   └── evaluator.py          # Defines the Evaluator agent
├── crew.py                   # Sets up and wires agents/tasks into a Crew
├── run.py                    # Runs the interactive interview session
├── requirements.txt          # Python dependencies
├── .gitignore                # Git ignore rules
├── Dockerfile                # Container definition
└── docker-compose.yml        # Optional orchestration (if applicable)
```

## ⚙️ Features

* **Dynamic Topic Input** – Select your own technical topic to simulate an interview.
* **Conversational Interviewing** – The interviewer adapts questions based on past answers.
* **Real-Time Evaluation** – Instant feedback with a score and detailed critique from the evaluator.
* **Extendable Agents** – Easily plug in additional agents (e.g., ResumeReviewer, BehavioralCoach).

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/ai-tech-interviewer.git
cd ai-tech-interviewer
```

### 2. Set Environment Variable

Export your OpenAI API key (or use `.env` file as needed):

```bash
set OPENAI_API_KEY=your-openai-key
```

### 3. Install Dependencies

Using pip:

```bash
pip install -r requirements.txt
```

Or with Chocolatey Python setup:

```cmd
choco install python
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Run the App

```bash
python run.py
```

### 5. Using Docker (Optional)

Build and run with Docker Compose:

```bash
docker-compose up --build
```

Ensure your `.env` or Docker secrets contain `OPENAI_API_KEY`.

---

## 🧠 How It Works

* `interviewer.py`: Creates an interviewer agent that asks topic-relevant questions.
* `evaluator.py`: Creates an evaluator agent that scores and critiques your answers.
* `crew.py`: Assembles both agents with task descriptions into a CrewAI instance.
* `run.py`: Provides the interactive CLI session — continuously cycles through Q\&A and feedback.

---

## 📦 Dependencies

* `crewai`
* `langchain`
* `langchain-openai`
* `python-dotenv` *(if using .env support)*

Add others as needed in `requirements.txt`.
