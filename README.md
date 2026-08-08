# Script2Screen: AI Video Generation and YouTube Automation

An automated **text-to-video workflow** built with **n8n** that transforms plain text into an animated video with AI-generated voice narration and automatically uploads the final video to YouTube.

The workflow combines AI video generation, audio processing, video processing, and YouTube automation into a single pipeline with minimal manual intervention.

## Overview

Script2Screen automates the process of converting a text-based idea or script into a complete video.

The workflow handles the major stages of video production:

1. Receive the input text.
2. Prepare the video-generation request.
3. Generate an AI video.
4. Wait for the video-generation process to complete.
5. Retrieve the generated video.
6. Process the generated video and audio.
7. Merge the video and audio using FFmpeg.
8. Prepare the final video.
9. Upload the completed video to YouTube.

## Workflow

```text
Input Text
    |
    v
n8n Workflow Trigger
    |
    v
Prepare Input Data
    |
    v
AI Video Generation
    |
    v
Wait for Generation
    |
    v
Check Generation Status
    |
    v
Retrieve Video
    |
    v
Process Video & Audio
    |
    v
Merge Using FFmpeg
    |
    v
Final Video
    |
    v
YouTube Upload
```

## Key Features

* Automated text-to-video generation
* AI-generated video content
* AI voice narration
* Automated video and audio processing
* FFmpeg-based audio and video merging
* Generation-status monitoring
* Automatic retrieval of generated media
* Webhook or manual workflow triggering
* Automatic YouTube upload
* End-to-end workflow automation

## Technologies Used

### n8n

The workflow is built using **n8n**, an open-source workflow automation platform.

n8n connects the different services and controls the complete video-generation pipeline.

### AI Video Generation API

An AI video generation service is used to create the visual content from the provided input.

### HTTP Requests

HTTP Request nodes are used to communicate with external APIs for:

* Starting video generation
* Checking generation status
* Retrieving generated media

### JavaScript

JavaScript Code nodes are used within the workflow for processing and transforming data.

### FFmpeg

FFmpeg is used to process and merge the generated video and audio into the final video file.

### YouTube Data API

The YouTube Data API is used to automatically upload the completed video to a YouTube channel.

## Repository Structure

```text
script2screen/
│
├── animatedvideo-voiceover-youtube.json
├── picture of project.png
└── README.md
```

## Workflow File

The main workflow is stored in:

```text
animatedvideo-voiceover-youtube.json
```

This JSON file contains the complete n8n workflow and can be imported into an n8n instance.

## Prerequisites

Before running the workflow, make sure you have:

* n8n installed or access to an n8n instance
* An AI video generation API
* AI video generation API credentials
* YouTube Data API credentials
* FFmpeg installed and accessible
* An active internet connection

## Setup

### 1. Install n8n

Set up an n8n environment either locally or through a hosted instance.

### 2. Install FFmpeg

FFmpeg is required for processing and merging the generated video and audio.

Verify the installation:

```bash
ffmpeg -version
```

### 3. Configure API Credentials

Configure the required credentials inside n8n.

The workflow requires:

```text
AI Video Generation API
YouTube Data API
```

Keep API keys and credentials private and do not commit them directly to a public repository.

### 4. Import the Workflow

Open n8n and import:

```text
animatedvideo-voiceover-youtube.json
```

After importing the workflow, configure the required credentials and API settings.

### 5. Configure YouTube

Connect your YouTube account through the appropriate YouTube credentials in n8n.

The workflow can then upload the generated video automatically after the video-processing stage is completed.

## How to Use

### Step 1: Provide Input

Enter the text or script that will be used as the basis for the video.

### Step 2: Start the Workflow

The workflow can be triggered manually or through a webhook.

### Step 3: Generate the Video

The workflow sends the input to the configured AI video generation service.

### Step 4: Wait for Completion

The workflow monitors the generation status until the video is ready.

### Step 5: Retrieve the Output

Once generation is complete, the workflow retrieves the generated video and required audio files.

### Step 6: Merge Media

FFmpeg processes the media and combines the video and audio into a final synchronized video.

### Step 7: Upload to YouTube

The completed video is automatically sent to YouTube through the YouTube Data API.

## Workflow Components

The workflow contains several logical stages.

### Trigger

The workflow supports triggering through:

* Manual execution
* Webhook

### Input Preparation

The input text and required parameters are prepared before being sent to the video-generation service.

### Video Generation

The AI video generation API receives the prepared request and starts generating the video.

### Status Monitoring

The workflow checks whether the generation process has completed.

If the video is not ready, the workflow waits before checking again.

### Media Processing

The generated video and audio are downloaded and prepared for further processing.

### Audio and Video Merging

FFmpeg combines the generated video and voice audio into a single synchronized media file.

### YouTube Upload

The final video is uploaded automatically to YouTube.

## Automation Pipeline

The complete automation can be summarized as:

```text
Script
  |
  v
AI Video Generation
  |
  v
Generated Visuals
  |
  +----> Generated Voice
  |
  v
Media Processing
  |
  v
FFmpeg
  |
  v
Final Video
  |
  v
YouTube
```

## Benefits

This workflow reduces the amount of manual work required to produce and publish video content.

Instead of manually:

* Creating visuals
* Generating voiceovers
* Processing media
* Combining audio and video
* Uploading the final video

the complete pipeline can be automated through n8n.

## Use Cases

Script2Screen can be adapted for:

* Educational videos
* Short-form content
* Automated YouTube channels
* Explainer videos
* Storytelling videos
* Social media content
* News-style videos
* Marketing content
* AI-generated presentations

## Limitations

The workflow depends on external services and therefore may be affected by:

* API availability
* API rate limits
* Video-generation processing time
* API costs
* YouTube upload restrictions
* Internet connectivity
* FFmpeg configuration

The quality of the final video also depends on the capabilities of the selected AI video-generation service.

## Future Improvements

Possible improvements include:

* Automatic script generation using an LLM
* Automatic subtitle generation
* Background music generation
* Multiple voice options
* Automatic thumbnail generation
* Automatic YouTube title generation
* Automatic description generation
* Automatic tag generation
* Scheduled YouTube publishing
* Support for multiple video-generation APIs
* Automatic short-form video generation
* Error notifications through email or messaging platforms
* Analytics integration

## Conclusion

Script2Screen demonstrates how **AI video generation, voice narration, FFmpeg, n8n, and the YouTube Data API** can be combined to create an automated content-production pipeline.

The workflow minimizes manual video-production steps by connecting script input, AI media generation, media processing, and YouTube publishing into a single automated system.
