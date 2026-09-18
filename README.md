# 🧠 AI Learning Hub

> An AI-powered learning, development, productivity, and career workspace built with Next.js, React, TypeScript, Prisma, Supabase, Clerk, and multiple AI providers.

AI Learning Hub is a full-stack AI platform that brings AI chat, AI agents, code generation, project architecture, learning tools, interview preparation, creative tools, and developer utilities into one unified workspace.

**Learn → Build → Test → Debug → Improve → Deploy**

---

## 🌐 Live Demo

🚀 **Live Application:**  
https://ai-learning-hub-ik62.vercel.app/

📦 **GitHub Repository:**  
Add your GitHub repository URL here.

> Some dashboard features require authentication.

---

# ✨ About AI Learning Hub

AI Learning Hub is designed to help students, developers, and AI enthusiasts learn technology and turn their ideas into working projects.

Instead of switching between multiple applications for AI conversations, coding, learning, project planning, architecture, interview preparation, notes, and creative tools, AI Learning Hub brings these workflows together in one platform.

### Main capabilities

- 🤖 AI Chat
- 🧠 Nova AI Agent
- 💻 AI Code Generator
- 👀 Live Artifact Preview
- 🏗️ AI Project Architect
- 🎨 AI Image Studio
- 🖊️ AI Design Board
- 📚 Knowledge & Learning
- 📝 Notes
- 🧠 Flashcards
- 🧪 Quizzes
- 🗺️ Learning Roadmaps
- 🎯 Mock Tests & Interviews
- 💬 Persistent Conversation History
- 🔐 Authentication

---

# 🚀 Core Features

## 🤖 AI Chat

AI-powered conversational workspace for learning, technical questions, brainstorming, debugging, coding assistance, and general AI assistance.

### Features

- Multi-turn conversations
- Markdown responses
- Code formatting
- Conversation history
- Persistent sessions
- User-specific conversations
- Context-aware interactions
- Authentication-aware data

---

## 🧠 Nova AI Agent

Nova is the AI Agent inside AI Learning Hub.

It is designed to handle both simple questions and more complex tasks using an AI routing layer and multiple configured providers.

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
  ├──► Groq
  │
  └──► Other configured providers
  │
  ▼
AI Response
  │
  ▼
Persistent Session
```

### Provider fallback

The AI routing layer can use another configured provider when the primary provider fails or reaches a limitation.

```text
              ┌─────────────┐
              │  AI Router  │
              └──────┬──────┘
                     │
                 Try Gemini
                     │
              ┌──────┴──────┐
              │             │
           Success        Failure
              │             │
              ▼             ▼
           Response        Groq
                             │
                             ▼
                          Response
```

This architecture helps improve resilience against provider errors, quota limitations, and temporary availability problems.

---

# 💻 AI Code Generator

The AI Code Generator converts natural-language requirements into application code.

Example:

```text
Create a beautiful modern responsive login page
using React and Tailwind CSS.
```

The generated code can be inspected, copied, edited, and previewed.

### Features

- Natural-language coding prompts
- React code generation
- Tailwind CSS generation
- TypeScript support
- Modern UI generation
- Copyable code
- Editable generated code
- Code preview workflow
- Developer-focused interface

---

# 👀 Live Artifact Preview

AI Learning Hub includes a browser-based artifact preview system for generated React and TypeScript code.

Generated components can be transformed and rendered inside a sandboxed preview environment.

### Preview workflow

```text
AI Generated TSX
       │
       ▼
Artifact Sandbox
       │
       ▼
Babel TypeScript Transform
       │
       ▼
React Runtime
       │
       ▼
