# instant-markdown-d

A Node.js server enabling instant compilation and live preview of Markdown files in the browser.

![Node.js](https://img.shields.io/badge/Node.js-Server-green)
![Markdown](https://img.shields.io/badge/Markdown-Preview-blue)
![Vim](https://img.shields.io/badge/Vim-Integration-purple)

## Overview

instant-markdown-d is a lightweight local server that compiles Markdown to HTML in real-time and displays it in your browser. Designed to integrate with text editors via a simple REST API. The primary integration is with Vim via [vim-instant-markdown](https://github.com/suan/vim-instant-markdown).

## Features

- **Live Preview** - Real-time Markdown rendering in browser
- **REST API** - Simple HTTP interface for editor integration
- **MathJax Support** - Mathematical notation rendering
- **Security Options** - Script blocking, external resource control
- **Network Mode** - Optional LAN accessibility

## Tech Stack

| Component | Technology |
|-----------|------------|
| **Runtime** | Node.js |
| **Markdown** | marked.js |
| **Math** | MathJax |
| **Protocol** | HTTP REST API |

## Installation

```bash
# Install globally
[sudo] npm -g install instant-markdown-d

# Or pre-release version
[sudo] npm -g install instant-markdown-d@next
```

For Vim/Neovim integration, see [vim-instant-markdown](https://github.com/suan/vim-instant-markdown).

## REST API

| Action | Method | URL | Body |
|--------|--------|-----|------|
| Refresh Markdown | PUT | `http://localhost:<port>` | New Markdown content |
| Close Webpage | DELETE | `http://localhost:<port>` | - |

Default port: **8090**

## Environment Variables

| Variable | Description |
|----------|-------------|
| `INSTANT_MARKDOWN_OPEN_TO_THE_WORLD=1` | Allow network access (default: localhost only) |
| `INSTANT_MARKDOWN_ALLOW_UNSAFE_CONTENT=1` | Enable script execution (default: blocked) |
| `INSTANT_MARKDOWN_BLOCK_EXTERNAL=1` | Block external resources (default: allowed) |
| `INSTANT_MARKDOWN_MATHJAX_FONTS="/path/"` | Local MathJax fonts directory |

## Why This Project is Interesting

### Technical Highlights

1. **Real-Time Processing**
   - Instant Markdown compilation
   - WebSocket-like refresh behavior
   - Minimal latency preview

2. **Editor Integration**
   - Simple REST API for any editor
   - Primary Vim/Neovim support
   - Extensible to other editors

3. **Security-Conscious Design**
   - Script blocking by default
   - External resource controls
   - Network exposure options

4. **Developer Tooling**
   - Enhances Markdown workflow
   - Local development server
   - Cross-platform support

### Skills Demonstrated

- **Node.js**: HTTP server, file processing
- **REST API Design**: Simple, intuitive endpoints
- **Developer Tools**: Editor integration, workflow optimization
- **Security**: Content policy, network controls

## Credits

Fork of the original [instant-markdown-d](https://github.com/suan/instant-markdown-d) project.

## Author

[Kevin Mok](https://github.com/Kevin-Mok)
