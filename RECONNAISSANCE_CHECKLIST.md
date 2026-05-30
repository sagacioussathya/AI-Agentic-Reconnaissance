# Complete Reconnaissance Phase Checklist

This document provides a comprehensive checklist of all reconnaissance activities performed by the AI Agentic Reconnaissance framework. This is the complete operational scope of the reconnaissance phase.

## Overview

The reconnaissance phase consists of 8 specialized agents executing 100+ distinct checks across multiple categories. All activities are read-only, evidence-based, and designed for authorized assessment only.

---

## Agent 1: Target Classification Agent

**Purpose**: Identify target system type to guide subsequent reconnaissance

### Checks Performed

- [ ] HTTP response pattern analysis
- [ ] Server header examination
- [ ] Response timing analysis
- [ ] Content-Type header analysis
- [ ] API structure detection (REST, GraphQL, gRPC)
- [ ] Framework signature identification
- [ ] Error message pattern analysis
- [ ] Authentication mechanism detection
- [ ] Rate limiting behavior analysis
- [ ] CORS policy examination
- [ ] WebSocket support detection
- [ ] Server-Sent Events (SSE) detection
- [ ] AI-specific endpoint patterns
- [ ] LLM application indicators
- [ ] RAG system indicators
- [ ] Multi-agent system indicators
- [ ] MCP server indicators
- [ ] Traditional web application patterns
- [ ] API-only service patterns
- [ ] Microservice architecture indicators

### Classification Categories

- Traditional Web Application
- REST API Service
- GraphQL API Service
- LLM Application
- RAG System
- Agent System (Multi-Agent)
- MCP Server
- Hybrid System

---

## Agent 2: Passive Reconnaissance Agent

**Purpose**: Collect publicly available metadata without active probing

### HTTP Headers Analysis

- [ ] Server header detection
- [ ] X-Powered-By header
- [ ] X-AspNet-Version header
- [ ] X-Framework header
- [ ] Content-Security-Policy analysis
- [ ] X-Frame-Options detection
- [ ] Strict-Transport-Security (HSTS)
- [ ] X-Content-Type-Options
- [ ] X-XSS-Protection
- [ ] Referrer-Policy
- [ ] Permissions-Policy
- [ ] Cross-Origin headers (CORS, CORP, COEP)
- [ ] Cache-Control directives
- [ ] Set-Cookie attributes
- [ ] Custom headers analysis
- [ ] Server timing headers
- [ ] Feature-Policy headers

### HTML Metadata

- [ ] Meta tags extraction
- [ ] Title tag analysis
- [ ] Description meta tag
- [ ] Keywords meta tag
- [ ] Author information
- [ ] Generator meta tag
- [ ] Viewport configuration
- [ ] Canonical URL
- [ ] Open Graph tags
- [ ] Twitter Card tags
- [ ] Schema.org markup
- [ ] JSON-LD structured data

### JavaScript References

- [ ] External script sources
- [ ] Inline script analysis
- [ ] Framework detection (React, Vue, Angular)
- [ ] Library version identification
- [ ] CDN usage patterns
- [ ] Analytics tracking codes
- [ ] Third-party integrations
- [ ] WebSocket connections
- [ ] API endpoint references
- [ ] Configuration exposure in JS

### Standard Files

- [ ] robots.txt examination
- [ ] sitemap.xml parsing
- [ ] security.txt detection
- [ ] humans.txt detection
- [ ] .well-known directory
- [ ] favicon.ico analysis
- [ ] manifest.json (PWA)
- [ ] browserconfig.xml

### SSL/TLS Analysis

- [ ] Certificate information
- [ ] Certificate chain validation
- [ ] Cipher suite detection
- [ ] TLS version identification
- [ ] Certificate expiration
- [ ] Subject Alternative Names (SANs)
- [ ] Certificate issuer
- [ ] OCSP stapling status

---

## Agent 3: Service Discovery Agent

**Purpose**: Map accessible endpoints and API surface

### Common Endpoint Discovery

