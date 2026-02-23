---
name: technical-blog-writer
description: A specialized skill for researching and writing authentic, in-depth technical blogs (up to 3000 words) on computer science, programming languages, and system architecture. It includes capabilities to generate architecture diagrams (including animated ones) and synthesize information from technical papers or web sources to ensure original, non-plagiarized content. Use this skill when asked to write a technical blog post or article.
---

# Technical Blog Writer

## Overview

This skill specializes in researching, drafting, and refining high-quality technical blog posts. It emphasizes authenticity, avoiding plagiarism by synthesizing information from scholarly papers and web sources, and supports the inclusion of visual aids like architecture diagrams and animations.

## Core Capabilities

### 1. Research and Synthesis

- **Scope**: Computer science, software engineering, programming languages, system architecture, etc.
- **Sourcing**: Actively use your available web searching and reading tools to scout the internet or refer to provided technical papers.
- **Authenticity**: Synthesize findings in your own words. Do not copy-paste or closely paraphrase existing articles. The voice should be authoritative yet accessible.
- **Citations**: Include links to the original technical papers or web sources at the bottom when applicable.

### 2. Constraints & Formatting

- **Word Count**: Strictly maintain a maximum of 3000 words.
- **Structure**: Use markdown formatting, clear headings, code syntax highlighting where appropriate, and a logical flow (Introduction, Core Concepts, Deep Dive, Conclusion).

### 3. Architecture Diagrams & Animations

For explaining complex systems, you must include architecture diagrams. You have two primary ways to create them:

**A. Static Diagrams**
Use Mermaid.js within markdown fenced code blocks (`mermaid`). Ensure the diagram syntaxes are correct.

**B. Animated Diagrams (Preferred for Dynamic Systems)**
When illustrating data flow, state transitions, or algorithm execution over time, create an animated diagram using HTML/CSS/JS and capture it as a video:

1. Write a standalone HTML file containing the architecture diagram with CSS animations or JavaScript-based transitions. Ensure the animation runs as soon as the page loads.
2. Use the `browser_subagent` tool to open this HTML file locally. Set a task such as "Watch the animation complete".
3. The `browser_subagent` will automatically record the session as a WebP video and save it to the artifacts directory. Provide a good `RecordingName` (e.g., `recording_name: "oauth_flow_animation"`).
4. Embed the resulting WebP video into your markdown blog using the standard image embed syntax: `![Animation Description](/absolute/path/to/artifact/oauth_flow_animation.webp)`.

## Workflow

1. **Topic Analysis & Outlining**: Start by creating a brief outline based on the user's topic. Determine if architecture diagrams (static or animated) will be needed and where they fit best.
2. **Research**: Gather information from technical papers or the web. Assure your sources are credible.
3. **Generate Visuals**: Produce the HTML files for animations and capture them using the browser subagent, or write the mermaid diagram code.
4. **Drafting Content**: Write the blog post iteratively following the outline, weaving in the researched facts and the diagrams. Ensure the word count stays under 3000 words.
5. **Review & Refine**: Check for authenticity, tone, formatting, and word count constraints before delivering the final blog to the user.
