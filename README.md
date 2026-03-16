# Raven Milosh Devhub

Official engineering platform and personal developer hub for **Raven Milosh**.

This project serves as:

- A **developer portfolio**
- An **engineering blog**
- A **technical experimentation lab**
- A **future extensible developer platform**

The repository is intentionally designed to be **AI-assisted development friendly**, meaning its architecture, documentation, and conventions are structured so autonomous agents or developer copilots can safely contribute improvements over time.

---

# Project Overview

**Raven Milosh Devhub** is a modern developer platform built with a **performance-first architecture** using static rendering, edge deployment, and minimal runtime overhead.

The project emphasizes:

- Performance
- Security
- Maintainability
- Long-term scalability
- AI-assisted development

Primary public features:

- Developer landing page
- Engineering blog
- Technical notes
- Contact system

Private features:

- Admin dashboard
- Content management
- Message management
- Future developer tools

---

# Domain

Primary domain:

ravenmilosh.dev

Infrastructure will be managed through:

- DNS
- Edge network
- Web Application Firewall (WAF)

---

# License

This project is released under the **Apache License 2.0**.

Why Apache 2.0:

- Allows open collaboration
- Protects contributors
- Includes patent protection
- Enables future commercial evolution of the project

---

# Core Technology Stack

Frontend Framework

Astro

Astro provides a hybrid rendering model optimized for performance and static generation.

Styling

Tailwind CSS

Utility-first styling framework used to build a minimal, modern design system.

Content System

MDX

Used for the engineering blog and technical articles.

Database and Authentication

Supabase

Supabase provides:

- PostgreSQL database
- Authentication system
- Storage
- REST APIs

Client Library

supabase-js

JavaScript client used to interact with Supabase services.

Hosting and Edge Infrastructure

Cloudflare

The platform will be deployed through Cloudflare's edge network.

Deployment Platform

Cloudflare Pages

Provides global CDN distribution and edge-optimized builds.

CI/CD

GitHub Actions

Used for automated build verification and deployment pipelines.

Future Interactive Components

Vue.js

Vue components will be used as Astro Islands for interactive UI elements.

---

# Architecture Overview

- Internet
  - Cloudflare DNS + WAF
  - Cloudflare Pages (Edge Deployment)
  - Astro Application
    - Static Content (MDX Blog)
    - Interactive UI (Vue Islands)
    - API Endpoints
  - Supabase Backend
  - PostgreSQL Database
  - Authentication
  - Storage

---

# Repository Structure

src

components
Reusable UI components

layouts
Page layout templates

pages
Astro page routes

pages/blog
Engineering blog routes

pages/admin
Admin dashboard routes

content/blog
MDX engineering articles

styles
Global styling and Tailwind configuration

lib
External service integrations

lib/supabase.js
Supabase client configuration

lib/api.js
Future API helpers

public
Static assets

---

# Blog Content System

All engineering posts are stored as **MDX documents**.

Location

src/content/blog/

Example article structure:

```
---
title: "Building an Astro Engineering Blog"
description: "Architecture decisions and lessons learned"
date: 2026-03-16
tags: ["astro", "engineering", "architecture"]
draft: false
---

# Article Title

Content written using MDX.
```

Advantages of file-based blog content:

- Git version control
- Zero database dependency
- Maximum performance
- SEO optimized
- Easy long-term archival

---

# Database Strategy

Database provider:

Supabase

Database engine:

PostgreSQL

Initial schema scope:

users
contact_messages
admin_sessions

Future schema expansion:

technical_notes
analytics_events
dashboard_data
user_profiles

---

# Authentication

Authentication is handled through Supabase Auth.

Supported flows:

Email authentication
Admin access control
Session tokens

Initial usage:

Admin dashboard access only.

Future expansion:

User accounts
Developer community access
Private content areas

---

# Admin Dashboard

Route:

/admin

Access:

Restricted via authentication.

Admin capabilities planned:

- Manage blog content
- Review contact messages
- Manage notes
- View analytics
- Manage platform data

The dashboard architecture is designed to allow future **multi-user support**.

---

# API Architecture

Initial phase:

Astro server endpoints.

Location:

src/pages/api/

Future architecture:

Edge APIs using Cloudflare Workers if scaling requirements increase.

API responsibilities:

- Secure communication with Supabase
- Form submissions
- Dashboard actions
- Data processing

---

# CI/CD Pipeline

Deployment workflow:

Commit
↓
GitHub Actions
↓
Build Verification
↓
Cloudflare Pages
↓
Edge Deployment

GitHub Actions responsibilities:

- Install dependencies
- Run build
- Validate project structure
- Trigger deployment

---

# Deployment Strategy

Deployment target:

Cloudflare Pages

Key benefits:

- Global CDN
- Edge performance
- Built-in TLS
- DDoS protection
- WAF security

Repository integration:

GitHub → Cloudflare Pages automatic deploys.

---

# Security Model

Security layers include:

Cloudflare DNS protection
Cloudflare WAF
Edge TLS encryption
Supabase authentication
Environment variable protection
Admin route protection

Future improvements:

Rate limiting
API validation middleware
Security logging

---

# AI Contribution Guidelines

This repository is structured to support **AI-assisted development**.

Agents interacting with this project should:

1. Follow existing project architecture.
2. Respect repository structure.
3. Avoid introducing unnecessary dependencies.
4. Maintain performance-first principles.
5. Document architectural changes.

Preferred agent contribution workflow:

- Analyze architecture
- Suggest improvements
- Submit isolated changes
- Maintain compatibility with the stack

Agents must avoid modifying:

- deployment configuration
- authentication logic
- database schema

without explicit documentation updates.

---

# Development Workflow

Recommended workflow:

Create feature branch

Implement changes

Run local build

Submit pull request

Validate via CI pipeline

Merge after review

---

# Local Development

Install dependencies:

npm install

Run development server:

npm run dev

Build project:

npm run build

Preview build:

npm run preview

---

# Roadmap

Version 0.1 – Project Initialization

Project setup
Astro configuration
Tailwind integration
Repository structure

Version 0.2 – Blog System

MDX blog implementation
Article routing
SEO metadata system

Version 0.3 – Supabase Integration

Supabase client setup
Database initialization
Contact message storage

Version 0.4 – Authentication

Supabase authentication
Admin route protection
Session validation

Version 0.5 – Admin Dashboard

Basic dashboard UI
Message management
Content tools

Version 0.6 – API Layer

Astro API endpoints
Secure form handling
Data validation

Version 0.7 – Vue Interactive Components

Search system
Dashboard UI components
Interactive tools

Version 0.8 – Observability

Analytics integration
Logging system
Performance monitoring

Version 1.0 – Platform Stabilization

Production hardening
Security improvements
Full documentation

---

# Long-Term Vision

Raven Milosh Devhub is intended to evolve beyond a simple portfolio.

Potential future directions:

Developer tools
Engineering knowledge base
Public technical research
AI-assisted documentation platform
Developer community hub

---

# Maintainer

Marco A. Sánchez a.k.a Raven Milosh - Web Developer
