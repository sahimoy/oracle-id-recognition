# Oracle ID Recognition

AI-powered recognition of Mexican identity documents. Upload a photo of an **INE**, **passport** or **driver's license**, and the app extracts the key fields into structured data in seconds, with a confidence score for each result.

I built it as a working prototype to show executives how AI can automate identity capture in onboarding, hiring and customer registration.

## What it does

- **Reads Mexican ID documents:** INE (including CURP and Clave de Elector), passports and driver's licenses
- **Extracts structured data:** full name, date of birth, nationality, address, issue and expiry dates, and document numbers
- **Scores confidence** for every extraction, so low-quality images are easy to spot
- **Bulk processing:** drop a whole folder of documents and the app processes them one by one
- **Excel export:** download all results as a spreadsheet, ready for the next system

## How it works

- **Frontend:** a single HTML page with drag-and-drop upload
- **Backend:** a small Node.js / Express server that forwards each image to Claude Vision (Anthropic API)
- **Security:** each user enters their own Anthropic API key in the browser. The key is never stored in the code or on the server.

## Run it locally

```bash
git clone https://github.com/sahimoy/oracle-id-recognition.git
cd oracle-id-recognition
npm install
node server.js
```

Open http://localhost:3333, enter your Anthropic API key (get one at console.anthropic.com), and upload a document.

## Built by

Sahi Camacho Moy · [LinkedIn](https://www.linkedin.com/in/mba-sahi-camacho-moy-9399823)
