# **RAG Chatbot for the Constitution of India**

This project implements a chatbot capable of answering queries related to the Constitution of India. It uses **Retrieval-Augmented Generation (RAG)**, combining retrieval techniques and generative models to provide accurate, context-aware answers. The chatbot simplifies understanding legal texts for students, researchers, and legal professionals.

## **Features**
- Answers questions about the Constitution of India.
- Utilizes **sentence embeddings** for semantic understanding.
- Generates responses using a **transformer-based language model**.
- Interactive **Streamlit web interface** for easy user access.
- Employs **ChromaDB** for fast and efficient similarity-based document retrieval.

---

## **Table of Contents**
1. [Technologies Used](#technologies-used)
2. [Installation](#installation)
3. [How to Use](#how-to-use)
4. [Architecture Overview](#architecture-overview)
5. [Screenshots](#screenshots)
6. [Future Improvements](#future-improvements)
7. [License](#license)

---

## **Technologies Used**
- **Python 3.8+**
- **PyPDF2**: For extracting text from PDF files.
- **Sentence Transformers**: For creating document embeddings.
- **ChromaDB**: For storing and querying document embeddings.
- **Transformers (Hugging Face)**: For generating human-like responses.
- **Streamlit**: For building the web-based user interface.
- **Torch**: For supporting the transformer models.

---

## **Installation**

Follow these steps to set up the project on your local machine:

### **1. Clone the Repository**
```bash
git clone https://github.com/your-username/rag-chatbot.git
cd rag-chatbot
```

### **2. Create a Virtual Environment**
```bash
python -m venv venv
source venv/bin/activate  # For Linux/MacOS
venv\Scripts\activate     # For Windows
```

### **3. Install Required Libraries**
Install the dependencies listed in `requirements.txt`:
```bash
pip install -r requirements.txt
```

### **4. Add the Constitution PDF**
Place the `constitution_of_india.pdf` file in the project root directory.

---

## **How to Use**

### **1. Start the Streamlit App**
Run the Streamlit server:
```bash
streamlit run app.py
```

### **2. Open the Web Interface**
Once the server is running, a browser window will open at `http://localhost:8501`. If it doesn’t, manually open this URL in your browser.

### **3. Interact with the Chatbot**
- Type your query in the text box (e.g., *"What is Article 370?"*).
- The chatbot retrieves relevant information from the Constitution and provides a response.

---

## **Architecture Overview**

1. **PDF Text Extraction**: 
   - **Tool**: PyPDF2
   - **Function**: Extracts text content from the Constitution PDF.
2. **Document Embedding**:
   - **Tool**: Sentence Transformers (all-MiniLM-L6-v2)
   - **Function**: Converts text into embeddings for similarity-based search.
3. **Vector Database**:
   - **Tool**: ChromaDB
   - **Function**: Stores embeddings and enables efficient querying.
4. **Query Processing**:
   - **Function**: Matches user queries with stored embeddings to fetch relevant sections.
5. **Response Generation**:
   - **Tool**: GPT-Neo
   - **Function**: Generates human-like responses based on retrieved content.
6. **User Interface**:
   - **Tool**: Streamlit
   - **Function**: Provides an interactive web interface for user interaction.

---

## **Screenshots**

### **Home Page**
![Home Page](https://via.placeholder.com/800x400?text=Screenshot+Coming+Soon)

### **Query Response Example**
![Query Response](https://via.placeholder.com/800x400?text=Screenshot+Coming+Soon)

---

## **Future Improvements**
- **Multilingual Support**: Enable querying in multiple Indian languages.
- **Enhanced Retrieval**: Add more advanced semantic search techniques.
- **Scaling**: Deploy on a cloud platform like AWS, Streamlit Cloud, or Google Cloud.
- **User Authentication**: Allow personalized user sessions.
- **Real-Time Updates**: Integrate updates for constitutional amendments.

---

## **License**
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## **Contributors**
- **Shubhi Pandey** (Developer)

For any queries or contributions, feel free to contact me at: [pandeyshubhi2605@gmail.com].

