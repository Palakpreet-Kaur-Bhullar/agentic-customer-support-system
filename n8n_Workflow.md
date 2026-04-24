A production-grade n8n workflow that automates customer support from message intake to response — using AI classification, sentiment analysis, and a vector-backed FAQ agent.
A user message hits a webhook, gets stored in Supabase, then passes through an LLM classifier that assigns a category and urgency level. A second AI layer analyzes sentiment and flags threatening or inappropriate messages, blocking them before they reach the response pipeline. High-urgency or angry conversations are automatically routed to a human agent queue. For everything else, a Groq-powered FAQ agent queries a Pinecone vector database using Gemini embeddings to find the best match from the knowledge base — and if no match is found, a validity check filters out irrelevant queries before sending a fallback response.
Every message and response is stored in Supabase with a labeled sender field, giving a clean full conversation trail.

<img width="652" height="446" alt="image" src="https://github.com/user-attachments/assets/70a8932b-f48f-43bb-8a62-078edaf54a4c" />
<img width="648" height="687" alt="image" src="https://github.com/user-attachments/assets/be4a836a-af0c-4005-a625-aad82ab56a9e" />
<img width="644" height="342" alt="image" src="https://github.com/user-attachments/assets/bc66e982-adb9-42f6-a771-7febbabef195" />
