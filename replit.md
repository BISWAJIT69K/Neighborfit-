# NeighborFit - Neighborhood Search Application

## Overview

NeighborFit is a full-stack web application designed to help users find their perfect neighborhood in India. The platform allows users to search through neighborhoods based on various criteria including budget, location preferences, user type, and desired facilities. The application features a React frontend with a Node.js Express backend, using PostgreSQL for data storage.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript
- **Build Tool**: Vite for fast development and optimized builds
- **UI Library**: Radix UI components with shadcn/ui design system
- **Styling**: Tailwind CSS with custom Indian-themed color palette
- **State Management**: TanStack Query for server state management
- **Routing**: Wouter for lightweight client-side routing
- **Form Handling**: React Hook Form with Zod validation

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **Database**: PostgreSQL (configured for Neon Database)
- **ORM**: Drizzle ORM for type-safe database operations
- **Session Management**: Express sessions with PostgreSQL storage
- **Development**: TSX for TypeScript execution during development

### Data Storage
- **Database**: PostgreSQL with Drizzle ORM
- **Schema**: Centralized schema definitions in `shared/schema.ts`
- **Migrations**: Handled through Drizzle Kit
- **Development Storage**: In-memory storage fallback for development/testing

## Key Components

### Database Schema
- **Neighborhoods Table**: Stores neighborhood data including name, city, state, rent prices, safety scores, suitable user types, and facilities
- **Users Table**: Basic user authentication structure (currently minimal)
- **Shared Types**: TypeScript interfaces shared between frontend and backend

### API Endpoints
- `GET /api/neighborhoods` - Retrieve all neighborhoods
- `GET /api/neighborhoods/:id` - Get specific neighborhood by ID
- `POST /api/neighborhoods/search` - Search neighborhoods with criteria filtering

### Frontend Components
- **SearchForm**: Multi-step form with filters for location, budget, user type, and facilities
- **SearchResults**: Displays filtered neighborhoods with sorting options
- **NeighborhoodCard**: Individual neighborhood display with key information
- **UI Components**: Comprehensive set of reusable UI components from shadcn/ui

## Data Flow

1. **User Input**: Users fill out search criteria through the SearchForm component
2. **Client Validation**: Form data is validated using Zod schemas
3. **API Request**: Search criteria sent to backend via TanStack Query
4. **Backend Processing**: Server validates request and queries database using Drizzle ORM
5. **Database Query**: PostgreSQL returns filtered neighborhood data
6. **Response Processing**: Backend formats and returns results
7. **Frontend Display**: Results displayed in SearchResults component with sorting capabilities

## External Dependencies

### Database
- **Neon Database**: PostgreSQL-compatible serverless database
- **Connection**: Uses `@neondatabase/serverless` for optimal performance

### UI and Styling
- **Radix UI**: Accessible, unstyled UI primitives
- **Tailwind CSS**: Utility-first CSS framework
- **Lucide React**: Icon library for consistent iconography
- **Font Awesome**: Additional icons via CDN

### Development Tools
- **ESBuild**: Fast bundling for production builds
- **Replit Integration**: Development environment optimizations
- **Runtime Error Overlay**: Enhanced error handling during development

## Deployment Strategy

### Build Process
1. **Frontend Build**: Vite builds React application to `dist/public`
2. **Backend Build**: ESBuild compiles TypeScript server to `dist/index.js`
3. **Database Setup**: Drizzle migrations ensure schema is up-to-date

### Environment Configuration
- **Development**: Uses TSX for direct TypeScript execution
- **Production**: Compiled JavaScript execution with NODE_ENV=production
- **Database**: Requires DATABASE_URL environment variable

### Hosting Requirements
- Node.js runtime environment
- PostgreSQL database access
- Environment variable support for database connection

## Changelog

```
Changelog:
- July 03, 2025. Initial setup
```

## User Preferences

```
Preferred communication style: Simple, everyday language.
```