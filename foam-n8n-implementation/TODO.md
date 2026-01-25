# FOAM N8N Implementation TODO

**Current Iteration:** 1 - Project Scaffolding  
**Last Updated:** 2025-01-21  
**Status:** In Progress

---

## Iteration 1: Project Scaffolding

### Objectives
- Create complete directory structure
- Set up all JSON schemas
- Create placeholder files for all components
- Establish documentation framework

### Tasks

#### Directory Structure
- [x] Create root project directory
- [x] Create IMPLEMENTATION_FRAMEWORK.md
- [x] Create TODO.md (this file)
- [x] Create schemas/ directory with all schema files
- [x] Create workflows/ directory structure
- [x] Create prompts/ directory with placeholder prompts
- [x] Create templates/ directory (copy from skill)
- [x] Create code/ directory structure
- [x] Create config/ directory with examples
- [x] Create tests/ directory with sample data
- [x] Create docs/ directory

#### JSON Schemas
- [x] topic-request.schema.json
- [x] evidence-package.schema.json
- [x] draft-content.schema.json
- [x] review-request.schema.json

#### Configuration Files
- [x] n8n-env.example
- [x] postgres-init.sql
- [x] ollama-models.txt
- [ ] docker-compose.yml (documented in IMPLEMENTATION_FRAMEWORK.md)

#### Code Utilities
- [x] logging.js
- [x] error-handler.js
- [x] schema-validator.js

#### Test Data
- [x] journal-club-sample.json
- [x] case-based-sample.json
- [x] clinical-review-sample.json

#### Documentation
- [x] CHANGELOG.md
- [x] README.md
- [ ] docs/deployment.md (stub)
- [ ] docs/troubleshooting.md (stub)

### Blockers
- None

### Notes
- Iteration 1 substantially complete
- All four JSON schemas created with comprehensive field definitions
- Code utilities include N8N Code Node compatibility
- Sample requests cover all three content formats
- docker-compose.yml spec documented in framework (extract to separate file in Iteration 2)

---

## Upcoming Iterations

### Iteration 2: Core Infrastructure (Next)
- [ ] PostgreSQL schema for content storage
- [ ] Basic N8N orchestrator workflow
- [ ] Webhook trigger configuration
- [ ] Error handling framework
- [ ] Logging setup

### Iteration 3: Evidence Search Pipeline
- [ ] PubMed search integration
- [ ] GPT-4o web search configuration
- [ ] FOAM resource scraping
- [ ] Evidence package assembly

### Iteration 4: Journal Club Workflow
- [ ] Trial data extraction prompts
- [ ] Critical appraisal automation
- [ ] Bottom line generation
- [ ] Template assembly

### Iteration 5: Case-Based Workflow
- [ ] Progressive revelation logic
- [ ] Decision point identification
- [ ] Clinical pearl placeholders
- [ ] Vignette generation

### Iteration 6: Clinical Review Workflow
- [ ] Section-by-section drafting
- [ ] Multi-section assembly
- [ ] Cross-referencing system
- [ ] Quality checkpoint integration

---

## Completed Iterations

### Pre-Implementation
- [x] FOAM resource analysis completed
- [x] Style guide developed
- [x] Templates created
- [x] Skill documentation written
- [x] N8N orchestration research completed

---

## Quick Reference

### Key Files
| File | Purpose |
|------|---------|
| IMPLEMENTATION_FRAMEWORK.md | Master specification document |
| TODO.md | This file - iteration tracking |
| schemas/*.json | Data contract definitions |
| workflows/*.json | N8N workflow exports |
| prompts/*.md | LLM system prompts |

### Model Allocation (Quick Reference)
| Task | Model |
|------|-------|
| Evidence synthesis | Claude Sonnet 4 |
| Web research | GPT-4o + Search |
| Content drafting | Claude Sonnet 4 |
| Preprocessing | Ollama Llama 3.2 |
| Validation | Ollama Mistral |

### Contact
- Project Lead: Sean (REdI, Metro North Health)
- Workflow: foam-content-orchestrator

---

## Iteration Completion Checklist

Before marking an iteration complete:
- [ ] All tasks checked off
- [ ] Code tested (where applicable)
- [ ] Documentation updated
- [ ] TODO.md updated with next iteration details
- [ ] CHANGELOG.md entry added
- [ ] Blockers documented for next iteration
