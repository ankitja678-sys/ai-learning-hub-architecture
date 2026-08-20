# AI LEARNING HUB

AI Learning Hub is an AI-powered learning, development, and productivity workspace built with Next.js, React, TypeScript, Prisma, Supabase, Clerk, and multiple AI providers.

It brings AI chat, code generation, project architecture, learning roadmaps, quizzes, mock interviews, notes, image generation, and developer tools into one unified dashboard.

## Live Demo

[![Live Demo](https://img.shields.io/badge/Live-Demo-000000?logo=vercel)](https://ai-learning-hub-ik62.vercel.app)

[![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?logo=github)](https://github.com/YOUR_USERNAME/ai-learning-hub)

> Some dashboard features require user authentication.

## Overview

AI Learning Hub is designed for students, developers, and technology learners who want to learn, build, test, and track progress from one workspace.

The platform follows this workflow:

```text
Learn
  ↓
Ask AI
  ↓
Understand
  ↓
Build
  ↓
Test
  ↓
Debug
  ↓
Document
  ↓
Track Progress
```

## Features

### AI Chat

- Multi-turn conversations
- Markdown and code formatting
- Persistent conversation history
- User-specific sessions
- Context-aware responses
- Authentication-aware data

### Nova AI Agent

Nova AI Agent handles general questions and complex development tasks through a provider-routing layer.

```text
User
  ↓
AI Agent UI
  ↓
Next.js API Route
  ↓
AI Router
  ├── Gemini
  ├── Groq fallback
  └── Other configured providers
  ↓
Response
  ↓
Persistent Session History
```

When configured, the application can fall back to another AI provider if the primary provider is unavailable or rate-limited.

### AI Code Generator

- Natural-language coding prompts
- Structured code generation
- Next.js-oriented workflows
- Copyable code output
- Developer-focused responses
- AI-generated UI experiments

### AI Project Architect

The Project Architect converts an application idea into a structured development plan.

```text
Project Idea
  ↓
Requirements
  ↓
Architecture
  ├── Frontend
  ├── Backend
  ├── Database
  ├── APIs
  └── Authentication
  ↓
File Structure
  ↓
Development Roadmap
```

### AI Image Studio

- Prompt-based image generation
- Multiple aspect ratios
- Image preview
- Loading states
- Client-side image actions

Supported layouts include:

- 1:1
- 16:9
- 4:3
- 3:4

### AI Design Board

An interactive workspace for creating and refining software architectures.

Tools include:

- Pencil
- Shapes
- Text
- Eraser
- Selection
- AI-generated architecture diagrams

### Learning Workspace

- Learning resources
- Tutorials
- Notes
- Flashcards
- Quizzes
- Learning roadmaps
- Progress tracking

### Mock Tests and Interviews

- Coding interviews
- Multiple-choice quizzes
- System design practice
- HR interview preparation
- Technical interview preparation

### Persistent Sessions

Conversations are persisted using Prisma and Supabase PostgreSQL.

```text
User
  ├── Session 1
  │     ├── Message
  │     ├── Message
  │     └── Message
  ├── Session 2
  │     └── Message
  └── Session 3
        └── Message
```

### Authentication

Authentication is handled using Clerk.

- Sign up
- Sign in
- Protected dashboard routes
- User identity
- User-specific data

## Tech Stack

### Frontend

- Next.js
- React
- TypeScript
- Tailwind CSS
- Lucide Icons
- HTML5 Canvas

### Backend

- Next.js App Router
- Next.js API Routes
- Server-side AI integrations
- Prisma ORM

### Database

- Supabase PostgreSQL
- Prisma Client

### Authentication

- Clerk

### AI Providers

- Google Gemini
- Groq
- OpenRouter, when enabled

### Deployment

- Vercel

## Project Structure

```text
ai-learning-hub/
├── app/
│   ├── api/
│   │   ├── agent/
│   │   ├── chat/
│   │   ├── code-generator/
│   │   ├── draw/
│   │   ├── flashcards/
│   │   ├── history/
│   │   ├── images/
│   │   ├── knowledge/
│   │   ├── memory/
│   │   ├── mock-test/
│   │   ├── notes/
│   │   ├── project-architect/
│   │   ├── quiz/
│   │   ├── roadmap/
│   │   └── run-code/
│   │
│   ├── dashboard/
│   │   ├── agent/
│   │   ├── chat/
│   │   ├── code-generator/
│   │   ├── design-board/
│   │   ├── flashcards/
│   │   ├── images/
│   │   ├── knowledge/
│   │   ├── mock-test/
│   │   ├── notes/
│   │   ├── project-architect/
│   │   ├── quiz/
│   │   ├── roadmap/
│   │   └── tutorials/
│   │
│   ├── docs/
│   ├── pricing/
│   └── ...
│
├── components/
├── lib/
│   └── ai/
│       ├── providers/
│       └── router.ts
│
├── prisma/
│   ├── schema.prisma
│   └── generated-client/
│
├── public/
├── types/
├── .env.example
├── package.json
└── README.md
```

## Database

The application uses Prisma with Supabase PostgreSQL.

Current entities include:

- Note
- ChatMessage
- User profile
- Global session

Example session structure:

```text
GlobalSession
├── id
├── userId
├── title
├── toolType
├── createdAt
└── updatedAt
```

## Environment Variables

Create a local `.env.local` file:

```env
DATABASE_URL="your_supabase_pooler_connection_string"
DIRECT_URL="your_supabase_direct_connection_string"

GEMINI_API_KEY="your_gemini_api_key"
GROQ_API_KEY="your_groq_api_key"
OPENROUTER_API_KEY="your_openrouter_api_key"

NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY="your_clerk_publishable_key"
CLERK_SECRET_KEY="your_clerk_secret_key"
```

Never commit these files or values:

```text
.env
.env.local
API keys
Database passwords
Clerk secret keys
Private deployment credentials
```

Use `.env.example` to document variable names without exposing secrets:

```env
DATABASE_URL=
DIRECT_URL=
GEMINI_API_KEY=
GROQ_API_KEY=
OPENROUTER_API_KEY=
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=
```

## Local Development

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/ai-learning-hub.git
cd ai-learning-hub
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Create `.env.local` and add the required credentials.

### 4. Generate Prisma Client

```bash
npx prisma generate
```

### 5. Push the database schema

```bash
npx prisma db push
```

### 6. Start the development server

```bash
npm run dev
```

Open:

```text
http://localhost:3000
```

## Build Verification

Before deployment, run:

```bash
npm run build
```

Also verify the application locally with:

```bash
npm run dev
```

Do not claim that the production build passed unless the command has actually completed successfully on the current codebase.

## Deployment

AI Learning Hub is designed for deployment on Vercel.

```text
GitHub
  ↓
Vercel
  ↓
Next.js Build
  ↓
Production Deployment
```

Add environment variables in:

```text
Vercel Dashboard
→ Project
→ Settings
→ Environment Variables
```

Configure variables for the correct environment:

- Development
- Preview
- Production

After changing environment variables, redeploy the project. [32]

## Current Status

### Phase 1 — Foundation

- Next.js application foundation
- Dashboard
- Authentication
- Core UI
- API architecture
- AI integrations
- Database integration
- Initial learning tools

### Phase 2 — Unified Workspace

- Persistent sessions
- Conversation history
- AI Agent
- Code Generator
- Project Architect
- Design Board
- Learning tools
- Career tools

### Phase 3 — Autonomous AI Workflows

In progress:

- Multi-agent workflows
- Improved provider routing
- Voice interaction
- Advanced code execution
- Automated debugging
- Project generation
- Persistent user memory
- Development workflow automation

## Roadmap

### AI

- Multi-agent orchestration
- Improved provider routing
- Tool-use improvements
- Voice interaction
- Better contextual memory
- More reliable AI workflows

### Development

- Advanced code execution
- Automated debugging
- GitHub workflow improvements
- Project generation improvements
- Deployment automation

### Learning

- More learning paths
- Personalized curriculum
- Progress analytics
- Interview simulations
- Advanced practice environments

### Creative Tools

- More image-generation workflows
- Improved design board
- AI-assisted UI generation
- Exportable architecture diagrams

## Security

Never expose or commit:

- API keys
- Database passwords
- Clerk secret keys
- Private deployment credentials
- Authentication secrets

Only expose environment variables that are intentionally public. Server-side secrets must remain on the server.

## Why I Built This

Developers and students often move between many tools while learning and building software.

AI Learning Hub brings these workflows into one place:

- Learn
- Ask questions
- Understand concepts
- Generate code
- Plan projects
- Practice interviews
- Debug applications
- Track progress

The long-term goal is to help users turn knowledge into working software.

## Creator

### Ankit Jatav

Founder and Lead Developer of AI Learning Hub.

Focused on:

- Artificial Intelligence
- Generative AI
- Full-stack development
- AI agents
- RAG systems
- Developer tools
- Learning platforms

## Support the Project

If you find AI Learning Hub useful:

- Star the repository
- Report bugs
- Suggest features
- Contribute improvements
- Share the project

## License

This project is currently unlicensed.

If you want to release it as open source under the MIT License, add a `LICENSE` file and update this section accordingly.
