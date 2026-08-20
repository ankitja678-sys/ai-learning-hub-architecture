# 🧠 AI Learning Hub

> **An AI-powered learning, development, and productivity workspace built with Next.js, React, TypeScript, Prisma, Supabase, Clerk, and multiple AI providers.**

AI Learning Hub is a full-stack web platform designed to bring **AI learning tools, development utilities, career preparation, and intelligent assistants** into one unified workspace.

Instead of using separate applications for AI chat, code generation, learning roadmaps, quizzes, mock interviews, notes, image generation, and project planning, AI Learning Hub brings these capabilities together inside a single dashboard.

---

## 🌐 Live Demo

🚀 **Live Application:**
https://ai-learning-hub-ik62.vercel.app

📦 **GitHub Repository:**
https://github.com

> The live application may require authentication for some dashboard features.

---

## ✨ What is AI Learning Hub?

AI Learning Hub is built around the idea of creating a personal **AI-powered learning and development workspace**.

The platform combines:

* 🤖 AI conversations
* 🧠 AI Agent
* 💻 AI code generation
* 🏗️ Project architecture planning
* 🎨 AI image generation
* 🖊️ Interactive design board
* 📚 Learning resources
* 📝 Notes
* 🧪 Quizzes
* 🧠 Flashcards
* 🎯 Mock interviews
* 🗺️ Learning roadmaps
* 📊 Progress tracking
* 💬 Persistent conversation history
* 🔐 User authentication

The goal is to make learning technology and building software more accessible through one integrated platform.

---

# 🚀 Core Features

## 🤖 AI Chat

A conversational AI workspace designed for learning, technical questions, brainstorming, and general assistance.

### Features

* Multi-turn conversations
* Markdown responses
* Code formatting
* Conversation history
* User-specific sessions
* AI response actions
* Context-aware conversations
* Authentication-aware data

---

# 🧠 Nova AI Agent

The AI Agent is one of the central features of AI Learning Hub.

It is designed to handle both simple questions and more complex tasks.

### Architecture

```text
User
  │
  ▼
AI Agent UI
  │
  ▼
Next.js API Route
  │
  ▼
AI Router
  │
  ├──► Gemini
  │
  ├──► Groq fallback
  │
  └──► Other configured providers
  │
  ▼
Response
  │
  ▼
Persistent Session History
```

### Provider fallback

The application can attempt to use Gemini first and fall back to another configured provider when Gemini is unavailable or exceeds its quota.

This makes the AI experience more resilient during provider failures or quota limitations.

---

# 💻 AI Code Generator

Generate application code from natural-language requirements.

The code-generation workflow is designed to help users quickly create project foundations and experiment with ideas.

### Capabilities

* Natural-language coding prompts
* Structured generated code
* Modern web development workflows
* Next.js-oriented generation
* Copyable code output
* Developer-friendly interface

---

# 🏗️ AI Project Architect

Turn an application idea into a structured development plan.

The Project Architect can help organize:

```text
Project Idea
     │
     ▼
Requirements
     │
     ▼
Architecture
     │
     ├── Frontend
     ├── Backend
     ├── Database
     ├── APIs
     └── Authentication
     │
     ▼
File Structure
     │
     ▼
Development Roadmap
```

This is intended to help developers move from **idea → architecture → implementation**.

---

# 🎨 AI Image Studio

AI-powered image generation interface for creating visual assets from prompts.

### Features

* Prompt-based image generation
* Multiple aspect ratios
* Modern dark UI
* Loading states
* Generated image preview
* Client-side image actions

Supported layouts include common formats such as:

* `1:1`
* `16:9`
* `4:3`
* `3:4`

---

# 🖊️ AI Design Board

An interactive visual workspace for designing and explaining software architectures.

The design board combines AI-generated architecture concepts with manual editing capabilities.

### Interactive tools

* ✏️ Pencil
* 🔲 Shapes
* 📝 Text
* 🧹 Eraser
* 🖱️ Selection
* 🤖 AI-generated architecture

The goal is to allow developers to **generate an architecture with AI and then manually refine it**.

---

# 📚 Knowledge & Learning Workspace

AI Learning Hub includes tools designed specifically for technical learning.

### Learning features

* Knowledge workspace
* Learning resources
* Tutorials
* Notes
* Flashcards
* Quizzes
* Learning roadmaps
* Progress tracking

These tools are designed to support both structured learning and self-directed experimentation.

---

# 🧪 Mock Test & Interview Preparation

The platform includes multiple interview-preparation experiences.

### Available areas

* 💻 Coding interviews
* 🧠 MCQ quizzes
* 🏗️ System design
* 👔 HR interviews
* 🎯 Technical preparation

The goal is to provide an interactive environment for practicing before real interviews.

---

# 🗺️ Learning Roadmaps

Users can work through structured learning paths.

The roadmap system is designed around:

```text
Goal
 │
 ▼
Learning Topics
 │
 ▼
Projects
 │
 ▼
Practice
 │
 ▼
Progress
```

This helps connect theoretical learning with practical development.

---

# 📝 Notes

