Workflow: Basic AI Agent using Groq + Memory + Gmail

1. User Message

Collects the user input and passes it into the workflow.

This message is the starting point for perception.

2. AI Agent (Perception Layer)

Understands the user’s task or message.

Connects to the Groq Chat Model as the “Brain.”

Also reads and writes memory to maintain context.

If the user asks to send an email, the agent triggers the Gmail Action node.

3. Groq Chat Model (Brain)

Requires a Groq API Key.

Select any model you prefer (example: mixtral-8x7b, llama3-8b, etc.).

Used for reasoning and planning:

Reasoning → identifies what information is needed

Planning → decides where or how the task should be performed

4. Simple Memory

Set “Memory Length” to 5.

Stores the last 5 user–agent messages to maintain short-term context.

Helps the agent behave like a continuous chat.

5. Gmail (Action Layer)

Requires Gmail API credentials.

Add the recipient, subject, and message using expression values.

Use “magic wand” icons (expression builders) to insert dynamic text from the agent.

Turn OFF “Append n8n Attribution” so the email does not show
“This email was sent automatically with n8n.”

🚀Workflow Behavior

If the user sends normal questions → Groq responds as an AI assistant.

If the user asks to send an email → the message is routed to Gmail and delivered automatically.

Memory keeps the last 5 interactions so the AI understands context.

🚀API Keys Used

Groq API Key → for the Chat Model

Gmail API Key → for sending email through the Gmail node
