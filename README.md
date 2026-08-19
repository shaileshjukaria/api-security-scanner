API Security Scanner


«A full-stack API security testing platform designed to identify common REST API vulnerabilities based on the OWASP API Security Top 10.»

Overview

API Security Scanner is a cybersecurity project that automates security checks against REST APIs and presents the results through a web-based dashboard.

The project combines a Python/FastAPI backend with a React frontend to provide a practical environment for learning API security testing, vulnerability detection, and security reporting.

It can be used for authorized security testing of APIs in development, lab, and educational environments.

Features

- 🔍 Automated REST API security scanning
- 🛡️ Checks inspired by the OWASP API Security Top 10
- 🔐 Authentication and authorization security testing
- 💉 SQL injection detection
- 🔓 Authentication bypass testing
- 🆔 IDOR / Broken Object Level Authorization testing
- 🚦 Rate-limit weakness detection
- 🔑 JWT-based authentication
- 🔒 Bcrypt password hashing
- 📊 Web dashboard for managing and reviewing scans
- 📝 Detailed vulnerability reports
- 📚 Scan history and endpoint-level results
- ⚙️ Configurable scanning modules and payloads
- 🐳 Docker-based deployment

Vulnerability Checks

The scanner currently focuses on several common API security issues:

Security Check| Description
SQL Injection| Tests API parameters for SQL injection weaknesses
Authentication| Identifies weaknesses in authentication mechanisms
IDOR| Tests for unauthorized access to other users' resources
Rate Limiting| Checks whether endpoints adequately restrict excessive requests
JWT Security| Evaluates authentication flows using JSON Web Tokens

«Note: This project is intended for authorized testing only. Do not scan APIs or systems without explicit permission.»

Architecture

                    ┌──────────────────────┐
                    │     React Dashboard  │
                    │   TypeScript + Vite  │
                    └──────────┬───────────┘
                               │
                               │ HTTP API
                               ▼
                    ┌──────────────────────┐
                    │      FastAPI         │
                    │   Security Scanner   │
                    └──────────┬───────────┘
                               │
             ┌─────────────────┼─────────────────┐
             │                 │                 │
             ▼                 ▼                 ▼
       ┌───────────┐     ┌────────────┐    ┌────────────┐
       │ SQLi Test │     │ Auth / JWT │    │ IDOR Test  │
       └───────────┘     └────────────┘    └────────────┘
             │                 │                 │
             └─────────────────┼─────────────────┘
                               ▼
                    ┌──────────────────────┐
                    │      PostgreSQL      │
                    │   Scan Results/Data  │
                    └──────────────────────┘

Technology Stack

Backend

- Python
- FastAPI
- SQLAlchemy
- PostgreSQL
- Alembic
- HTTPX
- AIOHTTP

Frontend

- React
- TypeScript
- Vite

Security

- OWASP API Security Top 10
- JWT
- Bcrypt
- SQL Injection testing
- IDOR testing
- Authentication testing
- Rate-limit testing

Deployment

- Docker
- Docker Compose

Project Structure

api-security-scanner/
│
├── backend/
│   ├── app/
│   ├── scanners/
│   ├── models/
│   └── ...
│
├── frontend/
│   ├── src/
│   ├── components/
│   └── ...
│
├── learn/
│   ├── 00-OVERVIEW.md
│   ├── 01-CONCEPTS.md
│   ├── 02-ARCHITECTURE.md
│   ├── 03-IMPLEMENTATION.md
│   └── 04-CHALLENGES.md
│
├── docker-compose.yml
└── README.md

Installation & Setup

Prerequisites

Make sure the following are installed:

- Git
- Docker
- Docker Compose

Clone your repository:

git clone https://github.com/YOUR-USERNAME/api-security-scanner.git
cd api-security-scanner

Start the Application

Run:

docker compose up -d

After the containers start, open:

http://localhost:8080

The React dashboard should now be available.

Stop the Application

docker compose down

To remove the containers and associated volumes:

docker compose down -v

Learning Resources

The project includes learning material covering the concepts behind the scanner.

Module| Topic
00 - Overview| Prerequisites, project setup and introduction
01 - Concepts| API security concepts and common vulnerabilities
02 - Architecture| Application architecture and data flow
03 - Implementation| Scanner implementation and code walkthrough
04 - Challenges| Possible improvements and extension ideas

These materials can also be used as a roadmap for understanding how API security testing tools are designed.

Future Improvements

Some areas I plan to explore further:

- [ ] Add additional OWASP API Security checks
- [ ] Improve vulnerability detection accuracy
- [ ] Add customizable scan profiles
- [ ] Add severity-based vulnerability scoring
- [ ] Improve security report generation
- [ ] Add API endpoint discovery
- [ ] Add OpenAPI/Swagger import
- [ ] Add asynchronous scanning improvements
- [ ] Improve dashboard visualizations
- [ ] Add automated security regression testing

Security & Responsible Use

This project is intended for:

- Personal cybersecurity labs
- Educational purposes
- Development environments
- Authorized penetration testing
- Security research

Only test APIs and systems that you own or have explicit permission to assess.

Unauthorized scanning of third-party systems may violate laws, terms of service, or organizational policies.

Inspiration & Attribution

This project was developed as a cybersecurity learning and implementation project and was inspired by existing open-source API security scanner projects, including the work by Carter Perez.

The original project provided useful inspiration for understanding API security scanning concepts, architecture, and learning resources.

This repository is maintained independently and should not be considered the original author's repository.

License

AGPL-3.0

---

Author

Shailesh Jukaria

Computer Science & Engineering Student
Cybersecurity & Full-Stack Development

GitHub: "https://github.com/shaileshjukaria"
