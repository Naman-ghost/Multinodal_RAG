# 🔍 Multimodal RAG on a PDF using LangChain & GPT-4 Vision

This project demonstrates how to build a **multimodal Retrieval-Augmented Generation (RAG)** pipeline that extracts and summarizes **text** and **images** from a single online PDF. It leverages:

- 📘 **LangChain** for prompt orchestration  
- 🧠 **OpenAI GPT-4 Vision** for understanding images  
- 📄 **PyMuPDF** for PDF parsing  
- 🧰 **Unstructured** (optional) for advanced document parsing

We apply this to a physics document on **Kinematics**, showing how you can combine visual and textual context for smarter AI-powered insights.

---

## 📌 What It Does

- Downloads a **PDF from a URL**
- Extracts **text** and **images**
- Sends images to **GPT-4 Vision** for **diagram-aware summarization**
- Prints a combined textual and visual summary

---

## 🛠️ Installation

```bash
pip install openai langchain unstructured PyMuPDF requests
```

---

## 🔑 API Key Setup

You'll need an OpenAI API key with access to GPT-4-Vision. Set it in your environment:

```bash
export OPENAI_API_KEY=your-key-here
```

Or within your script:

```python
import os
os.environ["OPENAI_API_KEY"] = "your-key-here"
```

---

## 🚀 Usage

Run the Python script:

```bash
python multimodal_rag.py
```

It will:

1. Download the PDF from:
   ```
   https://www.uvm.edu/~ldonfort/P21S20/2_Kinematics.pdf
   ```
2. Extract images and text.
3. Use **GPT-4 Vision** to describe figures, graphs, and plots in a research-aware way.
4. Print both text and image summaries to your terminal.

---

## 📂 Project Structure

```
multimodal_rag.py     # Single file RAG pipeline
README.md             # You're reading it
```

---

## 🧠 Example Use Cases

- Summarize **scientific papers** with equations and plots  
- Query **technical manuals** with diagrams  
- Understand **PDFs with charts, forms, or handwritten notes**  
- Combine **visual + textual** features in smart assistants

---

## 📈 Sample Output

```
=== TEXT SUMMARY ===
Page 1: ... basic concepts of displacement, velocity ...
Page 2: ... graphical representation of motion ...

=== IMAGE SUMMARIES ===
--- Image 1 ---
This plot shows a velocity vs time graph. The curve suggests constant acceleration...
```

---

## 🔒 License

MIT License

---

## 🙋‍♂️ Questions?

Feel free to open an issue or discussion for help adapting this to:
- Local PDF files
- Multiple PDFs
- Vector databases like FAISS or Chroma
