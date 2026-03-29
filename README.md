# 📄 DocuAgent

**DocuAgent** is an AI-powered document analysis and risk detection platform designed to automate the review of legal, business, and policy documents. It enables users to upload documents (PDF, DOCX, etc.) and leverages AI to generate summaries, extract key metadata, detect potential risks, and notify teams in real-time.

Built using **FastAPI, Next.js, and Azure OpenAI**, DocuAgent streamlines document workflows, making them faster, smarter, and more secure.

---

## 🚀 Features

### 📂 Document Management
- Upload documents in multiple formats (PDF, DOCX, TXT, CSV, Excel)
- Secure storage and retrieval

### 🤖 AI-Powered Analysis
- Automatic document summarization
- Metadata extraction (title, author, dates, etc.)
- Risk detection (legal, compliance, ethical issues)

### ☁️ Cloud Integration
- Azure Blob Storage for file storage
- Azure Cosmos DB for structured data

### 🔔 Real-Time Notifications
- Microsoft Teams integration
- Instant alerts with summaries and risk insights

### 📊 Dashboard & Insights
- View processed document statistics
- Monitor risks and processing time
- Access recent documents and reports

---

## 🏗️ Project Structure

DocuAgent/
│
├── docuagent-backend/ # FastAPI backend
│ ├── app.py
│ ├── services/
│ └── requirements.txt
│
├── docuagent-client/ # Next.js frontend
│ ├── pages/
│ ├── components/
│ └── package.json
│
└── README.md


---

## ⚙️ Tech Stack

- **Frontend**: Next.js, React
- **Backend**: FastAPI (Python)
- **AI**: Azure OpenAI
- **Database**: Azure Cosmos DB
- **Storage**: Azure Blob Storage
- **Notifications**: Microsoft Teams Webhooks
- **Deployment**: Docker, Vercel (optional)

---

## 🛠️ Getting Started

### 📌 Prerequisites

Make sure you have installed:

- Python 3.10+
- Node.js 16+
- npm / yarn
- Docker (optional)
- Azure account (for full functionality)


## 🔧 Backend Setup

```bash
cd docuagent-backend
pip install -r requirements.txt

````
## Create .env file:

```bash
AZURE_BLOB_CONN=your_blob_connection_string
AZURE_COSMOS_URI=your_cosmos_uri
AZURE_COSMOS_KEY=your_cosmos_key
AZURE_OPENAI_API_KEY=your_openai_key
AZURE_OPENAI_API_VERSION=2024-02-15-preview
AZURE_OPENAI_ENDPOINT=your_endpoint
TEAMS_WEBHOOK_URL=your_teams_webhook

````
### Run backend:

```bash
uvicorn app:app --host 0.0.0.0 --port 8000
```

### 👉 API Docs:
```bash
http://localhost:8000/docs
```

## 🎨 Frontend Setup

```bash
cd docuagent-client
npm install
```
### Create .env.local:
```bash
NEXT_PUBLIC_API_URL=http://localhost:8000
```
## Run frontend:
```bash
npm run dev
```

### 👉 Open in browser:
```bash
http://localhost:3000
```
## 🐳 Deployment

### Backend (Docker)
```bash
docker build -t docuagent-backend .
docker run -p 8000:8000 --env-file .env docuagent-backend
```

### Frontend (Production)
```bash
npm run build
npm start
```

## 🧪 Development Notes
* You can run the project in mock mode without Azure by using dummy .env values
* Azure services are required for:
    * File storage
    * AI analysis
    * Real-time notifications

## 📌 Future Improvements
* Role-based access control (RBAC)
* Multi-language document support
* Advanced analytics dashboard
* Integration with more collaboration tools

## 📄 License
This project is licensed under the MIT License.
See the LICENSE file for more details.

## 👨‍💻 Author
Vishnuka Yahan
Software Engineer | Flutter | MERN | Spring Boot


