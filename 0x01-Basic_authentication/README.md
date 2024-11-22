# Basic Authentication API

## Project Overview
This project implements a Flask-based API with Basic Authentication, providing secure user management and authentication mechanisms.

## Features
- RESTful API endpoints
- Basic Authentication system
- User management
- Custom error handling for unauthorized and forbidden access

## Requirements
- Python 3.7
- Flask
- pycodestyle (version 2.5)
- Ubuntu 18.04 LTS

## Installation
1. Clone the repository
2. Install dependencies:
```bash
pip3 install -r requirements.txt
```

## Running the Application
```bash
API_HOST=0.0.0.0 API_PORT=5000 python3 -m api.v1.app
```

## Authentication Methods
- Basic Authentication
- Flexible authentication type configuration via environment variables

## Project Structure
- `api/`: Main API implementation
- `api/v1/auth/`: Authentication modules
- `models/`: Data models
- `api/v1/views/`: API route implementations

## Testing
Use curl or Postman to test API endpoints
```bash
# Check API status
curl http://0.0.0.0:5000/api/v1/status
```

## Coding Standards
- All files must pass pycodestyle checks
- Comprehensive documentation for modules, classes, and functions
- Executable Python scripts with proper shebang

## Contributors
Silas Edet

## License
ALX
