# Video to Reel Generator

## Overview
The **Video to Reel Generator** is an AI-powered tool that automatically converts long-form videos into short-form reels with captions, highlights, and thumbnails. It leverages FastAPI for the backend and integrates AI models to generate engaging short-form content.

## Features
- Extracts short clips from long-form videos based on AI-generated highlights.
- Adds AI-generated captions and subtitles.
- Generates engaging thumbnails.
- Provides an API for automation and integration.

## Tech Stack
- **Backend**: FastAPI (Python)
- **AI Models**: LLMs/GenAI for captions and highlights
- **Frontend**: Optional (React/Vue.js for UI)
- **Storage**: Local/MongoDB/PostgreSQL (for metadata and processed files)
- **Processing**: FFMPEG, OpenCV

## Installation
```sh
# Clone the repository
git clone https://github.com/your-username/video-to-reel-generator.git
cd video-to-reel-generator

# Create and activate a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

# Install dependencies
pip install -r requirements.txt
```

## Usage
### 1. Run the FastAPI Server
```sh
uvicorn app.main:app --host 0.0.0.0 --port 8000 --reload
```
The API will be available at `http://localhost:8000/docs`

### 2. Process a Video
#### API Endpoint:
`POST /process-video`

#### Request Body:
```json
{
  "video_url": "https://example.com/video.mp4",
  "duration": 30,
  "custom_captions": true,
  "thumbnail": true
}
```

#### Response:
```json
{
  "status": "success",
  "reel_url": "https://your-storage.com/output.mp4",
  "thumbnail_url": "https://your-storage.com/thumbnail.jpg"
}
```

## Customization
- Modify **caption styles** in `config/captions.json`
- Adjust **video processing parameters** in `config/settings.json`
- Use **custom AI models** by replacing the LLM integration in `app/utils.py`

## Contributing
1. Fork the repo & clone locally
2. Create a feature branch (`git checkout -b feature-name`)
3. Commit changes (`git commit -m 'Add feature'`)
4. Push to your fork & create a PR

## License
This project is licensed under the MIT License.

## Contact
For issues and support, open an issue on GitHub or contact mohansivatejakavvala2011@gmail.com.

