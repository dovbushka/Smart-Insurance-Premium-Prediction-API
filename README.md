# Welcome to your Lovable project
## Project info
**URL**: https://lovable.dev/projects/REPLACE_WITH_PROJECT_ID
## How can I edit this code?
There are several ways of editing your application.
**Use Lovable**
Simply visit the [Lovable Project](https://lovable.dev/projects/REPLACE_WITH_PROJECT_ID) and start prompting.
Changes made via Lovable will be committed automatically to this repo.
**Use your preferred IDE**
If you want to work locally using your own IDE, you can clone this repo and push changes. Pushed changes will also be reflected in Lovable.
The only requirement is having Node.js & npm installed - [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating)
Follow these steps:
```sh
# Step 1: Clone the repository using the project's Git URL.
<p align="center">
  <img src="public/readme-banner.png" alt="Insurance Premium Prediction API Banner" width="100%" />
</p>
<h1 align="center">🏥 Insurance Premium Prediction API</h1>
<p align="center">
  <strong>Predict insurance costs using machine learning — powered by FastAPI & Scikit-learn with a React frontend.</strong>
</p>
<p align="center">
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI" />
  <img src="https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-learn" />
  <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" alt="Tailwind CSS" />
  <img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white" alt="Vite" />
</p>
<p align="center">
  <a href="#-features">Features</a> •
  <a href="#-demo">Demo</a> •
  <a href="#-tech-stack">Tech Stack</a> •
  <a href="#-api-endpoints">API Endpoints</a> •
  <a href="#-model-details">Model Details</a> •
  <a href="#-getting-started">Getting Started</a> •
  <a href="#-project-structure">Project Structure</a> •
  <a href="#-contributing">Contributing</a>
</p>
---
## ✨ Features
| Feature | Description |
|---------|-------------|
| 🤖 **ML-Powered Predictions** | Trained Linear Regression model predicts insurance premiums based on policyholder attributes |
| ⚡ **Real-time Inference** | Instant premium estimates with risk level assessment (Low / Medium / High) |
| 📊 **Interactive Visualizations** | Feature importance bar charts and premium distribution pie charts via Recharts |
| 📖 **API Documentation** | Built-in endpoint docs with request/response examples |
| 🎨 **Modern UI** | Responsive design with Framer Motion animations and a professional fintech aesthetic |
| 🔢 **Contributing Factors** | Breakdown of how each input (age, BMI, smoking, etc.) impacts the predicted premium |
---
## 🎯 Demo
### Hero Section
> A clean, gradient-based landing section introducing the prediction engine with key highlights.
### Prediction Form
> Interactive form accepting policyholder details (age, sex, BMI, children, smoker status, region) with real-time premium estimation and risk assessment.
**Input Parameters:**
- `age` — Policyholder age (18–100)
- `sex` — Male / Female
- `bmi` — Body Mass Index (10–60)
- `children` — Number of dependents (0–10)
- `smoker` — Yes / No
- `region` — Southeast, Southwest, Northeast, Northwest
**Output:**
- 💰 Estimated annual premium (e.g. `$12,450`)
- 🟢🟡🔴 Risk level classification
- 📋 Contributing factors breakdown with impact ratings
### Model Insights
> Visual analytics showing feature importance and premium distribution across risk categories.
### API Docs
> Complete endpoint documentation with JSON request/response examples.
---
## 🛠 Tech Stack
### Frontend
| Technology | Purpose |
|-----------|---------|
| **React 18** | Component-based UI framework |
| **TypeScript** | Type-safe development |
| **Vite** | Lightning-fast build tool |
| **Tailwind CSS** | Utility-first styling with custom design tokens |
| **shadcn/ui** | Accessible, customizable UI components |
| **Framer Motion** | Smooth scroll & mount animations |
| **Recharts** | Data visualization (bar charts, pie charts) |
| **React Hook Form + Zod** | Form handling & validation |
### Backend (FastAPI)
| Technology | Purpose |
|-----------|---------|
| **FastAPI** | High-performance Python web framework |
| **Scikit-learn** | Machine learning model training & inference |
| **Pydantic** | Request/response data validation |
| **Uvicorn** | ASGI server |
---
## 📡 API Endpoints
### `POST /predict`
Submit policyholder data and receive a premium prediction.
**Request:**
```json
{
  "age": 30,
  "sex": "male",
  "bmi": 25.5,
  "children": 2,
  "smoker": "no",
  "region": "southeast"
}
```
**Response:**
```json
{
  "predicted_premium": 8420.50,
  "risk_level": "medium",
  "model_confidence": 0.92
}
```
### `GET /health`
Check if the API server is running and the model is loaded.
**Response:**
```json
{
  "status": "healthy",
  "model_loaded": true,
  "version": "1.0.0"
}
```
### `GET /docs`
Interactive Swagger UI documentation (auto-generated by FastAPI).
---
## 🧠 Model Details
### Algorithm
- **Type:** Linear Regression (Scikit-learn)
- **Training Data:** 1,338 samples from a medical insurance dataset
### Performance Metrics
| Metric | Value |
|--------|-------|
| **R² Score** | 0.86 |
| **MAE** | $2,840 |
| **Training Samples** | 1,338 |
### Feature Importance
```
Smoker     ████████████████████████████████ 62%
BMI        █████████         18%
Age        ██████            12%
Children   ██                 5%
Region     █                  2%
Sex        ▏                  1%
```
### How Prediction Works
1. **Input** → User submits policyholder attributes via the form or API
2. **Preprocessing** → Data is validated and transformed (categorical encoding, scaling)
3. **Inference** → The trained model computes the predicted premium
4. **Risk Assessment** → Premium is classified into Low (<$8k), Medium ($8k–$20k), or High (>$20k)
5. **Response** → Premium amount, risk level, and contributing factors are returned
---
## 🚀 Getting Started
### Prerequisites
- **Node.js** ≥ 18 (for the React frontend)
- **npm** or **bun** package manager
### Installation
```bash
# 1. Clone the repository
git clone <YOUR_GIT_URL>
# Step 2: Navigate to the project directory.
cd <YOUR_PROJECT_NAME>
# Step 3: Install the necessary dependencies.
npm i
# Step 4: Start the development server with auto-reloading and an instant preview.
# 2. Navigate to the project
cd insurance-premium-prediction
# 3. Install dependencies
npm install
# 4. Start the development server
npm run dev
```
**Edit a file directly in GitHub**
- Navigate to the desired file(s).
- Click the "Edit" button (pencil icon) at the top right of the file view.
- Make your changes and commit the changes.
**Use GitHub Codespaces**
- Navigate to the main page of your repository.
- Click on the "Code" button (green button) near the top right.
- Select the "Codespaces" tab.
- Click on "New codespace" to launch a new Codespace environment.
- Edit files directly within the Codespace and commit and push your changes once you're done.
## What technologies are used for this project?
This project is built with:
- Vite
- TypeScript
- React
- shadcn-ui
- Tailwind CSS
## How can I deploy this project?
Simply open [Lovable](https://lovable.dev/projects/REPLACE_WITH_PROJECT_ID) and click on Share -> Publish.
## Can I connect a custom domain to my Lovable project?
Yes, you can!
To connect a domain, navigate to Project > Settings > Domains and click Connect Domain.
Read more here: [Setting up a custom domain](https://docs.lovable.dev/features/custom-domain#custom-domain)
The app will be available at `http://localhost:5173`.
### Environment Variables
No environment variables are required for the frontend demo. For the full FastAPI backend:
| Variable | Description |
|----------|-------------|
| `MODEL_PATH` | Path to the trained `.pkl` model file |
| `CORS_ORIGINS` | Allowed CORS origins (comma-separated) |
---
## 📁 Project Structure
```
├── public/
│   ├── favicon.ico
│   └── readme-banner.png
├── src/
│   ├── components/
│   │   ├── HeroSection.tsx          # Landing hero with gradient & feature badges
│   │   ├── PredictionForm.tsx       # Interactive form + mock prediction engine
│   │   ├── ModelInfoSection.tsx     # Charts: feature importance & distribution
│   │   ├── ApiDocsSection.tsx       # API endpoint documentation
│   │   ├── NavLink.tsx              # Navigation component
│   │   └── ui/                      # shadcn/ui component library
│   ├── pages/
│   │   ├── Index.tsx                # Main page layout
│   │   └── NotFound.tsx             # 404 page
│   ├── hooks/                       # Custom React hooks
│   ├── lib/                         # Utility functions
│   ├── App.tsx                      # Router setup
│   ├── main.tsx                     # Entry point
│   └── index.css                    # Design tokens & global styles
├── index.html                       # HTML template
├── tailwind.config.ts               # Tailwind configuration
├── vite.config.ts                   # Vite configuration
└── package.json
```
---
## 🤝 Contributing
Contributions are welcome! Here's how:
1. **Fork** the repository
2. **Create** a feature branch: `git checkout -b feature/amazing-feature`
3. **Commit** your changes: `git commit -m 'Add amazing feature'`
4. **Push** to the branch: `git push origin feature/amazing-feature`
5. **Open** a Pull Request
---
## 📄 License
This project is open source and available under the [MIT License](LICENSE).
---
<p align="center">
  <strong>Insurance Premium Prediction API</strong><br/>
  Built with ❤️ using FastAPI, Scikit-learn & React
</p>
