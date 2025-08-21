# Hezeruna AI Cybersecurity/IT AI Assistant
Hezeruna is an AI-powered chatbot assistant that is focused on IT and Cybersecurity topics through the use of python. 
Hezeruna is combines:
- Google Custome Search API: It fetches relevant security information through notable sources from aticles, blogs, and frameworks
- OpenAI GPT API: This expands, explains, and contextulizes results in a professional tone

Hezeruna demonstrates how to integrate multiple AI services into one workflow that showcases practical skills when it comes to API integration, error handling, and security focused development.

---

# Architecture 

Workflow: 
1. The user submits a query (e.g., "What is incident response?")
2. Google Search API fetches relevant articles and snippets
3. If the results are valid it passes into OpenAI to expand and explain
4. If Google Search fails there is a fallback to OpenAI that handles explanation alone and keeps it professional 
5. The final answer is returned to the user

---

# Tools & Technologies 
- Python 3.13.5
- OpenAI GPT-3.5 API
- Google Custom Search API
- dotenv for environment variable management

---

# Setup & Configurations
1. brain.py - The orchestrator of Hezeruna. This controls all the overall logic by sending user's query to Google Search and then it devides OpenAI should expand on the information retrieved or fallback and have OpenAI explain it without the use of relevant findings
2. google_search.py - Handles the retrieval of information. Connecting to Google Custom Search API, it processes the results, filters snippets that are weak, and returns the most relevant one
3. OpenAI.py - Handles the reasoning. Connecting to OpenAI API and returns the explanation in a professional tone with natural langauage.

Input --> Brain.py
Retrieval --> google.search.py
Reasoning --> OpenAI.py
Final Output --> User

# Lessons Learned
- Chaining and combining APIs increases trust and accuracy for responses when compared to only using one
- Error handling is critical which is why implementing fallback logic can ensure that a professional accurate response will always work
- Modular code structure makes projects clear to reviewers and demonstrates best practices
- Integrating .env variables should be the standard way when it comes to API key safety

---

# Future Considerations 
If I were to expand on Hezeruna I would:
- Add a simple web UI replacing the terminal output
- Improve the snippet selection based on ranking multiple Google results
- Expand on notable sources and add framework mapping for more enrich responses

Hezeruna is not meant to be a public chatbot. This project was focused on how to design, implement, document, and understand an AI workflow. 





