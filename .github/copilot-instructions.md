# AI Coding Guidelines for io-saDHin.io

## Project Overview
This is a personal portfolio website built with Laravel, deployed on Tencent CloudBase. The repository is currently in a minimal/placeholder state with core configuration files established.

## Architecture & Tech Stack
- **Framework**: Laravel (PHP)
- **Deployment**: Tencent CloudBase
- **License**: Apache 2.0

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