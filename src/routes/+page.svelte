<script lang="ts">
  // Icons
  import { Play, Mic, Music, Wand2, Type, Languages, Video, Share2, ArrowRight, Plus, X, Search, Settings, ChevronRight, ChevronDown } from 'lucide-svelte';

  // State for FAQ
  let openFaq = -1;
  const faqs = [
    "Do I need coding experience to use Replit?",
    "How does Replit Agent work?",
    "Can I import my existing projects from GitHub?",
    "What programming languages does Replit support?",
    "How much does Replit cost?",
    "Can I deploy my apps to production?",
    "Does Replit include database and authentication?",
    "Can I collaborate with my team in real-time?",
    "Is Replit suitable for enterprise use?",
    "How fast can I build an app with Replit?",
    "Can I use my own domain name?",
    "What kind of apps can I build with Replit?"
  ];

  function toggleFaq(index: number) {
    openFaq = openFaq === index ? -1 : index;
  }
</script>

<main class="w-full overflow-hidden">
  <!-- Hero Section -->
  <section class="max-w-[1400px] mx-auto px-6 pt-16 pb-24">
    <div class="flex flex-col lg:flex-row justify-between items-start gap-12 mb-12">
      <div class="max-w-3xl">
        <h1 class="text-5xl md:text-[80px] leading-[0.95] font-medium tracking-tighter mb-10 text-gray-900">
          Transform ideas into<br>production apps
        </h1>
        <button class="bg-black text-white px-8 py-4 rounded-full font-medium hover:bg-gray-800 transition-colors text-sm">
          Start building for free
        </button>
      </div>
      
      <div class="max-w-sm pt-2 lg:pt-4">
        <p class="text-gray-500 text-sm leading-relaxed">
          Built for non-technical founders and product managers — turn your ideas into working prototypes in minutes with AI-powered development and instant deployment.
        </p>
      </div>
    </div>

    <!-- Interface Mockup -->
    <div class="relative w-full aspect-[16/9] bg-[#1C1C1C] rounded-3xl overflow-hidden shadow-2xl border border-gray-800 mt-8">
        <!-- Mockup Content Recreated with CSS -->
        <div class="absolute inset-0 bg-[#1C1C1C] flex flex-col">
            <!-- Toolbar -->
            <div class="h-14 border-b border-gray-800 flex items-center justify-between px-4 bg-[#1C1C1C] z-10">
                <div class="flex items-center gap-4">
                    <svg class="w-6 h-6 text-white" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                      <path
                        d="M3.9364 4.8793V10.4948C3.9364 10.662 4.02563 10.8166 4.17048 10.9003L9.0342 13.7087M3.9364 4.8793L9.03472 7.82219M3.9364 4.8793L8.79813 2.07158C8.94299 1.98793 9.12143 1.9879 9.26634 2.0715L14.132 4.8793M9.0342 13.7087L14.132 10.7651M9.0342 13.7087L9.03472 7.82219M9.0342 13.7087V19.3241C9.0342 19.4914 9.12344 19.646 9.26835 19.7296L14.1325 22.5374M9.0342 13.7087L14.1325 16.6516M9.03472 7.82219L14.132 4.8793M14.132 4.8793V10.7651M14.132 10.7651L19.2298 13.7087M14.1325 22.5374V16.6516M14.1325 22.5374L18.9957 19.7296C19.1405 19.646 19.2298 19.4914 19.2298 19.3241V13.7087M14.1325 16.6516L19.2298 13.7087"
                        stroke="currentColor"
                        stroke-width="1.82353"
                        stroke-linejoin="round"
                      />
                    </svg>
                    <div class="text-sm font-medium text-gray-400">My First App</div>
                </div>
                <div class="flex items-center gap-3">
                    <div class="px-3 py-1.5 bg-primary-600 text-white text-xs rounded-full font-medium">Deploy</div>
                    <div class="px-3 py-1.5 bg-gray-800 text-white text-xs rounded-full">Share</div>
                </div>
            </div>
            
            <div class="flex-1 flex overflow-hidden">
                <!-- Sidebar -->
                <div class="w-64 border-r border-gray-800 bg-[#0E0E0E] p-4 flex flex-col gap-2">
                    <div class="text-[10px] text-gray-500 uppercase tracking-wide mb-2">Files</div>
                    <div class="flex items-center gap-2 text-xs text-gray-300 py-1.5 px-2 bg-gray-800 rounded">
                        <span>📄</span> index.html
                    </div>
                    <div class="flex items-center gap-2 text-xs text-gray-500 py-1.5 px-2 hover:bg-gray-800 rounded">
                        <span>📄</span> app.js
                    </div>
                    <div class="flex items-center gap-2 text-xs text-gray-500 py-1.5 px-2 hover:bg-gray-800 rounded">
                        <span>📄</span> styles.css
                    </div>
                </div>
                
                <!-- Main Code Editor -->
                <div class="flex-1 bg-[#1C1C1C] relative p-6 font-mono text-xs overflow-hidden">
                    <div class="text-gray-400 space-y-1">
                        <div><span class="text-purple-400">import</span> <span class="text-blue-400">React</span> <span class="text-purple-400">from</span> <span class="text-green-400">'react'</span>;</div>
                        <div><span class="text-purple-400">import</span> <span class="text-blue-400">{ useState }</span> <span class="text-purple-400">from</span> <span class="text-green-400">'react'</span>;</div>
                        <div class="h-3"></div>
                        <div><span class="text-purple-400">function</span> <span class="text-yellow-400">App</span>() {`{`}</div>
                        <div class="pl-4"><span class="text-purple-400">const</span> [count, setCount] = <span class="text-blue-400">useState</span>(<span class="text-orange-400">0</span>);</div>
                        <div class="h-3"></div>
                        <div class="pl-4"><span class="text-purple-400">return</span> (</div>
                        <div class="pl-8"><span class="text-gray-500">&lt;</span><span class="text-blue-400">div</span> <span class="text-blue-300">className</span>=<span class="text-green-400">"app"</span><span class="text-gray-500">&gt;</span></div>
                        <div class="pl-12"><span class="text-gray-500">&lt;</span><span class="text-blue-400">h1</span><span class="text-gray-500">&gt;</span>Counter: {`{count}`}<span class="text-gray-500">&lt;/</span><span class="text-blue-400">h1</span><span class="text-gray-500">&gt;</span></div>
                        <div class="pl-12"><span class="text-gray-500">&lt;</span><span class="text-blue-400">button</span> <span class="text-blue-300">onClick</span>={`{() => setCount(count + 1)}`}<span class="text-gray-500">&gt;</span></div>
                        <div class="pl-16">Click me</div>
                        <div class="pl-12"><span class="text-gray-500">&lt;/</span><span class="text-blue-400">button</span><span class="text-gray-500">&gt;</span></div>
                        <div class="pl-8"><span class="text-gray-500">&lt;/</span><span class="text-blue-400">div</span><span class="text-gray-500">&gt;</span></div>
                        <div class="pl-4">);</div>
                        <div>{`}`}</div>
                    </div>
                    
                    <!-- AI Assistant Suggestion -->
                    <div class="absolute bottom-6 right-6 bg-primary-600/10 border border-primary-600/30 rounded-lg p-3 max-w-xs backdrop-blur-sm">
                        <div class="text-[10px] text-primary-400 font-semibold mb-1">✨ AI Suggestion</div>
                        <div class="text-[10px] text-gray-300">Add a reset button to clear the counter</div>
                    </div>
                </div>
            </div>
            
            <!-- Console/Output -->
            <div class="h-48 border-t border-gray-800 bg-[#0E0E0E] p-4 relative font-mono text-xs">
                <div class="flex items-center justify-between mb-3">
                    <div class="text-gray-400 text-[10px] uppercase tracking-wide">Console</div>
                    <div class="flex items-center gap-2">
                        <div class="px-2 py-1 bg-green-600/20 text-green-400 text-[10px] rounded">✓ Build successful</div>
                        <div class="px-2 py-1 bg-primary-600/20 text-primary-400 text-[10px] rounded">🚀 Deployed</div>
                    </div>
                </div>
                <div class="space-y-1 text-gray-500">
                    <div class="flex items-start gap-2">
                        <span class="text-gray-600">$</span>
                        <span>npm run build</span>
                    </div>
                    <div class="flex items-start gap-2">
                        <span class="text-green-500">✓</span>
                        <span class="text-gray-400">Built in 234ms</span>
                    </div>
                    <div class="flex items-start gap-2">
                        <span class="text-blue-400">→</span>
                        <span class="text-gray-400">Deploying to production...</span>
                    </div>
                    <div class="flex items-start gap-2">
                        <span class="text-green-500">✓</span>
                        <span class="text-gray-400">Deployment complete</span>
                    </div>
                    <div class="flex items-start gap-2">
                        <span class="text-primary-400">🌐</span>
                        <span class="text-primary-400 underline">https://my-first-app.replit.app</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <div class="flex justify-center gap-8 mt-6 text-sm text-gray-400">
        <span class="flex items-center gap-2">💻 Code Editor</span>
        <span class="flex items-center gap-2">🚀 Instant Deploy</span>
    </div>
  </section>

  <!-- Intro Section -->
  <section class="max-w-[1000px] mx-auto px-6 py-24 text-center">
    <span class="text-sm font-medium text-gray-500 mb-4 block">Introducing Replit Agent</span>
    <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-8 leading-tight">
      Build production apps in minutes with AI-powered development. From idea to deployment — no coding experience required.
    </h2>
    
    <div class="flex flex-wrap justify-center gap-x-6 gap-y-3 text-sm text-gray-600 mb-10">
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100"><Wand2 size={14} /> AI Code Generation</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100">🚀 Instant Deployment</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100">🔐 Authentication</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100">💾 Database</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100">🌐 Hosting</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100">📊 Monitoring</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100"><Share2 size={14} /> GitHub Import</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100">📱 Mobile Apps</span>
    </div>

    <button class="inline-flex items-center gap-2 bg-black text-white pl-3 pr-5 py-2 rounded-full text-sm font-medium hover:bg-gray-800 transition-colors">
      <div class="w-6 h-6 bg-white rounded-full flex items-center justify-center">
        <Play size={10} class="fill-black text-black ml-0.5" />
      </div>
      Watch demo
    </button>
  </section>

  <!-- Features List Section -->
  <section class="max-w-[1400px] mx-auto px-6 py-12 relative">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-24">
        
        <!-- Feature 1 -->
        <div class="flex flex-col justify-center order-1 md:order-1">
            <h3 class="text-3xl font-medium mb-4">Build with AI assistance</h3>
            <p class="text-gray-600 leading-relaxed mb-6">
                Describe your app idea in plain English and watch as Replit Agent writes the code, sets up the infrastructure, and deploys your application — all in minutes.
            </p>
        </div>
        <div class="bg-gray-50 rounded-2xl p-6 border border-gray-100 order-2 md:order-2 min-h-[400px]">
            <div class="text-xs text-gray-400 mb-4 font-medium uppercase tracking-wide">AI Chat</div>
            <div class="space-y-4">
                <div class="bg-white rounded-xl p-4 border border-gray-100 shadow-sm">
                    <div class="text-xs text-gray-500 mb-2">You</div>
                    <div class="text-sm text-gray-900">Build me a task management app with user authentication</div>
                </div>
                <div class="bg-primary-50 rounded-xl p-4 border border-primary-100">
                    <div class="flex items-center gap-2 mb-2">
                        <Wand2 size={14} class="text-primary-600" />
                        <div class="text-xs text-primary-600 font-medium">Replit Agent</div>
                    </div>
                    <div class="text-sm text-gray-900 mb-3">I'll create a task management app for you with:</div>
                    <div class="space-y-2 text-xs text-gray-700">
                        <div class="flex items-center gap-2">
                            <span class="text-green-500">✓</span>
                            <span>User authentication & registration</span>
                        </div>
                        <div class="flex items-center gap-2">
                            <span class="text-green-500">✓</span>
                            <span>Task CRUD operations</span>
                        </div>
                        <div class="flex items-center gap-2">
                            <span class="text-green-500">✓</span>
                            <span>Database setup</span>
                        </div>
                        <div class="flex items-center gap-2">
                            <span class="text-green-500">✓</span>
                            <span>Responsive UI</span>
                        </div>
                    </div>
                </div>
                <div class="flex items-center gap-2 text-xs text-gray-500">
                    <div class="animate-pulse">●</div>
                    <span>Building your app...</span>
                </div>
            </div>
        </div>

        <!-- Feature 2 -->
        <div class="bg-gray-50 rounded-2xl p-6 border border-gray-100 min-h-[400px] flex items-center justify-center order-4 md:order-3 relative overflow-hidden">
             <!-- Deployment visualization -->
             <div class="absolute inset-0 flex items-center justify-center">
                 <div class="w-full h-full bg-[radial-gradient(circle_at_center,_var(--tw-gradient-stops))] from-primary-100 via-gray-50 to-gray-50"></div>
                 <div class="absolute w-64 h-64 border border-primary-200 rounded-full flex items-center justify-center animate-pulse">
                     <div class="w-48 h-48 border border-primary-300 rounded-full flex items-center justify-center">
                         <div class="w-32 h-32 bg-primary-500/10 rounded-full backdrop-blur-sm flex items-center justify-center">
                             <span class="text-4xl">🚀</span>
                         </div>
                     </div>
                 </div>
             </div>
        </div>
        <div class="flex flex-col justify-center order-3 md:order-4">
            <h3 class="text-3xl font-medium mb-4">Deploy instantly to production</h3>
            <p class="text-gray-600 leading-relaxed">
                No complex configuration or DevOps knowledge required. One click deploys your app to production with automatic scaling, SSL certificates, and global CDN.
            </p>
        </div>

        <!-- Feature 3 -->
        <div class="flex flex-col justify-center order-5 md:order-5">
            <h3 class="text-3xl font-medium mb-4">Built-in services, zero configuration</h3>
            <p class="text-gray-600 leading-relaxed">
                Authentication, databases, hosting, and monitoring — all included out of the box. No API keys to manage, no third-party services to configure.
            </p>
        </div>
        <div class="bg-gray-50 rounded-2xl p-6 border border-gray-100 min-h-[300px] flex items-center justify-center order-6 md:order-6">
             <div class="w-full max-w-sm space-y-3">
                 <div class="bg-white rounded-xl shadow-sm p-4 border border-gray-100 flex items-center gap-3">
                     <div class="w-10 h-10 bg-blue-100 rounded-lg flex items-center justify-center text-xl">
                         🔐
                     </div>
                     <div>
                         <div class="text-sm font-medium">Authentication</div>
                         <div class="text-xs text-gray-500">User management built-in</div>
                     </div>
                 </div>
                 <div class="bg-white rounded-xl shadow-sm p-4 border border-gray-100 flex items-center gap-3">
                     <div class="w-10 h-10 bg-green-100 rounded-lg flex items-center justify-center text-xl">
                         💾
                     </div>
                     <div>
                         <div class="text-sm font-medium">Database</div>
                         <div class="text-xs text-gray-500">PostgreSQL ready to use</div>
                     </div>
                 </div>
                 <div class="bg-white rounded-xl shadow-sm p-4 border border-gray-100 flex items-center gap-3">
                     <div class="w-10 h-10 bg-purple-100 rounded-lg flex items-center justify-center text-xl">
                         📊
                     </div>
                     <div>
                         <div class="text-sm font-medium">Monitoring</div>
                         <div class="text-xs text-gray-500">Real-time analytics</div>
                     </div>
                 </div>
             </div>
        </div>

        <!-- Feature 4 -->
        <div class="bg-gray-50 rounded-2xl p-6 border border-gray-100 min-h-[300px] flex items-center justify-center order-8 md:order-7">
            <div class="relative w-full max-w-md bg-white rounded-xl shadow-sm p-6 border border-gray-100">
                <div class="flex items-center gap-3 mb-4">
                    <div class="w-8 h-8 bg-gray-900 rounded-full flex items-center justify-center">
                        <svg class="w-4 h-4 text-white" fill="currentColor" viewBox="0 0 24 24"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
                    </div>
                    <div>
                        <div class="text-sm font-medium">Import from GitHub</div>
                        <div class="text-xs text-gray-500">github.com/user/my-project</div>
                    </div>
                </div>
                <div class="space-y-2 text-xs">
                    <div class="flex items-center gap-2 text-gray-600">
                        <span class="text-green-500">✓</span>
                        <span>Repository cloned</span>
                    </div>
                    <div class="flex items-center gap-2 text-gray-600">
                        <span class="text-green-500">✓</span>
                        <span>Dependencies installed</span>
                    </div>
                    <div class="flex items-center gap-2 text-gray-600">
                        <span class="text-green-500">✓</span>
                        <span>Environment configured</span>
                    </div>
                    <div class="flex items-center gap-2 text-primary-600 font-medium mt-3">
                        <span>→</span>
                        <span>Ready to run</span>
                    </div>
                </div>
            </div>
        </div>
        <div class="flex flex-col justify-center order-7 md:order-8">
            <h3 class="text-3xl font-medium mb-4">Import from GitHub instantly</h3>
            <p class="text-gray-600 leading-relaxed">
                Bring your existing projects to Replit with one click. Automatically detects your stack, installs dependencies, and gets you running in seconds.
            </p>
        </div>

        <!-- Feature 5 -->
        <div class="flex flex-col justify-center order-9 md:order-9">
            <h3 class="text-3xl font-medium mb-4">Collaborate in real-time</h3>
            <p class="text-gray-600 leading-relaxed">
                Work together with your team in the same codebase simultaneously. See changes in real-time, share feedback, and ship faster together.
            </p>
        </div>
        <div class="bg-gray-50 rounded-2xl p-6 border border-gray-100 min-h-[300px] flex items-center justify-center order-10 md:order-10">
             <div class="w-full max-w-sm">
                 <div class="bg-white p-4 rounded-xl border border-gray-100 shadow-sm">
                     <div class="flex items-center justify-between mb-4">
                         <div class="text-xs text-gray-500 font-medium">Active collaborators</div>
                         <div class="flex -space-x-2">
                             <div class="w-8 h-8 rounded-full bg-blue-500 border-2 border-white flex items-center justify-center text-white text-xs font-bold">JD</div>
                             <div class="w-8 h-8 rounded-full bg-green-500 border-2 border-white flex items-center justify-center text-white text-xs font-bold">SK</div>
                             <div class="w-8 h-8 rounded-full bg-purple-500 border-2 border-white flex items-center justify-center text-white text-xs font-bold">AL</div>
                         </div>
                     </div>
                     <div class="space-y-3">
                         <div class="flex items-start gap-2">
                             <div class="w-6 h-6 rounded-full bg-blue-500 flex items-center justify-center text-white text-[10px] font-bold flex-shrink-0 mt-0.5">JD</div>
                             <div class="flex-1">
                                 <div class="text-xs font-medium text-gray-900">John edited app.js</div>
                                 <div class="text-[10px] text-gray-500">2 minutes ago</div>
                             </div>
                         </div>
                         <div class="flex items-start gap-2">
                             <div class="w-6 h-6 rounded-full bg-green-500 flex items-center justify-center text-white text-[10px] font-bold flex-shrink-0 mt-0.5">SK</div>
                             <div class="flex-1">
                                 <div class="text-xs font-medium text-gray-900">Sarah deployed to production</div>
                                 <div class="text-[10px] text-gray-500">5 minutes ago</div>
                             </div>
                         </div>
                         <div class="flex items-start gap-2">
                             <div class="w-6 h-6 rounded-full bg-purple-500 flex items-center justify-center text-white text-[10px] font-bold flex-shrink-0 mt-0.5">AL</div>
                             <div class="flex-1">
                                 <div class="text-xs font-medium text-gray-900">Alex is typing...</div>
                                 <div class="text-[10px] text-gray-500">now</div>
                             </div>
                         </div>
                     </div>
                 </div>
             </div>
        </div>
    </div>
  </section>
  
  <!-- Floating Action Bar (Stickyish) -->
  <div class="sticky bottom-6 z-40 flex justify-center pointer-events-none">
      <div class="bg-white/80 backdrop-blur-md border border-gray-200 shadow-lg rounded-full py-3 px-6 flex items-center gap-6 pointer-events-auto">
          <span class="text-sm font-medium text-gray-900 hidden sm:block">Transform ideas into production apps with AI</span>
          <button class="bg-black text-white text-xs font-bold px-4 py-2 rounded-full hover:bg-gray-800 transition-colors">
              Start building
          </button>
      </div>
  </div>

  <!-- Seamless Timeline Section -->
  <section class="max-w-[1400px] mx-auto px-6 py-24">
    <div class="text-center max-w-2xl mx-auto mb-16">
        <h2 class="text-4xl font-medium tracking-tight mb-4">Everything you need to build and ship</h2>
        <p class="text-gray-600">From AI code generation to deployment and monitoring, Replit combines every tool you need to build, collaborate, and scale your applications.</p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <!-- Card 1: AI Agent (Wide) -->
        <div class="md:col-span-2 bg-gray-50 rounded-3xl p-8 border border-gray-100 overflow-hidden relative min-h-[300px]">
            <div class="relative z-10 max-w-md">
                <h3 class="text-xl font-medium mb-2">Replit Agent</h3>
                <p class="text-sm text-gray-600 leading-relaxed">Describe your app in plain English and watch as AI builds it for you. From database schema to UI components, Agent handles the entire development process.</p>
            </div>
            <div class="absolute right-0 bottom-0 w-2/3 h-2/3 translate-x-10 translate-y-10">
                 <!-- AI Agent visual -->
                 <div class="w-full h-full bg-white rounded-tl-xl shadow-lg border border-gray-100 p-4 transform -rotate-6">
                     <div class="space-y-2">
                         <div class="h-6 bg-primary-100 rounded w-full flex items-center px-2 text-[10px] text-primary-700">✨ Generating components...</div>
                         <div class="h-6 bg-blue-100 rounded w-3/4 flex items-center px-2 text-[10px] text-blue-700">Setting up database...</div>
                         <div class="h-6 bg-green-100 rounded w-1/2 flex items-center px-2 text-[10px] text-green-700">✓ Ready to deploy</div>
                     </div>
                 </div>
            </div>
        </div>

        <!-- Card 2: Deployment -->
        <div class="bg-gray-50 rounded-3xl p-8 border border-gray-100 overflow-hidden relative min-h-[300px]">
             <div class="relative z-10">
                <h3 class="text-xl font-medium mb-2">Instant Deployment</h3>
                <p class="text-sm text-gray-600 leading-relaxed">Deploy with one click to production. Automatic scaling, SSL certificates, and global CDN included — no DevOps required.</p>
            </div>
            <div class="absolute inset-x-0 bottom-0 h-40 bg-gradient-to-t from-primary-100 to-transparent"></div>
            <div class="absolute bottom-4 right-4 left-4 h-32 bg-gradient-to-br from-primary-600 to-primary-800 rounded-lg shadow-lg overflow-hidden flex items-center justify-center">
                <div class="text-center text-white">
                    <div class="text-4xl mb-2">🚀</div>
                    <div class="text-sm font-medium">Deployed in 2.3s</div>
                </div>
            </div>
        </div>

        <!-- Card 3: GitHub Integration -->
        <div class="bg-gray-50 rounded-3xl p-8 border border-gray-100 overflow-hidden relative min-h-[300px]">
            <div class="relative z-10">
                <h3 class="text-xl font-medium mb-2">GitHub Integration</h3>
                <p class="text-sm text-gray-600 leading-relaxed">Import existing repositories or push your Replit projects to GitHub. Seamless two-way sync keeps everything in sync.</p>
            </div>
            <div class="absolute bottom-6 left-6 right-6 flex gap-4">
                <div class="flex-1 bg-black text-white p-3 rounded-lg text-xs flex items-center justify-center gap-2 shadow-lg">
                    <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 24 24"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
                    Import
                </div>
                <div class="flex-1 bg-white text-black border border-gray-200 p-3 rounded-lg text-xs flex items-center justify-center gap-2 shadow-sm">
                    <ArrowRight size={12} />
                    Push
                </div>
            </div>
        </div>

        <!-- Card 4: Real-time Collaboration -->
        <div class="bg-gray-50 rounded-3xl p-8 border border-gray-100 overflow-hidden relative min-h-[300px]">
            <div class="relative z-10">
                <h3 class="text-xl font-medium mb-2">Real-time Collaboration</h3>
                <p class="text-sm text-gray-600 leading-relaxed">Work together with your team in the same codebase. See changes instantly, share feedback, and ship faster.</p>
            </div>
            <div class="absolute bottom-6 left-6 right-6 bg-white rounded-xl border border-gray-100 p-3 shadow-md">
                <div class="flex items-center gap-3 mb-2">
                    <div class="w-8 h-8 bg-green-500 rounded-full flex items-center justify-center text-white text-xs font-bold">SK</div>
                    <div>
                        <div class="text-xs font-bold">Sarah Kim</div>
                        <div class="text-[10px] text-gray-500">Just pushed the new feature!</div>
                    </div>
                </div>
                <div class="flex -space-x-2 mt-2">
                    <div class="w-6 h-6 rounded-full bg-blue-500 border-2 border-white"></div>
                    <div class="w-6 h-6 rounded-full bg-purple-500 border-2 border-white"></div>
                    <div class="w-6 h-6 rounded-full bg-orange-500 border-2 border-white"></div>
                </div>
            </div>
        </div>

        <!-- Card 5: Built-in Services -->
        <div class="bg-gray-50 rounded-3xl p-8 border border-gray-100 overflow-hidden relative min-h-[300px]">
            <div class="relative z-10">
                <h3 class="text-xl font-medium mb-2">Built-in Services</h3>
                <p class="text-sm text-gray-600 leading-relaxed">Authentication, database, hosting, and monitoring included out of the box. No configuration, no API keys to manage.</p>
            </div>
            <div class="absolute bottom-6 left-6 right-6 space-y-2">
                <div class="bg-white rounded-lg p-2 flex items-center gap-2 shadow-sm border border-gray-100">
                    <span class="text-lg">🔐</span> <span class="text-xs font-medium">Authentication</span>
                </div>
                <div class="bg-white rounded-lg p-2 flex items-center gap-2 shadow-sm border border-gray-100 ml-4">
                    <span class="text-lg">💾</span> <span class="text-xs font-medium">PostgreSQL Database</span>
                </div>
                <div class="bg-white rounded-lg p-2 flex items-center gap-2 shadow-sm border border-gray-100">
                    <span class="text-lg">📊</span> <span class="text-xs font-medium">Monitoring</span>
                </div>
            </div>
        </div>
    </div>
  </section>

  <!-- Built for Every Creator -->
  <section class="max-w-[1400px] mx-auto px-6 py-24">
      <div class="text-center max-w-2xl mx-auto mb-16">
        <h2 class="text-4xl font-medium tracking-tight mb-4">Built for builders of all backgrounds</h2>
        <p class="text-gray-600">From non-technical founders to product managers and solopreneurs, Replit empowers anyone with an idea to build production-ready applications — no coding experience required.</p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- User 1 -->
        <div class="group">
            <div class="aspect-square rounded-2xl overflow-hidden mb-6 relative">
                <img src="/generated/image-a-non-technical-founder-working-on-lapto-1766000804948-0.webp" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105" alt="Non-technical Founder" />
                <div class="absolute inset-0 bg-gradient-to-t from-primary-900/60 to-transparent mix-blend-multiply"></div>
                <div class="absolute inset-0 bg-primary-500/20 mix-blend-color"></div>
            </div>
            <h3 class="text-lg font-medium mb-2">Non-technical founders</h3>
            <p class="text-xs text-gray-500 leading-relaxed">Turn your startup idea into a working prototype in minutes. Build MVPs, validate concepts, and iterate quickly without hiring a development team.</p>
        </div>

        <!-- User 2 -->
        <div class="group">
            <div class="aspect-square rounded-2xl overflow-hidden mb-6 relative">
                <img src="/generated/image-a-product-manager-reviewing-app-prototyp-1766000810165-1.webp" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105" alt="Product Manager" />
                <div class="absolute inset-0 bg-gradient-to-t from-blue-900/60 to-transparent mix-blend-multiply"></div>
                <div class="absolute inset-0 bg-blue-500/20 mix-blend-color"></div>
            </div>
            <h3 class="text-lg font-medium mb-2">Product managers</h3>
            <p class="text-xs text-gray-500 leading-relaxed">Create functional prototypes to test ideas with users before committing engineering resources. Move from concept to clickable demo in hours, not weeks.</p>
        </div>

        <!-- User 3 -->
        <div class="group">
            <div class="aspect-square rounded-2xl overflow-hidden mb-6 relative">
                <img src="/generated/image-a-solopreneur-entrepreneur-working-from--1766000814511-2.webp" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105" alt="Solopreneur" />
                <div class="absolute inset-0 bg-gradient-to-t from-purple-900/60 to-transparent mix-blend-multiply"></div>
                <div class="absolute inset-0 bg-purple-500/20 mix-blend-color"></div>
            </div>
            <h3 class="text-lg font-medium mb-2">Solopreneurs</h3>
            <p class="text-xs text-gray-500 leading-relaxed">Build custom tools and apps for your business without technical dependencies. From client portals to automation tools, create exactly what you need.</p>
        </div>
    </div>
  </section>

  <!-- Testimonials Section -->
  <section class="max-w-[1400px] mx-auto px-6 py-24">
      <div class="text-center max-w-2xl mx-auto mb-16">
        <h2 class="text-4xl font-medium tracking-tight mb-4">Trusted by founders and innovators</h2>
        <p class="text-gray-600">See how Replit is helping entrepreneurs and teams turn ideas into reality faster than ever before.</p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-6 max-w-5xl mx-auto">
        <!-- Testimonial 1 -->
        <div class="bg-white rounded-2xl border border-gray-200 p-8 shadow-sm">
            <div class="mb-6">
                <p class="text-gray-700 leading-relaxed mb-4">"I asked Replit to 'clone LinkedIn' just to see how far it would get with a single prompt. The result? A surprisingly functional prototype. It's a powerful reminder: with the right framing, today's AI tools can turn a single idea into working software."</p>
            </div>
            <div class="flex items-center gap-3">
                <div class="w-12 h-12 rounded-full bg-gray-200"></div>
                <div>
                    <div class="font-medium text-gray-900">Reid Hoffman</div>
                    <div class="text-sm text-gray-500">Co-founder, LinkedIn</div>
                </div>
            </div>
        </div>

        <!-- Testimonial 2 -->
        <div class="bg-white rounded-2xl border border-gray-200 p-8 shadow-sm">
            <div class="mb-6">
                <p class="text-gray-700 leading-relaxed mb-4">"I can honestly say that if it weren't for Replit and that prototype that I was able to build in two weeks, it just wouldn't have happened. The opportunity would have perished. Someone else would have done it first."</p>
            </div>
            <div class="flex items-center gap-3">
                <div class="w-12 h-12 rounded-full bg-gray-200"></div>
                <div>
                    <div class="font-medium text-gray-900">Scott Stevenson</div>
                    <div class="text-sm text-gray-500">Co-founder & CEO, Spellbook</div>
                </div>
            </div>
        </div>

        <!-- Testimonial 3 -->
        <div class="bg-white rounded-2xl border border-gray-200 p-8 shadow-sm">
            <div class="mb-6">
                <p class="text-gray-700 leading-relaxed mb-4">"If I went to my developer and said, make this, it would probably take him a week of his time. I did it in an hour or two."</p>
            </div>
            <div class="flex items-center gap-3">
                <div class="w-12 h-12 rounded-full bg-gray-200"></div>
                <div>
                    <div class="font-medium text-gray-900">Preston Zeller</div>
                    <div class="text-sm text-gray-500">Chief Growth Officer, Batchdata</div>
                </div>
            </div>
        </div>

        <!-- Testimonial 4 -->
        <div class="bg-white rounded-2xl border border-gray-200 p-8 shadow-sm">
            <div class="mb-6">
                <p class="text-gray-700 leading-relaxed mb-4">"Ok, I'm addicted to Replit. For my entire design career, I've always had to hire developers to do even the most basic stuff for me. Having an absolute blast having a free AI programmer at my behest."</p>
            </div>
            <div class="flex items-center gap-3">
                <div class="w-12 h-12 rounded-full bg-gray-200"></div>
                <div>
                    <div class="font-medium text-gray-900">Andrew Wilkinson</div>
                    <div class="text-sm text-gray-500">Co-founder, Tiny</div>
                </div>
            </div>
        </div>
    </div>
  </section>

  <!-- FAQ Section -->
  <section class="max-w-[1000px] mx-auto px-6 py-24">
      <h2 class="text-3xl font-medium mb-12">Frequently asked questions</h2>
      
      <div class="divide-y divide-gray-100">
          {#each faqs as question, i}
            <div class="py-4">
                <button class="w-full flex items-center justify-between text-left group" on:click={() => toggleFaq(i)}>
                    <span class="text-sm md:text-base text-gray-700 group-hover:text-black transition-colors">{question}</span>
                    <span class="text-gray-400">
                        <Plus size={16} class="transition-transform duration-200 {openFaq === i ? 'rotate-45' : ''}" />
                    </span>
                </button>
                {#if openFaq === i}
                    <div class="mt-4 text-sm text-gray-500 leading-relaxed pb-2">
                        {#if i === 0}
                            No coding experience required! Replit is specifically designed for non-technical founders and product managers. Simply describe your app idea in plain English, and Replit Agent will build it for you.
                        {:else if i === 1}
                            Replit Agent is an AI-powered development assistant that understands natural language. Describe what you want to build, and it writes the code, sets up the infrastructure, and deploys your application automatically.
                        {:else if i === 2}
                            Yes! You can import any GitHub repository with one click. Replit automatically detects your tech stack, installs dependencies, and gets your project running in seconds.
                        {:else if i === 3}
                            Replit supports all major programming languages including JavaScript, Python, TypeScript, Go, Rust, Java, C++, and many more. You can build web apps, APIs, mobile backends, and more.
                        {:else if i === 4}
                            Replit offers a free tier to get started. Paid plans start at affordable monthly rates and include additional compute resources, faster deployments, and team collaboration features.
                        {:else if i === 5}
                            Absolutely! Deploy your apps to production with one click. Replit includes automatic scaling, SSL certificates, global CDN, and monitoring — no DevOps knowledge required.
                        {:else if i === 6}
                            Yes! Replit includes built-in authentication, PostgreSQL database, hosting, and monitoring services out of the box. No configuration or API keys needed.
                        {:else if i === 7}
                            Yes! Multiple team members can work in the same codebase simultaneously. See changes in real-time, share feedback, and collaborate seamlessly.
                        {:else if i === 8}
                            Yes! Replit offers enterprise plans with SOC2 compliance, dedicated support, custom deployment options, and advanced security features for large organizations.
                        {:else if i === 9}
                            With Replit Agent, you can go from idea to working prototype in minutes. What traditionally took weeks or months can now be accomplished in hours or even minutes.
                        {:else if i === 10}
                            Yes! You can connect your own custom domain to any deployed Replit app. SSL certificates are automatically provisioned and renewed.
                        {:else}
                            You can build virtually any type of application: web apps, mobile backends, APIs, SaaS products, internal tools, prototypes, MVPs, and more. If it runs on the web, you can build it on Replit.
                        {/if}
                    </div>
                {/if}
            </div>
          {/each}
      </div>
  </section>

  <!-- Bottom CTA -->
  <section class="max-w-[1400px] mx-auto px-6 py-24 flex flex-col items-center text-center border-t border-gray-100">
      <h2 class="text-4xl font-medium tracking-tight mb-4">Start building your app today</h2>
      <p class="text-gray-600 mb-8 max-w-2xl">Join millions of creators building the next generation of software. From idea to production in minutes.</p>
      <div class="flex items-center gap-4">
          <button class="bg-black text-white px-6 py-3 rounded-full font-medium hover:bg-gray-800 transition-colors text-sm">
              Start building for free
          </button>
          <button class="bg-white text-black border border-gray-200 px-6 py-3 rounded-full font-medium hover:bg-gray-50 transition-colors text-sm">
              Talk to sales
          </button>
      </div>
  </section>
</main>

<style>
    /* Custom scrollbar hide for clean look in some areas if needed */
    .no-scrollbar::-webkit-scrollbar {
        display: none;
    }
    .no-scrollbar {
        -ms-overflow-style: none;
        scrollbar-width: none;
    }
</style>

