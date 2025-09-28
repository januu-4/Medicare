# MediReportInterpreter

## Overview

MediReportInterpreter is a comprehensive healthcare platform that helps patients understand their medical reports through AI-powered analysis. The system combines OCR technology, natural language processing, and medical expertise to transform complex medical documents into easily understandable insights. Built as a full-stack application with React frontend and Express backend, it integrates with Firebase for authentication and data storage, Google Cloud Vision for OCR processing, and AI models (Gemini/OpenAI) for intelligent medical analysis.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
The client application uses **React with TypeScript** and follows a component-based architecture with modern tooling:
- **UI Framework**: Shadcn/ui components built on Radix UI primitives for accessibility and consistency
- **Styling**: Tailwind CSS with a healthcare-focused design system featuring medical blue color palette and Material Design patterns
- **State Management**: React Query (TanStack Query) for server state management and caching
- **Routing**: Wouter for client-side routing
- **Build Tool**: Vite for fast development and optimized production builds
- **Component Structure**: Modular components including Dashboard, FileUpload, HealthTimeline, ChatInterface, and Reminders

### Backend Architecture
The server follows a **RESTful API design** with Express.js:
- **Framework**: Express.js with TypeScript for type safety
- **Authentication**: Firebase Admin SDK for server-side token verification
- **File Processing**: Multer for file upload handling with memory storage
- **API Structure**: Organized route handlers for uploads, OCR processing, AI analysis, and user management
- **Error Handling**: Centralized error middleware with proper HTTP status codes

### Data Storage Solutions
**Firebase Ecosystem** serves as the primary data layer:
- **Authentication**: Firebase Auth with email/password and Google OAuth
- **Database**: Firestore with collections for users, reports, health timelines, reminders, and chat data
- **File Storage**: Firebase Storage for medical document storage
- **Real-time Updates**: Firestore real-time listeners for live data synchronization

### OCR and AI Processing Pipeline
**Multi-stage processing** ensures reliable document analysis:
- **Primary OCR**: Client-side Tesseract.js for initial text extraction
- **Fallback OCR**: Google Cloud Vision API for complex or low-confidence documents
- **AI Analysis**: Gemini AI for medical interpretation and clinical value extraction
- **Multilingual Support**: OpenAI integration for translation and multilingual prescription analysis

### Authentication and Authorization
**Firebase-based security** with role-based access:
- **Client Authentication**: Firebase Auth SDK with redirect-based Google OAuth
- **Server Verification**: Firebase Admin SDK for ID token validation
- **Access Control**: Middleware-based user validation and resource protection
- **Session Management**: JWT tokens with automatic refresh handling

## External Dependencies

### Core Services
- **Firebase**: Complete backend-as-a-service for authentication, database, and storage
- **Google Cloud Vision API**: Advanced OCR capabilities for medical documents
- **Google Gemini AI**: Medical text analysis and clinical value extraction
- **OpenAI GPT**: Multilingual translation and prescription analysis

### Development and UI Libraries
- **Shadcn/ui + Radix UI**: Accessible component library with healthcare-appropriate styling
- **React Query**: Server state management and caching
- **React Hook Form**: Form validation and management
- **Recharts**: Medical data visualization and health trend charts
- **React Dropzone**: File upload interface with drag-and-drop support

### Processing Libraries
- **Tesseract.js**: Client-side OCR processing
- **Multer**: Server-side file upload handling
- **Zod**: Runtime type validation and schema definition
- **UUID**: Unique identifier generation for reports and records

### Development Tools
- **Vite**: Fast development server and build tool
- **TypeScript**: Type safety across frontend and backend
- **Tailwind CSS**: Utility-first styling with healthcare design system
- **ESBuild**: Fast server-side bundling for production