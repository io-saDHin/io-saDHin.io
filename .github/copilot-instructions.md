# AI Coding Guidelines for io-saDHin.io

## Project Overview
This is a personal portfolio website built with Laravel, deployed on Tencent CloudBase. The repository is currently in a minimal/placeholder state with core configuration files established.

## Architecture & Tech Stack
- **Framework**: Laravel (PHP) - Full-stack framework with MVC architecture
- **Deployment**: Tencent CloudBase - Serverless cloud platform with container support
- **Database**: Laravel supports multiple databases (MySQL, PostgreSQL, SQLite, etc.)
- **Frontend**: Blade templating engine with optional modern frontend integration
- **License**: Apache 2.0

### Laravel + CloudBase Integration
- **Containerization**: Application runs in CloudBase containers defined in `.cloudbase/container/`
  - Use Dockerfiles for PHP/Laravel applications with Nginx + PHP-FPM setup
  - Container exposes port 80 for web traffic
  - CloudBase handles container orchestration and scaling
- **Environment**: Use Laravel's `.env` files for configuration; CloudBase handles environment variables
  - Environment variables set via CloudBase console or cloudbaserc.json
  - Access via `env()` helper or `$_ENV` in Laravel
  - Separate environments (dev/staging/prod) supported
- **Storage**: Leverage CloudBase's cloud storage for Laravel's storage needs
  - File uploads handled via CloudBase Storage SDK
  - Static assets served through CloudBase Hosting/CDN
  - Database files and user uploads stored in cloud storage
- **Routing**: Standard Laravel routing with CloudBase's reverse proxy handling
  - Nginx configuration routes requests to Laravel's public/index.php
  - URL rewriting for clean URLs (`/about` → `/index.php/about`)
  - API routes and web routes work seamlessly
- **Assets**: Public assets served through CloudBase's CDN capabilities
  - Static files (CSS/JS/images) deployed to CloudBase Hosting
  - CDN acceleration for faster global delivery
  - Laravel Mix/Webpack builds output to `public/` directory

## Development Workflow
- **Local Development**: Standard Laravel development practices
- **Deployment**: CloudBase handles build and deployment automatically
- **Version Control**: Git with main branch as default

## Key Conventions
- **Environment**: Use `.env` files for configuration (Laravel standard)
- **Assets**: Public assets go in `public/` directory
- **Storage**: Laravel storage conventions apply
- **Dependencies**: Composer for PHP packages

## File Structure Expectations
```
/
├── app/           # Laravel application code
├── public/        # Public assets and entry point
├── resources/     # Views, assets, language files
├── routes/        # Route definitions
├── storage/       # File storage
├── .cloudbase/    # CloudBase deployment config
└── .vscode/       # VS Code workspace settings
```

## Deployment Notes
- CloudBase container configuration in `.cloudbase/container/`
- Build process handled by CloudBase platform
- No manual build steps required locally

## Current State
Repository is initialized but application code not yet implemented. Focus on establishing Laravel project structure and basic portfolio functionality.