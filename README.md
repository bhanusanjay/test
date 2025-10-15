import React, { useState } from 'react';
import { ChevronLeft, ChevronRight, Shield, Zap, Target, TrendingUp } from 'lucide-react';

const DemoPresentation = () => {
  const [currentSlide, setCurrentSlide] = useState(0);

  const slides = [
    {
      title: "AI-Powered Threat Intelligence Automation",
      subtitle: "From Intelligence to Action in Minutes, Not Hours",
      content: (
        <div className="space-y-8">
          <div className="grid grid-cols-3 gap-6 mt-12">
            <div className="bg-gradient-to-br from-red-50 to-red-100 p-6 rounded-lg border-l-4 border-red-500">
              <div className="text-4xl font-bold text-red-600 mb-2">Hours → Minutes</div>
              <div className="text-gray-700 font-medium">Time to Hunt</div>
            </div>
            <div className="bg-gradient-to-br from-blue-50 to-blue-100 p-6 rounded-lg border-l-4 border-blue-500">
              <div className="text-4xl font-bold text-blue-600 mb-2">100%</div>
              <div className="text-gray-700 font-medium">Coverage Consistency</div>
            </div>
            <div className="bg-gradient-to-br from-green-50 to-green-100 p-6 rounded-lg border-l-4 border-green-500">
              <div className="text-4xl font-bold text-green-600 mb-2">Zero</div>
              <div className="text-gray-700 font-medium">Manual Query Writing</div>
            </div>
          </div>
          
          <div className="bg-gray-50 p-8 rounded-lg mt-8">
            <div className="text-xl font-semibold text-gray-800 mb-4">The Challenge</div>
            <div className="text-gray-700 leading-relaxed">
              Threat hunters spend critical hours manually translating intelligence reports into actionable Splunk queries. This process is error-prone, inconsistent, and delays response to emerging threats affecting our environment.
            </div>
          </div>

          <div className="bg-gradient-to-r from-purple-600 to-blue-600 p-8 rounded-lg text-white mt-6">
            <div className="text-xl font-semibold mb-3">Our Solution</div>
            <div className="text-lg leading-relaxed">
              Automatically extract technologies from threat intelligence, validate organizational exposure, and generate targeted Splunk queries—enabling immediate threat hunting.
            </div>
          </div>
        </div>
      )
    },
    {
      title: "How It Works",
      subtitle: "Three-Step Intelligence-to-Action Pipeline",
      content: (
        <div className="space-y-6 mt-8">
          <div className="flex items-start space-x-6">
            <div className="flex-shrink-0 w-16 h-16 bg-blue-600 rounded-full flex items-center justify-center text-white text-2xl font-bold">1</div>
            <div className="flex-1">
              <div className="text-2xl font-bold text-gray-800 mb-3">Extract & Understand</div>
              <div className="bg-blue-50 p-6 rounded-lg border-l-4 border-blue-600">
                <div className="text-gray-700 mb-3 font-medium">Open Source LLM analyzes threat intelligence documents</div>
                <div className="text-gray-600">→ Identifies affected technologies, vulnerabilities, and attack indicators</div>
                <div className="text-gray-600">→ Nomic embeddings enable semantic understanding beyond keyword matching</div>
              </div>
            </div>
          </div>

          <div className="flex items-start space-x-6">
            <div className="flex-shrink-0 w-16 h-16 bg-purple-600 rounded-full flex items-center justify-center text-white text-2xl font-bold">2</div>
            <div className="flex-1">
              <div className="text-2xl font-bold text-gray-800 mb-3">Validate Exposure</div>
              <div className="bg-purple-50 p-6 rounded-lg border-l-4 border-purple-600">
                <div className="text-gray-700 mb-3 font-medium">Cross-reference against organizational assets</div>
                <div className="text-gray-600">→ Checks extracted technologies against our environment (demo: Artifactory data)</div>
                <div className="text-gray-600">→ Filters out irrelevant threats, focuses on actual exposure</div>
              </div>
            </div>
          </div>

          <div className="flex items-start space-x-6">
            <div className="flex-shrink-0 w-16 h-16 bg-green-600 rounded-full flex items-center justify-center text-white text-2xl font-bold">3</div>
            <div className="flex-1">
              <div className="text-2xl font-bold text-gray-800 mb-3">Generate Hunt Queries</div>
              <div className="bg-green-50 p-6 rounded-lg border-l-4 border-green-600">
                <div className="text-gray-700 mb-3 font-medium">Automatically create Splunk queries tailored to our environment</div>
                <div className="text-gray-600">→ Knowledge base built from 100+ parsed Splunk indices</div>
                <div className="text-gray-600">→ Queries ready for immediate threat hunting execution</div>
              </div>
            </div>
          </div>
        </div>
      )
    },
    {
      title: "Technical Architecture",
      subtitle: "Built on Enterprise-Ready Components",
      content: (
        <div className="space-y-8 mt-6">
          <div className="grid grid-cols-2 gap-8">
            <div className="bg-gradient-to-br from-indigo-50 to-indigo-100 p-6 rounded-lg">
              <div className="flex items-center mb-4">
                <Shield className="w-8 h-8 text-indigo-600 mr-3" />
                <div className="text-xl font-bold text-gray-800">AI & ML Layer</div>
              </div>
              <div className="space-y-3 text-gray-700">
                <div className="flex items-start">
                  <div className="w-2 h-2 bg-indigo-600 rounded-full mt-2 mr-3 flex-shrink-0"></div>
                  <div><span className="font-semibold">Open Source LLMs</span> for intelligence extraction and query generation</div>
                </div>
                <div className="flex items-start">
                  <div className="w-2 h-2 bg-indigo-600 rounded-full mt-2 mr-3 flex-shrink-0"></div>
                  <div><span className="font-semibold">Nomic Embeddings</span> for semantic technology matching</div>
                </div>
              </div>
            </div>

            <div className="bg-gradient-to-br from-cyan-50 to-cyan-100 p-6 rounded-lg">
              <div className="flex items-center mb-4">
                <Zap className="w-8 h-8 text-cyan-600 mr-3" />
                <div className="text-xl font-bold text-gray-800">Data & Interface</div>
              </div>
              <div className="space-y-3 text-gray-700">
                <div className="flex items-start">
                  <div className="w-2 h-2 bg-cyan-600 rounded-full mt-2 mr-3 flex-shrink-0"></div>
                  <div><span className="font-semibold">Cyber GenAI UI</span> for intuitive interaction</div>
                </div>
                <div className="flex items-start">
                  <div className="w-2 h-2 bg-cyan-600 rounded-full mt-2 mr-3 flex-shrink-0"></div>
                  <div><span className="font-semibold">Splunk Knowledge Base</span> parsed from 100+ indices</div>
                </div>
              </div>
            </div>
          </div>

          <div className="bg-white border-2 border-gray-200 rounded-lg p-8">
            <div className="text-lg font-bold text-gray-800 mb-6 text-center">Data Flow Architecture</div>
            <div className="flex items-center justify-between">
              <div className="text-center flex-1">
                <div className="bg-red-100 border-2 border-red-500 rounded-lg p-4 mb-2">
                  <div className="font-bold text-red-700">Threat Intel</div>
                  <div className="text-sm text-gray-600">PDFs, Reports</div>
                </div>
              </div>
              <div className="text-3xl text-gray-400 mx-4">→</div>
              <div className="text-center flex-1">
                <div className="bg-blue-100 border-2 border-blue-500 rounded-lg p-4 mb-2">
                  <div className="font-bold text-blue-700">LLM Processing</div>
                  <div className="text-sm text-gray-600">Extract + Embed</div>
                </div>
              </div>
              <div className="text-3xl text-gray-400 mx-4">→</div>
              <div className="text-center flex-1">
                <div className="bg-purple-100 border-2 border-purple-500 rounded-lg p-4 mb-2">
                  <div className="font-bold text-purple-700">Asset Validation</div>
                  <div className="text-sm text-gray-600">Environment Check</div>
                </div>
              </div>
              <div className="text-3xl text-gray-400 mx-4">→</div>
              <div className="text-center flex-1">
                <div className="bg-green-100 border-2 border-green-500 rounded-lg p-4 mb-2">
                  <div className="font-bold text-green-700">Splunk Queries</div>
                  <div className="text-sm text-gray-600">Ready to Hunt</div>
                </div>
              </div>
            </div>
          </div>

          <div className="bg-amber-50 border-l-4 border-amber-500 p-6 rounded-r-lg">
            <div className="flex items-start">
              <Target className="w-6 h-6 text-amber-600 mr-3 flex-shrink-0 mt-1" />
              <div>
                <div className="font-bold text-gray-800 mb-2">Demo Environment</div>
                <div className="text-gray-700">Prototype validated using sample Artifactory data and production-representative Splunk log patterns</div>
              </div>
            </div>
          </div>
        </div>
      )
    },
    {
      title: "Impact & Next Steps",
      subtitle: "From Prototype to Production",
      content: (
        <div className="space-y-8 mt-8">
          <div className="grid grid-cols-2 gap-8">
            <div>
              <div className="flex items-center mb-6">
                <TrendingUp className="w-8 h-8 text-green-600 mr-3" />
                <div className="text-2xl font-bold text-gray-800">Expected Impact</div>
              </div>
              <div className="space-y-4">
                <div className="bg-green-50 p-5 rounded-lg border-l-4 border-green-500">
                  <div className="font-bold text-gray-800 mb-2">Speed to Detection</div>
                  <div className="text-gray-700">Reduce intelligence-to-hunt time from hours to minutes</div>
                </div>
                <div className="bg-blue-50 p-5 rounded-lg border-l-4 border-blue-500">
                  <div className="font-bold text-gray-800 mb-2">Consistency</div>
                  <div className="text-gray-700">Eliminate variability in query quality across threat hunters</div>
                </div>
                <div className="bg-purple-50 p-5 rounded-lg border-l-4 border-purple-500">
                  <div className="font-bold text-gray-800 mb-2">Coverage</div>
                  <div className="text-gray-700">Ensure comprehensive detection across all affected technologies</div>
                </div>
                <div className="bg-orange-50 p-5 rounded-lg border-l-4 border-orange-500">
                  <div className="font-bold text-gray-800 mb-2">Analyst Efficiency</div>
                  <div className="text-gray-700">Free hunters to focus on analysis, not query construction</div>
                </div>
              </div>
            </div>

            <div>
              <div className="flex items-center mb-6">
                <Zap className="w-8 h-8 text-blue-600 mr-3" />
                <div className="text-2xl font-bold text-gray-800">Immediate Next Steps</div>
              </div>
              <div className="space-y-4">
                <div className="bg-white border-2 border-gray-200 p-5 rounded-lg">
                  <div className="flex items-center mb-2">
                    <div className="w-8 h-8 bg-blue-600 text-white rounded-full flex items-center justify-center font-bold mr-3">1</div>
                    <div className="font-bold text-gray-800">Incorporate Day 1 Feedback</div>
                  </div>
                  <div className="text-gray-600 ml-11">Refine extraction accuracy and query templates</div>
                </div>
                <div className="bg-white border-2 border-gray-200 p-5 rounded-lg">
                  <div className="flex items-center mb-2">
                    <div className="w-8 h-8 bg-blue-600 text-white rounded-full flex items-center justify-center font-bold mr-3">2</div>
                    <div className="font-bold text-gray-800">Expand Knowledge Base</div>
                  </div>
                  <div className="text-gray-600 ml-11">Include additional Splunk indices and query patterns</div>
                </div>
                <div className="bg-white border-2 border-gray-200 p-5 rounded-lg">
                  <div className="flex items-center mb-2">
                    <div className="w-8 h-8 bg-blue-600 text-white rounded-full flex items-center justify-center font-bold mr-3">3</div>
                    <div className="font-bold text-gray-800">Production Integration</div>
                  </div>
                  <div className="text-gray-600 ml-11">Connect to live asset inventory and Splunk environment</div>
                </div>
                <div className="bg-white border-2 border-gray-200 p-5 rounded-lg">
                  <div className="flex items-center mb-2">
                    <div className="w-8 h-8 bg-blue-600 text-white rounded-full flex items-center justify-center font-bold mr-3">4</div>
                    <div className="font-bold text-gray-800">Pilot with Live Threats</div>
                  </div>
                  <div className="text-gray-600 ml-11">Test against current threat intelligence feeds</div>
                </div>
              </div>
            </div>
          </div>

          <div className="bg-gradient-to-r from-blue-600 to-purple-600 p-8 rounded-lg text-white mt-6">
            <div className="text-2xl font-bold mb-3">Strategic Value</div>
            <div className="text-lg leading-relaxed">
              This prototype demonstrates how GenAI can transform threat intelligence from static reports into dynamic, actionable defense. By automating the translation layer, we enable threat hunters to operate at machine speed while maintaining human judgment where it matters most.
            </div>
          </div>
        </div>
      )
    }
  ];

  const nextSlide = () => {
    setCurrentSlide((prev) => (prev + 1) % slides.length);
  };

  const prevSlide = () => {
    setCurrentSlide((prev) => (prev - 1 + slides.length) % slides.length);
  };

  return (
    <div className="min-h-screen bg-gradient-to-br from-slate-50 to-slate-100 p-8">
      <div className="max-w-7xl mx-auto">
        <div className="bg-white rounded-2xl shadow-2xl overflow-hidden">
          {/* Header */}
          <div className="bg-gradient-to-r from-slate-800 to-slate-900 text-white p-8">
            <div className="flex items-center justify-between">
              <div>
                <div className="text-sm font-semibold text-slate-300 mb-2">AI FOR CYBER THREAT HUNTERS | DAY 1 DEMO</div>
                <h1 className="text-4xl font-bold mb-2">{slides[currentSlide].title}</h1>
                <p className="text-xl text-slate-300">{slides[currentSlide].subtitle}</p>
              </div>
              <Shield className="w-16 h-16 text-blue-400 opacity-80" />
            </div>
          </div>

          {/* Content */}
          <div className="p-12 min-h-[600px]">
            {slides[currentSlide].content}
          </div>

          {/* Footer Navigation */}
          <div className="bg-slate-100 px-12 py-6 flex items-center justify-between border-t-2 border-slate-200">
            <button
              onClick={prevSlide}
              disabled={currentSlide === 0}
              className={`flex items-center space-x-2 px-6 py-3 rounded-lg font-semibold transition-all ${
                currentSlide === 0
                  ? 'bg-slate-200 text-slate-400 cursor-not-allowed'
                  : 'bg-slate-700 text-white hover:bg-slate-800 shadow-md hover:shadow-lg'
              }`}
            >
              <ChevronLeft className="w-5 h-5" />
              <span>Previous</span>
            </button>

            <div className="flex items-center space-x-3">
              {slides.map((_, index) => (
                <button
                  key={index}
                  onClick={() => setCurrentSlide(index)}
                  className={`transition-all ${
                    index === currentSlide
                      ? 'w-12 h-3 bg-blue-600 rounded-full'
                      : 'w-3 h-3 bg-slate-300 rounded-full hover:bg-slate-400'
                  }`}
                />
              ))}
            </div>

            <button
              onClick={nextSlide}
              disabled={currentSlide === slides.length - 1}
              className={`flex items-center space-x-2 px-6 py-3 rounded-lg font-semibold transition-all ${
                currentSlide === slides.length - 1
                  ? 'bg-slate-200 text-slate-400 cursor-not-allowed'
                  : 'bg-blue-600 text-white hover:bg-blue-700 shadow-md hover:shadow-lg'
              }`}
            >
              <span>Next</span>
              <ChevronRight className="w-5 h-5" />
            </button>
          </div>

          {/* Slide Counter */}
          <div className="bg-slate-800 text-white text-center py-2 text-sm font-medium">
            Slide {currentSlide + 1} of {slides.length}
          </div>
        </div>
      </div>
    </div>
  );
};

export default DemoPresentation;





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
