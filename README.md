#  Agentic AI Workflow for Job Automation – n8n Integration

###  Project Title:  
**Job Seeker**

---

##  Overview  
This project demonstrates how **Agentic AI** can autonomously perform end-to-end job searching and notification tasks without constant human intervention.  
It uses **n8n** (an open-source automation platform) integrated with **Google Workspace** and **AI models** to fetch, process, and deliver curated job listings directly to the user.

The system acts as an **intelligent job assistant** that:
- Fetches job data from sources like LinkedIn or job boards.  
- Analyzes the data using **AI (Gemini / GPT)**.  
- Summarizes and filters job listings.  
- Stores results in Google Sheets.  
- Automatically sends an email with job recommendations to the user.  

---

##  Problem Statement  
Manually browsing through multiple job portals, filtering jobs by skill or location, and tracking updates is time-consuming and inefficient.  
There is a need for an **automated, intelligent job search agent** that can:
- Collect and clean job data,  
- Apply user-specific filters, and  
- Deliver insights directly via email.  

---

##  Project Workflow  

### Step-by-Step Flow:
1. **Trigger Setup** – The workflow starts on a scheduled basis using n8n.  
2. **Data Extraction** – The agent fetches job listings from APIs or job boards (e.g., LinkedIn).  
3. **Data Cleaning & Formatting** – Extracts relevant fields such as title, company, location, and skills.  
4. **AI Processing** – Sends data to an LLM (Gemini / GPT) to analyze and summarize jobs.  
5. **Storage** – Saves processed jobs in Google Sheets for easy tracking.  
6. **Email Automation** – Sends top job matches to the user via Gmail.  
7. **Loop Execution** – The process repeats daily or weekly based on the trigger frequency.  

---

##  Agentic AI Concepts Used  

### 1. **Autonomous Task Execution**  
The AI acts as an **agent** that performs the entire workflow without human supervision once triggered.

### 2. **Dynamic Decision-Making**  
Uses condition nodes and AI analysis to decide which job listings are relevant or worth notifying.

### 3. **Goal-Oriented Planning**  
The system breaks the goal (“Find suitable jobs”) into subtasks:
- Fetch data  
- Filter  
- Summarize  
- Notify  

### 4. **Memory and Context Management**  
Previous job searches and user preferences are stored in Sheets, allowing the agent to learn and improve relevance over time.

### 5. **Tool Integration**  
The AI agent doesn’t act alone — it orchestrates multiple digital tools (Sheets, Gmail, Drive, and APIs) autonomously via **n8n**.

---

##  Tools and Resources Used  

| Category | Tool / Resource | Purpose |
|-----------|----------------|----------|
| **Automation Platform** | [n8n](https://n8n.io) | To create and orchestrate the AI-powered workflow |
| **AI Model** | Google Gemini / OpenAI GPT | For intelligent summarization and filtering of job listings |
| **Data Storage** | Google Sheets | To store job listings and summaries |
| **File Access** | Google Drive | For fetching and storing CSV or JSON data files |
| **Communication** | Gmail API | For automated email notifications |
| **Workflow Nodes** | HTTP Request, Google Sheets, Gmail, AI Agent | Core building blocks of n8n automation |
| **Visualization** | PlantUML | To design the project flowchart |
| **Version Control** | GitHub | For maintaining project documentation and version tracking |

---

##  How to Run the Project  

1. **Set up n8n locally or on n8n Cloud.**  
2. **Create a new workflow.**  
3. Add the following nodes in sequence:
   - Google Drive → Google Sheets → HTTP Request → AI Agent → If → Gmail.  
4. Configure OAuth connections for all Google services.  
5. Set the workflow to **trigger daily** using a **Cron node**.  
6. Run the workflow manually once to verify connections.  
7. Monitor executions and email summaries.  

---

##  Expected Output  

- **Google Sheets:** Contains clean, structured job listings.  
- **Email Notification:** Summarized list of top job recommendations delivered to inbox.  
- **Logs:** Successful workflow execution in n8n dashboard.  

---

##  Future Enhancements  

- Add **user authentication** to customize preferences.  
- Integrate **LinkedIn API** officially.  
- Extend to **resume-based AI matching** (LLM compares resume vs. job description).  
- Add **Telegram / WhatsApp bot integration** for notifications.  
- Use **vector databases** for semantic similarity in job matching.  

---

##  Author  
**Pragna Budigem**  
*VNR Vignana Jyothi Institute of Engineering and Technology*  
Department of Computer Science and Business Systems  

---

