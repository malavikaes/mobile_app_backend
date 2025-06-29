# Voice Recognition Backend

A Node.js backend for voice recognition and processing with MySQL database integration.

## Features

- Audio file upload and processing
- Speech-to-text transcription
- MySQL database integration
- Selenium automation
- RESTful API endpoints

## Deployment to Render

### 1. Create a Render Account
- Go to [render.com](https://render.com)
- Sign up for a free account

### 2. Create a New Web Service
- Click "New +" → "Web Service"
- Connect your GitHub repository
- Select the `cloud-backend` directory

### 3. Configure Environment Variables
Add these environment variables in Render dashboard:

```
DB_HOST=88.150.227.117
DB_USER=nrktrn_web_admin
DB_PASSWORD=GOeg&*$*657
DB_PORT=3306
DB_NAME=nrkindex_trn
PORT=10000
NODE_ENV=production
CORS_ORIGIN=*
```

### 4. Build Settings
- **Build Command**: `npm install`
- **Start Command**: `npm start`
- **Node Version**: 18.x or higher

### 5. Deploy
- Click "Create Web Service"
- Wait for deployment to complete
- Copy the provided URL (e.g., `https://your-app.onrender.com`)

## API Endpoints

- `POST /upload` - Upload audio file
- `POST /login` - User authentication
- `POST /insert` - Process text data
- `GET /notifications` - Get notifications
- `POST /notifications` - Create notification
- `DELETE /notification/:id` - Delete notification
- `GET /test` - Health check

## Local Development

1. Install dependencies:
   ```bash
   npm install
   ```

2. Create `.env` file (copy from `env.example`)

3. Start server:
   ```bash
   npm start
   ```

## Dependencies

- Express.js
- MySQL2
- Multer (file uploads)
- FFmpeg (audio processing)
- CORS
- OpenAI Whisper (speech recognition) 