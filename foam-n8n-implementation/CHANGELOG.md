# Changelog

All notable changes to the FOAM N8N Implementation will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Planned
- Evidence search pipeline with PubMed and web search integration
- Journal club workflow implementation
- Case-based discussion workflow implementation
- Clinical review workflow implementation
- Human-in-the-loop review system
- Deployment automation

---

## [0.1.0] - 2025-01-21

### Added
- **Project Structure**: Complete directory scaffolding for all workflow components
- **Implementation Framework**: Comprehensive specification document (`IMPLEMENTATION_FRAMEWORK.md`)
  - Architecture overview with system component diagrams
  - Data flow specifications
  - Multi-LLM orchestration patterns
  - Model allocation strategy
  - 12-iteration implementation plan
  - Quality assurance framework
  - Deployment guide with Docker Compose configuration

- **JSON Schemas**: Full data contract definitions
  - `topic-request.schema.json` - Incoming content requests
  - `evidence-package.schema.json` - Research output structure
  - `draft-content.schema.json` - Generated content with placeholders
  - `review-request.schema.json` - Expert review workflow

- **Configuration Files**:
  - `postgres-init.sql` - Database schema with all tables, views, and triggers
  - `n8n-env.example` - Environment configuration template
  - `ollama-models.txt` - Local model documentation

- **Code Utilities**:
  - `logging.js` - Structured logging with N8N Code Node integration
  - `error-handler.js` - Error classification, retry logic, graceful degradation
  - `schema-validator.js` - JSON schema validation for workflow data

- **Templates**: Copied from existing FOAM skill
  - `case-based-template.md`
  - `journal-club-template.md`
  - `clinical-review-template.md`
  - `style-guide.md`
  - `SKILL.md`

- **Test Data**: Sample requests for each content format
  - `journal-club-sample.json` - TTM2 trial review request
  - `case-based-sample.json` - Septic shock vasopressor case
  - `clinical-review-sample.json` - Push dose vasopressors review

- **Documentation**:
  - `TODO.md` - Iteration tracking with task lists
  - `CHANGELOG.md` - This file

### Technical Decisions
- Selected Claude Sonnet 4 as primary model for drafting and synthesis
- GPT-4o designated for web search tasks via SerpAPI integration
- Ollama (Llama 3.2 / Mistral) for local preprocessing and validation
- PostgreSQL for conversation memory and content storage
- 15-second retry delay for rate limit recovery

### Notes
- Framework document serves as single source of truth for specifications
- All schemas include detailed field descriptions for documentation
- Error handler includes model fallback chains for resilience
- Logging utility designed for N8N Code Node compatibility

---

## Version History Summary

| Version | Date | Summary |
|---------|------|---------|
| 0.1.0 | 2025-01-21 | Initial scaffolding and framework |

---

## Roadmap

### Phase 1: Foundation (v0.1.x - v0.3.x)
- [x] 0.1.0 - Project scaffolding
- [ ] 0.2.0 - Core infrastructure (PostgreSQL, N8N orchestrator)
- [ ] 0.3.0 - Evidence search pipeline

### Phase 2: Content Generation (v0.4.x - v0.6.x)
- [ ] 0.4.0 - Journal club workflow
- [ ] 0.5.0 - Case-based workflow
- [ ] 0.6.0 - Clinical review workflow

### Phase 3: Quality & Validation (v0.7.x - v0.9.x)
- [ ] 0.7.0 - Validation system
- [ ] 0.8.0 - Human-in-the-loop review
- [ ] 0.9.0 - Quality assurance automation

### Phase 4: Deployment (v1.0.0)
- [ ] 1.0.0 - Production-ready self-hosted deployment
