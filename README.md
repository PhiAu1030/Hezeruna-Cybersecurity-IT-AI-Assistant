# Hezeruna AI Cybersecurity/IT AI Assistant
Hezeruna is an AI-powered chatbot assistant that is focused on IT and Cybersecurity topics through the use of python. 
Hezeruna combines:
- Google Custome Search API: It fetches relevant security information through notable sources from articles, blogs, and frameworks
- OpenAI GPT API: This expands, explains, and contextualizes results in a professional tone

Hezeruna demonstrates how to integrate multiple AI services into one workflow that showcases practical skills when it comes to API integration, error handling, and security focused development.

---

# Tools & Technologies 
- Python 3.13.5
- OpenAI GPT-3.5 API
- Google Custom Search API
- dotenv for environment variable management

---

# Architecture 

Input --> Brain.py
Retrieval --> google.search.py
Reasoning --> OpenAI.py
Final Output --> User

Workflow: 
1. The user submits a query (e.g., "What is incident response?")
2. Google Search API fetches relevant articles and snippets
3. If the results are valid it passes into OpenAI to expand and explain
4. If Google Search fails there is a fallback to OpenAI that handles explanation alone and keeps it professional 
5. The final answer is returned to the user

---

# Setup & Configurations
1. brain.py - The orchestrator of Hezeruna. This controls all the overall logic by sending user's query to Google Search and then it devides OpenAI should expand on the information retrieved or fallback and have OpenAI explain it without the use of relevant findings
2. google_search.py - Handles the retrieval of information. Connecting to Google Custom Search API, it processes the results, filters snippets that are weak, and returns the most relevant one
3. OpenAI.py - Handles the reasoning. Connecting to OpenAI API and returns the explanation in a professional tone with natural langauage.

---

# Lessons Learned
- Chaining and combining APIs increases trust and accuracy for responses when compared to only using one
- Error handling is critical which is why implementing fallback logic can ensure that a professional accurate response will always work
- Modular code structure makes projects clear to reviewers and demonstrates best practices
- Integrating .env variables should be the standard way when it comes to API key safety

---

# Future Considerations 
If I were to expand on Hezeruna I would:
- Add a simple web UI replacing the terminal output for interactive use.
- Improve the snippet selection for Google results.
- Map responeses to frameworks for real-world alignment
- Add a conversation memory for follow-ups and context retention 

Hezeruna is a showcase project. It highlights my ability to design, implement, and document an AI workflow that integrates multiple services in a cybersecurity context. 

---

# Screenshots for demonstrating Hezeruna responding to different topics related to IT and Cybersecurity 
1. Startup & First Query 
<img width="1681" height="431" alt="Hezeruna Example 1" src="https://github.com/user-attachments/assets/fc1695ad-141d-4e85-aaf3-b105c06c36fc" />

2. SIEM Explanation
<img width="1679" height="275" alt="example 2" src="https://github.com/user-attachments/assets/9b14e7af-a185-470d-947b-98a8910b0a4b" />

3. NIST Cybersecurity Framework

<img width="1678" height="281" alt="example 3" src="https://github.com/user-attachments/assets/adca9c0c-0df9-44d8-886a-feeb2c01d07b" />

4. Zero Trust Model
<img width="1661" height="308" alt="example 4" src="https://github.com/user-attachments/assets/a4bbb46e-d072-48ca-8e27-1d2ba182bcfe" />

5. Malware Removal Guidance
<img width="1668" height="366" alt="example 5" src="https://github.com/user-attachments/assets/1d2e90e8-9352-4cab-88e8-652f1011e856" />

6. Error Handling
<img width="1678" height="339" alt="example 6" src="https://github.com/user-attachments/assets/f8b47afa-2933-4a6b-b2f5-25576dc5d742" />





