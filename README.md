

# GenAI Development Estimation Templates

## UI Development Estimation

| **Activity Category** | **Effort (Person-Hours)** | **% of Total** | **Notes** |
|----------------------|---------------------------|----------------|-----------|
| **Pre-Development** | | 15-20% | Requirements, prototyping, design, API specs |
| **Development** | | 45-50% | Frontend, Backend APIs, Database implementation |
| **Testing** | | 20-25% | Functional, regression, performance testing |
| **UAT & Coordination** | | 10-15% | UAT prep, execution, sign-off |
| **Release & Production** | | 5-10% | Deployment, validation, hypercare |
| **Contingency Buffer** | | 10-15% | Risk mitigation, unknowns |
| **TOTAL** | | **100%** | |

---

## Data Source Integration Estimation (Per Source)

| **Activity Category** | **Base Effort (Person-Hours)** | **Complexity Multiplier** | **Adjusted Effort** | **% of Total** | **Notes** |
|----------------------|-------------------------------|--------------------------|---------------------|----------------|-----------|
| **Pre-Development** | | × | | 20-25% | Analysis, contracts, access setup |
| **Development** | | × | | 40-45% | Integration, processing, MCP/RAG pipeline |
| **Testing** | | × | | 15-20% | Functional, regression, performance |
| **Governance** | | × | | 10-15% | Model Risk Management, compliance review |
| **UAT & Coordination** | | × | | 5-10% | UAT execution, sign-off |
| **Release & Production** | | × | | 5-10% | Deployment, validation, monitoring |
| **Contingency Buffer** | | × | | 15-20% | Unknown data sources, quality issues |
| **TOTAL** | | | | **100%** | |

### Complexity Multipliers (Apply to Base Effort)

| **Data Source Type** | **Multiplier** | **Examples** |
|---------------------|----------------|--------------|
| Simple/Standard | 1.0x | CSV files, REST APIs with documentation |
| Moderate | 1.5x | SQL databases, cloud storage, standard SaaS APIs |
| Complex | 2.0x | Legacy systems, custom protocols, no documentation |
| Highly Complex | 2.5-3.0x | Real-time streams, multiple hops, data quality issues, PII-heavy |

---

## Prompt Engineering & LLM Selection Estimation

| **Activity Category** | **Effort (Person-Hours)** | **% of Total** | **Notes** |
|----------------------|---------------------------|----------------|-----------|
| **Pre-Development** | | 25-30% | Use case definition, LLM evaluation, strategy design |
| **Development** | | 35-40% | Prompt creation, testing, optimization, management system |
| **Testing** | | 15-20% | Functional, regression, performance, evaluation framework |
| **UAT & Coordination** | | 10-15% | User validation, feedback incorporation |
| **Release & Production** | | 5-10% | Deployment, monitoring, continuous improvement |
| **Contingency Buffer** | | 10-15% | Model changes, prompt drift, iteration cycles |
| **TOTAL** | | **100%** | |

---

## Activity Breakdown Reference

### Pre-Development Activities

| **UI Development** | **Data Integration** | **Prompt Engineering** |
|-------------------|---------------------|------------------------|
| • Requirements gathering<br>• Wireframing<br>• UI/UX design<br>• API design<br>• Database schema design<br>• Technical specifications | • Data source analysis<br>• Data contracts & SLAs<br>• Access implementation<br>• Data quality assessment<br>• Compliance review | • Use case definition<br>• LLM landscape analysis<br>• Model evaluation & selection<br>• Prompt strategy design<br>• Success criteria definition |

### Development Activities

| **UI Development** | **Data Integration** | **Prompt Engineering** |
|-------------------|---------------------|------------------------|
| • Frontend development<br>• Backend API development<br>• Database implementation<br>• API integration<br>• Real-time updates<br>• Error handling | • ETL/ELT pipeline development<br>• Data transformation<br>• Data processing & cleansing<br>• Vector store setup<br>• MCP/RAG pipeline implementation<br>• Data validation rules | • Prompt development<br>• Few-shot examples<br>• Advanced techniques (RAG, CoT)<br>• Prompt optimization<br>• Prompt management system<br>• A/B testing framework |

### Post-Development Activities

