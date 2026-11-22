# Multi-Channel Social Content Automation Studio

> Full-stack content generation and cross-platform publishing suite for marketing workflows.

[![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?style=flat-square&logo=github)](https://github.com/sohailahmed-bsrh/social-post-studio)
[![Live Showcase](https://img.shields.io/badge/Live-Showcase-0A66C2?style=flat-square&logo=googlechrome)](https://sohail.devsil.com/projects.html)
[![Author](https://img.shields.io/badge/Author-Sohail%20Ahmed-20BEFF?style=flat-square)](https://sohail.devsil.com)

---

## Overview

Content creators and growth teams struggle to maintain consistent publication schedules across disparate social networks with varying format constraints.

This project provides an end-to-end, reproducible implementation engineered to solve this challenge through verified data transformations, reliable algorithms, and production-ready architecture.

---

## Key Features

- Automated copy adaptation for Twitter, LinkedIn, and Instagram character and tone specifications
- Integrated image generator previewing promotional card designs
- Multi-channel scheduling and publication queue management
- TypeScript agents architecture for background automation tasks

---

## System Architecture

```mermaid
flowchart TD
    Prompt[Campaign Idea / Source Article] --> Agent[Content Generation Agent]
    Agent --> Twitter[Twitter Thread Formatter]
    Agent --> LinkedIn[LinkedIn Post Formatter]
    Agent --> Instagram[Visual Caption Formatter]
    Twitter --> Queue[Publishing Scheduler Queue]
    LinkedIn --> Queue
    Instagram --> Queue
    Queue --> Publish[Live Social Channel Distribution]
```

---

## Technology Stack

| Technology | Version / Spec | Role in Architecture |
| :--- | :--- | :--- |
| **React & TypeScript** | `18.2+` | Frontend studio interface with live card previews |
| **Node.js & Express** | `18+` | Backend scheduling engine and API connectors |
| **Drizzle ORM** | `0.28+` | PostgreSQL relational data persistence |
| **Tailwind CSS** | `3.3+` | Component design system |

---

## Repository Structure

```text
social-post-studio/
|-- agents/
|   |-- src/
|   `-- package.json
|-- src/
|-- .env.example
|-- .gitignore
|-- package.json
`-- README.md
```

---

## Installation and Execution

### Prerequisites
- Node.js 18+ / Python 3.10+
- Git version control

### Setup Instructions
1. Clone the repository:
```bash
git clone https://github.com/sohailahmed-bsrh/social-post-studio.git
cd social-post-studio
```

2. Configure environment and dependencies:
```bash
npm install
cp .env.example .env
npm run dev
```

---

## Interface and Verification
The system produces verifiable execution logs, prediction matrices, or interactive browser interfaces depending on the target mode. Verify operation by executing the commands specified above or inspecting the demonstration notebooks.

---

## Author and Contact
Developed by **Sohail Ahmed** — Full Stack AI Engineer & Machine Learning Specialist.
- **Portfolio:** [sohail.devsil.com](https://sohail.devsil.com)
- **GitHub:** [@sohailahmed-bsrh](https://github.com/sohailahmed-bsrh)
- **Email:** [sohail.bsrh@gmail.com](mailto:sohail.bsrh@gmail.com)

---

## Author & Contact Information

<table width="100%" align="center">
  <tr>
    <td align="center" style="padding: 20px;">
      <h3>Sohail Ahmed</h3>
      <p><strong>Full-Stack Artificial Intelligence & Computer Vision Engineer</strong></p>
      <p>
        <a href="https://sohail.devsil.com"><img src="https://img.shields.io/badge/Live_Portfolio-sohail.devsil.com-0052FF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Portfolio"/></a>
        <a href="https://github.com/sohailahmed-bsrh"><img src="https://img.shields.io/badge/GitHub-Profile-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/></a>
        <a href="https://linkedin.com/in/sohail-ahmed-dev"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
        <a href="mailto:sohail.bsrh@gmail.com"><img src="https://img.shields.io/badge/Email-Contact_Me-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
      </p>
      <p><em>Available for technical roles in Artificial Intelligence, Computer Vision, and Full-Stack Engineering.</em></p>
      <hr style="border: 0; height: 1px; background: #30363d; margin: 15px 0;">
      <small>Distributed under the MIT License.</small>
    </td>
  </tr>
</table>