Live Preview
```

The artifact workflow supports:

- React components
- TypeScript
- JSX
- Tailwind CSS
- Lucide React icons
- Editable generated code
- Preview / Code tabs
- Run Code workflow
- Browser-safe component replacements
- Runtime error display

This makes it easier to inspect AI-generated interfaces before integrating them into a real project.

---

# 🏗️ AI Project Architect

AI Project Architect helps transform an application idea into a structured development plan.

### Workflow

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

It can help developers understand:

- Project requirements
- Technology choices
- Frontend architecture
- Backend architecture
- Database requirements
- API structure
- Authentication requirements
- File organization
- Development steps

---

# 🎨 AI Image Studio

AI-powered image generation workspace for creating visual assets from text prompts.

### Features

- Prompt-based image generation
- Image preview
- Multiple aspect ratios
- Loading states
- Modern interface
- Generated image workflows

Supported formats include:

```text
1:1
16:9
4:3
3:4
```

---

# 🖊️ AI Design Board

An interactive visual workspace for designing and explaining software architectures.

### Tools

- ✏️ Pencil
- 🔲 Shapes
- 📝 Text
- 🧹 Eraser
- 🖱️ Selection
- 🤖 AI-generated architecture

### Workflow

```text
Architecture Idea
       │
       ▼
   AI Generation
       │
       ▼
   Design Board
       │
       ▼
 Manual Editing
       │
       ▼
Final Architecture
```

The goal is to combine AI-generated architecture with manual visual editing.

---

# 📚 Learning Workspace

AI Learning Hub contains multiple tools designed for technical learning.

### Learning features

- 📚 Knowledge workspace
- 📖 Tutorials
- 📝 Notes
- 🧠 Flashcards
- 🧪 Quizzes
- 🗺️ Learning roadmaps
- 📊 Progress tracking

The learning system is designed to connect theoretical knowledge with practical development.

---

# 🧪 Mock Tests & Interview Preparation

AI Learning Hub provides interactive preparation tools for technical and career development.

### Areas

- 💻 Coding interviews
- 🧠 MCQ tests
- 🏗️ System design
- 👔 HR interviews
- 🎯 Technical preparation

The goal is to provide an interactive environment where users can practice before real interviews.

---

# 🗺️ Learning Roadmaps

Learning roadmaps help users organize their learning journey.

```text
Goal
 │
 ▼
Learning Topics
 │
 ▼
Practice
 │
 ▼
Projects
 │
 ▼
Interview Preparation
 │
 ▼
Progress
```

The roadmap system connects learning goals with practical projects and preparation.

---

# 📝 Notes

The Notes system allows users to create and store learning material and important information inside the platform.

Notes can be associated with users and stored persistently through the application's database layer.

---

# 💬 Persistent Conversation History

AI Learning Hub supports persistent conversation sessions.

The application uses:

- Prisma ORM
- Supabase PostgreSQL
- User-specific sessions
- Persistent message history

### Concept

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

This allows conversations to remain available instead of existing only in temporary client state.

---

# 🔐 Authentication

Authentication is handled using Clerk.

### Authentication features

- Sign up
- Sign in
- User identity
- Protected dashboard routes
- User-specific data
- Authentication-aware API requests

---

# 🏛️ Application Architecture

AI Learning Hub follows a modern full-stack Next.js architecture.

```text
                         ┌─────────────────────┐
                         │       Browser       │
                         │    React 19 UI      │
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │     Next.js 15      │
                         │     App Router      │
                         └──────────┬──────────┘
                                    │
              ┌─────────────────────┼─────────────────────┐
              │                     │                     │
              ▼                     ▼                     ▼
       Application APIs        Authentication          AI Layer
              │                     │                     │
              ▼                     ▼                     ▼
       Next.js API Routes         Clerk              AI Router
                                                          │
                                      ┌───────────────────┼──────────────────┐
                                      │                   │                  │
                                      ▼                   ▼                  ▼
                                   Gemini               Groq            OpenRouter
                                      │                   │                  │
                                      └───────────────────┼──────────────────┘
                                                          │
                                                          ▼
                                                   AI Response
                                                          │
                                                          ▼
                                                    Prisma ORM
                                                          │
                                                          ▼
                                                Supabase PostgreSQL
