# AI Stack & Tooling

Een AI-First organisatie werkt niet met losse tools, maar met een samenhangende AI-stack. Die stack evolueert per kwartaal, afhankelijk van use cases, modelvoorkeuren, compliance en productstrategie.

---

## 1. Principes van een AI Stack

- Alles API-first, cloud-native
- Combineer best-of-breed met low-code tools
- Beschrijf stack als “service catalogus”
- Centraliseer promptbeheer en evaluatie
- Zorg voor auditability en monitoring

---

## 2. Stacklagen

| Laag           | Voorbeelden                                              |
|----------------|-----------------------------------------------------------|
| Interface      | ChatGPT, Notion AI, Slack, Copilot, Custom UI             |
| Orchestration  | LangChain, Flowise, Vercel AI SDK, CrewAI, OpenAgents     |
| Model Layer    | GPT-4o, Claude 3, Gemini 1.5, Mistral, Llama, Cohere       |
| Middleware     | API Gateway, Prompt-perfectie, Cache/Vector DB, Guardrails|
| Storage        | Pinecone, Weaviate, Supabase, Elasticsearch, MongoDB      |
| Ops & Monitoring | Weights & Biases, Humanloop, Traceloop, PromptLayer     |

---

## 3. Tooling per Rol

| Rol               | Tools                                                |
|------------------|-------------------------------------------------------|
| Prompt Engineer  | GPT, Claude, Promptfoo, PromptLayer                   |
| Developer        | GitHub Copilot, LangChain, Replit, Postman            |
| AI Product Owner | Notion, Miro, Flowchart-tools, Airtable               |
| Trainer / Coach  | Teachfloor, Notion, Slack                             |
| AI Integrator    | Zapier, Make, Vercel, REST tooling                    |

---

## 4. Prompt Management

- Gebruik een centrale promptbibliotheek (bv. Notion, GitHub of PromptLayer)
- Maak versies en testresultaten traceerbaar
- Gebruik tags per use case, rol en modeltype
- Documenteer inputs, expected outputs, edge cases

---

## 5. Stackdocumentatie

Minimaal per kwartaal:
- Actualiseer de stack (in Notion of Confluence)
- Archiveer tooling die niet meer gebruikt wordt
- Voeg lessons learned per tool toe
- Stel beleid op voor modelgebruik (OpenAI, Anthropic, etc.)

---

## 6. API en Model Integratie

| Wat               | Hoe                                                  |
|-------------------|------------------------------------------------------|
| LLM-koppeling     | API key, Auth via backend of directe call            |
| Retrieval         | via LangChain, RAG pipelines of Vector DB connector  |
| Workflow-triggers | via Webhooks, Zapier, Power Automate                 |
| Inputvalidatie    | Guardrails, schema's in Pydantic of JSON Schema      |

---

## 7. Governance en Beheer

- Model usage logs (bijv. OpenAI usage dashboards)
- Logging van user prompts en system prompts
- Evaluatiemetrics: accuracy, hallucination-rate, user satisfaction
- Beperk risico’s met model firewalls / red teaming

---

## 8. Valkuilen

- Te snel teveel tools → fragmentatie
- Geen zicht op prompt-kwaliteit → inconsistentie
- Geen fallback bij API-failures
- Geen single source of truth voor toolbeleid

---

## 9. Conclusie

Een AI-stack is niet technisch supportend, maar strategisch funderend.  
Je stack bepaalt of je schaalbaar, betrouwbaar en compliant AI kunt inzetten.  
Investeer in tooling als core business – niet als experiment.

---
