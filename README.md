# Social-Post-Studio - Autonomous Multi-Agent Social Publishing Engine

<p align="center">
  <a href="https://sohail.devsil.com"><strong>Portfolio</strong></a> | 
  <a href="https://github.com/sohailahmed-bsrh"><strong>GitHub Profile</strong></a> | 
  <a href="https://github.com/sohailahmed-bsrh/social-post-studio"><strong>Source Repository</strong></a>
</p>

---

## Executive Summary & Problem Statement

Maintaining an active, high-quality social media presence across enterprise channels requires multidisciplinary coordination between copywriters, graphic designers, brand compliance managers, and digital publishers. Coordinating these specialized roles manually causes publishing delays and uneven content output.

Social-Post-Studio replaces this fragmented pipeline with an Autonomous Multi-Agent Publishing Engine. Built on TypeScript and Google Gemini, independent autonomous agents coordinate to research topics, write platform-optimized copy, generate branded visual assets via Gemini Imagen 3, validate brand safety, and publish directly through Meta Graph APIs.

---

## Real-World Industry Applications

- **Autonomous Brand Marketing**: Executes automated marketing campaigns with continuous generation of copy, graphics, and scheduled releases.
- **E-Commerce Product Launches**: Translates product catalog data into eye-catching social posts with promotional imagery and calls to action.
- **Agency Client Management**: Manages multi-brand social accounts with dedicated persona prompts, image aspect ratios, and compliance rules.
- **Content Syndication**: Transforms internal engineering updates, blogs, and announcements into bite-sized social updates.

---

## Technical Architecture & Multi-Agent Workflow

The system is organized into modular autonomous agent roles (`agents/main`, `agents/designer`, `agents/publisher`):

```
       [Topic Directive / Campaign Input]
                       │
                       ▼
            [Content Strategy Agent]
         (agents/main/src/content.ts)
                       │
       ┌───────────────┴───────────────┐
       ▼                               ▼
[Copywriting Agent]         [Visual Prompt Agent]
(Platform Tone, Hooks,     (Art Style, Lighting, Composition)
 Hashtags, Character Limits)           │
       │                               ▼
       │                    [Gemini Image Designer Agent]
       │                   (agents/designer/src/gemini-image.ts)
       │                               │
       └───────────────┬───────────────┘
                       │
                       ▼
            [Brand Compliance Agent]
         (Tone check, safety filters,
           aspect-ratio verification)
                       │
                       ▼
            [Social Publisher Agent]
      (agents/publisher/src/facebook-publish.ts)
                       │
                       ▼
         [Meta Graph API Live Post]
```

### Step 1: Content Strategy & Topic Deconstruction
The strategy agent (`agents/main/src/content.ts`) receives campaign themes, determines audience personas, and produces an outline detailing the target mood, key takeaway, and messaging hierarchy.

### Step 2: Copywriting & Caption Optimization
The copywriting agent formats the narrative specifically for the target platform: LinkedIn (professional tone, structured whitespace), Instagram/Facebook (engaging hook, concise paragraphs, targeted hashtags).

### Step 3: AI Visual Generation with Gemini Imagen 3
The designer agent (`agents/designer/src/gemini-image.ts`) translates content themes into rich visual generation prompts. It invokes Google's Gemini / Imagen 3 API, generating high-resolution branded promotional assets with precise artistic framing.

### Step 4: Quality & Compliance Validation
Before publication, the validation routine evaluates output assets: ensuring image resolutions adhere to platform standards (1:1 square or 4:5 vertical), verifying text safety guidelines, and ensuring hashtag counts remain optimal.

### Step 5: Direct Platform Publishing
The publisher agent (`agents/publisher/src/facebook-publish.ts`) signs API requests using OAuth credentials and posts the combined image and caption payload to Facebook Pages and Instagram Business accounts via the Meta Graph API.

---

## Technology Stack & Implementation Specifications

| Component | Technology | Version | Architectural Function |
| :--- | :--- | :--- | :--- |
| **Execution Runtime** | Bun Runtime / Node.js | Latest | High-speed TypeScript orchestration and task execution |
| **Agent Framework** | TypeScript Agent Core | Custom | Decentralized agent messaging and state pipeline |
| **Generative LLM** | Google Gemini 1.5 Pro | API v1 | Strategic ideation, copywriting, and prompt synthesis |
| **Image Synthesis** | Google Gemini Imagen 3 | API v1 | Automated high-resolution graphic asset generation |
| **Social Publishing** | Meta Graph API | v19.0+ | Authenticated direct deployment to Facebook & Instagram |
| **Frontend UI** | Vite / React / Tailwind | 18.x | Interactive campaign dashboard and agent monitoring |
| **Database & Auth** | Supabase PostgreSQL | Latest | Campaign log persistence, asset history, and credentials |

---

## Installation & Setup Guide

### 1. Environment Configuration
Create a `.env` file in the repository root:
```env
GEMINI_API_KEY=your_gemini_api_key
FACEBOOK_PAGE_ACCESS_TOKEN=your_meta_page_token
FACEBOOK_PAGE_ID=your_page_id
```

### 2. Run Autonomous Pipeline via Bun
```bash
bun install

# Test content generation agent:
bun run agents/main/src/content-cli.ts --topic "AI in Healthcare"

# Run full end-to-end multi-agent pipeline:
bun run agents/main/src/e2e-test.ts
```

---

## Author & Contact Information

<table width="100%">
  <tr>
    <td width="150" align="center" valign="middle">
      <img src="https://avatars.githubusercontent.com/u/231165170?v=4" width="120" style="border-radius: 50%;" alt="Sohail Ahmed"/>
    </td>
    <td>
      <h3>Sohail Ahmed</h3>
      <p><strong>Senior Software Engineer & AI Systems Architect</strong></p>
      <p>Specializing in Full-Stack AI Application Development, Computer Vision, Deep Learning Pipelines, and Scalable Automation Architectures.</p>
      <p>
        <a href="https://sohail.devsil.com"><strong>Portfolio Website</strong></a> | 
        <a href="https://github.com/sohailahmed-bsrh"><strong>GitHub Profile</strong></a> | 
        <a href="https://www.linkedin.com/in/sohail-ahmed-devsil/"><strong>LinkedIn</strong></a> | 
        <a href="https://www.kaggle.com/sohail2411126"><strong>Kaggle</strong></a> | 
        <a href="https://x.com/ahmed241126"><strong>Twitter/X</strong></a> | 
        <a href="mailto:se906403@gmail.com"><strong>Email Contact</strong></a>
      </p>
    </td>
  </tr>
</table>
