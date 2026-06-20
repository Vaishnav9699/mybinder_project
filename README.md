#     AI Clipper 

An automated pipeline that takes long-form movies, dynamically detects high-interest scenes using AI, and automatically cuts them into short, engaging clips optimized for social media platforms.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Vaishnav/antigravity-ai-clipper/HEAD)

---

## What It Does

* **Intelligent Scene Detection:** Automatically scans long video files to pinpoint high-leverage timestamps and cinematic spikes.
* **Local-First Transcription:** Leverages Faster-Whisper locally to process audio data rapidly without accumulating massive cloud transcription bills.
* **Context-Aware Trimming:** Utilizes advanced LLM context processing to ensure clips are cut precisely where dialogue or narrative action naturally starts and ends.

## Tech Stack

* **Frontend:** Next.js, React, Tailwind CSS
* **Backend / Database:** Node.js, Supabase
* **Infrastructure:** Docker (for fully containerized, isolated processing)
* **AI / Processing:** Faster-Whisper, Gemini 3.1 Flash API

---

## Getting Started

Follow these steps to get a local development copy running on your machine.

### Prerequisites

Make sure you have these installed before moving forward:
* [Node.js](https://nodejs.org/) (v18 or higher recommended)
* [Docker](https://www.docker.com/) (Highly recommended for isolated background video processing)

### Setup & Installation

1. Clone the repo:
   bash this in your terminal any where 
   git clone [https://github.com/Vaishnav/antigravity-ai-clipper.git](https://github.com/Vaishnav/antigravity-ai-clipper.git)
   cd antigravity-ai-clipper
   Install dependencies:

Bash
npm install
Set up your environment variables:
Create a .env file in the root directory and add your keys.

Code snippet
NEXT_PUBLIC_SUPABASE_URL=your_supabase_project_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_public_key
GEMINI_API_KEY=your_gemini_3.1_flash_api_key
Run the local dev server:

Bash
npm run dev
Open http://localhost:3000 in your browser to see the application.

Running with Docker
To run the entire processing pipeline inside a fully isolated environment without installing video dependencies locally:

Build the image:

Bash
docker build -t antigravity-clipper .
Run the container:

Bash
docker run -p 3000:3000 --env-file .env antigravity-clipper
How to Contribute
If you find a bug or have an idea for an optimization, feel free to open an issue or submit a pull request:

Fork the project.

Create your feature branch (git checkout -b feature/AmazingFeature).

Commit your changes (git commit -m 'Add some AmazingFeature').

Push to the branch (git push origin feature/AmazingFeature).

Open a Pull Request.
