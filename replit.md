# JSON Editor Online

## Overview

This is a full-stack JSON editor web application built with React, TypeScript, and Express.js. The application provides a comprehensive JSON editing experience with features like dual-panel editing, multiple view modes (text, tree, and table views), JSON validation, formatting, and transformation capabilities. It's designed as a modern web-based alternative to desktop JSON editors, offering real-time validation, syntax highlighting, and advanced JSON manipulation tools.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript for type safety and modern development
- **Build Tool**: Vite for fast development and optimized production builds
- **UI Framework**: Shadcn/ui component library built on Radix UI primitives
- **Styling**: Tailwind CSS for utility-first styling with custom CSS variables for theming
- **State Management**: React Query (@tanstack/react-query) for server state and caching
- **Routing**: Wouter for lightweight client-side routing
- **Form Handling**: React Hook Form with Zod schema validation

### Component Structure
- **Dual Editor Panels**: Left and right editing panels that can be swapped and compared
- **Multiple View Modes**: Text editor, tree view, and table view for different JSON visualization needs
- **Transform System**: Modal-based JSON transformation with support for JSONPath, JMESPath, and custom JavaScript
- **Theme Support**: Light/dark mode toggle with system preference detection

### Backend Architecture
- **Framework**: Express.js with TypeScript for the REST API server
- **Development Setup**: Hot module replacement with Vite integration in development
- **Static Serving**: Production builds served as static files with Express fallback
- **Storage Interface**: Abstracted storage layer with in-memory implementation (ready for database integration)

### Database Design
- **ORM**: Drizzle ORM with PostgreSQL dialect for type-safe database operations
- **Schema**: Documents table with UUID primary keys, name, content, and timestamps
- **Migrations**: Drizzle Kit for schema management and database migrations
- **Validation**: Zod schemas for runtime type checking and API validation

### Authentication & Sessions
- **Session Management**: Express sessions with PostgreSQL session store (connect-pg-simple)
- **User System**: Basic user schema with username/password fields prepared for authentication

### Development Tools
- **TypeScript**: Strict type checking across the entire stack
- **ESBuild**: Fast TypeScript compilation for production server builds
- **Hot Reload**: Development server with automatic reloading for both client and server
- **Path Aliases**: Organized import structure with @ aliases for clean code organization

## External Dependencies

### Database & Storage
- **Neon Database**: PostgreSQL-compatible serverless database (@neondatabase/serverless)
- **Session Store**: PostgreSQL session storage for user sessions

### UI & Styling
- **Radix UI**: Accessible, unstyled UI primitives for complex components
- **Lucide Icons**: Modern icon library for consistent iconography  
- **Tailwind CSS**: Utility-first CSS framework with PostCSS processing
- **Google Fonts**: Inter and JetBrains Mono fonts for typography

### Development & Build
- **Vite**: Build tool with React plugin and runtime error overlay
- **Replit Integration**: Development environment integration with cartographer plugin
- **ESBuild**: Fast JavaScript/TypeScript bundler for production builds

### Utilities & Libraries
- **Date-fns**: Date manipulation and formatting
- **Class Variance Authority**: Type-safe CSS class variants
- **CLSX & Tailwind Merge**: Conditional CSS class composition
- **Nanoid**: URL-safe unique ID generation
- **CMDK**: Command palette component for advanced user interactions

### JSON Processing
- **Native JSON**: Built-in JavaScript JSON parsing and stringification
- **Custom Utilities**: JSON validation, formatting, minification, and CSV conversion
- **Transform Support**: JSONPath and JMESPath query language support for data transformation