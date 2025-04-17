# FlareCast: SaaS Video Recording & Collaboration Platform

![flarecast-logo](https://github.com/AnanthuTD/flarecast/blob/trunk/flare-cast-logo.svg)

FlareCast is a scalable, microservices-based SaaS platform for real-time video recording, streaming, and collaboration. It features AI-powered transcription, video transcoding, and cross-platform support via a desktop app built with Electron.js. The platform is designed for creators, educators, and businesses, offering seamless user and admin experiences.

## Features

- **Real-Time Video Streaming**: Stream and record videos with adaptive bitrate support (1080p, 720p, 480p) using RTMP-to-HLS conversion.
- **AI-Powered Transcription**: Automatically transcribe videos with high accuracy, reducing processing time by 30%.
- **User & Admin Clients**: Responsive Next.js-based web interfaces for end-users and platform administrators.
- **Cross-Platform Desktop App**: Built with Electron.js for Windows and macOS, enabling offline recording and streaming.
- **Scalable Architecture**: Event-driven microservices with Kafka, deployed on Kubernetes (GKE) for high availability.

## Architecture

FlareCast consists of **7 microservices**, each handling a specific domain, plus **user and admin clients**:

- **Video Service**: Uses websocket to capture the video from the user in real time.
- **Transcoding Service**: Processes videos using FFmpeg with AI transcription integration.
- **Streaming Service**: Handles RTMP ingestion and HLS output with NodeMediaServer.
- **User Service**: Manages admin, user and subscription.
- **Notification Service**: Sends real-time updates via firebase cloud messaging.
- **API Gateway**: Manages JWT validation and Routes requests between services using Express.js.
- **User Client**: Next.js frontend for video recording and playback.
- **Admin Client**: Next.js dashboard for platform management.
- **Collaboration Service**: Manages workspace, folders and spaces.
- **Flarecast Electron App**: Crossplatform app using electron used to record and stream.

![Architecture Diagram](link-to-diagram.png)

## Tech Stack

- **Frontend**: Next.js, TypeScript, Tailwind CSS
- **Backend**: Express.js, Node.js, Kafka, Prisma
- **Database**: MongoDB
- **DevOps**: Kubernetes (GKE), Docker, Skaffold, GitHub Actions
- **Desktop**: Electron.js
- **Streaming**: FFmpeg, NodeMediaServer
- **Cloud**: AWS S3, Google Kubernetes Engine, Cloudfront

## Repositories

FlareCast is split across multiple GitHub repositories for modularity. Key repositories include:

- [User Client](link-to-repo) <!-- Replace with public repo link or remove if private -->
- [API Gateway](link-to-repo)
- [Transcoding Service](link-to-repo)
- https://github.com/AnanthuTD/FlareCast-Electron
- https://github.com/AnanthuTD/FlareCast-infra (private)
- https://github.com/AnanthuTD/FlareCast-user-service
- https://github.com/AnanthuTD/FlareCast-client-main
- https://github.com/AnanthuTD/FlareCast-notification-service
- https://github.com/AnanthuTD/FlareCast-collaboration-service
- https://github.com/AnanthuTD/FlareCast-video-service
- https://github.com/AnanthuTD/FlareCast-email-service
- https://github.com/AnanthuTD/flarecast-ingest-service (live stream)
- https://github.com/AnanthuTD/FlareCast-admin-client
- https://github.com/AnanthuTD/FlareCast-transcode-service
- 

*Note*: Most repositories are private due to proprietary code. Code samples or demos are available upon request.

## CI/CD

- **GitHub Actions**: Automated build, test, and deployment pipelines for each service.
- **Auto-Updates**: Electron app updates delivered via GitHub Releases.

## Demo

[Live Demo](https://flarecast.ananthutd.live) 
[Screencast](link-to-video)

## Contact

For questions or code samples, reach out via [email](mailto:ananthu.td.official@gmail.com) or [LinkedIn](https://linkedin.com/in/AnanthuTD).

---
Built by Ananthu TD