| **UI Development** | **Data Integration** | **Prompt Engineering** |
|-------------------|---------------------|------------------------|
| • All testing phases<br>• UAT preparation & execution<br>• Production deployment<br>• Post-production validation<br>• Hypercare support<br>• Documentation | • All testing phases<br>• Model Risk Governance<br>• UAT coordination<br>• Production deployment<br>• Data quality monitoring<br>• Pipeline optimization | • All testing phases<br>• Evaluation framework<br>• UAT coordination<br>• Production deployment<br>• Response monitoring<br>• Continuous improvement |

---

## PI Capacity Planning (Quick Reference)

| **Metric** | **Value** | **Notes** |
|-----------|----------|-----------|
| PI Duration | 10-12 weeks | Standard quarterly planning |
| Sprints per PI | 5-6 sprints | 2-week sprints |
| Hours per Person/Sprint | 60-70 hours | After meetings/ceremonies |
| Velocity Factor | 70-80% | Realistic capacity |
| **Capacity per Person/PI** | **~450-550 hours** | Planning baseline |

### Example Calculation
```
Team of 5 × 500 hours/person = 2,500 person-hours available per PI
```

---

## Estimation Guidelines

### How to Use These Templates

1. **Start with base estimates** for each activity category
2. **Apply complexity multipliers** for data sources based on type
3. **Sum totals** to get overall effort per component
4. **Divide by team capacity** to determine PI duration
5. **Review percentages** - adjust if significantly different from guidelines

### Risk Factors (Apply Additional Buffers)

| **Factor** | **Additional Buffer** |
|-----------|---------------------|
| New technology/first GenAI project | +20-30% |
| Regulated industry (finance, healthcare) | +15-25% |
| Distributed/offshore teams | +15-20% |
| Legacy system integration | +20-30% |
| Unclear requirements | +25-35% |

---

**Document Version:** 2.0 (Compact)  
**Last Updated:** December 2025




------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# GenAI Development Estimation Templates

## Template 1: UI Development Estimation

| **Phase** | **Activities** | **Deliverables** | **Effort (Person-Hours)** | **Dependencies** | **Notes** |
|-----------|---------------|------------------|---------------------------|------------------|-----------|
| **1. Discovery & Requirements** | Requirements gathering, stakeholder interviews, user journey mapping | Requirements document, User stories | | Prerequisites | Include accessibility requirements |
| **2. UI Prototyping** | Low-fidelity wireframes, User flow diagrams, Interactive prototypes | Figma/Sketch prototypes, Clickable wireframes | | Phase 1 | Include feedback cycles |
| **3. UI Design** | High-fidelity mockups, Design system components, Responsive design specifications, GenAI chat interface patterns | Design specifications, Asset library, Style guide | | Phase 2 | GenAI-specific: conversation UI, streaming responses, token usage display |
| **4. Frontend Development** | Component development, State management, API integration, Real-time updates handling, Error handling & retry logic | Working UI components, Integrated frontend | | Phase 3, 5 | Framework: React/Angular/Vue |
| **5. Backend API Development** | API design & documentation, Endpoint implementation, Authentication & authorization, Rate limiting, LLM orchestration layer | OpenAPI specs, API endpoints, Auth middleware | | Phase 1 | Include API versioning strategy |
| **6. Database Design & Implementation** | Schema design, Conversation history storage, User preferences/context storage, Audit logging, Database optimization | ERD, Database scripts, Migration files | | Phase 1 | Consider vector DB for embeddings |
| **7. Functional Testing** | Unit testing, Integration testing, UI automation, API testing, Conversation flow testing | Test cases, Test reports, Bug registry | | Phase 4, 5, 6 | Target: >80% code coverage |
| **8. Regression Testing** | Regression test suite, Automated regression runs, Cross-browser/device testing | Regression test results, Defect log | | Phase 7 | Automated suite maintenance |
| **9. Performance Testing** | Load testing, Stress testing, LLM response time profiling, Concurrent user testing, Token usage optimization | Performance benchmarks, Bottleneck analysis, Optimization recommendations | | Phase 4, 5, 6 | Tools: JMeter, K6, Locust |
| **10. UAT Preparation** | UAT plan creation, Test data preparation, UAT environment setup, User guide documentation | UAT plan, Test scenarios, User documentation | | Phase 7, 8 | Include rollback procedures |
| **11. UAT Coordination** | UAT session facilitation, Defect triage, Stakeholder communication, Sign-off management | UAT reports, Sign-off documentation, Defect closure | | Phase 10 | 2-3 UAT cycles typical |
| **12. Production Release Preparation** | Release notes, Deployment scripts, Rollback procedures, Production checklist, Feature flags configuration | Release package, Deployment runbook, Go-live checklist | | Phase 11 | Include smoke test plan |
| **13. Post-Production Validation** | Production smoke testing, Monitoring setup, Performance validation, User feedback collection, Incident response | Validation report, Monitoring dashboards, Incident log | | Phase 12 | First 72 hours critical |
| **14. Hypercare & Stabilization** | Issue resolution, Performance tuning, User support, Documentation updates | Stabilization report, Lessons learned | | Phase 13 | Typically 2 weeks post-launch |

