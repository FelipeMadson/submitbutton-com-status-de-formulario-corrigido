> 🇧🇷 **[Versão em Português](README.pt-BR.md)** | 🇺🇸 **English Version**

# SubmitButton with Fixed Form Status (React 19 / Server Actions)

[![Node.js Version](https://img.shields.io/badge/Node.js-22%20%7C%2024%20LTS-brightgreen.svg)](https://nodejs.org)
[![Tests](https://img.shields.io/badge/Tests-Passing-brightgreen.svg)](backend/tests)
[![License](https://img.shields.io/badge/License-MIT-lightgrey.svg)](LICENSE)

> **Deterministic solution for React useFormStatus hook returning false in nested form actions.**

## 🎯 The Real Problem

In React 19 and Next.js App Router, components utilizing `useFormStatus()` must be rendered as direct or nested children of a `<form>` element executing a Server Action. When submit buttons or triggers are placed outside or wrapped in complex component boundaries, `pending` erroneously resolves to `false`, resulting in duplicated submissions and broken UX.

## 🏗️ Architecture & Solution

This project provides a robust, zero-dependency context-bridged button component and test runner that guarantees deterministic form state tracking, debounce protection, and automated accessibility (ARIA aria-busy/aria-disabled).

## 🚀 Installation & Quickstart

```bash
npm install
npm test
```

## 📊 Quality Gates & Verifications

- **Unit & Integration Tests**: Executable via `node --test backend/tests/*.test.ts`
- **Zero External Dependencies**: Native ESM and strict typing
- **Security**: Timing-safe CSRF & HMAC verifications

## ⚖️ License

MIT License - Copyright (c) Felipe Madson.
