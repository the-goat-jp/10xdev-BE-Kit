# 10xDev-BE-Kit 🚀

**The Ultimate Backend Development Kit** - Streamline your API & database specification workflow with proven templates, examples, and AI-powered development rules.

## 📦 What's Inside

### 🧩 Core Templates
- **`template.md`** - Canonical backend API & DB specification template
- **`samples/`** - Real-world examples (password reset, user auth, etc.)

### 🤖 AI Development Rules (`cursor/rules/`)
- **Smart Context Attachment** - Auto-includes relevant project files
- **Implementation Plans** - Structured development phases
- **Code Generation** - AI behavior for clean, consistent code
- **Code Review** - Automated review criteria and feedback
- **Control Keywords** - Human-AI workflow management

## 🎯 Quick Start

### 1. Spec Creation
```bash
# Copy the template to your project
cp template.md docs/api/your-feature.md
```

### 2. Fill the Template
- **Manual**: Replace `<PLACEHOLDER>` values with your feature details
- **AI-Powered**: Let Claude/Cursor auto-fill by selecting relevant code files

### 3. Save & Review
- Save as `docs/api/<feature>.md` in your service repo
- Open PR → reviewers confirm diagrams render & SQL lint passes

## 📚 Examples

> **See `samples/password-reset.md`** for a fully-populated specification example with:
> - Complete API endpoints (request/reset/validate)
> - Database schema with ER diagrams
> - Sequence diagrams for user flows
> - Comprehensive error handling

## 🤖 AI Workflow Integration

This kit includes **Cursor AI rules** that transform your development workflow:

### Implementation Workflow
1. **Spec First** - Create detailed API/DB specs using our template
2. **AI Implementation** - Use "Implementor" chat for phased development
3. **Code Review** - Use "Reviewer" chat for quality validation
4. **Keywords Control** - Use `NEXT_PHASE`, `STOP`, `VIBE_REVIEW` for workflow control

### Smart Context Management
The kit automatically attaches relevant project files:
- Tech specs (`docs/spec/*.md`)
- Implementation plans (`docs/implementation-plan.md`) 
- Project structure (`docs/project-structure.md`)

## 🏗️ Development Phases

Our AI rules follow a structured approach:
1. **Database Setup** - Migrations, models, tests
2. **Repository Layer** - CRUD operations with tests
3. **Service Layer** - Business logic implementation
4. **API Layer** - HTTP handlers and routes
5. **Integration & Testing** - End-to-end validation

## 🎨 Features

- ✅ **Mermaid Diagrams** - ER diagrams, sequence flows, and more
- ✅ **SQL Schema** - Production-ready database definitions  
- ✅ **API Specs** - Complete request/response documentation
- ✅ **Error Handling** - Comprehensive error response patterns
- ✅ **AI Integration** - Smart development workflow automation
- ✅ **Real Examples** - Battle-tested specification samples

## 🤝 Contributing

1. Fork this repository
2. Add new templates or examples to `samples/`
3. Enhance AI rules in `cursor/rules/`
4. Submit PR with clear description

## 📄 License

MIT License - Build amazing backends! 🚀

---

*Made with ❤️ for 10x developers who value clean specs and efficient workflows* 