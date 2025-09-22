# PacMan Game

## Overview

This is a full-stack web application featuring a PacMan game built with React and TypeScript. The project uses a modern tech stack with React Three Fiber for 3D graphics capabilities, a comprehensive UI component library based on Radix UI, and Express.js for the backend. The game implements classic PacMan mechanics including ghost AI, pellet collection, power pellets, and progressive difficulty levels.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript for type safety and modern development practices
- **Build Tool**: Vite for fast development and optimized production builds
- **Styling**: Tailwind CSS for utility-first styling with custom design system variables
- **State Management**: Zustand for lightweight, hook-based state management
- **UI Components**: Comprehensive component library built on Radix UI primitives for accessibility
- **3D Graphics**: React Three Fiber and Drei for 3D rendering capabilities (though currently used for a 2D game)
- **Data Fetching**: TanStack Query for server state management and caching

### Game Engine Architecture
- **Core Engine**: Custom GameEngine class managing game loop, collision detection, and game state
- **Entity System**: Separate classes for PacMan, Ghost, and GameMap with clear separation of concerns
- **Game Loop**: RequestAnimationFrame-based rendering with fixed timestep updates
- **Audio System**: HTML5 Audio API integration with mute/unmute functionality
- **Input Handling**: Keyboard event system with direction queuing for smooth movement
- **Persistence**: LocalStorage for high score tracking

### Backend Architecture
- **Framework**: Express.js with TypeScript for type-safe server development
- **Database ORM**: Drizzle ORM configured for PostgreSQL with type-safe queries
- **Database**: PostgreSQL configured through environment variables
- **Session Management**: Connect-pg-simple for PostgreSQL-backed session storage
- **Development**: Hot reload setup with tsx for development server
- **Production**: ESBuild for server bundling and optimization

### Data Storage Solutions
- **Primary Database**: PostgreSQL with Neon Database serverless connection
- **ORM**: Drizzle ORM for type-safe database operations and migrations
- **Schema Management**: Centralized schema definitions in shared directory
- **Session Storage**: PostgreSQL-backed session management for scalability
- **Client Storage**: LocalStorage for game state persistence (high scores)

### Authentication and Authorization
- **User System**: Basic user schema with username/password authentication
- **Session Management**: Server-side session storage with PostgreSQL backend
- **Memory Fallback**: In-memory storage implementation for development/testing
- **Schema Validation**: Zod integration for runtime type validation

## External Dependencies

### Core Framework Dependencies
- **@neondatabase/serverless**: Serverless PostgreSQL connection for Neon Database
- **drizzle-orm**: Type-safe ORM for database operations
- **express**: Web server framework for API endpoints
- **react**: Core React library for UI development
- **vite**: Build tool and development server

### UI and Styling
- **@radix-ui/react-***: Complete collection of accessible UI primitives
- **tailwindcss**: Utility-first CSS framework
- **@fontsource/inter**: Self-hosted Inter font family
- **class-variance-authority**: Type-safe CSS class variance management
- **clsx**: Utility for conditional CSS classes

### 3D Graphics and Animation
- **@react-three/fiber**: React renderer for Three.js
- **@react-three/drei**: Useful helpers for React Three Fiber
- **@react-three/postprocessing**: Post-processing effects for 3D scenes
- **vite-plugin-glsl**: GLSL shader support for custom graphics

### State Management and Data Fetching
- **zustand**: Lightweight state management solution
- **@tanstack/react-query**: Server state management and caching
- **zod**: Runtime type validation and schema parsing

### Development Tools
- **typescript**: Static type checking
- **tsx**: TypeScript execution for development
- **esbuild**: Fast JavaScript bundler for production
- **@replit/vite-plugin-runtime-error-modal**: Development error overlay

### Audio and Media Support
- **HTML5 Audio API**: Native browser audio support for game sounds
- **Asset Support**: Vite configuration for GLTF, GLB, MP3, OGG, and WAV files