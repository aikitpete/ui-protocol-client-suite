# UI Protocol Client Suite

[![Licence](https://img.shields.io/badge/licence-see%20NOTICE-lightgrey)](NOTICE.md) ![Java](https://img.shields.io/badge/Java-ED8B00?logo=openjdk&logoColor=white) ![ActionScript 3](https://img.shields.io/badge/ActionScript%203-E34F26) ![XML](https://img.shields.io/badge/XML-005FAD) ![Status](https://img.shields.io/badge/status-archived-lightgrey)

> **Status:** historical prototype (Flex/ActionScript and Java), not maintained. Contains third-party code under its own licence (see NOTICE.md).

This repository explores an architectural idea: instead of shipping every screen as compiled native code, the client downloads **UI definitions from a server** and renders them dynamically at runtime.

The approach is conceptually similar to modern **server‑driven UI**, **remote configuration**, and **dynamic interface rendering** systems.

## Key Ideas

- **Server‑driven UI**
- **Dynamic interface rendering**
- **Protocol‑based UI definition**
- **Decoupling UI structure from mobile app releases**

## Repository Structure

```
client/
└─ current/
   Main mobile client implementation that parses and renders UI definitions.

servers/
├─ testing-server/
│  Java server used to host and serve protocol UI definitions for testing.
│
└─ policy-server/
   Lightweight Java cross-domain policy server used by the client environment.

samples/
└─ xml/
   Example UI definitions and protocol payloads used during development.

docs/
└─ screenshots/
   Screenshots demonstrating rendered interfaces and client behavior.
```

## How the System Works

1. A UI is defined in **XML using the UI protocol language**.
2. The definition is served by the **testing server**.
3. The mobile client fetches the UI specification.
4. The client parses the structure and **renders the screen dynamically**.

This allows interface updates without rebuilding the mobile app.

## Technologies

Client

- mobile client runtime
- XML-based UI protocol parsing
- dynamic UI rendering

Servers

- Java testing server
- Java policy server

## Why This Project Is Interesting

This repository explores a design pattern that became common in production systems:

- server-driven UI architectures
- dynamic UI delivery
- remote configuration of application behavior
- separation of UI structure from application releases

While this project is an early prototype, the core concept aligns with modern systems used by companies to ship UI updates without app store releases.
