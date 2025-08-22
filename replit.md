# Emergency Response System

## Overview

This is a comprehensive emergency response web application built with React, Express.js, and PostgreSQL. The system connects users to emergency services, hospitals, and ambulance dispatch with real-time tracking and communication features. It provides a complete workflow from emergency request submission to hospital assignment and patient care coordination.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript using Vite as the build tool
- **UI Components**: Shadcn/UI component library with Radix UI primitives
- **Styling**: Tailwind CSS with custom emergency-themed color palette
- **State Management**: TanStack Query (React Query) for server state management
- **Routing**: Wouter for client-side routing
- **Forms**: React Hook Form with Zod validation

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **API Design**: RESTful API structure with modular route handlers
- **Development**: Hot reloading with Vite middleware integration
- **Error Handling**: Centralized error handling middleware

### Data Storage
- **Database**: PostgreSQL with Drizzle ORM
- **Schema Design**: Comprehensive emergency management schema including:
  - Users and authentication
  - Hospital network with location data
  - Emergency requests with status tracking
  - Patient information management
  - Status updates for real-time communication
- **In-Memory Fallback**: MemStorage class for development/testing

### Authentication & Authorization
- Session-based authentication using express-session
- PostgreSQL session store with connect-pg-simple
- User management with secure password handling

### Key Features
- **Emergency Request System**: Multi-step form for emergency submission with severity classification
- **Hospital Search & Matching**: Geolocation-based hospital discovery with availability filtering
- **Real-time Status Updates**: Live tracking of emergency request progress
- **Patient Information Management**: Comprehensive medical history and contact information
- **Ambulance Dispatch**: Direct hospital communication and ETA tracking

### Design Patterns
- **Monorepo Structure**: Shared schema and types between client/server
- **Component-based UI**: Reusable UI components with consistent styling
- **Form Validation**: Zod schemas for type-safe data validation
- **Error Boundaries**: Graceful error handling with user feedback
- **Responsive Design**: Mobile-first approach with emergency-optimized UX

## External Dependencies

### Core Framework Dependencies
- **@neondatabase/serverless**: PostgreSQL serverless driver for database connectivity
- **drizzle-orm** & **drizzle-kit**: Type-safe ORM with PostgreSQL dialect
- **express**: Web application framework for API server
- **react** & **react-dom**: Frontend framework and rendering

### UI & Styling Dependencies
- **@radix-ui/**: Complete set of accessible UI primitives (dialogs, forms, navigation)
- **tailwindcss**: Utility-first CSS framework
- **class-variance-authority**: Utility for managing CSS class variants
- **lucide-react**: Icon library for consistent iconography

### Development & Build Tools
- **vite**: Fast build tool and dev server
- **typescript**: Type safety across the application
- **@replit/vite-plugin-runtime-error-modal**: Development error overlay
- **tsx**: TypeScript execution for server development

### Form & Validation Libraries
- **react-hook-form**: Performant form library with validation
- **@hookform/resolvers**: Integration between React Hook Form and Zod
- **zod**: Schema validation library for type-safe data handling

### Database & Session Management
- **connect-pg-simple**: PostgreSQL session store for Express sessions
- **drizzle-zod**: Integration between Drizzle ORM and Zod schemas

### Utility Libraries
- **@tanstack/react-query**: Server state management and caching
- **date-fns**: Date manipulation and formatting
- **clsx** & **tailwind-merge**: CSS class management utilities