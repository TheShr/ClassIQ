# AI-Powered Quiz Generation System

An **end-to-end AI system** that automatically generates high-quality **multiple-choice quizzes** from educational documents using **Retrieval-Augmented Generation (RAG)**, **schema validation**, and **human-in-the-loop review**.

---

## Features

- Automatic quiz generation from documents  
- Context-aware question creation using RAG  
- Strict JSON schema validation with Pydantic  
- Feedback loop for invalid model outputs  
- Human-in-the-loop content verification  
- Persistent storage using MongoDB  
- Interactive user interface built with Streamlit  

---

## Architecture Overview

### 1. Document Ingestion
Educational documents are chunked, embedded, and stored in a **vector database** for semantic retrieval.

### 2. Prompt Engineering
Carefully designed prompts with **few-shot examples** guide the LLM to generate structured and consistent quiz data.

### 3. Retrieval-Augmented Generation (RAG)
Relevant document context is retrieved from the vector database and injected into the LLM prompt to ensure factual accuracy.

### 4. LLM-Based Quiz Generation
The language model generates:
- Multiple-choice questions  
- Exactly **four options per question**  
- **One correct** and **three incorrect** answers  

### 5. Schema Validation (Pydantic)
Generated outputs are validated to ensure:
- Correct JSON structure  
- Required fields are present  
- Option and answer constraints are enforced  

Invalid outputs are automatically sent back for regeneration.

### 6. Human-in-the-Loop Review
Validated quizzes undergo a **manual quality check** before final approval.

### 7. Post-Processing and Storage
Approved quizzes are normalized and stored in **MongoDB**, marked as deployment-ready.

### 8. User Interface
A **Streamlit-based UI** enables document upload, quiz generation, and validation monitoring.

---

## Technology Stack

- **Python**
- **Pydantic**
- **LangChain**
- **Chroma Vector Database**
- **Large Language Models (LLMs)**
- **MongoDB**
- **Streamlit**

---

## Output Format

- Structured **JSON**
- Schema-validated quiz data
- Ready for integration into APIs or learning platforms

---

## Use Cases

- Educational technology platforms  
- Automated assessment systems  
- Personalized learning tools  
- AI-assisted content authoring  

---

## Project Status

- Production-ready architecture  
- Modular and scalable design  
- Easy to extend and customize  

---

## Future Enhancements

- REST API support  
- Role-based access control  
- Difficulty-level tuning  
- Analytics and reporting dashboard  

---