```

---

# ⚙️ Tech Stack

### Frontend

- Next.js 15
- React 19
- TypeScript
- Tailwind CSS
- Lucide React
- HTML5 Canvas

### Backend

- Next.js App Router
- Next.js API Routes
- Server-side AI integrations
- Prisma ORM
- PostgreSQL

### Database

- Supabase PostgreSQL
- Prisma Client

### Authentication

- Clerk

### AI Providers

- Google Gemini
- Groq
- OpenRouter where configured

### Deployment

- Vercel

### Development

- VS Code
- Git
- GitHub
- npm
- Prisma CLI

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
│   ├── artifact-preview/
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
├── types/
│
├── package.json
├── tsconfig.json
├── next.config.*
└── README.md
```

---

# 🗄️ Database Architecture

The application uses Prisma ORM with Supabase PostgreSQL.

The database layer supports application entities such as sessions, messages, notes, user-related data, and other platform features.

### Session concept

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

The database architecture can evolve as new features are introduced.

---

# 🔑 Environment Variables

Create a `.env.local` file.

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

### ⚠️ Important

Never commit secrets to GitHub.

Never expose:

```text
API keys
Database passwords
Clerk secret keys
Private tokens
Deployment credentials
```

Recommended `.gitignore`:

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

Add the required credentials.

## 4. Generate Prisma Client

```bash
npx prisma generate
```

## 5. Synchronize the database

For the current development workflow:

```bash
npx prisma@6.2.1 db push
```

## 6. Start the development server

```bash
npm run dev
```

Open:

```text
http://localhost:3000
```

---

# 🧪 Production Build Verification

Before deploying, verify the production build:

```bash
npm run build
```

A successful build should complete the Next.js compilation and TypeScript validation process.

Expected output includes:

```text
✓ Compiled successfully
✓ Linting and checking validity of types
✓ Collecting page data
✓ Generating static pages
✓ Collecting build traces
✓ Finalizing page optimization
```

---

# 🚀 Deployment

AI Learning Hub is designed to run on Vercel.

### Deployment workflow

```text
Local Development
       │
       ▼
      Git
       │
       ▼
    GitHub
       │
       ▼
    Vercel
       │
       ▼
 Next.js Build
       │
       ▼
 Production
```

### Vercel Environment Variables

Configure the required environment variables in:

```text
Vercel
 → Project
 → Settings
 → Environment Variables
```



After changing environment variables, redeploy the application.

---

# 🔄 AI Provider Fallback

The application uses an AI routing architecture to manage multiple AI providers.

```text
Application
     │
     ▼
  AI Router
     │
     ▼
   Gemini
     │
 ┌───┴────┐
 │        │
Success  Failure
 │        │
 ▼        ▼
Response  Groq
           │
           ▼
        Response
```

This architecture can help handle:

- Provider downtime
- API errors
- Rate limits
- Usage quotas
- Temporary provider failures

---

# 🧩 API Architecture

The backend is organized into separate API routes for different product capabilities.

Examples:

```text
/api/agent
/api/chat
/api/code-generator
/api/draw
/api/images
/api/history
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

This keeps individual application capabilities separated instead of relying on one monolithic API endpoint.

---

# 📊 Current Development Status

## Phase 1 — Foundation

**Status: ✅ Completed**

- Next.js application foundation
- React UI
- Tailwind CSS
- Dashboard
- Authentication
- API architecture
- Database integration
- Initial AI integrations

## Phase 2 — Unified AI Workspace

**Status: ✅ Completed**

- AI Chat
- Nova AI Agent
- AI Code Generator
- AI Project Architect
- AI Image Studio
- AI Design Board
- Learning tools
- Notes
- Quizzes
- Flashcards
- Roadmaps
- Mock tests
- Persistent sessions
- Conversation history

## Phase 3 — Developer AI Workflows

**Status: 🚧 In Progress**

Current development focus includes:

- Improved AI code generation
- Live artifact preview
- Better code validation
- Improved AI provider routing
- Developer workflows
- Project generation
- Deployment workflows
- Advanced AI agents

---

# 🎯 Development Philosophy

AI Learning Hub is built around this workflow:

```text
        LEARN
          │
          ▼
        ASK AI
          │
          ▼
      UNDERSTAND
          │
          ▼
         BUILD
          │
          ▼
         TEST
          │
          ▼
        DEBUG
          │
          ▼
       IMPROVE
          │
          ▼
        DEPLOY
