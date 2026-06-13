# Vision-to-RAG Prompt Builder for Energy Billing

**Special Challenge by ΔΕΗ/PPC | ACE AI Hackathon 2026**

# Team
* **Aggelos Ladas**, Computer Engineer – [LinkedIn](https://www.linkedin.com/in/AggelosLadasDev) | [GitHub](https://github.com/AggelosLadas)
* **Anastasia Andromida**, AI Developer – [LinkedIn](https://www.linkedin.com/in/anastasia-andromida-14ab7a227/) | [GitHub](https://github.com/anastasia230)
* **Vasileios Kotronis**, Electrical and Computer Engineer – [LinkedIn](https://www.linkedin.com/in/vasileios-kotronis-998909344/) | [GitHub](https://github.com/ntua-el21432)


# Info
An AI-powered system that combines OCR, Retrieval-Augmented Generation (RAG), and hybrid retrieval techniques to analyze energy bills and generate automated insights. Developed as part of the ΔΕΗ/PPC Special Challenge during the ACE AI Hackathon 2026.

![Vision-to-RAG Interface](data/IMG_20260309_171106.jpg)

## Technologies

* Python
* LangChain
* Streamlit
* Retrieval-Augmented Generation (RAG)
* Tesseract OCR
* Azure AI Search
* FastAPI

---

# Getting Started

## 1. Clone the Repository

```bash
git clone <repository-url>
cd <repository-name>
```

## 2. Create a Virtual Environment

```bash
python -m venv venv
```

## 3. Verify Python Version

Open `venv/pyvenv.cfg` and ensure the environment is using **Python 3.12.6**.

> The project depends on several libraries that may behave differently across Python versions, so using the recommended version is strongly advised.

## 4. Activate the Environment

Windows:

```bash
.\venv\Scripts\activate
```

Linux/macOS:

```bash
source venv/bin/activate
```

## 5. Install Dependencies

Make sure you are using an up-to-date version of pip:

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

## 6. Configure Environment Variables

Create a `.env` file in the project root and add the required API keys and environment variables.

## 7. Build the Knowledge Base

Run the ingestion pipeline:

```bash
python ingest.py
```

This process creates and populates the vector database used by the RAG pipeline.

## 8. Launch the Application

```bash
streamlit run app.py --server.port 8888
```

If everything is configured correctly, the demo interface should now be available locally.

---

# Project Structure

### `data/`

Contains source datasets, customer information, and billing-related documents used by the system.

### `knowledge_base/`

Stores PDFs, text files, and reference material that are processed by the ingestion pipeline and indexed into the vector database.

### `ingest.py`

Builds and updates the knowledge base by processing documents and generating vector embeddings.

### `app.py`

Main Streamlit application containing the user interface and overall workflow.

### `utils/helpers.py`

Utility functions and helper methods used throughout the application.

### `api.py`

Contains the exposed API endpoints for external integrations and service communication.

---

# Team

Created for the ACE AI Hackathon 2026.

