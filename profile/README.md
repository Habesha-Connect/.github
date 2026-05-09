# Habesha Connect

<div align="center">

[![Built in Ethiopia](https://img.shields.io/badge/Built%20in-Ethiopia-brightgreen)]()
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](CODE_OF_CONDUCT.md)

**Connecting Ethiopian homeowners with verified informal workers**

</div>

---

## Our Mission

Habesha Connect is transforming how Ethiopian homeowners and contractors find reliable informal workers. We're building a structured marketplace that connects **verified** electricians, plumbers, carpenters, masons, painters, and cleaners with clients who need their services.

In Ethiopia's current system, finding skilled informal workers relies entirely on personal connections and word-of-mouth referrals. This creates inefficiency, uncertainty, and limits opportunities for both clients and workers. Habesha Connect solves this by providing:

- **Trust through verification** - In-person practical and theoretical testing by vocational teachers
- **Transparent pricing** - Fixed prices per job type, no haggling
- **Accessible technology** - SMS-based interaction for workers with basic phones
- **Structured process** - From job posting to payment, everything is organized and trackable
- **Two-way accountability** - Both clients and workers build reputations through ratings and trust scores

---

## What We Build

### Web Platform
A responsive web application built with React, TypeScript, and Vite, designed primarily for Ethiopian mobile users on 3G/4G networks.

### RESTful API
A robust backend providing structured data access, authentication via phone OTP, and integration with Ethiopian payment systems.

### SMS Interface
Job matching and notification system powered by TeleRivet SMS gateway, enabling workers with basic phones to receive and accept job offers without internet access.

### Admin Portal
Comprehensive platform management for user verification, dispute resolution, pricing configuration, and analytics.

---

## Technology Stack

<table>
  <tr>
    <th>Category</th>
    <th>Technology</th>
    <th>Purpose</th>
  </tr>
  <tr>
    <td><strong>Frontend</strong></td>
    <td>React 18, TypeScript, Vite, Tailwind CSS, Radix UI</td>
    <td>Responsive web application</td>
  </tr>
  <tr>
    <td><strong>State Management</strong></td>
    <td>Zustand, TanStack Query (React Query v5)</td>
    <td>Client and server state</td>
  </tr>
  <tr>
    <td><strong>Forms</strong></td>
    <td>React Hook Form, Zod</td>
    <td>Form handling and validation</td>
  </tr>
  <tr>
    <td><strong>Backend</strong></td>
    <td>Node.js</td>
    <td>API service</td>
  </tr>
  <tr>
    <td><strong>Database</strong></td>
    <td>PostgreSQL</td>
    <td>Primary data store</td>
  </tr>
  <tr>
    <td><strong>SMS Gateway</strong></td>
    <td>TeleRivet</td>
    <td>OTP and job notifications</td>
  </tr>
  <tr>
    <td><strong>Payments</strong></td>
    <td>Telebirr, Chapa, Bank Transfer</td>
    <td>Ethiopian payment processing</td>
  </tr>
  <tr>
    <td><strong>Testing</strong></td>
    <td>Vitest, React Testing Library, Playwright</td>
    <td>Unit, integration, and E2E testing</td>
  </tr>
  <tr>
    <td><strong>CI/CD</strong></td>
    <td>GitHub Actions</td>
    <td>Continuous integration and deployment</td>
  </tr>
  <tr>
    <td><strong>Languages</strong></td>
    <td>Amharic (Primary), English</td>
    <td>User interface</td>
  </tr>
</table>

---

## Repository Structure

<table>
  <tr>
    <th>Repository</th>
    <th>Description</th>
    <th>Status</th>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Habesha-Connect/habesha-connect-web">habesha-connect-web</a>
    </td>
    <td>Frontend web application (React + Vite + TypeScript)</td>
    <td>In Development</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Habesha-Connect/habesha-connect-api">habesha-connect-api</a>
    </td>
    <td>Backend API service</td>
    <td>Planning</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Habesha-Connect/habesha-connect-database">habesha-connect-database</a>
    </td>
    <td>Database schema, migrations, and seeds</td>
    <td>Schema Complete</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Habesha-Connect/habesha-connect-docs">habesha-connect-docs</a>
    </td>
    <td>Centralized documentation and architecture</td>
    <td>In Progress</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Habesha-Connect/habesha-connect-infra">habesha-connect-infra</a>
    </td>
    <td>Infrastructure as Code and deployment configs</td>
    <td>Planning</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Habesha-Connect/habesha-connect-e2e">habesha-connect-e2e</a>
    </td>
    <td>End-to-end tests</td>
    <td>Planning</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Habesha-Connect/habesha-connect-shared">habesha-connect-shared</a>
    </td>
    <td>Shared types, utilities, and constants</td>
    <td>Planning</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Habesha-Connect/habesha-connect-design">habesha-connect-design</a>
    </td>
    <td>Design system, assets, and brand guidelines</td>
    <td>Planning</td>
  </tr>
</table>

---

## Quick Start

### Prerequisites
- Node.js 20+
- PostgreSQL 16+
- Git
- TeleRivet account (for SMS features)

### Local Development Setup

```bash
# Clone the frontend repository
git clone https://github.com/Habesha-Connect/habesha-connect-web.git
cd habesha-connect-web

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env.local

# Start development server
npm run dev
```

For full development setup instructions, see our [Development Guide](https://github.com/Habesha-Connect/habesha-connect-docs/blob/main/guides/development-setup.md).

---

## Documentation

### Core Documentation
- **[API Documentation](https://github.com/Habesha-Connect/habesha-connect-docs/blob/main/api/README.md)** - Complete REST API reference
- **[Database Schema](https://github.com/Habesha-Connect/habesha-connect-database/blob/main/README.md)** - PostgreSQL schema and relationships
- **[Frontend Architecture](https://github.com/Habesha-Connect/habesha-connect-docs/blob/main/architecture/frontend.md)** - Component design and state management
- **[User Stories](https://github.com/Habesha-Connect/habesha-connect-docs/blob/main/project/user-stories.md)** - Complete feature requirements

### Project Planning
- **[Roadmap](https://github.com/Habesha-Connect/habesha-connect-docs/blob/main/project/roadmap.md)** - Development timeline and milestones
- **[Changelog](https://github.com/Habesha-Connect/habesha-connect-docs/blob/main/project/changelog.md)** - Version history and release notes

### Guides
- **[Development Setup](https://github.com/Habesha-Connect/habesha-connect-docs/blob/main/guides/development-setup.md)** - Get started developing
- **[Testing Guide](https://github.com/Habesha-Connect/habesha-connect-docs/blob/main/guides/testing.md)** - Testing standards and practices
- **[Deployment Guide](https://github.com/Habesha-Connect/habesha-connect-docs/blob/main/guides/deployment.md)** - Production deployment process

---

## Key Features

### For Clients (Homeowners & Contractors)
- Browse verified workers by trade, location, and rating
- Fixed transparent pricing - Know the cost before booking
- Schedule jobs at your preferred date and time
- Rate and review workers after job completion
- Build trust through verification and activity history
- Mobile-first design optimized for Ethiopian networks

### For Workers (Electricians, Plumbers, etc.)
- SMS job matching - Works on any phone, no internet required
- In-person verification - Practical and theoretical testing by TVET teachers
- Build reputation through ratings and completed jobs
- Consistent work opportunities based on your verified skills
- Location-based matching - Jobs in your area
- Track earnings and job history

### For Administrators
- User management - Full control over platform users
- Verification oversight - Manage worker testing and client documents
- Pricing configuration - Set and adjust fixed prices per trade
- Dispute resolution - Mediate conflicts with evidence review
- Analytics dashboard - Monitor platform health and growth

---

## Architecture Overview

```
Client Layer
    Web App (React)        SMS Worker Interface        Admin Portal
         |                        |                        |
API Layer
         RESTful API Gateway (Authentication, Validation, Routing)
         |                        |                        |
Service Layer
    Auth Service          Job Matching Service        Payment Service
         |                        |                        |
Data Layer
              PostgreSQL Database
         |                        |
    TeleRivet SMS Gateway        Payment Gateways
```

---

## Security

We take security seriously:
- No hardcoded secrets - All credentials via environment variables
- Encrypted data - Sensitive information encrypted at rest
- Phone verification - All accounts verified via OTP
- Admin MFA - Multi-factor authentication for admin access
- Rate limiting - Protection against brute force attacks
- Input validation - All user inputs validated and sanitized
- HTTPS everywhere - TLS 1.2+ for all communications
- Regular audits - Dependencies scanned for vulnerabilities

Read our full [Security Policy](SECURITY.md).

---

## Contributing

We welcome contributions from developers passionate about improving Ethiopia's informal labor market.

### How to Contribute
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Write/update tests
5. Update documentation
6. Submit a Pull Request

Please read our:
- [Contributing Guide](CONTRIBUTING.md) for development process
- [Code of Conduct](CODE_OF_CONDUCT.md) for community standards
- [Development Setup](https://github.com/Habesha-Connect/habesha-connect-docs/blob/main/guides/development-setup.md) for technical setup

### Good First Issues
Look for issues labeled `good first issue` or `help wanted`:
- [Frontend Issues](https://github.com/Habesha-Connect/habesha-connect-web/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22)
- [Backend Issues](https://github.com/Habesha-Connect/habesha-connect-api/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22)

---

## Roadmap

### Phase 1 - MVP (Current)
- [x] Database schema design
- [x] API documentation
- [x] Frontend design system
- [x] User stories definition
- [ ] User authentication (Phone OTP)
- [ ] Worker registration and profile
- [ ] Client job posting
- [ ] SMS job matching
- [ ] Basic payments
- [ ] Rating system

### Phase 2 - Trust & Scale
- [ ] In-person verification workflow
- [ ] Client trust score system
- [ ] Advanced matching algorithm
- [ ] Dispute resolution system
- [ ] Admin portal
- [ ] Analytics dashboard

### Phase 3 - Growth
- [ ] PWA for offline access
- [ ] Advanced search and filters
- [ ] Worker portfolio
- [ ] Recurring job scheduling
- [ ] Referral program

See the full [Roadmap](https://github.com/Habesha-Connect/habesha-connect-docs/blob/main/project/roadmap.md) for details.

---

## Team

Coming soon!

---

## Project Status

| Metric | Status |
|--------|--------|
| **Current Version** | Pre-Alpha / Planning |
| **Frontend** | Architecture Defined |
| **Backend** | Planning |
| **Database** | Schema Complete |
| **API Docs** | v2.0 Complete |
| **User Stories** | 154 Stories Defined |
| **Design System** | Complete |

---

## Community

- **Website:** [habeshaconnect.com](https://habeshaconnect.com) (Coming Soon)
- **Email:** info@habeshaconnect.com
- **Support:** support@habeshaconnect.com
- **Security:** security@habeshaconnect.com

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2026 Habesha Connect

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## Acknowledgments

- Ethiopian TVET institutions for their role in worker verification
- TeleRivet for reliable SMS infrastructure in Ethiopia
- The Ethiopian developer community for their support and contributions
- All the informal workers whose skills and hard work build our communities

---

<div align="center">

**Built in Ethiopia, for Ethiopia**

*"Abero meserrat new yemeekanyaw" - Working together brings success*

</div>

---

## Contact

- **General Inquiries:** info@habeshaconnect.com
- **Partnerships:** partners@habeshaconnect.com
- **Careers:** careers@habeshaconnect.com
- **Security Issues:** security@habeshaconnect.com

---

<div align="center">

**[Documentation](https://docs.habeshaconnect.com)** | **[Contributing](CONTRIBUTING.md)** | **[Security](SECURITY.md)** | **[Code of Conduct](CODE_OF_CONDUCT.md)**

(c) 2026 Habesha Connect. All rights reserved.

</div>