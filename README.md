# Cyber Threat Intelligence Analysis Prototype - Features & Jira Stories

## High-Level Features

### 1. Enhanced Multi-Modal PDF Parser for Threat Intelligence
### 2. Technology Asset Matching System
### 3. Splunk Index Knowledge Base Integration
### 4. Threat Hunter Chat Interface
### 5. Automated Splunk Query Generation

---

## JIRA STORIES

### **EPIC: CTI-001 - Cyber Threat Intelligence Analysis Prototype**
**Description:** Develop a prototype system to parse cyber threat intelligence from PDFs/emails, identify affected technologies, match against bank's tech stack, and generate Splunk queries for threat hunting.

---

### **Story 1: CTI-002 - Extend PDF Parser for Technology Extraction**

**Title:** Enhance Multi-Modal PDF Parser to Extract Affected Technologies from Threat Intelligence

**Description:**
As a Cyber Threat Hunter, I need the existing PDF parser to identify and extract technology-related information (software, versions, CVEs, IoCs) from threat intelligence documents so that I can quickly understand what technologies are potentially affected.

**Acceptance Criteria:**
- [ ] Parser extracts technology names, versions, and CVE references from PDFs
- [ ] Parser identifies IoCs (IPs, domains, file hashes, registry keys)
- [ ] Parser handles both text and image-based content using Llama Vision
- [ ] Extracted data is structured in JSON format with confidence scores
- [ ] Parser processes at least 90% of common CTI PDF formats successfully

**Technical Considerations:**
- Extend existing Llama Vision prompts for technology extraction
- Create new prompt templates for structured technology data extraction
- Implement confidence scoring for extracted entities
- Use existing Python/MongoDB infrastructure

**Limitations:**
- May miss technologies mentioned only in complex diagrams
- Accuracy depends on document quality and format
- Limited to technologies explicitly mentioned in documents

**Story Points:** 5

---

### **Story 2: CTI-003 - Implement Technology Asset Matching Service**

**Title:** Build Technology Matching Service Against Bank's Asset Knowledge Base

**Description:**
As a Cyber Threat Hunter, I need to automatically match extracted threat intelligence technologies against our bank's technology inventory so that I can focus only on threats relevant to our infrastructure.

**Acceptance Criteria:**
- [ ] Service queries semantically searchable tech knowledge base using Nomic embeddings
- [ ] Returns match results with similarity scores above 0.7 threshold
- [ ] Handles technology aliases and version matching (e.g., "Apache 2.4.x" matches "Apache 2.4.41")
- [ ] Processes batch queries efficiently (<2 seconds for 20 technologies)
- [ ] Logs all matching activities for audit purposes

**Technical Considerations:**
- Integrate with existing Elastic vector datastore
- Use Nomic embedding model for semantic similarity
- Implement fuzzy matching for technology versions
- Create RESTful API using Java/Spring Boot

**Limitations:**
- Depends on completeness of bank's technology knowledge base
- May produce false positives with common technology names
- Version matching logic may be imperfect for complex versioning schemes

**Story Points:** 8

---

### **Story 3: CTI-004 - Build Splunk Index Knowledge Base**

**Title:** Create Semantically Searchable Splunk Index Knowledge Base with SIEM Integration

**Description:**
As a Cyber Threat Hunter, I need a searchable knowledge base of all Splunk indices mapped to technologies so that I can quickly identify relevant data sources for investigation.

**Acceptance Criteria:**
- [ ] Kafka consumer ingests Splunk index metadata from SIEM feed
- [ ] Index descriptions and technology mappings stored in MongoDB
- [ ] Vector embeddings generated using Nomic model and stored in Elastic
- [ ] RESTful API provides semantic search across indices
- [ ] Data pipeline updates knowledge base every 4 hours
- [ ] Search returns top 5 relevant indices with confidence scores

**Technical Considerations:**
- Set up Kafka consumer for SIEM data integration
- Create embedding pipeline for index descriptions
- Design MongoDB schema for index metadata
- Implement incremental updates to avoid full reprocessing

**Limitations:**
- Quality depends on SIEM metadata accuracy
- Initial setup requires manual technology-to-index mapping validation
- May miss newly created indices between update cycles

**Story Points:** 13

---

### **Story 4: CTI-005 - Customize Chat UI for Threat Hunters**

**Title:** Enhance Existing Chat UI with Threat Hunter Specific Features

**Description:**
As a Cyber Threat Hunter, I need a specialized chat interface that supports threat intelligence analysis workflows so that I can efficiently process CTI documents and initiate investigations.

**Acceptance Criteria:**
- [ ] Upload interface accepts PDF files and email attachments
- [ ] Display extracted technologies in structured format with match status
- [ ] Show relevant Splunk indices with rationale for selection
- [ ] Generate and display Splunk queries with copy-to-clipboard functionality
- [ ] Maintain conversation history for audit trail
- [ ] Add "Threat Hunter Mode" toggle to existing UI

**Technical Considerations:**
- Extend existing React/JavaScript frontend
- Add file upload components with drag-and-drop
- Integrate with existing chat backend APIs
- Implement responsive design for large data displays

**Limitations:**
- Limited to basic UI enhancements due to time constraints
- No advanced visualization features
- File size limited to 10MB for prototype

**Story Points:** 5

---

### **Story 5: CTI-006 - Implement Splunk Query Generator**

