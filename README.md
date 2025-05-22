# <a name="mcq-generator"></a> QuizzyBee: Automatically Create Multiple-Choice Questions from Uploaded Text Documents

## Table of Contents
- [Code Overview and Breakdown](#code-overview-and-breakdown) 
- [Skills Acquired](#skills-acquired)
- [Technologies Used](#technologies-used)
- [How To Run the Code](#how-to-run-the-code)
- [Contributing](#contributing)

## <a name="detailed-breakdown"></a> Code Overview and Breakdown

This project is an AI-powered web application designed to generate multiple-choice questions (MCQs) from text documents, using Streamlit as the web interface and Google’s Gemini-1.5 Pro AI model for generating questions. Users can upload files (PDF, DOCX, or TXT), and the application extracts text from the document, processes it, and generates a specified number of MCQs with four answer options (A-D). The correct answer is also provided for each question.

The project is divided into several major segments:

1. **File Upload and Text Extraction**

This part allows users to upload files in multiple formats, including PDF, TXT, and DOCX. It extracts text from the files using libraries like pdfplumber (for PDF) and python-docx (for DOCX).

<img width="722" alt="MCQ-Generator" src="https://github.com/Dev-Godswill/picture-files/blob/main/19.png?raw=true">

2. **MCQ Generation Using AI**

The Google Generative AI (Gemini model) is used to generate MCQs from the extracted text. The code sends a formatted prompt to the AI model, asking it to generate a specified number of questions.

<img width="722" alt="MCQ-Generator" src="https://github.com/Dev-Godswill/picture-files/blob/main/20.png?raw=true">

3. **Displaying and Downloading MCQs**

Once the MCQs are generated, they are displayed on the webpage, and users can download them as either a TXT or PDF file. The PDF generation is handled using the FPDF library.

<img width="722" alt="MCQ-Generator" src="https://github.com/Dev-Godswill/picture-files/blob/main/21.png?raw=true">

4. **Web Application Interface**

The user interface is built using Streamlit, which allows for interactive web apps in Python. Users can upload files, select the number of questions, and regenerate questions if needed. The results are displayed directly in the app.

<img width="722" alt="MCQ-Generator" src="https://github.com/Dev-Godswill/picture-files/blob/main/22.png?raw=true">

## Skills Acquired:
* **Text Processing:** Handling text extraction from multiple file formats (PDF, DOCX, TXT).
* **API Integration:** Integrating Google’s Generative AI API for content generation.
* **Web Development with Streamlit:** Building interactive web apps with file uploads, user inputs, and downloadable results.
* **PDF Generation:** Utilizing FPDF to convert generated questions into a professional-looking PDF.
* **Error Handling:** Managing different file encodings and edge cases during text extraction.

## Technologies Used
* **Streamlit:** Used to create the web interface for uploading documents, interacting with users, and displaying MCQs.
* **pdfplumber:** A library for extracting text from PDF documents.
* **python-docx:** Extracts text from DOCX (Microsoft Word) files.
* **FPDF:** A lightweight library to generate PDF files.
* **Google Generative AI (Gemini Model):** This API is used to generate the actual MCQs from the text provided by the user.
* **OS Module:** Handles file paths and directory creation.

## How To Run the Code
To run the code on your local machine, follow these steps:

**Step 1: Clone the Repository and Install Requirements**

1. Clone the project repository or copy the code to your local machine.
2. Ensure you have Python installed.
3. Create a virtual environment (optional but recommended):

<img width="722" alt="MCQ-Generator" src="https://github.com/Dev-Godswill/picture-files/blob/main/23.png?raw=true">

    Then, activate the virtual environment:
      **Windows:** env\Scripts\activate
      **Mac/Linux:** source env/bin/activate
      
4. Install the required Python libraries. If you have a requirements.txt file (as you do), you can install the dependencies directly:

<img width="722" alt="MCQ-Generator" src="https://github.com/Dev-Godswill/picture-files/blob/main/24.png?raw=true">

**Step 2: Set up API Key**
The project requires an API key to access Google’s Generative AI model. You must set up your **Google API Key** and place it in your environment as follows:

1. Go to Google Cloud Console and generate an API key for the Gemini Model.
2. Update the code where the GOOGLE_API_KEY is required:

<img width="722" alt="MCQ-Generator" src="https://github.com/Dev-Godswill/picture-files/blob/main/25.png?raw=true">

**Step 3: Run the Streamlit Application**
Once the environment is set up and dependencies are installed, run the Streamlit web app using the following command:

<img width="722" alt="MCQ-Generator" src="https://github.com/Dev-Godswill/picture-files/blob/main/26.png?raw=true">

Replace your_script_name.py with the name of the script that contains the code above.

**Step 4: Access the Web Interface**
After running the Streamlit app, a URL will be provided in your terminal (usually http://localhost:8501). Open this in your web browser to start using the MCQ generator.

**Step 5: Upload Files and Generate MCQs**
* Upload a text document in PDF, DOCX, TXT or image format
* Specify the number of questions you want to generate or the number of points.
* Download the MCQs as TXT or PDF files.
* Translation to Hindi available
* Focus Mode enabled

## <a name="extra-features"></a>✨ Additional Features

Beyond core MCQ generation, QuizzyBee offers powerful study tools:

| Feature | Description | Icon |
|---------|-------------|------|
| **Short Notes Generator** | AI-powered concise summaries of uploaded content | 📝 |
| **Hindi Translation** | Instantly translates generated content to Hindi | 🌐 |
| **Focus Mode Timer** | Built-in Pomodoro timer (25/5 min intervals) | ⏱️ |
| **Multi-Format OCR** | Reads text from images (PNG/JPG) and scanned PDFs | 📸 |
| **Difficulty Levels** | Adjust output complexity (Easy/Moderate/Hard) | 🎚️ |
| **Export Options** | Download as PDF (formatted) or TXT | 💾 |
| **Progress Tracking** | Visual timer with completion percentage | 📊 |

**Why these matter?**
- Makes learning more accessible (Hindi support)
- Boosts productivity (Focus Mode)
- Handles real-world documents (images/scans)
- Adapts to different skill levels


## <a name="extra-features"></a>🌟 Extended Feature Set

### 1. Multi-Format Content Processing
- **Image OCR Support**: 
  - Uses Tesseract OCR engine to extract text from images (PNG/JPG)
  - Handles scanned documents in PDFs by processing embedded images
  - Automatic language detection for multilingual documents
- **Document Parsing**:
  - PDF text extraction via pdfplumber (preserves layout)
  - DOCX parsing with python-docx (retains formatting)
  - Fallback encoding support for legacy TXT files

### 2. Advanced Study Tools
#### Short Notes Generator
- **AI Summarization**: 
  - Creates bullet-point summaries from source material
  - Adjusts length based on user-selected complexity
  - Preserves key terminologies and concepts
- **Output Formatting**:
  - Hierarchical organization (main points → subpoints)
  - Highlighted key terms

#### Hindi Translation
- **Full Workflow Integration**:
  - Uses Google Translate API for accurate translations
  - Preserves MCQ formatting during translation
  - Handles technical/specialized vocabulary

### 3. Productivity Enhancements
#### Focus Mode Timer
- **Customizable Intervals**:
  - Default 25/5 Pomodoro cycle
  - Adjustable work/break durations
- **Visual Feedback**:
  - Progress bar with percentage completion
  - Color-coded time remaining indicators
  - End-of-session notification system

### 4. Customization Options
- **Difficulty Scaling**:
  - Easy: Basic recall questions
  - Moderate: Application-based questions
  - Hard: Analysis/synthesis questions
- **Output Control**:
  - Number of items (1-20 adjustable)
  - PDF/TXT format selection
  - Font size customization in PDF exports

### 5. Technical Capabilities
- **Batch Processing**:
  - Handles multiple files sequentially
  - Maintains separate outputs per document
- **Error Handling**:
  - Graceful OCR fallback for poor-quality images
  - Encoding detection for text files
  - API failure recovery mechanisms

### 6. Accessibility Features
- **Bilingual Interface**:
  - English-Hindi toggle (UI coming in v2.0)
- **Low-Vision Support**:
  - High-contrast PDF outputs
  - Adjustable text sizes

