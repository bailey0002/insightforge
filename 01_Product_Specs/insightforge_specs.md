# InsightForge MVP Specifications

## Overview
InsightForge is a SaaS platform for AI-driven business ideation, validation, and prototyping. The MVP (target: Nov 10-17, 2025) focuses on core features: X sentiment analysis for market validation and a prototyping tool for rapid business model mockups.

## MVP Features
| Feature | Description | Priority | Status |
|---------|-------------|----------|--------|
| X Sentiment Analysis | Analyze X posts to gauge market sentiment for business ideas using AI (LangChain). | High | Not Started |
| Prototyping Tool | Create basic business model mockups (e.g., canvas templates) with drag-and-drop UI. | High | Not Started |
| User Dashboard | Next.js UI for managing ideas, viewing sentiment results, and accessing prototypes. | Medium | Not Started |
| Supabase Backend | Store user data, ideas, and prototype metadata securely. | Medium | Not Started |

## Feature Details
### 1. X Sentiment Analysis
- **Description**: Users input a business idea (e.g., “sustainable coffee shop in Seattle”). The platform queries X posts via API, processes them with LangChain for sentiment (positive/negative/neutral), and summarizes market demand.
- **Tech**:
  - Backend: FastAPI endpoint (`/analyze-sentiment`) using LangChain for NLP.
  - X API: Fetch posts with keywords (e.g., “coffee shop Seattle”).
  - Output: JSON with sentiment scores (e.g., 60% positive, 30% neutral, 10% negative).
- **User Story**: As a user, I want to input a business idea and see how the market feels about it based on X posts, so I can validate demand before prototyping.
- **Acceptance Criteria**:
  - Input field accepts text (max 200 chars).
  - Results display in <10s with sentiment breakdown and sample X posts.
  - Error handling for API rate limits or invalid queries.

### 2. Prototyping Tool
- **Description**: Users create visual business model mockups (e.g., business model canvas) using predefined templates and drag-and-drop components.
- **Tech**:
  - Frontend: Next.js with React-Konva or similar for drag-and-drop UI.
  - Backend: Supabase to store prototype metadata (e.g., canvas JSON).
  - Templates: 2-3 predefined layouts (e.g., lean canvas, SWOT).
- **User Story**: As a user, I want to build a visual prototype of my business idea, so I can test and share it with stakeholders.
- **Acceptance Criteria**:
  - Drag-and-drop interface for adding text, shapes, connectors.
  - Save/load prototypes to Supabase.
  - Export as PNG/PDF.

### 3. User Dashboard
- **Description**: Centralized UI for managing ideas, viewing sentiment results, and accessing prototypes.
- **Tech**:
  - Frontend: Next.js with Tailwind CSS for responsive design.
  - Backend: FastAPI for API routes, Supabase for auth/data.
- **User Story**: As a user, I want a dashboard to track my ideas and prototypes, so I can manage my projects efficiently.
- **Acceptance Criteria**:
  - Displays list of ideas with sentiment scores.
  - Links to saved prototypes.
  - User login via Supabase Auth (email or OAuth).

### 4. Supabase Backend
- **Description**: Secure storage for user data, ideas, sentiment results, and prototype metadata.
- **Tech**:
  - Supabase: PostgreSQL for data, Auth for user management.
  - FastAPI: CRUD endpoints for ideas/prototypes.
- **User Story**: As a user, I want my data stored securely and accessible across sessions, so I can revisit my work.
- **Acceptance Criteria**:
  - User signup/login with email or OAuth.
  - Store/retrieve ideas and prototypes via API.
  - GDPR-compliant data handling.

## Non-Functional Requirements
- **Performance**: Sentiment analysis <10s, prototype rendering <2s.
- **Scalability**: Handle 100 concurrent users (Vercel hosting).
- **Security**: Supabase Auth, HTTPS, no sensitive data in X queries.
- **Compatibility**: Chrome, Safari, Firefox (latest versions).

## Risks
- X API rate limits: Implement caching in FastAPI.
- LangChain setup: Ensure Python 3.11 compatibility in venv.
- Next.js learning curve: Use Vercel templates for quick start.

## Next Steps
- Set up Next.js frontend (`npx create-next-app`, Oct 1).
- Configure Supabase project and Auth (Oct 3).
- Test X API integration with mock queries (Oct 5).
