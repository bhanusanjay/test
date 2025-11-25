<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Penpal — Wireframe</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Lucide icons -->
  <script src="https://cdn.jsdelivr.net/npm/lucide@0.267.0/dist/lucide.min.js"></script>
  <style>
    /* small helper to simulate disabled look for inputs when context not set */
    .disabled-overlay {
      pointer-events: none;
      opacity: 0.6;
    }
    /* keep body full height */
    html,body,#app { height: 100%; }
  </style>
</head>
<body class="bg-gray-50">
  <!-- View switcher -->
  <div id="app" class="flex flex-col h-full">
    <div class="bg-gray-800 text-white p-4 flex gap-4 justify-center">
      <button id="btn-context" class="px-4 py-2 rounded bg-blue-600">1. Context Setup View</button>
      <button id="btn-chat" class="px-4 py-2 rounded bg-gray-700">2. Conversation View</button>
    </div>

    <!-- Container for views -->
    <div id="views" class="flex-1">
      <!-- Context Setup View -->
      <section id="context-setup" class="flex h-[calc(100vh-64px)]">
        <!-- Left Sidebar -->
        <aside class="w-64 bg-white border-r border-gray-200 p-4">
          <div class="flex items-center gap-2 mb-8">
            <i data-lucide="shield" class="w-6 h-6 text-blue-600"></i>
            <span class="font-bold text-lg">CyberGenAI - Penpal</span>
          </div>
          <nav class="space-y-2">
            <div class="px-4 py-2 bg-blue-50 text-blue-700 rounded-lg font-medium">
              Set Context
            </div>
            <div class="px-4 py-2 text-gray-400 rounded-lg">
              Chat (Disabled)
            </div>
            <div class="px-4 py-2 text-gray-400 rounded-lg">
              History (Disabled)
            </div>
          </nav>
        </aside>

        <!-- Main Content -->
        <main class="flex-1 flex flex-col">
          <!-- Header -->
          <header class="bg-white border-b border-gray-200 px-6 py-4">
            <h1 class="text-2xl font-bold text-gray-800">Set Assessment Context</h1>
            <p class="text-sm text-gray-500 mt-1">Import and configure your application context before starting</p>
          </header>

          <!-- Context Form -->
          <div class="flex-1 overflow-auto p-6">
            <div class="max-w-4xl mx-auto space-y-6">

              <!-- Import Section -->
              <div class="bg-white rounded-lg border border-gray-200 p-6">
                <h2 class="text-lg font-semibold mb-4 flex items-center gap-2">
                  <i data-lucide="file-text" class="w-5 h-5 text-blue-600"></i>
                  Import from VAMP
                </h2>
                <div class="space-y-4">
                  <div>
                    <label class="block text-sm font-medium text-gray-700 mb-2">
                      Assessment ID
                    </label>
                    <div class="flex gap-2">
                      <input id="assessment-id" type="text" placeholder="Enter Assessment ID (e.g., ASS-2024-1234)"
                        class="flex-1 px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent" />
                      <button id="import-btn" class="px-6 py-2 bg-blue-600 text-white rounded-lg hover:bg-blue-700 font-medium">
                        Import
                      </button>
                    </div>
                  </div>
                  <div class="flex items-center gap-2 text-sm text-gray-500">
                    <i data-lucide="alert-circle" class="w-4 h-4"></i>
                    <span>This will automatically populate application details below</span>
                  </div>
                </div>
              </div>

              <!-- Application Details -->
              <div class="bg-white rounded-lg border border-gray-200 p-6">
                <h2 class="text-lg font-semibold mb-4 flex items-center gap-2">
                  <i data-lucide="globe" class="w-5 h-5 text-blue-600"></i>
                  Application Details
                </h2>
                <div class="grid grid-cols-2 gap-4">
                  <div>
                    <label class="block text-sm font-medium text-gray-700 mb-2">
                      Application Name *
                    </label>
                    <input id="app-name" type="text" placeholder="e.g., E-Commerce Platform"
                      class="w-full px-4 py-2 border border-gray-300 rounded-lg" />
                  </div>
                  <div>
                    <label class="block text-sm font-medium text-gray-700 mb-2">
                      Application Type
                    </label>
                    <select id="app-type" class="w-full px-4 py-2 border border-gray-300 rounded-lg">
                      <option>Web Application</option>
                      <option>Mobile App (iOS)</option>
                      <option>Mobile App (Android)</option>
                      <option>API</option>
                      <option>Desktop Application</option>
                    </select>
                  </div>
                  <div>
                    <label class="block text-sm font-medium text-gray-700 mb-2">
                      Target URL/Endpoint
                    </label>
                    <input id="target-url" type="text" placeholder="https://example.com"
                      class="w-full px-4 py-2 border border-gray-300 rounded-lg" />
                  </div>
                  <div>
                    <label class="block text-sm font-medium text-gray-700 mb-2">
                      Environment
                    </label>
                    <select id="environment" class="w-full px-4 py-2 border border-gray-300 rounded-lg">
                      <option>Staging</option>
                      <option>Production</option>
                      <option>Development</option>
                      <option>QA</option>
                    </select>
                  </div>
                </div>
              </div>

              <!-- Technology Stack -->
              <div class="bg-white rounded-lg border border-gray-200 p-6">
                <h2 class="text-lg font-semibold mb-4 flex items-center gap-2">
                  <i data-lucide="layers" class="w-5 h-5 text-blue-600"></i>
                  Technology Stack
                </h2>
                <div class="grid grid-cols-2 gap-4">
                  <div>
                    <label class="block text-sm font-medium text-gray-700 mb-2">
                      Frontend Framework
                    </label>
                    <input id="frontend-fw" type="text" placeholder="e.g., React, Angular, Vue"
                      class="w-full px-4 py-2 border border-gray-300 rounded-lg" />
                  </div>
                  <div>
                    <label class="block text-sm font-medium text-gray-700 mb-2">
                      Backend Framework
                    </label>
                    <input id="backend-fw" type="text" placeholder="e.g., Node.js, Django, Spring Boot"
                      class="w-full px-4 py-2 border border-gray-300 rounded-lg" />
                  </div>
                  <div>
                    <label class="block text-sm font-medium text-gray-700 mb-2">
                      Database
                    </label>
                    <input id="database" type="text" placeholder="e.g., PostgreSQL, MongoDB"
                      class="w-full px-4 py-2 border border-gray-300 rounded-lg" />
                  </div>
                  <div>
                    <label class="block text-sm font-medium text-gray-700 mb-2">
                      Authentication Method
                    </label>
                    <input id="auth-method" type="text" placeholder="e.g., JWT, OAuth 2.0, Session-based"
                      class="w-full px-4 py-2 border border-gray-300 rounded-lg" />
                  </div>
                </div>
                <div class="mt-4">
                  <label class="block text-sm font-medium text-gray-700 mb-2">
                    Additional Technologies
                  </label>
                  <textarea id="additional-tech"
                    placeholder="e.g., Redis for caching, AWS S3 for storage, GraphQL API..."
                    class="w-full px-4 py-2 border border-gray-300 rounded-lg h-20"></textarea>
                </div>
              </div>

              <!-- Assessment Scope -->
              <div class="bg-white rounded-lg border border-gray-200 p-6">
                <h2 class="text-lg font-semibold mb-4 flex items-center gap-2">
                  <i data-lucide="lock" class="w-5 h-5 text-blue-600"></i>
                  Assessment Scope
                </h2>
                <div class="space-y-3">
                  <label class="flex items-center gap-3">
                    <input id="scope-owasp" type="checkbox" class="w-4 h-4 text-blue-600" checked />
                    <span class="text-sm">OWASP Top 10 Testing</span>
                  </label>
                  <label class="flex items-center gap-3">
                    <input id="scope-auth" type="checkbox" class="w-4 h-4 text-blue-600" checked />
                    <span class="text-sm">Authentication & Authorization</span>
                  </label>
                  <label class="flex items-center gap-3">
                    <input id="scope-api" type="checkbox" class="w-4 h-4 text-blue-600" checked />
                    <span class="text-sm">API Security Testing</span>
                  </label>
                  <label class="flex items-center gap-3">
                    <input id="scope-logic" type="checkbox" class="w-4 h-4 text-blue-600" />
                    <span class="text-sm">Business Logic Testing</span>
                  </label>
                  <label class="flex items-center gap-3">
                    <input id="scope-infra" type="checkbox" class="w-4 h-4 text-blue-600" />
                    <span class="text-sm">Infrastructure Testing</span>
                  </label>
                </div>
              </div>

              <!-- Action Buttons -->
              <div class="flex justify-end gap-3 pt-4">
                <button id="save-draft" class="px-6 py-3 border border-gray-300 rounded-lg hover:bg-gray-50 font-medium">
                  Save as Draft
                </button>
                <button id="start-chat" class="px-6 py-3 bg-blue-600 text-white rounded-lg hover:bg-blue-700 font-medium flex items-center gap-2">
                  <i data-lucide="check" class="w-5 h-5"></i>
                  Start Assessment Chat
                </button>
              </div>
            </div>
          </div>
        </main>
      </section>

      <!-- Chat View -->
      <section id="chat-view" class="hidden flex h-[calc(100vh-64px)]">
        <!-- Left Sidebar -->
        <aside class="w-64 bg-white border-r border-gray-200 p-4 flex flex-col">
          <div class="flex items-center gap-2 mb-8">
            <i data-lucide="shield" class="w-6 h-6 text-blue-600"></i>
            <span class="font-bold text-lg">PenTest AI</span>
          </div>

          <nav class="space-y-2 mb-6">
            <div class="px-4 py-2 bg-blue-50 text-blue-700 rounded-lg font-medium">
              Chat
            </div>
            <div class="px-4 py-2 text-gray-600 rounded-lg hover:bg-gray-50 cursor-pointer">
              History
            </div>
          </nav>

          <!-- Context Card -->
          <div id="active-context-card" class="bg-blue-50 border border-blue-200 rounded-lg p-4 mb-4">
            <div class="flex items-start justify-between mb-2">
              <h3 class="font-semibold text-sm text-blue-900">Active Context</h3>
              <button id="edit-context" class="text-blue-600 hover:text-blue-700">
                <i data-lucide="settings" class="w-4 h-4"></i>
              </button>
            </div>
            <div class="space-y-2 text-xs text-blue-800">
              <div class="flex justify-between">
                <span class="font-medium">App:</span>
                <span id="card-app">E-Commerce Platform</span>
              </div>
              <div class="flex justify-between">
                <span class="font-medium">Type:</span>
                <span id="card-type">Web Application</span>
              </div>
              <div class="flex justify-between">
                <span class="font-medium">Tech:</span>
                <span id="card-tech">React + Node.js</span>
              </div>
              <div class="flex justify-between">
                <span class="font-medium">ID:</span>
                <span id="card-id">ASS-2024-1234</span>
              </div>
            </div>
          </div>

        <!--  <div class="mt-auto">
            <button id="end-assessment" class="w-full px-4 py-2 bg-red-50 text-red-700 rounded-lg hover:bg-red-100 font-medium text-sm">
              End Assessment
            </button>
          </div> -->
        </aside>

        <!-- Main Chat Area -->
        <main class="flex-1 flex flex-col">
          <!-- Header with Context Banner -->
          <div class="bg-white border-b border-gray-200">
            <div class="px-6 py-3 bg-blue-600 text-white flex items-center justify-between">
              <div class="flex items-center gap-2">
                <i data-lucide="shield" class="w-5 h-5"></i>
                <span class="font-semibold">E-Commerce Platform Assessment</span>
                <span class="text-blue-200 text-sm">• <span id="banner-id">ASS-2024-1234</span></span>
              </div>
              <button id="edit-context-2" class="text-white hover:text-blue-100 text-sm flex items-center gap-1">
                <i data-lucide="settings" class="w-4 h-4"></i>
                Edit Context
              </button>
            </div>
          </div>

          <!-- Chat Messages -->
          <div id="chat-messages" class="flex-1 overflow-auto p-6 space-y-4">
            <!-- Welcome Message -->
            <div class="flex gap-3">
              <div class="w-8 h-8 rounded-full bg-blue-600 flex items-center justify-center flex-shrink-0">
                <i data-lucide="shield" class="w-5 h-5 text-white"></i>
              </div>
              <div class="flex-1 bg-white rounded-lg border border-gray-200 p-4">
                <p class="text-gray-800 mb-3">
                  Hello! I'm ready to assist with the <strong id="highlight-app">E-Commerce Platform</strong> penetration test.
                  I have context about your <span id="highlight-tech">React + Node.js</span> web application.
                </p>
                <p class="text-gray-800 mb-3">Here are some suggested test cases to get started:</p>
                <div class="space-y-2 pl-4">
                  <div class="flex items-start gap-2">
                    <div class="w-1.5 h-1.5 rounded-full bg-blue-600 mt-2"></div>
                    <div>
                      <p class="font-medium text-sm">SQL Injection in Product Search</p>
                      <p class="text-xs text-gray-600">Test search parameters for SQLi vulnerabilities</p>
                    </div>
                  </div>
                  <div class="flex items-start gap-2">
                    <div class="w-1.5 h-1.5 rounded-full bg-blue-600 mt-2"></div>
                    <div>
                      <p class="font-medium text-sm">JWT Token Analysis</p>
                      <p class="text-xs text-gray-600">Verify JWT signature validation and expiration</p>
                    </div>
                  </div>
                  <div class="flex items-start gap-2">
                    <div class="w-1.5 h-1.5 rounded-full bg-blue-600 mt-2"></div>
                    <div>
                      <p class="font-medium text-sm">XSS in User Reviews</p>
                      <p class="text-xs text-gray-600">Test review submission for stored XSS</p>
                    </div>
                  </div>
                  <div class="flex items-start gap-2">
                    <div class="w-1.5 h-1.5 rounded-full bg-blue-600 mt-2"></div>
                    <div>
                      <p class="font-medium text-sm">Price Manipulation</p>
                      <p class="text-xs text-gray-600">Check if cart prices can be modified client-side</p>
                    </div>
                  </div>
                </div>
                <p class="text-gray-800 mt-3">What would you like to explore first?</p>
              </div>
            </div>

            <!-- User Message -->
            <div class="flex gap-3 justify-end">
              <div class="bg-blue-600 text-white rounded-lg p-4 max-w-2xl">
                Tell me more about JWT token analysis for this application
              </div>
            </div>

            <!-- AI Response -->
            <div class="flex gap-3">
              <div class="w-8 h-8 rounded-full bg-blue-600 flex items-center justify-center flex-shrink-0">
                <i data-lucide="shield" class="w-5 h-5 text-white"></i>
              </div>
              <div class="flex-1 bg-white rounded-lg border border-gray-200 p-4">
                <p class="text-gray-800 mb-3">
                  For your <strong>Node.js backend</strong> using JWT authentication, here's a comprehensive testing approach:
                </p>
                <div class="bg-gray-50 rounded p-3 mb-3">
                  <p class="font-semibold text-sm mb-2">Test Cases for JWT Analysis:</p>
                  <ol class="space-y-2 text-sm text-gray-700 list-decimal list-inside">
                    <li>Verify the algorithm used (check for "none" algorithm vulnerability)</li>
                    <li>Test if tokens expire properly after the stated time</li>
                    <li>Attempt to modify payload data and re-sign with weak secrets</li>
                    <li>Check if tokens are invalidated on logout</li>
                    <li>Test for token reuse after password change</li>
                  </ol>
                </div>
                <p class="text-gray-800 mb-2">
                  <strong>Recommended Tools:</strong> jwt_tool, Burp Suite JWT extensions
                </p>
                <p class="text-gray-800">
                  Would you like me to provide specific payloads for any of these test cases?
                </p>
              </div>
            </div>
          </div>

          <!-- Input Area -->
          <div class="bg-white border-t border-gray-200 p-4">
            <div class="max-w-4xl mx-auto">
              <div class="flex gap-3">
                <input id="chat-input" type="text"
                  placeholder="Ask about test cases, vulnerabilities, or specific attack vectors for E-Commerce Platform..."
                  class="flex-1 px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent" />
                <button id="send-btn" class="px-6 py-3 bg-blue-600 text-white rounded-lg hover:bg-blue-700 font-medium">
                  Send
                </button>
              </div>
              <p class="text-xs text-gray-500 mt-2">
                All responses are contextualized to your E-Commerce Platform assessment
              </p>
            </div>
          </div>
        </main>
      </section>
    </div>
  </div>

  <script>
    // Initialize lucide icons
    document.addEventListener('DOMContentLoaded', function () {
      if (window.lucide) {
        window.lucide.replace();
      }
    });

    // Simple view switching logic and context propagation
    const btnContext = document.getElementById('btn-context');
    const btnChat = document.getElementById('btn-chat');
    const ctxView = document.getElementById('context-setup');
    const chatView = document.getElementById('chat-view');

    const importBtn = document.getElementById('import-btn');
    const assessmentId = document.getElementById('assessment-id');
    const appName = document.getElementById('app-name');
    const appType = document.getElementById('app-type');
    const targetUrl = document.getElementById('target-url');
    const environment = document.getElementById('environment');
    const frontendFw = document.getElementById('frontend-fw');
    const backendFw = document.getElementById('backend-fw');
    const database = document.getElementById('database');
    const authMethod = document.getElementById('auth-method');
    const additionalTech = document.getElementById('additional-tech');

    const cardApp = document.getElementById('card-app');
    const cardType = document.getElementById('card-type');
    const cardTech = document.getElementById('card-tech');
    const cardId = document.getElementById('card-id');
    const bannerId = document.getElementById('banner-id');
    const highlightApp = document.getElementById('highlight-app');
    const highlightTech = document.getElementById('highlight-tech');

    const startChatBtn = document.getElementById('start-chat');
    const editContext = document.getElementById('edit-context');
    const editContext2 = document.getElementById('edit-context-2');
    const endAssessment = document.getElementById('end-assessment');

    function showContext() {
      ctxView.classList.remove('hidden');
      chatView.classList.add('hidden');
      btnContext.classList.add('bg-blue-600');
      btnChat.classList.remove('bg-blue-600');
      btnChat.classList.add('bg-gray-700');
    }

    function showChat() {
      ctxView.classList.add('hidden');
      chatView.classList.remove('hidden');
      btnChat.classList.add('bg-blue-600');
      btnContext.classList.remove('bg-blue-600');
      btnContext.classList.add('bg-gray-700');
    }

    btnContext.addEventListener('click', showContext);
    btnChat.addEventListener('click', showChat);

    // Fake import: populate fields with sample data or based on entered assessment id
    importBtn.addEventListener('click', function () {
      const id = assessmentId.value.trim() || 'ASS-2024-1234';
      // Populate sample details — in a real integration you'd call an API
      appName.value = 'E-Commerce Platform';
      appType.value = 'Web Application';
      targetUrl.value = 'https://example.com';
      environment.value = 'Staging';
      frontendFw.value = 'React';
      backendFw.value = 'Node.js';
      database.value = 'PostgreSQL';
      authMethod.value = 'JWT';
      additionalTech.value = 'Redis, AWS S3, GraphQL';
      assessmentId.value = id;
      // update context card immediately
      updateContextCard();
    });

    function updateContextCard() {
      const aName = appName.value || 'E-Commerce Platform';
      const aType = appType.value || 'Web Application';
      const tech = (frontendFw.value ? frontendFw.value : 'React') + (backendFw.value ? ' + ' + backendFw.value : '');
      const id = assessmentId.value || 'ASS-2024-1234';
      cardApp.textContent = aName;
      cardType.textContent = aType;
      cardTech.textContent = tech;
      cardId.textContent = id;
      bannerId.textContent = id;
      highlightApp.textContent = aName;
      highlightTech.textContent = tech;
    }

    // Start chat — mark context set and show chat
    startChatBtn.addEventListener('click', function () {
      updateContextCard();
      showChat();
      // Make context fields read-only visually
      document.querySelectorAll('#context-setup input, #context-setup select, #context-setup textarea, #context-setup button')
        .forEach(el => {
          if (el.id !== 'btn-context' && el.id !== 'btn-chat') {
            el.classList.add('disabled-overlay');
          }
        });
    });

    editContext.addEventListener('click', showContext);
    editContext2.addEventListener('click', showContext);

    endAssessment.addEventListener('click', function () {
      if (confirm('End assessment and clear context?')) {
        // simple reset
        assessmentId.value = '';
        appName.value = '';
        appType.selectedIndex = 0;
        targetUrl.value = '';
        environment.selectedIndex = 0;
        frontendFw.value = '';
        backendFw.value = '';
        database.value = '';
        authMethod.value = '';
        additionalTech.value = '';
        updateContextCard();
        showContext();
        // remove disabled overlay
        document.querySelectorAll('#context-setup .disabled-overlay').forEach(el => el.classList.remove('disabled-overlay'));
      }
    });

    // Small demo: send button echoes the message into the chat area
    const sendBtn = document.getElementById('send-btn');
    const chatInput = document.getElementById('chat-input');
    const chatMessages = document.getElementById('chat-messages');

    sendBtn.addEventListener('click', function () {
      const text = chatInput.value.trim();
      if (!text) return;
      // Append user bubble
      const userDiv = document.createElement('div');
      userDiv.className = 'flex gap-3 justify-end';
      userDiv.innerHTML = `<div class="bg-blue-600 text-white rounded-lg p-4 max-w-2xl">${escapeHtml(text)}</div>`;
      chatMessages.appendChild(userDiv);
      chatInput.value = '';
      chatMessages.scrollTop = chatMessages.scrollHeight;
      // Simulate AI response
      setTimeout(function () {
        const aiDiv = document.createElement('div');
        aiDiv.className = 'flex gap-3';
        aiDiv.innerHTML = `<div class="w-8 h-8 rounded-full bg-blue-600 flex items-center justify-center flex-shrink-0">
            <i data-lucide="shield" class="w-5 h-5 text-white"></i>
          </div>
          <div class="flex-1 bg-white rounded-lg border border-gray-200 p-4">
            <p class="text-gray-800">Thanks — I received: <strong>${escapeHtml(text)}</strong></p>
            <p class="text-gray-800 mt-2">I can provide test steps, payloads, or tool recommendations for this topic.</p>
          </div>`;
        chatMessages.appendChild(aiDiv);
        if (window.lucide) window.lucide.replace();
        chatMessages.scrollTop = chatMessages.scrollHeight;
      }, 600);
    });

    function escapeHtml(unsafe) {
      return unsafe
       .replaceAll('&','&amp;')
       .replaceAll('<','&lt;')
       .replaceAll('>','&gt;')
       .replaceAll('"','&quot;')
       .replaceAll("'",'&#039;');
    }

  </script>
</body>
</html>
