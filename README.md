# CreativeGen Background Removal API

AI-powered background removal service for packshot images using FastAPI and rembg.

## 🌟 Features

- **Single Image Processing**: Remove background from individual images
- **Batch Processing**: Process up to 10 images simultaneously
- **Docker Support**: Easy deployment with Docker

## 🚀 Quick Start

### Prerequisites

- Python 3.10 or higher
- pip (Python package manager)

### Local Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd <repository-name>
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   ```

3. **Activate the virtual environment**
   
   On Windows:
   ```bash
   venv\Scripts\activate
   ```
   
   On macOS/Linux:
   ```bash
   source venv/bin/activate
   ```

4. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

5. **Run the application**
   ```bash
   python main.py
   ```
   
   Or using uvicorn directly:
   ```bash
   uvicorn main:app --reload --host 0.0.0.0 --port 8000
   ```

6. **Access the API**
   - API: http://localhost:8000
   - Interactive API docs: http://localhost:8000/docs
   - Alternative API docs: http://localhost:8000/redoc



## 🔧 Configuration

### File Limits
- **Max File Size**: 10MB per image
- **Allowed Formats**: PNG, JPG, JPEG, WEBP
- **Batch Limit**: 10 images per request

### Environment Variables
- `PORT`: Server port (default: 8000)

## 📦 Dependencies

- **FastAPI**: Modern web framework for building APIs
- **rembg**: AI-powered background removal
- **Pillow**: Image processing library
- **uvicorn**: ASGI server
- **onnxruntime**: Runtime for AI models

## 🛠️ Development

### Project Structure
```
.
├── main.py              # Main application file
├── requirements.txt     # Python dependencies
├── Dockerfile          # Docker configuration
├── .gitignore          # Git ignore rules
└── README.md           # This file
```



## 📝 Notes

- First request may take longer as the AI model is downloaded and cached
- CORS is configured to allow all origins (`*`) - update this in production for security
- The API uses the u2net model from rembg for background removal