**Total UI Development Effort: _____ Person-Hours**

---

## Template 2: Data Source Integration Estimation

| **Phase** | **Activities** | **Deliverables** | **Effort (Person-Hours)** | **Dependencies** | **Notes** |
|-----------|---------------|------------------|---------------------------|------------------|-----------|
| **1. Data Source Analysis** | Data source identification, Data availability assessment, Access requirements analysis, Data quality evaluation, PII/sensitive data identification | Data source inventory, Feasibility report, Risk assessment | | Prerequisites | Include compliance review |
| **2. Data Contracts & Governance** | SLA definition, Data ownership clarification, Usage rights negotiation, Data retention policies, Update frequency agreements | Signed data contracts, Governance documentation, DPA agreements | | Phase 1 | Legal review required |
| **3. Data Access Implementation** | Authentication setup, API/connector development, Credential management, Network/firewall configuration, VPN/secure tunnels | Working data connections, Access documentation, Secret management setup | | Phase 2 | Security team involvement |
| **4. Data Integration** | ETL/ELT pipeline development, Data transformation logic, Data validation rules, Error handling & retry logic, Incremental load strategy | Integration pipelines, Data flow diagrams, Error handling framework | | Phase 3 | Tools: Airflow, Databricks, etc. |
| **5. Data Processing** | Data cleansing, Normalization, Deduplication, Data enrichment, Format standardization | Processed datasets, Data quality reports, Processing scripts | | Phase 4 | Define quality thresholds |
| **6. Vector Store & Embeddings** | Document chunking strategy, Embedding model selection, Vector database setup, Indexing optimization, Metadata extraction | Vector store implementation, Embedding pipelines, Search configuration | | Phase 5 | For RAG: ChromaDB, Pinecone, Weaviate |
| **7. MCP/RAG Pipeline** | **MCP Option:** MCP server development, Tool/resource implementation, Protocol compliance<br>**RAG Option:** Retrieval strategy, Prompt augmentation, Context window optimization, Hybrid search implementation | Working MCP server OR RAG pipeline, Performance benchmarks, Relevance metrics | | Phase 6 | Choose MCP vs RAG based on use case |
| **8. Functional Testing** | Data pipeline testing, Data quality validation, Integration testing, MCP/RAG accuracy testing, Edge case testing | Test cases, Data validation reports, Quality metrics | | Phase 7 | Include data lineage testing |
| **9. Regression Testing** | Automated data tests, Schema change detection, Historical data validation, Pipeline regression suite | Regression test suite, Test results, Defect log | | Phase 8 | Data versioning critical |
| **10. Performance Testing** | Data load performance, Query response times, Embedding generation speed, Concurrent access testing, Vector search latency | Performance benchmarks, Optimization report, Capacity plan | | Phase 7 | Test at expected scale + 50% |
| **11. UAT Preparation** | UAT data preparation, Test scenario creation, Data masking/anonymization, UAT environment setup | UAT plan, Masked test data, UAT checklist | | Phase 8, 9 | Ensure production-like data |
| **12. UAT Coordination** | UAT facilitation, Data quality validation with users, Feedback incorporation, Defect resolution, Sign-off management | UAT reports, User acceptance documentation, Defect closure report | | Phase 11 | Business user involvement |
| **13. Model Risk Governance** | Model risk assessment, Data lineage documentation, Bias evaluation, Model validation, Regulatory compliance check, MRM approval process | MRM documentation, Risk rating, Approval certificates, Audit trail | | Phase 8, 9, 10 | Finance/regulated industries |
| **14. Production Release Preparation** | Production data migration, Release documentation, Rollback procedures, Monitoring setup, Alert configuration | Release package, Runbook, Monitoring dashboards, Rollback plan | | Phase 12, 13 | Include data reconciliation |
| **15. Post-Production Validation** | Data quality monitoring, Pipeline performance validation, Data freshness checks, User feedback collection, Incident response | Validation report, Data quality dashboards, Issue log | | Phase 14 | Monitor first full cycle |
| **16. Hypercare & Optimization** | Performance tuning, Data quality improvements, Pipeline optimization, Issue resolution, Documentation updates | Optimization report, Updated documentation, Lessons learned | | Phase 15 | 2-4 weeks typical |