**Title:** Build Automated Splunk Query Generation for Threat Hunting

**Description:**
As a Cyber Threat Hunter, I need automatically generated Splunk queries based on extracted IoCs and affected technologies so that I can quickly begin investigations without manual query construction.

**Acceptance Criteria:**
- [ ] Generate basic search queries using extracted IoCs (IPs, domains, hashes)
- [ ] Include relevant index restrictions based on affected technologies
- [ ] Create time-bounded queries (last 30 days default)
- [ ] Generate both basic and advanced query variants
- [ ] Validate query syntax before presentation
- [ ] Include explanatory comments in generated queries

**Technical Considerations:**
- Create Splunk query templates using Jinja2
- Use Llama Instruct model for query optimization
- Implement query validation logic
- Store query patterns in MongoDB for reuse

**Limitations:**
- Generates basic queries only (no complex correlations)
- Limited to common IoC types
- May require manual tuning for specific use cases
- No query performance optimization

**Story Points:** 8

---

### **Story 6: CTI-007 - Integrate End-to-End Pipeline**

**Title:** Build Complete CTI Analysis Pipeline Integration

**Description:**
As a Cyber Threat Hunter, I need a seamless end-to-end pipeline that processes uploaded CTI documents and provides actionable intelligence so that I can efficiently respond to emerging threats.

**Acceptance Criteria:**
- [ ] Single API endpoint orchestrates entire pipeline
- [ ] Process completes within 30 seconds for typical PDF
- [ ] Error handling for each pipeline stage with meaningful messages
- [ ] Results cached in MongoDB for quick retrieval
- [ ] Pipeline status tracking and progress indicators
- [ ] Integration testing across all components

**Technical Considerations:**
- Implement async processing using Python asyncio
- Add comprehensive error handling and logging
- Create pipeline orchestrator service
- Use existing Kafka for inter-service communication

**Limitations:**
- No parallel processing of multiple documents
- Limited error recovery mechanisms
- Basic caching strategy only
- No pipeline performance metrics

**Story Points:** 8

---

## **Technical Architecture Summary**

**Core Technologies:**
- **LLMs:** Llama Vision + Instruct models
- **Embeddings:** Nomic embedding model
- **Vector Store:** Elasticsearch
- **Message Queue:** Kafka
- **Database:** MongoDB
- **Backend:** Python (FastAPI) + Java (Spring Boot)
- **Frontend:** Existing React-based chat UI

**Data Flow:**
1. PDF upload → Multi-modal parser → Technology extraction
2. Extracted technologies → Asset matching service → Bank relevance check
3. Relevant technologies → Splunk index search → Index identification
4. IoCs + Indices → Query generator → Splunk queries
5. Results → Chat UI → Threat Hunter review

**Prototype Limitations:**
- No production-grade security or scalability
- Basic error handling and monitoring
- Limited to common document formats
- Manual validation required for accuracy
- No advanced analytics or reporting features



----------------------------------------------------------------
Opening & Context Setting
"I'm Ricardo, leading our Singapore-based GenAI cybersecurity team and serving as tech lead for our flagship PenPal assistant platform. Having transitioned from EMEA operations a year ago, I've been focused on establishing our APAC cybersecurity AI capabilities and leveraging the exceptional talent pool across this region."
Core Platform Overview
"We're building a comprehensive Cyber GenAI Platform that's transforming how our security teams operate globally. This platform combines on-premises open-source LLMs running on our AI HPC infrastructure with Azure-hosted OpenAI APIs, giving us both control and cutting-edge capabilities."
"The platform delivers four core capabilities: NLP-based semantic search across our security data lakes, intelligent summarization of threat intelligence, automated content generation for security documentation, and GenAI-augmented data analysis that's revolutionizing how we interpret security events."
Technical Innovation & Methodology
"Our architecture leverages advanced methodologies including RAG for contextual information retrieval, sophisticated tool calling for automated security workflows, Model Context Protocol for seamless AI integration, robust guardrails for security compliance, and targeted fine-tuning for cybersecurity-specific use cases."
APAC Team Value Proposition
"The APAC and India talent pool has been instrumental in this platform's development. Our distributed team brings deep technical expertise in AI/ML, combined with around-the-clock development cycles that accelerate our delivery. The cost-effectiveness and technical depth available in this region allows us to compete with any global AI initiative."
Flagship Product: PenPal
"PenPal, our GenAI assistant for penetration testers, exemplifies our platform's potential. It's reducing testing time by 40% while improving coverage quality. This success story demonstrates how APAC-developed solutions can drive global cybersecurity value."
Regional Growth Vision (Subtle)
"We're seeing strong demand signals across APAC for these capabilities. The region's digital transformation pace creates unique opportunities for cybersecurity AI applications. Our current Singapore hub positions us well to support regional expansion as business cases mature."
Competitive Advantage
"Our hybrid cloud-on-premises approach addresses regulatory requirements across APAC markets while maintaining the agility to leverage latest commercial models. This architectural decision, driven by our APAC team's understanding of regional compliance needs, differentiates us from purely cloud-based competitors."
Closing Value Statement
"We're not just building AI tools – we're creating a platform that scales cybersecurity expertise globally while being developed and refined by world-class APAC talent. The early success metrics and stakeholder feedback position us for significant expansion of both capabilities and team size."