```

The goal is not only to provide AI answers, but to help users turn those answers into practical results.

---

# 💡 Why I Built AI Learning Hub

Students and developers often need many different tools for learning and building software.

For example:

```text
AI Chat
Code Generator
Learning Platform
Interview Preparation
Architecture Tool
Notes
Image Generator
Project Planner
```

AI Learning Hub is an attempt to bring these workflows together.

### Long-term vision

```text
Learn a technology
       ↓
Ask AI questions
       ↓
Generate a project
       ↓
Understand the architecture
       ↓
Write code
       ↓
Preview the result
       ↓
Test and debug
       ↓
Deploy
```

The long-term goal is to build an AI-powered workspace where users can learn technology and immediately turn that knowledge into working products.

---

# 🛣️ Roadmap

## 🤖 AI

- [ ] Multi-agent orchestration
- [ ] Improved AI provider routing
- [ ] Better tool usage
- [ ] Voice interaction
- [ ] Better contextual memory
- [ ] More reliable AI workflows
- [ ] Advanced AI agents

## 💻 Developer Tools

- [ ] Advanced code execution
- [ ] Automated debugging
- [ ] GitHub workflow improvements
- [ ] Project generation improvements
- [ ] Deployment automation
- [ ] Better artifact preview
- [ ] More framework support

## 📚 Learning

- [ ] Personalized learning paths
- [ ] More learning resources
- [ ] Personalized curriculum
- [ ] Better progress analytics
- [ ] More interview simulations
- [ ] Advanced coding practice

## 🎨 Creative Tools

- [ ] Improved image workflows
- [ ] Better design-board features
- [ ] AI-assisted UI generation
- [ ] Exportable architecture diagrams
- [ ] More visual AI tools

---

# 🔒 Security

Security is an important part of the application architecture.

Never expose:

```text
API Keys
Database Passwords
Clerk Secret Keys
Private Tokens
Deployment Credentials
```

Sensitive values should remain in server-side environment variables.

Only values intentionally designed to be public should use the `NEXT_PUBLIC_` prefix.

---

# ⚠️ Important Notes

AI providers can have:

- Rate limits
- Usage quotas
- Temporary outages
- Model availability changes
- API changes

For example:

```text
HTTP 429
Rate Limit Exceeded
```

can occur when a provider reaches a usage limit.

The application therefore supports fallback behavior where configured.

Database connectivity also depends on correctly configured Supabase connection strings and production environment variables.

---

# 🧑‍💻 Creator

## Ankit Jatav

**Founder & Lead Developer — AI Learning Hub**

Building AI-powered software focused on:

- Artificial Intelligence
- Generative AI
- AI Agents
- Full-stack development
- RAG systems
- Developer tools
- Learning platforms
- AI-powered productivity

### Mission

> Build practical AI tools that help people learn faster, build better software, and turn ideas into working products.

---

# 🤝 Contributing

Contributions, ideas, feedback, and bug reports are welcome.

### Development workflow

```bash
git clone YOUR_GITHUB_REPOSITORY_URL

cd ai-learning-hub

npm install

npm run dev
```

Create a feature branch:

```bash
git checkout -b feature/your-feature
```

After making changes:

```bash
git add .
git commit -m "feat: improve AI Learning Hub"
git push origin feature/your-feature
```

Then create a Pull Request on GitHub.

---

# ⭐ Support the Project

If you find AI Learning Hub interesting:

- ⭐ Star the repository
- 🐛 Report bugs
- 💡 Suggest features
- 🔧 Contribute improvements
- 📢 Share the project

---

# 📄 License

This project is currently intended for personal and educational use.

A formal open-source license can be added when the project is officially released as open source.

---

# 🚀 AI Learning Hub

> **Learn. Build. Experiment. Improve. Deploy.**

**AI Learning Hub — One workspace for learning, building, and working with AI.**
