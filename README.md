## AI Video Generation & Upload Automation Workflow

# Overview
This project automates the complete AI video creation pipeline using a workflow automation platform. It takes a trigger, generates a video with AI, processes the output, merges audio and video, and automatically uploads the final video to YouTube.

# Workflow Features
Trigger workflow manually or via webhook
Edit and prepare input data
Generate AI video
Wait for video generation to complete
Retrieve generated video
Split workflow based on generation status
Clean and process output
Download video and audio files
Merge video and audio
Read merged video
Respond with generated video
Upload final video to YouTube automatically

# Technologies Used
Workflow Automation Platform (n8n)
AI Video Generation API
HTTP Request Nodes
JavaScript (Code Nodes)
FFmpeg (Video & Audio Merging)
YouTube Data API

# Prerequisites
Before running the workflow, configure:
AI Video Generation API Key
YouTube Data API Credentials
FFmpeg Installation
Workflow Automation Platform (e.g., n8n)
Internet connection
