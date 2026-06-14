# Code Plagiarism Detection Tool

## Repository

**Advanced Multi-Language Source Code Similarity & Plagiarism Detection System**

### Repository

GitHub Repository

```bash
git clone https://github.com/IkjyotKaur/Code-Plagiarism-Detection-Tool.git
cd Code_Plagiarism_Detection_Tool
```

A full-stack web application that detects plagiarism in source code files using lexical analysis, token similarity, AST comparison, compiler feature extraction, and advanced similarity metrics. The system generates detailed reports and plagiarism scores for academic and educational use.

---

## Tech Stack

| Layer         | Technologies                  |
| ------------- | ----------------------------- |
| Frontend      | HTML5, CSS3, JavaScript, Vite |
| Backend       | Node.js, Express.js           |
| Database      | SQLite (better-sqlite3)       |
| Security      | Helmet, CORS, Rate Limiter    |
| File Handling | Multer                        |
| Utilities     | UUID, dotenv                  |

---

## Project Structure

```text
Code_Plagiarism_Detection_Tool/
│
├── client/
│   ├── index.html
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── styles/
│   │   └── services/
│   ├── package.json
│   └── vite.config.js
│
├── server/
│   ├── src/
│   │   ├── controllers/
│   │   │   └── analysisController.js
│   │   │
│   │   ├── routes/
│   │   │   └── api.js
│   │   │
│   │   ├── services/
│   │   │   ├── tokenizer.js
│   │   │   ├── similarity.js
│   │   │   ├── astParser.js
│   │   │   ├── preprocessor.js
│   │   │   ├── normalizer.js
│   │   │   ├── compilerFeatures.js
│   │   │   └── reportGenerator.js
│   │   │
│   │   ├── db/
│   │   │   └── database.js
│   │   │
│   │   ├── utils/
│   │   │   └── languageDetector.js
│   │   │
│   │   └── index.js
│   │
│   └── package.json
│
├── sample-library/
│   ├── c/
│   ├── cpp/
│   └── python/
│
└── README.md
```

---

## Quick Start

### Backend

```bash
cd server
npm install
npm run dev
```

Backend runs on:

```text
http://localhost:5000
```

---

### Frontend

```bash
cd client
npm install
npm run dev
```

Frontend runs on:

```text
http://localhost:5173
```

---

## Environment Configuration

### Backend (.env)

```env
PORT=5000
DATABASE_URL=plagiarism.db
```

### Frontend

```env
VITE_API_URL=http://localhost:5000
```

---

## Features

### File Upload & Processing

* Upload multiple source code files
* Automatic language detection
* Batch file comparison

### Multi-Language Support

* C
* C++
* Python

### Similarity Analysis

* Token-Based Similarity
* AST-Based Structural Comparison
* N-Gram Analysis
* Cosine Similarity
* Longest Common Subsequence (LCS)
* Compiler Feature Matching

### Report Generation

* Similarity Percentage
* Detailed Comparison Report
* Plagiarism Ranking
* Analysis Statistics

### Database Storage

* Session Management
* Result Persistence
* Historical Reports

---

## Detection Pipeline

```text
Source Code Files
        │
        ▼
 Preprocessing
        │
        ▼
 Tokenization
        │
        ▼
 AST Generation
        │
        ▼
 Similarity Analysis
        │
        ▼
 Score Calculation
        │
        ▼
 Report Generation
```

---

## Similarity Techniques

### Lexical Analysis

Extracts tokens such as:

* Keywords
* Operators
* Identifiers
* Literals
* Delimiters

### Structural Analysis

Compares program structure using Abstract Syntax Trees (AST).

### N-Gram Similarity

Detects copied code segments and patterns.

### Cosine Similarity

Measures similarity between token frequency vectors.

### Longest Common Subsequence (LCS)

Finds longest matching token sequences.

### Compiler Feature Analysis

Compares:

* Loops
* Functions
* Conditionals
* Control Flow Structures

---

## API Endpoints

| Endpoint            | Purpose                   |
| ------------------- | ------------------------- |
| POST /upload        | Upload source code files  |
| POST /analyze       | Run plagiarism analysis   |
| GET /results/:id    | Retrieve analysis results |
| GET /report/:id     | Generate detailed report  |
| DELETE /session/:id | Delete stored session     |
| GET /health         | Server health check       |

---

## Sample Input

```c
int factorial(int n){
    if(n==0)
        return 1;
    return n * factorial(n-1);
}
```

### Output

```text
Compared Files:
factorial.c
factorial_copy.c

Similarity Score: 94%

Potential Plagiarism Detected

Matching Structures:
✓ Recursive Function
✓ Conditional Statement
✓ Return Pattern
```

---

## Educational Relevance

This project demonstrates practical implementation of:

* Compiler Design
* Lexical Analysis
* Tokenization
* Abstract Syntax Trees
* String Matching Algorithms
* Similarity Detection
* Data Structures & Algorithms
* Full Stack Web Development

---

## Future Enhancements

* AI-Based Plagiarism Detection
* Machine Learning Models
* PDF Report Export
* Real-Time Comparison
* User Authentication
* Dashboard Analytics
* Java Support
* JavaScript Support
* C# Support

---

## License

Educational and Academic Use Only.

---

## Support

If you found this project useful, consider giving it a ⭐ on GitHub.
