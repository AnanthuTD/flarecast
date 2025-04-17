# FlareCast: SaaS Video Recording & Collaboration Platform

![FlareCast Logo](https://raw.githubusercontent.com/AnanthuTD/flarecast/trunk/flare-cast-logo.svg)

FlareCast is a scalable, microservices-based SaaS platform for real-time video recording, streaming, and collaboration. Designed for creators, educators, and businesses, it offers AI-powered transcription, video transcoding, and cross-platform support via a desktop app built with Electron.js. The platform includes responsive web clients for users and administrators, ensuring seamless experiences.

## Features

- **Real-Time Video Streaming**: Stream and record videos with adaptive bitrate support (1080p, 720p, 480p) using RTMP-to-HLS conversion.
- **AI-Powered Transcription**: Automatically transcribe videos with high accuracy, reducing processing time by 30%.
- **User & Admin Clients**: Responsive Next.js-based web interfaces for end-users and platform administrators.
- **Cross-Platform Desktop App**: Electron.js app for Windows and macOS, supporting offline recording and streaming.
- **Scalable Architecture**: Event-driven microservices with Kafka, deployed on Kubernetes (GKE) for high availability.

## Architecture

FlareCast consists of **9 microservices**, each handling a specific domain, plus **user and admin web clients** and an **Electron app**:

- **Video Service**: Captures real-time video from users via WebSocket.
- **Transcoding Service**: Processes videos using FFmpeg with AI transcription integration.
- **Streaming Service**: Handles RTMP ingestion and HLS output with NodeMediaServer.
- **User Service**: Manages user accounts, admin roles, and subscription plans.
- **Notification Service**: Delivers real-time updates via Firebase Cloud Messaging.
- **Collaboration Service**: Manages workspaces, folders, and shared spaces.
- **Email Service**: Sends transactional emails for user onboarding and updates.
- **Ingest Service**: Processes live stream inputs for real-time delivery.
- **API Gateway**: Validates JWT tokens and routes requests using Express.js.
- **User Client**: Next.js frontend for video recording and playback.
- **Admin Client**: Next.js dashboard for platform management.
- **FlareCast Electron App**: Cross-platform desktop app for recording and streaming.

![Architecture Diagram](https://raw.githubusercontent.com/AnanthuTD/flarecast/trunk/architecture-diagram.png)

## Tech Stack

- **Frontend**: Next.js, TypeScript, Tailwind CSS
- **Backend**: Express.js, Node.js, Kafka, Prisma
- **Database**: MongoDB
- **DevOps**: Kubernetes (GKE), Docker, Skaffold, GitHub Actions
- **Desktop**: Electron.js
- **Streaming**: FFmpeg, NodeMediaServer
- **Cloud**: AWS S3, Google Kubernetes Engine, CloudFront

## Repositories

FlareCast is split across multiple GitHub repositories for modularity. Key public repositories include:

- [FlareCast Electron](https://github.com/AnanthuTD/FlareCast-Electron)
- [FlareCast Client Main](https://github.com/AnanthuTD/FlareCast-client-main)

*Note*: Some repositories are private due to proprietary code. Code samples or demos are available upon request via [email](mailto:ananthu.td.official@gmail.com).

## CI/CD

- **GitHub Actions**: Automated build, test, and deployment pipelines for each service.
- **Auto-Updates**: Electron app updates delivered via GitHub Releases.

## Demo

- [Live Demo](https://flarecast.ananthutd.live)
- [Screencast](https://youtu.be/VIDEO_ID)

## Contact

For questions, code samples, or demo access, reach out via [email](mailto:ananthu.td.official@gmail.com) or [LinkedIn](https://linkedin.com/in/AnanthuTD).

---
Built by Ananthu TD