The Notes system allows users to save learning material and important information inside the platform.

Notes can be associated with users and stored persistently using the application's database layer.

---

# 💬 Persistent Conversation History

AI Learning Hub supports persistent sessions for conversations.

The application uses:

* Prisma ORM
* Supabase PostgreSQL
* Global sessions
* User-specific history

Conceptually:

```text
User
 │
 ├── Session 1
 │     ├── Message
 │     ├── Message
 │     └── Message
 │
 ├── Session 2
 │     ├── Message
 │     └── Message
 │
 └── Session 3
       └── Message
```

This allows conversations to remain available across sessions rather than existing only in temporary client state.

---

# 🔐 Authentication

Authentication is handled using **Clerk**.

The authentication layer provides:

* Sign up
* Sign in
* Protected dashboard routes
* User identity
* User-specific application data

---

# 🏛️ Application Architecture

The application follows a modern full-stack Next.js architecture.

```text
                         ┌─────────────────────┐
                         │       Browser       │
                         │   React 19 / UI     │
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │     Next.js 15      │
                         │    App Router       │
                         └──────────┬──────────┘
                                    │
                  ┌─────────────────┼─────────────────┐
                  │                 │                 │
                  ▼                 ▼                 ▼
             AI APIs           Auth Layer        Application APIs
                  │                 │                 │
                  ▼                 ▼                 ▼
          ┌──────────────┐      Clerk          Next.js Routes
          │  AI Router   │
          └──────┬───────┘
                 │
        ┌────────┴────────┐
        ▼                 ▼
     Gemini             Groq
        │                 │
        └────────┬────────┘
                 │
                 ▼
          AI Response
                 │
                 ▼
        ┌─────────────────┐
        │ Prisma ORM      │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ Supabase        │
        │ PostgreSQL      │
        └─────────────────┘
```

---

# ⚙️ Tech Stack

## Frontend

* Next.js 15
* React 19
* TypeScript
* Tailwind CSS
* Lucide Icons
* HTML5 Canvas

## Backend

* Next.js App Router
* Next.js API Routes
* Server-side AI integrations
* Prisma ORM
* PostgreSQL

## Database

* Supabase PostgreSQL
* Prisma Client

## Authentication

* Clerk

## AI

* Google Gemini
* Groq
* OpenRouter where configured

## Deployment

* Vercel

---

# 📦 Project Structure

```text
ai-learning-hub/
│
├── app/
│   ├── api/
│   │   ├── agent/
│   │   ├── chat/
│   │   ├── certifications/
│   │   ├── code-generator/
│   │   ├── deploy-vercel/
│   │   ├── draw/
│   │   ├── explain-code/
│   │   ├── flashcards/
│   │   ├── github/
│   │   ├── history/
│   │   ├── images/
│   │   ├── knowledge/
│   │   ├── memory/
│   │   ├── mock-test/
│   │   ├── notes/
│   │   ├── project-architect/
│   │   ├── quiz/
│   │   ├── roadmap/
│   │   ├── run-code/
│   │   └── ...
│   │
│   ├── dashboard/
│   │   ├── agent/
│   │   ├── ai-tools/
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
│   └── reusable UI components
│
├── lib/
│   ├── ai/
│   │   ├── providers/
│   │   └── router.ts
│   └── ...
│
├── prisma/
│   ├── schema.prisma
│   └── generated-client/
│
├── public/
│
├── types/
│
├── .env
├── .env.local
├── package.json
└── README.md
```

---

# 🗄️ Database Architecture

The application uses Prisma with Supabase PostgreSQL.

Current database models include application entities such as:

```text
Note
ChatMessage
user_profiles
GlobalSession
```

The global session architecture allows the application to maintain conversations independently from the UI.

### Example

```text
GlobalSession
│
├── id
├── userId
├── title
├── toolType
├── createdAt
└── updatedAt
```

Additional message/session models can be extended as the platform evolves.

---

# 🔑 Environment Variables

Create a local `.env.local` file.

Example:

```env
DATABASE_URL="your_supabase_pooler_connection_string"
DIRECT_URL="your_supabase_direct_connection_string"

GEMINI_API_KEY="your_gemini_api_key"
GROQ_API_KEY="your_groq_api_key"
OPENROUTER_API_KEY="your_openrouter_api_key"

NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY="your_clerk_publishable_key"
CLERK_SECRET_KEY="your_clerk_secret_key"
```

> ⚠️ **Never commit `.env`, `.env.local`, API keys, database passwords, or Clerk secrets to GitHub.**

Recommended `.gitignore` entries:

```gitignore
.env
.env.local
.env*.local
```

---

# 🛠️ Local Development

