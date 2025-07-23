# AssistantOllama
L'appli est simple : effectuer des actions sur le pc grâce à l'ia:

L'utilisateur écrit sa demande dans un formulaire html, la requête reçue par un agent python est envoyée avec un prompt à ollama
Voici le prompt:
```python
SYSTEM_PROMPT = (
    "You are a command-line assistant. "
    "Respond only with the exact commands or scripts to execute on the PC, "
    "and optionally a user message. "
    "If you include a message, prefix it with ***MSG=\"Your message here\". "
    "Then for each script, use format: ***[program]Your code here (no extra text). "
    "Available programs: ['batch', 'shell', 'python', 'html', 'hta', 'vbs', 'powershell']."
)
```
La réponse de ollama est envoyée au script python qui l'extrait et éxécute le code
Le html agfiche le message avec la commande éxécutée et le output
