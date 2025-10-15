# Day 1 Workshop Summary: AI for Cyber Threat Hunters
**Date:** [Insert Date]  
**Attendees:** Cross-functional team including Cyber Threat Defense, Threat Intelligence, and GenAI Product Development teams

---

## Workshop Kickoff & Introductions

- Workshop commenced with introductions from all participants across threat hunting, threat intelligence, and development teams
- Established 4-day agenda focused on practical AI applications for cyber threat hunting operations
- Set collaborative tone for knowledge sharing between technical and operational teams

---

## Targeted Use Case Definition

- Workshop centered around specific threat hunting use case to drive practical outcomes
- Use case defined to align AI capabilities with operational threat hunting requirements
- Framework established for evaluating AI solution effectiveness against real-world scenarios

---

## Offensive AI Conference Insights (Presented by Josh & Don)

- Josh and Don delivered summaries from recent Offensive AI conference attendance
- Key takeaways covered emerging offensive AI techniques and threat landscape evolution
- Insights provided context for defensive AI strategies and potential adversarial use of AI in cyber operations
- Discussion highlighted importance of understanding offensive capabilities to build robust defensive measures

---

## Threat Intelligence Team Use Cases

- Threat Intelligence team presented high-level overview of potential AI use cases for their operations
- Multiple use cases identified spanning threat analysis, intelligence gathering, and automated reporting
- **Status:** Use cases pending internal prioritization by Cyber Threat Defense team
- Follow-up required to align use cases with organizational priorities and resource availability

---

## Development Team Prototype Demo: Threat Intelligence to Splunk Query Generation

**Use Case Demonstrated:**
- Extract affected technologies from threat intelligence documents
- Cross-reference extracted technologies against organizational asset inventory
- Automatically generate Splunk queries for technologies confirmed as present in the environment

**Technical Implementation:**
- **UI Platform:** Cyber GenAI UI
- **AI Models:** Open source LLMs for extraction and query generation
- **Embedding Model:** Nomic embedding model for semantic understanding
- **Knowledge Base:** Splunk query knowledge base constructed by parsing sample logs from approximately 100 indices using LLM
- **Sample Data:** Demo utilized sample Artifactory data for proof of concept

**Demo Workflow:**
1. Ingest threat intelligence document
2. LLM extracts mentioned technologies and vulnerabilities
3. System checks technologies against organizational environment
4. For confirmed matches, generates preliminary Splunk queries for threat hunting
5. Queries based on learned patterns from parsed log samples across 100 indices

**Feedback Received:**
- Prototype well-received with constructive feedback provided by workshop participants
- Specific improvement areas identified for Day 2 iteration
- Team committed to incorporating feedback and demonstrating enhanced version

---

## Additional Technology Discussion

- Elasticsearch discussed as potential component for search and analytics capabilities
- Exploration of integration opportunities with existing technology stack

---

## Day 1 Outcomes & Next Steps

- Successful establishment of common understanding across teams on AI capabilities for threat hunting
- Clear use case priorities emerging from collaborative discussion
- Development team has actionable feedback for prototype enhancement
- Foundation laid for Day 2 deep dives and iterative development

**Action Items:**
- Development team to implement feedback and prepare updated demo for Day 2
- Cyber Threat Defense team to complete prioritization of Threat Intelligence use cases
- All teams to prepare for deeper technical discussions based on Day 1 insights

---

**Prepared by:** [Your Name]  
**Distribution:** Executive Leadership & GenAI Product Development Team