**Total Data Integration Effort: _____ Person-Hours**

---

## Template 3: Prompt Engineering & LLM Selection Estimation

| **Phase** | **Activities** | **Deliverables** | **Effort (Person-Hours)** | **Dependencies** | **Notes** |
|-----------|---------------|------------------|---------------------------|------------------|-----------|
| **1. Use Case Definition** | Business requirements analysis, Success criteria definition, User persona development, Conversation flow mapping, Failure mode analysis | Requirements document, Success metrics, Use case specifications | | Prerequisites | Critical for scope control |
| **2. LLM Landscape Analysis** | Market research, Model capability comparison, Cost-benefit analysis, Vendor evaluation, API/deployment options assessment | LLM comparison matrix, Vendor shortlist, Cost estimates | | Phase 1 | GPT-4, Claude, Gemini, Llama, etc. |
| **3. Model Evaluation & Selection** | Benchmark testing, Accuracy evaluation, Latency testing, Cost per token analysis, Fine-tuning feasibility, Multi-model strategy assessment | Evaluation report, Model selection recommendation, POC results | | Phase 2 | Test with real data samples |
| **4. Prompt Strategy Design** | Prompt architecture design, System prompt definition, Few-shot example selection, Chain-of-thought design, Prompt templating strategy | Prompt framework, Template library, Design documentation | | Phase 3 | Include prompt versioning |
| **5. Initial Prompt Development** | Base prompt creation, Context engineering, Output format specification, Constraint definition, Safety guardrails | Prompt catalog, Prompt specifications, Examples library | | Phase 4 | Iterative refinement expected |
| **6. Prompt Testing & Iteration** | A/B testing, Edge case testing, Hallucination detection, Bias evaluation, Response consistency testing, Red-teaming | Test results, Refined prompts, Performance metrics | | Phase 5 | Plan 3-5 iteration cycles |
| **7. Advanced Techniques Implementation** | **As needed:** Retrieval-Augmented Generation (RAG), Few-shot learning optimization, Chain-of-thought prompting, Self-consistency techniques, Function calling/tool use, Prompt chaining/routing | Advanced prompt implementations, Routing logic, Tool definitions | | Phase 6 | Based on complexity |
| **8. Prompt Optimization** | Token usage optimization, Response time improvement, Cost optimization, Quality vs. speed tradeoffs, Caching strategy | Optimized prompts, Cost analysis, Performance benchmarks | | Phase 7 | Target 20-30% cost reduction |
| **9. Prompt Management System** | Version control setup, Prompt registry, A/B testing framework, Monitoring & observability, Rollback mechanisms | Prompt management platform, Versioning system, Analytics dashboard | | Phase 8 | Tools: Langfuse, PromptLayer, LangSmith |
| **10. Evaluation Framework** | Automated evaluation metrics, Human evaluation rubrics, Golden dataset creation, Evaluation pipeline, Regression detection | Evaluation framework, Golden test set, Quality metrics | | Phase 6 | BLEU, ROUGE, custom metrics |
| **11. Functional Testing** | End-to-end testing, Integration testing, Multi-turn conversation testing, Error handling, Fallback scenario testing | Test cases, Test results, Bug reports | | Phase 9, 10 | Conversation coherence critical |
| **12. Regression Testing** | Prompt regression suite, Model version comparison, Performance regression detection, Automated regression runs | Regression test suite, Comparison reports, Defect log | | Phase 11 | Run on model updates |
| **13. Performance & Load Testing** | Concurrent request testing, Response time under load, Token usage at scale, Failover testing, Rate limit handling | Performance report, Capacity plan, Load test results | | Phase 9 | Simulate peak usage |
| **14. UAT Preparation** | UAT scenario creation, Test prompt variations, Documentation, Training materials, UAT environment setup | UAT plan, User guides, Test scenarios | | Phase 11, 12 | Include prompt explanation |
| **15. UAT Coordination** | User feedback sessions, Response quality evaluation, Business validation, Iteration based on feedback, Sign-off management | UAT reports, Feedback analysis, Acceptance documentation | | Phase 14 | Domain expert involvement |
| **16. Production Release Preparation** | Prompt deployment, Monitoring setup, Alert configuration, Rollback procedures, Documentation finalization | Deployment package, Monitoring dashboard, Runbook | | Phase 15 | Include prompt fallbacks |
| **17. Post-Production Validation** | Production monitoring, Response quality validation, Cost tracking, User feedback collection, Performance validation | Validation report, Cost analysis, Quality metrics | | Phase 16 | First 2 weeks critical |
| **18. Continuous Improvement** | Ongoing optimization, Prompt drift detection, User feedback incorporation, Model update evaluation, Cost optimization | Improvement backlog, Updated prompts, Performance trends | | Phase 17 | Ongoing activity |

