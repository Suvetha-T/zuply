# Zuply — AI-Powered Hyperlocal E-Commerce Platform

> Connecting local sellers with nearby buyers through AI-driven product discovery, smart listings, and seamless payments.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Environment Variables](#environment-variables)
- [Deployment](#deployment)
- [Team](#team)

---

## Overview

Zuply is a hyperlocal e-commerce platform built to bridge the gap between local sellers and nearby buyers. It leverages **Generative AI** for automated product listing creation, **computer vision** for image enhancement, and a built-in **AI chatbot** to guide users through the platform.

---

## Features

| Feature | Description |
|---|---|
| **AI Listing Generation** | Gemini Vision API auto-generates product titles, descriptions, and tags from uploaded images |
| **Zuply AI Chatbot** | Conversational assistant to help buyers discover products |
| **Seller Dashboard** | Manage listings, orders, and analytics |
| **Secure Payments** | Razorpay integration — UPI, Cards, Net Banking, Wallets, COD |
| **Admin Panel** | Full platform control — users, listings, orders, categories |
| **Order Management** | End-to-end order tracking for buyers and sellers |
| **Role-Based Access** | Separate flows for Customer, Seller, and Admin |
| **Wishlist & Reviews** | Save favourites and rate purchases |

---

## Tech Stack

### Frontend
- **Angular 17** (Standalone Components, SPA)
- **TypeScript**, SCSS
- Deployed on **Netlify**

### Backend
- **Spring Boot 3** (REST API)
- **Spring Security** + **JWT** (Authentication & RBAC)
- **Maven**, Docker
- Deployed on **Render**

### Database
- **MySQL** hosted on **Aiven Cloud**

### AI & Integrations
- **Google Gemini Vision API** — AI product listing generation
- **Razorpay** — Payment gateway

---

## Project Structure

```
Zuply/
├── Backend/                        # Spring Boot REST API
│   ├── src/main/java/com/zuply/
│   │   └── modules/
│   │       ├── admin/              # Admin management
│   │       ├── ai/                 # Gemini AI service
│   │       ├── auth/               # JWT authentication
│   │       ├── cart/               # Shopping cart
│   │       ├── chat/               # AI chatbot
│   │       ├── listing/            # Product listings
│   │       ├── order/              # Order management
│   │       ├── payment/            # Razorpay integration
│   │       ├── product/            # Product catalogue
│   │       ├── seller/             # Seller dashboard
│   │       ├── upload/             # File & image upload
│   │       └── user/               # User profiles
│   ├── Dockerfile
│   └── pom.xml
├── Frontend/                       # Angular 17 SPA
│   └── Zuply-FrontEnd/
│       ├── zuply-all-pages/        # Feature pages
│       ├── environments/           # API base URL config
│       └── netlify.toml            # Netlify deployment config
└── render.yaml                     # Render deployment config
```

---

## Getting Started

### Prerequisites

- Java 17+
- Node.js 18+ & npm
- MySQL (local) or Aiven connection string
- Maven

### Backend

```bash
cd Backend
# Add your environment variables to application.properties
mvn spring-boot:run
```

### Frontend

```bash
cd Frontend/Zuply-FrontEnd
npm install
ng serve
```

App runs at `http://localhost:4200`

---

## Environment Variables

Set these in Render dashboard (backend) and Netlify dashboard (frontend):

### Backend (render.yaml)

| Variable | Description |
|---|---|
| `SPRING_DATASOURCE_URL` | Aiven MySQL JDBC URL |
| `SPRING_DATASOURCE_USERNAME` | DB username |
| `SPRING_DATASOURCE_PASSWORD` | DB password |
| `JWT_SECRET` | Secret key for JWT signing |
| `GEMINI_API_KEY` | Google Gemini Vision API key |
| `RAZORPAY_KEY_ID` | Razorpay key ID |
| `RAZORPAY_KEY_SECRET` | Razorpay secret |
| `CORS_ALLOWED_ORIGINS` | Frontend URL for CORS |

> **Never commit `application.properties` or any credentials to git.**

---

## Deployment

| Service | Platform | Config |
|---|---|---|
| Backend API | Render (Docker) | `render.yaml` |
| Frontend SPA | Netlify | `netlify.toml` |
| Database | Aiven Cloud MySQL | via env vars |
| Images | via env vars |

---

## Team

**Team Lampart** — POD2 · INTQEA26SD002  
Suvetha T
Tailor Mudassir Khan
Manjunath Sadgal Raghu
Dursetti Varsha
Rubini J S
Cognizant GenC Training Programme

---

> Built with ❤️ by Team Lampart