## 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd ai-learning-hub
```

## 2. Install dependencies

```bash
npm install
```

## 3. Configure environment variables

Create:

```text
.env.local
```

and add the required credentials.

## 4. Generate Prisma Client

```bash
npx prisma generate
```

## 5. Synchronize the database

If you are using the current development workflow:

```bash
npx prisma@6.2.1 db push
```

## 6. Start development server

```bash
npm run dev
```

Open:

```text
http://localhost:3000
```

---

# ✅ Production Build Verification

The project has been successfully verified using:

```bash
npm run build
```

The production build completed successfully with:

```text
✓ Compiled successfully
✓ Linting and checking validity of types
✓ Collecting page data
✓ Generating static pages
✓ Collecting build traces
✓ Finalizing page optimization
```

This confirms that the application can pass the Next.js production compilation and TypeScript validation pipeline.

---

# 🚀 Deployment

AI Learning Hub is designed to run on Vercel.

## Deployment workflow

```text
GitHub
   │
   ▼
Vercel
   │
   ▼
Next.js Build
   │
   ▼
Production Deployment
```

### Required Vercel environment variables

Add the same production credentials used by the application to:

**Vercel → Project → Settings → Environment Variables**

For example:

```text
DATABASE_URL
DIRECT_URL
GEMINI_API_KEY
GROQ_API_KEY
OPENROUTER_API_KEY
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY
CLERK_SECRET_KEY
```

After changing environment variables, redeploy the application.

> Environment variables are environment-specific. A variable existing on your local machine does not automatically make it available to Vercel.

---

# 🔄 AI Provider Fallback

One of the important backend improvements is provider fallback.

The application can use a routing layer instead of coupling every feature directly to one AI provider.

```text
Application
     │
     ▼
  AI Router
     │
     ▼
 Gemini
     │
     ├── Success ──► Response
     │
     └── Failure
          │
          ▼
        Groq
          │
          ▼
       Response
```

This approach helps reduce the impact of individual provider failures and quota limitations.

---

# 📈 Current Development Status

## Phase 1 — Foundation

**Status: ✅ Completed**

* Next.js application foundation
* Dashboard
* Authentication
* Core UI
* API architecture
* AI integrations
* Database integration
* Initial learning tools

## Phase 2 — Unified Workspace

**Status: ✅ Completed**

* Persistent sessions
* Conversation history
* AI Agent
* Code Generator
* Project Architect
* Design Board
* Learning tools
* Career tools

## Phase 3 — Autonomous AI Workflows

**Status: 🚧 In Progress**

Planned improvements include:

* Multi-agent workflows
* Better tool orchestration
* Voice interaction
* More advanced code execution
* Improved project generation
* More persistent user memory
* Better AI provider routing
* More automation across development workflows

---

# 🧪 Current API Surface

The application currently contains API routes for areas including:

```text
/api/agent
/api/chat
/api/code-generator
/api/draw
/api/images
/api/history/sessions
/api/knowledge
/api/memory
/api/mock-test
/api/notes
/api/project-architect
/api/quiz
/api/roadmap
/api/run-code
/api/videos
```

The API layer is organized around individual product capabilities rather than a single monolithic endpoint.

---

# 🎯 Why I Built This

AI tools are becoming increasingly powerful, but developers and students often have to move between many different applications.

AI Learning Hub is an attempt to bring these workflows together:

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

The long-term goal is to build a platform where users can **learn technology and immediately turn that knowledge into working projects**.

---

# 🛣️ Roadmap

### 🤖 AI

* [ ] Multi-agent orchestration
* [ ] Improved provider routing
* [ ] Tool-use improvements
* [ ] Voice interaction
* [ ] Better contextual memory
* [ ] More reliable AI workflows

### 💻 Development

* [ ] Advanced code execution
* [ ] Automated debugging
* [ ] GitHub workflow improvements
* [ ] Project generation improvements
* [ ] Deployment automation

### 📚 Learning

* [ ] More learning paths
* [ ] Personalized curriculum
* [ ] Better progress analytics
* [ ] More interview simulations
* [ ] Advanced practice environments

### 🎨 Creative Tools

* [ ] More image-generation workflows
* [ ] Improved design-board features
* [ ] AI-assisted UI generation
* [ ] Exportable architecture diagrams

---

# 🔒 Security Notes

This project uses several security-sensitive services.

Never expose:

* API keys
* Database passwords
* Clerk secret keys
* Authentication secrets
* Private deployment credentials

Frontend environment variables should only contain values intentionally designed to be public.

Server-side secrets should remain in server-side environment variables.

---

# ⚠️ Important Notes

AI provider availability and quotas can change.

For example, free-tier AI APIs may return rate-limit responses such as HTTP `429`.

The application therefore supports fallback behavior where configured.

Database connectivity also depends on the production environment and correctly configured Supabase connection strings.

---

# 👨‍💻 Creator

## Ankit Jatav

**Founder & Lead Developer — AI Learning Hub**

I am building AI-powered software with a focus on:

* Artificial Intelligence
* Generative AI
* Full-stack development
* AI Agents
* RAG systems
* Developer tools
* Learning platforms

### Mission

> **Build practical AI tools that help people learn faster, build better software, and turn ideas into working products.**

---

# ⭐ Support the Project

If you find AI Learning Hub interesting:

⭐ Star the repository
🐛 Report bugs
💡 Suggest features
🔧 Contribute improvements
📢 Share the project

---

# 📄 License

Add your preferred license here.

For example:

```text
MIT License
```

if the project is intended to be open source under MIT.