**Total Prompt Engineering & LLM Selection Effort: _____ Person-Hours**

---

## PI (Program Increment) Planning Guide

### Converting Person-Hours to PI Deliverables

**Standard Assumptions:**
- PI Duration: 10-12 weeks (1 quarter)
- Sprint Duration: 2 weeks (5-6 sprints per PI)
- Available Hours per Person per Sprint: 60-70 hours (accounting for ceremonies, meetings, overhead)
- Team Velocity Buffer: 70-80% of theoretical capacity

### Capacity Calculation Formula

```
Team Capacity per PI = Number of Team Members × Hours per Sprint × Number of Sprints × Velocity Factor

Example:
5 team members × 65 hours × 6 sprints × 0.75 = 1,462 available person-hours per PI
```

### PI Estimation Template

| **Component** | **Total Effort (Hours)** | **Team Size** | **PI Duration** | **Deliverables** | **Risks** |
|---------------|-------------------------|---------------|-----------------|------------------|-----------|
| UI Development | | | PI 1 / PI 2 | Functional UI with API integration | API dependencies |
| Data Integration | | | PI 1 / PI 2 | 3 data sources integrated with RAG | Data access delays |
| Prompt Engineering | | | PI 1 / PI 2 | Production-ready prompts with monitoring | Model availability |

### Recommended Effort Distribution per PI

| **Activity** | **% of Total Effort** | **Notes** |
|-------------|---------------------|-----------|
| Development | 45-50% | Core implementation |
| Testing (Functional + Regression + Performance) | 20-25% | Quality assurance |
| UAT & Coordination | 10-15% | User validation |
| Release & Production Activities | 10-15% | Deployment & stabilization |
| Contingency Buffer | 10-15% | Risk mitigation |

### Cross-Template Considerations

**Dependencies Across Templates:**
- UI Development requires APIs from Phase 5
- Data Integration must complete before full RAG testing
- Prompt Engineering needs data sources integrated
- MRM governance may gate production releases

**Shared Resources:**
- DevOps engineers (release preparation)
- QA team (testing phases)
- Security team (data access, authentication)
- Business stakeholders (UAT)

---

## Usage Instructions

1. **Fill in person-hour estimates** for each phase based on:
   - Complexity of your specific use case
   - Team experience level
   - Technology maturity
   - Organizational factors

2. **Adjust phases** as needed for your context (add/remove/merge)

3. **Factor in dependencies** across templates when planning PI deliverables

4. **Apply risk multipliers** (1.2-1.5x) for:
   - New technology adoption
   - Complex integrations
   - Regulatory requirements
   - Distributed teams

5. **Map to PI objectives** by grouping related phases into quarterly milestones

6. **Review and refine** estimates quarterly based on actual velocity

---

**Document Version:** 1.0  
**Last Updated:** December 2025  
**Owner:** Cyber GenAI Product Development Lead