- [ ] /api/* endpoints
- [ ] /v1/*, /v2/* versioned APIs
- [ ] /graphql endpoint
- [ ] /swagger.json
- [ ] /openapi.json
- [ ] /docs endpoint
- [ ] /api-docs endpoint
- [ ] /health endpoint
- [ ] /status endpoint
- [ ] /metrics endpoint
- [ ] /admin/* endpoints
- [ ] /debug/* endpoints
- [ ] /test/* endpoints
- [ ] /dev/* endpoints

### AI-Specific Endpoints

- [ ] /chat endpoint
- [ ] /completions endpoint
- [ ] /embeddings endpoint
- [ ] /models endpoint
- [ ] /generate endpoint
- [ ] /query endpoint
- [ ] /ask endpoint
- [ ] /search endpoint
- [ ] /retrieve endpoint
- [ ] /ingest endpoint

### API Documentation

- [ ] OpenAPI/Swagger specification
- [ ] GraphQL schema introspection
- [ ] API documentation pages
- [ ] Postman collections
- [ ] API versioning scheme
- [ ] Endpoint parameter analysis
- [ ] Request/response examples
- [ ] Authentication requirements

### Service Characteristics

- [ ] Response time measurement
- [ ] Rate limiting detection
- [ ] Pagination support
- [ ] Filtering capabilities
- [ ] Sorting options
- [ ] Search functionality
- [ ] Batch operation support
- [ ] Webhook endpoints

---

## Agent 4: Local Model Fingerprint Agent

**Purpose**: Identify local LLM deployments and configurations

### Platform Detection

- [ ] Ollama API detection
- [ ] vLLM API detection
- [ ] LocalAI detection
- [ ] Text Generation Inference (TGI)
- [ ] FastChat detection
- [ ] LM Studio detection
- [ ] GPT4All detection
- [ ] llama.cpp server detection
- [ ] Custom deployment detection

### Model Enumeration

- [ ] Available models list
- [ ] Model names extraction
- [ ] Model versions identification
- [ ] Model families detection
- [ ] Model sizes (parameters)
- [ ] Quantization levels
- [ ] Context window sizes
- [ ] Model capabilities

### Configuration Analysis

- [ ] API endpoint structure
- [ ] Authentication requirements
- [ ] Rate limiting configuration
- [ ] Concurrent request limits
- [ ] Timeout settings
- [ ] Model loading status
- [ ] GPU/CPU allocation
- [ ] Memory usage patterns

### API Capabilities

- [ ] Completion endpoint
- [ ] Chat endpoint
- [ ] Embedding endpoint
- [ ] Model management endpoints
- [ ] Streaming support
- [ ] Function calling support
- [ ] Tool use capabilities
- [ ] Multi-modal support

---

## Agent 5: Knowledge Access Reconnaissance Agent (RAG)

**Purpose**: Assess RAG systems for information exposure

### Endpoint Discovery

- [ ] /query endpoint
- [ ] /search endpoint
- [ ] /retrieve endpoint
- [ ] /documents endpoint
- [ ] /collections endpoint
- [ ] /embeddings endpoint
- [ ] /ingest endpoint
- [ ] /index endpoint
- [ ] /chunks endpoint
- [ ] /metadata endpoint

### Document Enumeration

- [ ] Document listing endpoints
- [ ] Document count exposure
- [ ] Document ID patterns
- [ ] Collection names
- [ ] Index names
- [ ] Namespace detection
- [ ] Document metadata fields
- [ ] Source attribution

### Chunk Exposure

- [ ] Chunk size detection
- [ ] Overlap configuration
- [ ] Chunking strategy
- [ ] Chunk metadata exposure
- [ ] Chunk ID patterns
- [ ] Chunk retrieval endpoints
- [ ] Context window analysis

### Retrieval Metadata

- [ ] Similarity scores exposure
- [ ] Distance metrics
- [ ] Ranking algorithms
- [ ] Re-ranking indicators
- [ ] Retrieval count (top-k)
- [ ] Filtering parameters
- [ ] Metadata filtering options
- [ ] Hybrid search indicators

### Model Disclosure

- [ ] Embedding model identification
- [ ] LLM model identification
- [ ] Model version exposure
- [ ] Model configuration details
- [ ] Prompt template exposure
- [ ] System prompt indicators

### Debug Endpoints

- [ ] /debug/* endpoints
- [ ] /admin/* endpoints
- [ ] /test/* endpoints
- [ ] Verbose logging endpoints
- [ ] Trace endpoints
- [ ] Metrics endpoints
- [ ] Health check details

### Vector Database Detection

- [ ] Pinecone indicators
- [ ] Weaviate indicators
- [ ] Chroma indicators
- [ ] FAISS indicators
- [ ] Qdrant indicators
- [ ] Milvus indicators
- [ ] Elasticsearch indicators
- [ ] Custom vector DB

---

## Agent 6: Tool/MCP Reconnaissance Agent

**Purpose**: Assess MCP servers and tool exposure

### MCP Server Detection

- [ ] /mcp endpoint
- [ ] /.well-known/mcp
- [ ] MCP protocol version
- [ ] Transport mechanism (stdio, HTTP, WebSocket)
- [ ] Server capabilities
- [ ] Server metadata
- [ ] Authentication requirements
- [ ] Authorization model

### Tool Discovery

- [ ] /tools endpoint
- [ ] /api/tools endpoint
- [ ] /functions endpoint
- [ ] Tool listing
- [ ] Tool names extraction
- [ ] Tool descriptions
- [ ] Tool categories
- [ ] Tool versioning

### Tool Schema Extraction

- [ ] Input parameter schemas
- [ ] Output schemas
- [ ] Parameter types
- [ ] Required parameters
- [ ] Optional parameters
- [ ] Default values
- [ ] Parameter constraints
- [ ] Validation rules

### Function Calling Detection

- [ ] OpenAI function calling format
- [ ] Anthropic tool use format
- [ ] Custom function schemas
- [ ] Function descriptions
- [ ] Function parameters
- [ ] Return types
- [ ] Error handling

### Resource Mapping

- [ ] Resource endpoints
- [ ] Resource types
- [ ] Resource URIs
- [ ] Resource templates
- [ ] Resource metadata
- [ ] Access patterns
- [ ] Resource permissions

### Prompt Template Analysis

- [ ] Template discovery
- [ ] Template parameters
- [ ] Template variables
- [ ] Context injection points
- [ ] Dynamic content indicators
- [ ] Template versioning

### Permission Surface

- [ ] Tool permissions
- [ ] Resource permissions
- [ ] User roles
- [ ] Access control lists
- [ ] Permission inheritance
- [ ] Scope definitions
- [ ] Capability-based access

### Sensitive Capabilities

- [ ] File system access tools
- [ ] Shell execution tools
- [ ] Database query tools
- [ ] Email sending tools
- [ ] Web browsing tools
- [ ] API calling tools
- [ ] Secret access tools
- [ ] Administrative tools

---

## Agent 7: Agent Workflow Reconnaissance Agent

**Purpose**: Map multi-agent system architectures

### Workflow Endpoint Discovery

- [ ] /agents endpoint
- [ ] /workflows endpoint
- [ ] /graph endpoint
- [ ] /orchestration endpoint
- [ ] /planner endpoint
- [ ] /executor endpoint
- [ ] /router endpoint
- [ ] /coordinator endpoint

### Agent Role Detection

- [ ] Planner agents
- [ ] Executor agents
- [ ] Router agents
- [ ] Coordinator agents
- [ ] Manager agents
- [ ] Worker agents
- [ ] Critic agents
- [ ] Reviewer agents
- [ ] Memory agents
- [ ] Retriever agents
- [ ] Researcher agents
- [ ] Analyst agents
- [ ] Writer agents
- [ ] Editor agents
- [ ] Validator agents
- [ ] Monitor agents

### Workflow Graph Detection

- [ ] Node identification
- [ ] Edge identification
- [ ] Workflow structure
- [ ] Graph topology
- [ ] Transition rules
- [ ] Dependencies
- [ ] DAG structure
- [ ] Cycle detection

### Handoff Detection

- [ ] Handoff mechanisms
- [ ] Routing logic
- [ ] Delegation patterns
- [ ] Transfer protocols
- [ ] Next-agent selection
- [ ] Conditional routing
- [ ] Priority handling
- [ ] Fallback mechanisms

### Multi-Agent Patterns

- [ ] Sequential execution
- [ ] Parallel execution
- [ ] Hierarchical structure
- [ ] Peer-to-peer communication
- [ ] Broadcast patterns
- [ ] Request-response patterns
- [ ] Publish-subscribe patterns
- [ ] Event-driven architecture

### Framework Identification

- [ ] LangGraph indicators
- [ ] CrewAI indicators
- [ ] AutoGen indicators
- [ ] Semantic Kernel indicators
- [ ] OpenAI Agents SDK indicators
- [ ] PydanticAI indicators
- [ ] Custom framework detection

### Orchestration Metadata

- [ ] State management approach
- [ ] Memory persistence
- [ ] Context sharing
- [ ] Error handling
- [ ] Retry logic
- [ ] Timeout configuration
- [ ] Monitoring hooks
- [ ] Logging configuration

### Sensitive Workflows

- [ ] Administrative workflows
- [ ] Data modification workflows
- [ ] External API workflows
- [ ] File system workflows
- [ ] Database workflows
- [ ] Authentication workflows
- [ ] Authorization workflows
- [ ] Privileged operations

---

## Agent 8: Reconnaissance Summary Agent

**Purpose**: Aggregate findings and generate recommendations

### Finding Aggregation

- [ ] Collect all findings from sub-agents
- [ ] Deduplicate similar findings
- [ ] Categorize by severity
- [ ] Categorize by threat type
- [ ] Categorize by attack surface
- [ ] Calculate coverage metrics
- [ ] Identify finding patterns
- [ ] Cross-reference findings

### Evidence Validation

- [ ] Verify evidence completeness
- [ ] Calculate confidence scores
- [ ] Validate evidence quality
- [ ] Check reproducibility
- [ ] Assess specificity
- [ ] Verify timestamps
- [ ] Validate request/response data
- [ ] Check evidence consistency

### Executive Summary Generation

- [ ] Target classification summary
- [ ] Key findings highlight
- [ ] Risk assessment
- [ ] Attack surface summary
- [ ] Technology stack summary
- [ ] Security posture overview
- [ ] Compliance considerations
- [ ] Business impact assessment

### Recommendations

- [ ] Immediate actions
- [ ] Short-term improvements
- [ ] Long-term enhancements
- [ ] Security best practices
- [ ] Configuration hardening
- [ ] Monitoring recommendations
- [ ] Testing recommendations
- [ ] Documentation improvements

### Next Phase Guidance

- [ ] Recommended next agents
- [ ] Assessment priorities
- [ ] Focus areas
- [ ] Risk-based sequencing
- [ ] Resource allocation
- [ ] Timeline estimation
- [ ] Skill requirements
- [ ] Tool requirements

---

## Cross-Cutting Concerns

### Evidence Collection (All Agents)

- [ ] Request details (method, URL, headers, body)
- [ ] Response details (status, headers, body, timing)
- [ ] Timestamp (ISO 8601 format)
- [ ] Confidence score (0.0-1.0)
- [ ] Validation status
- [ ] Error information (if applicable)
- [ ] Context information
- [ ] Related findings

### Safety Mechanisms (All Agents)

- [ ] Scope validation before execution
- [ ] Authorization verification
- [ ] Rate limiting enforcement
- [ ] Timeout enforcement
- [ ] Error handling
- [ ] Graceful degradation
- [ ] Audit logging
- [ ] Safety validator checks

### Quality Assurance (All Agents)

- [ ] Schema validation
- [ ] Data type verification
- [ ] Required field checks
- [ ] Format validation
- [ ] Consistency checks
- [ ] Duplicate detection
- [ ] Completeness verification
- [ ] Accuracy assessment

---

## Summary Statistics

**Total Reconnaissance Checks**: 400+

**Agent Breakdown**:
- Target Classification: 20 checks
- Passive Reconnaissance: 60 checks
- Service Discovery: 40 checks
- Local Model Fingerprint: 35 checks
- Knowledge Access (RAG): 55 checks
- Tool/MCP Reconnaissance: 70 checks
- Agent Workflow: 80 checks
- Reconnaissance Summary: 40 checks

**Categories**:
- Endpoint Discovery: 100+ checks
- Metadata Collection: 80+ checks
- Configuration Analysis: 60+ checks
- Security Assessment: 50+ checks
- Architecture Mapping: 50+ checks
- Evidence Collection: 40+ checks
- Framework Detection: 20+ checks

**Output**:
- Structured findings with evidence
- Confidence-scored observations
- Categorized by severity and type
- Deduplicated and validated
- Ready for next assessment phase

---

## Responsible Use Notice

All reconnaissance activities are designed for authorized assessment only. Every check is:

- Read-only (no modifications)
- Evidence-based (documented observations)
- Safe (no exploitation attempts)
- Audited (complete logging)
- Scoped (within authorization boundaries)

Users must obtain explicit written authorization before conducting any reconnaissance activities.

---

**Version**: 1.0.0  
**Last Updated**: 2026-05-30  
**Framework**: AI Agentic Reconnaissance