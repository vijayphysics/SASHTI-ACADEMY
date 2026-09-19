<!DOCTYPE html>
<html lang="en" class="scroll-smooth" data-theme="cyber-emerald">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Physics Insight Media | SASHTI ACADEMY</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    <!-- Client-Side QRCode.js CDN (Runs locally in browser) -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['"Plus Jakarta Sans"', 'sans-serif'],
                    },
                    colors: {
                        theme_bg: 'var(--bg-color)',
                        theme_text: 'var(--text-color)',
                        theme_card: 'var(--card-bg)',
                        theme_border: 'var(--border-color)',
                        theme_accent: 'var(--accent-glow)',
                    }
                }
            }
        }
    </script>
    <style>
        /* 1. Cyber Emerald (Default) */
        [data-theme="cyber-emerald"] {
            --bg-color: #03140e;
            --text-color: #ecfdf5;
            --card-bg: rgba(6, 32, 23, 0.82);
            --border-color: rgba(52, 211, 153, 0.2);
            --accent-glow: #10b981;
            --hero-grad-1: #34d399;
            --hero-grad-2: #06b6d4;
            --hero-grad-3: #a3e635;
        }

        /* 2. Royal Violet & Velvet Obsidian */
        [data-theme="royal-violet"] {
            --bg-color: #0d071a;
            --text-color: #faf5ff;
            --card-bg: rgba(24, 14, 46, 0.84);
            --border-color: rgba(192, 132, 252, 0.22);
            --accent-glow: #a855f7;
            --hero-grad-1: #c084fc;
            --hero-grad-2: #f43f5e;
            --hero-grad-3: #38bdf8;
        }

        /* 3. Nordic Slate & Ice Cyan */
        [data-theme="nordic-slate"] {
            --bg-color: #0b1320;
            --text-color: #f0fdfa;
            --card-bg: rgba(17, 28, 48, 0.84);
            --border-color: rgba(56, 189, 248, 0.22);
            --accent-glow: #0ea5e9;
            --hero-grad-1: #38bdf8;
            --hero-grad-2: #818cf8;
            --hero-grad-3: #2dd4bf;
        }

        /* 4. Carbon & Amber Gold */
        [data-theme="carbon-amber"] {
            --bg-color: #120e09;
            --text-color: #fffbeb;
            --card-bg: rgba(31, 23, 15, 0.85);
            --border-color: rgba(251, 191, 36, 0.24);
            --accent-glow: #f59e0b;
            --hero-grad-1: #fbbf24;
            --hero-grad-2: #f97316;
            --hero-grad-3: #ef4444;
        }

        /* 5. Studio Ivory Light */
        [data-theme="studio-light"] {
            --bg-color: #f8fafc;
            --text-color: #0f172a;
            --card-bg: #ffffff;
            --border-color: rgba(0, 0, 0, 0.1);
            --accent-glow: #0284c7;
            --hero-grad-1: #0369a1;
            --hero-grad-2: #4338ca;
            --hero-grad-3: #0f766e;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            transition: background-color 0.3s ease, color 0.3s ease;
        }

        .glass-card {
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            backdrop-filter: blur(16px);
        }
        
        .nav-btn {
            transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1);
        }
        .nav-btn:hover {
            transform: translateY(-2px);
        }
        
        /* Tab Active States */
        .btn-overview.active {
            background: linear-gradient(135deg, #065f46, #10b981) !important;
            color: #ffffff !important;
            border-color: #34d399 !important;
            box-shadow: 0 4px 20px rgba(16, 185, 129, 0.45);
        }
        .btn-fees.active {
            background: linear-gradient(135deg, #581c87, #9333ea) !important;
            color: #ffffff !important;
            border-color: #c084fc !important;
            box-shadow: 0 4px 20px rgba(147, 51, 234, 0.45);
        }
        .btn-faculty.active {
            background: linear-gradient(135deg, #075985, #0ea5e9) !important;
            color: #ffffff !important;
            border-color: #38bdf8 !important;
            box-shadow: 0 4px 20px rgba(14, 165, 233, 0.45);
        }
        .btn-jee.active {
            background: linear-gradient(135deg, #9a3412, #f59e0b) !important;
            color: #ffffff !important;
            border-color: #fbbf24 !important;
            box-shadow: 0 4px 20px rgba(245, 158, 11, 0.45);
        }
        .btn-neet.active {
            background: linear-gradient(135deg, #9f1239, #f43f5e) !important;
            color: #ffffff !important;
            border-color: #fb7185 !important;
            box-shadow: 0 4px 20px rgba(244, 63, 94, 0.45);
        }
        .btn-board.active {
            background: linear-gradient(135deg, #1e3a8a, #3b82f6) !important;
            color: #ffffff !important;
            border-color: #60a5fa !important;
            box-shadow: 0 4px 20px rgba(59, 130, 246, 0.45);
        }
        .btn-media.active {
            background: linear-gradient(135deg, #831843, #ec4899) !important;
            color: #ffffff !important;
            border-color: #f472b6 !important;
            box-shadow: 0 4px 20px rgba(236, 72, 153, 0.45);
        }
        .btn-admissions.active {
            background: linear-gradient(135deg, #134e4a, #14b8a6) !important;
            color: #ffffff !important;
            border-color: #2dd4bf !important;
            box-shadow: 0 4px 20px rgba(20, 184, 166, 0.45);
        }

        /* Strict Single View Display */
        .tab-panel {
            display: none;
        }
        .tab-panel.active {
            display: block;
            animation: fadeIn 0.25s ease-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(8px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .hero-title-grad {
            background-image: linear-gradient(135deg, var(--hero-grad-1), var(--hero-grad-2), var(--hero-grad-3));
        }

        /* Atomic spin animation */
        @keyframes spinSlow {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        .animate-spin-slow {
            animation: spinSlow 18s linear infinite;
        }

        /* QR Canvas styling for local files */
        .qr-wrapper canvas, .qr-wrapper img {
            margin: 0 auto;
            border-radius: 12px;
            max-width: 100%;
            height: auto;
            display: block;
        }
    </style>
</head>
<body class="antialiased min-h-screen flex flex-col font-sans">

    <!-- 1. TOP BRAND & UTILITY HEADER -->
    <header class="glass-card border-b px-4 py-2.5 flex flex-wrap justify-between items-center gap-4">
        
        <!-- TOP-LEFT: SASHTI ACADEMY BRAND IDENTITY & LOGO -->
        <a href="javascript:void(0)" onclick="switchView('overview')" class="flex items-center gap-3 group">
            <!-- Custom Institutional Quantum Atom Logo -->
            <div class="relative w-11 h-11 sm:w-12 sm:h-12 rounded-2xl bg-gradient-to-br from-emerald-950/80 via-slate-900 to-black p-0.5 border border-emerald-500/40 shadow-lg shadow-emerald-500/20 group-hover:scale-105 transition-transform flex items-center justify-center">
                <svg viewBox="0 0 100 100" class="w-full h-full animate-spin-slow text-emerald-400" fill="none" stroke="currentColor">
                    <ellipse cx="50" cy="50" rx="38" ry="14" stroke-width="3" stroke="currentColor" stroke-dasharray="4 2" transform="rotate(30 50 50)" class="opacity-80"/>
                    <ellipse cx="50" cy="50" rx="38" ry="14" stroke-width="3" stroke="currentColor" stroke-dasharray="4 2" transform="rotate(90 50 50)" class="opacity-70"/>
                    <ellipse cx="50" cy="50" rx="38" ry="14" stroke-width="3" stroke="currentColor" stroke-dasharray="4 2" transform="rotate(150 50 50)" class="opacity-80"/>
                </svg>
                <!-- Central Quantum Core -->
                <div class="absolute inset-0 flex items-center justify-center pointer-events-none">
                    <span class="w-6 h-6 rounded-full bg-gradient-to-r from-emerald-400 to-teal-300 text-black font-black text-xs flex items-center justify-center shadow-md shadow-emerald-400/50">
                        S
                    </span>
                </div>
            </div>

            <!-- Brand Typography -->
            <div class="flex flex-col">
                <div class="flex items-center gap-1.5">
                    <span class="text-lg sm:text-xl font-black tracking-tight text-white uppercase group-hover:text-emerald-400 transition-colors">
                        SASHTI ACADEMY
                    </span>
                    <span class="text-[9px] font-extrabold uppercase px-1.5 py-0.5 rounded bg-emerald-500/20 text-emerald-300 border border-emerald-500/30">
                        ESTD
                    </span>
                </div>
                <span class="text-[10px] font-bold tracking-wider uppercase opacity-70 text-emerald-200">
                    Accessible Physics Initiative • NEET & JEE
                </span>
            </div>
        </a>

        <!-- TOP-RIGHT: Direct Contact Points & Color Palette Switcher -->
        <div class="flex items-center gap-3 text-xs font-semibold flex-wrap">
            <a href="tel:+918248955157" class="flex items-center gap-1.5 hover:text-emerald-400 transition-colors">
                <svg class="w-3.5 h-3.5 text-emerald-400" fill="currentColor" viewBox="0 0 20 20"><path d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z"></path></svg>
                <span>+91 82489 55157</span>
            </a>
            <span class="opacity-25">|</span>
            <a href="https://whatsapp.com/channel/0029VbDhSiPEawdkXbHZ2K2b" target="_blank" class="flex items-center gap-1 text-emerald-400 hover:underline">
                <svg class="w-3.5 h-3.5" fill="currentColor" viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.095 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
                <span>WhatsApp Channel</span>
            </a>
            <span class="opacity-25">|</span>
            <a href="https://www.youtube.com/channel/UCDPrYT3_CuZu_5sw7kI61VQ" target="_blank" class="flex items-center gap-1 text-rose-400 hover:underline">
                <svg class="w-3.5 h-3.5" fill="currentColor" viewBox="0 0 24 24"><path d="M23.498 6.186a3.016 3.016 0 0 0-2.122-2.136C19.505 3.545 12 3.545 12 3.545s-7.505 0-9.377.505A3.017 3.017 0 0 0 .502 6.186C0 8.07 0 12 0 12s0 3.93.502 5.814a3.016 3.016 0 0 0 2.122 2.136c1.871.505 9.376.505 9.376.505s7.505 0 9.377-.505a3.015 3.015 0 0 0 2.122-2.136C24 15.93 24 12 24 12s0-3.93-.502-5.814zM9.545 15.568V8.432L15.818 12l-6.273 3.568z"/></svg>
                <span>YouTube</span>
            </a>

            <!-- Theme Color Switcher -->
            <div class="flex items-center gap-1.5 ml-2 border-l border-white/10 pl-3">
                <span class="text-[9px] font-bold uppercase opacity-50">Theme</span>
                <button onclick="setTheme('cyber-emerald')" title="Cyber Emerald Theme" class="w-5 h-5 rounded-full bg-[#03140e] border border-emerald-400 hover:scale-110 transition-transform flex items-center justify-center text-[8px] font-bold text-emerald-300">E</button>
                <button onclick="setTheme('royal-violet')" title="Royal Violet Theme" class="w-5 h-5 rounded-full bg-[#0d071a] border border-purple-400 hover:scale-110 transition-transform flex items-center justify-center text-[8px] font-bold text-purple-300">V</button>
                <button onclick="setTheme('nordic-slate')" title="Nordic Cyan Slate" class="w-5 h-5 rounded-full bg-[#0b1320] border border-sky-400 hover:scale-110 transition-transform flex items-center justify-center text-[8px] font-bold text-sky-300">C</button>
                <button onclick="setTheme('carbon-amber')" title="Carbon Amber Theme" class="w-5 h-5 rounded-full bg-[#120e09] border border-amber-400 hover:scale-110 transition-transform flex items-center justify-center text-[8px] font-bold text-amber-300">A</button>
                <button onclick="setTheme('studio-light')" title="Studio Ivory Theme" class="w-5 h-5 rounded-full bg-[#f8fafc] border border-slate-600 hover:scale-110 transition-transform flex items-center justify-center text-[8px] font-bold text-slate-800">L</button>
            </div>
        </div>
    </header>

    <!-- 2. STICKY NAVIGATION DOCK (POSITIONED ABOVE THE HERO HEADING) -->
    <nav class="sticky top-0 z-50 glass-card border-b shadow-xl px-2 py-2">
        <div class="max-w-7xl mx-auto flex flex-wrap justify-center items-center gap-1.5 sm:gap-2">
            <button onclick="switchView('overview')" id="btn-overview" class="nav-btn btn-overview active px-3 sm:px-4 py-1.5 rounded-xl font-bold text-xs sm:text-sm border glass-card">
                Overview
            </button>
            <button onclick="switchView('fees')" id="btn-fees" class="nav-btn btn-fees px-3 sm:px-4 py-1.5 rounded-xl font-bold text-xs sm:text-sm border glass-card">
                Free Coaching & Fees
            </button>
            <button onclick="switchView('faculty')" id="btn-faculty" class="nav-btn btn-faculty px-3 sm:px-4 py-1.5 rounded-xl font-bold text-xs sm:text-sm border glass-card">
                Faculty Profile
            </button>
            <button onclick="switchView('jee')" id="btn-jee" class="nav-btn btn-jee px-3 sm:px-4 py-1.5 rounded-xl font-bold text-xs sm:text-sm border glass-card">
                JEE Program
            </button>
            <button onclick="switchView('neet')" id="btn-neet" class="nav-btn btn-neet px-3 sm:px-4 py-1.5 rounded-xl font-bold text-xs sm:text-sm border glass-card">
                NEET Program
            </button>
            <button onclick="switchView('board')" id="btn-board" class="nav-btn btn-board px-3 sm:px-4 py-1.5 rounded-xl font-bold text-xs sm:text-sm border glass-card">
                Board Exam
            </button>
            <button onclick="switchView('media')" id="btn-media" class="nav-btn btn-media px-3 sm:px-4 py-1.5 rounded-xl font-bold text-xs sm:text-sm border glass-card flex items-center gap-1.5">
                <span class="w-2 h-2 rounded-full bg-pink-400 animate-pulse"></span>
                <span>Media & QR Hub</span>
            </button>
            <button onclick="switchView('admissions')" id="btn-admissions" class="nav-btn btn-admissions px-3 sm:px-4 py-1.5 rounded-xl font-bold text-xs sm:text-sm border glass-card">
                Admissions Intake
            </button>
        </div>
    </nav>

    <!-- 3. MASSIVE HERO HEADING LINE (POSITIONED UNDERNEATH NAVIGATION BAR) -->
    <section class="max-w-7xl mx-auto w-full px-4 pt-8 pb-4 text-center space-y-3">
        <div class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full text-xs font-black tracking-wider uppercase bg-emerald-500/10 border border-emerald-500/30 text-emerald-400">
            <span class="w-2 h-2 rounded-full bg-emerald-400 animate-ping"></span>
            <span>SASHTI ACADEMY FREE ONLINE PHYSICS COACHING INITIATIVE</span>
        </div>
        
        <h1 class="text-5xl sm:text-7xl md:text-8xl lg:text-9xl font-black tracking-tight uppercase leading-none drop-shadow-2xl">
            PHYSICS INSIGHT<br>
            <span class="text-transparent bg-clip-text hero-title-grad">MEDIA</span>
        </h1>
        
        <p class="text-sm sm:text-lg md:text-xl font-bold opacity-90 uppercase tracking-widest text-emerald-200">
            JEE Main & Advanced • NEET-UG • CUET and Competitive Exams
        </p>
        
        <p class="max-w-3xl mx-auto text-xs sm:text-sm opacity-75 leading-relaxed">
            Dedicated Physics Subject Coaching designed to build strong fundamentals, first-principles understanding, and high-speed problem-solving confidence.
        </p>
    </section>

    <!-- 4. STRICT SINGLE ACTIVE VIEW CONTENT AREA -->
    <main class="flex-grow max-w-7xl mx-auto w-full px-4 py-6">

        <!-- VIEW 1: OVERVIEW -->
        <section id="panel-overview" class="tab-panel active">
            <div class="glass-card rounded-3xl p-6 sm:p-10 border-t-4 border-emerald-500 shadow-2xl">
                <!-- Verbatim Mission Statement -->
                <div class="p-6 sm:p-8 rounded-2xl bg-emerald-950/40 border border-emerald-500/30 mb-8">
                    <span class="text-xs font-extrabold uppercase tracking-widest text-emerald-400 bg-emerald-500/10 px-3 py-1 rounded-full border border-emerald-500/30 inline-block mb-3">Our Core Mission</span>
                    <p class="text-base sm:text-xl font-medium leading-relaxed text-emerald-100">
                        "<strong>SASHTI ACADEMY</strong> is an initiative dedicated to providing quality and accessible Physics coaching for NEET and JEE aspirants. The academy offers <strong>free online Physics coaching</strong>, helping students build strong fundamentals and develop the confidence required for competitive examinations."
                    </p>
                </div>

                <h3 class="text-xl sm:text-2xl font-black mb-6 flex items-center gap-2">
                    <span class="w-3 h-3 rounded-full bg-emerald-400"></span>
                    <span>Its Teaching Approach Focuses On:</span>
                </h3>

                <!-- 6 Exact Teaching Pillars -->
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
                    <div class="p-5 rounded-2xl bg-black/20 border border-white/5 hover:border-emerald-500/40 transition-colors">
                        <div class="w-10 h-10 rounded-xl bg-emerald-500/20 text-emerald-400 font-black text-base flex items-center justify-center mb-3">01</div>
                        <h4 class="text-base font-bold mb-1.5">Strong Conceptual Understanding</h4>
                        <p class="text-xs opacity-75 leading-relaxed">No rote formulas. Concepts are taught directly from physical principles so students can tackle any question variation.</p>
                    </div>

                    <div class="p-5 rounded-2xl bg-black/20 border border-white/5 hover:border-emerald-500/40 transition-colors">
                        <div class="w-10 h-10 rounded-xl bg-emerald-500/20 text-emerald-400 font-black text-base flex items-center justify-center mb-3">02</div>
                        <h4 class="text-base font-bold mb-1.5">Step-by-Step Numerical Problem Solving</h4>
                        <p class="text-xs opacity-75 leading-relaxed">Systematic breakdown of physics problems into identifiable givens, governing laws, and clean algebraic execution.</p>
                    </div>

                    <div class="p-5 rounded-2xl bg-black/20 border border-white/5 hover:border-emerald-500/40 transition-colors">
                        <div class="w-10 h-10 rounded-xl bg-emerald-500/20 text-emerald-400 font-black text-base flex items-center justify-center mb-3">03</div>
                        <h4 class="text-base font-bold mb-1.5">NEET & JEE-Oriented Preparation</h4>
                        <p class="text-xs opacity-75 leading-relaxed">Targeted practice questions calibrated specifically for the speed demands of NEET-UG and calculus depth of JEE Advanced.</p>
                    </div>

                    <div class="p-5 rounded-2xl bg-black/20 border border-white/5 hover:border-emerald-500/40 transition-colors">
                        <div class="w-10 h-10 rounded-xl bg-emerald-500/20 text-emerald-400 font-black text-base flex items-center justify-center mb-3">04</div>
                        <h4 class="text-base font-bold mb-1.5">Interactive Online Learning</h4>
                        <p class="text-xs opacity-75 leading-relaxed">Engaging live sessions with real-time doubt clearing, visual mechanics breakdowns, and structured study plans.</p>
                    </div>

                    <div class="p-5 rounded-2xl bg-black/20 border border-white/5 hover:border-emerald-500/40 transition-colors">
                        <div class="w-10 h-10 rounded-xl bg-emerald-500/20 text-emerald-400 font-black text-base flex items-center justify-center mb-3">05</div>
                        <h4 class="text-base font-bold mb-1.5">Personalized Academic Guidance</h4>
                        <p class="text-xs opacity-75 leading-relaxed">One-on-one mentorship by Chief Faculty R. Vijayakumar to identify specific weak chapters and correct calculation traps.</p>
                    </div>

                    <div class="p-5 rounded-2xl bg-black/20 border border-white/5 hover:border-emerald-500/40 transition-colors">
                        <div class="w-10 h-10 rounded-xl bg-emerald-500/20 text-emerald-400 font-black text-base flex items-center justify-center mb-3">06</div>
                        <h4 class="text-base font-bold mb-1.5">Regular Practice & Exam-Focused Preparation</h4>
                        <p class="text-xs opacity-75 leading-relaxed">Daily Practice Problems (DPPs), chapter-wise tests, and timed mock evaluations to maximize exam performance.</p>
                    </div>
                </div>

                <div class="mt-8 flex flex-wrap gap-4 items-center justify-between p-5 rounded-2xl bg-emerald-500/10 border border-emerald-500/20">
                    <span class="text-xs sm:text-sm font-semibold text-emerald-200">Join our digital channels for daily problem sets and live lecture schedules.</span>
                    <button onclick="switchView('media')" class="px-5 py-2.5 rounded-xl bg-emerald-600 hover:bg-emerald-500 text-white font-bold text-xs transition-colors shadow-lg">
                        View WhatsApp & YouTube QR Codes &rarr;
                    </button>
                </div>
            </div>
        </section>

        <!-- VIEW 2: FREE COACHING & FEES -->
        <section id="panel-fees" class="tab-panel">
            <div class="glass-card rounded-3xl p-6 sm:p-10 border-t-4 border-purple-500 shadow-2xl">
                <div class="flex flex-wrap justify-between items-center gap-3 mb-6">
                    <div>
                        <h2 class="text-2xl sm:text-3xl font-black tracking-tight">Free Coaching & Fee Modes</h2>
                        <p class="text-xs sm:text-sm opacity-75">Committed to accessible physics education via free online coaching and premium cohorts</p>
                    </div>
                    <span class="px-3 py-1 rounded-full text-xs font-bold bg-emerald-500/20 text-emerald-300 border border-emerald-500/30">Official Schedule</span>
                </div>

                <!-- Free Online Coaching Callout -->
                <div class="p-5 sm:p-6 rounded-2xl bg-gradient-to-r from-emerald-950/40 to-slate-900/50 border border-emerald-500/40 mb-8 flex flex-col md:flex-row justify-between items-start md:items-center gap-4">
                    <div>
                        <span class="text-[10px] font-extrabold uppercase tracking-widest bg-emerald-500 text-black px-2.5 py-0.5 rounded font-mono">Sashti Academy Initiative</span>
                        <h3 class="text-xl font-black text-emerald-400 mt-2">Free Online Physics Coaching</h3>
                        <p class="text-xs sm:text-sm opacity-80 mt-1 max-w-2xl">
                            All students targeting NEET & JEE can attend our free foundational online physics masterclasses and concept sessions to build strong fundamentals without cost barrier.
                        </p>
                    </div>
                    <button onclick="switchView('admissions')" class="px-6 py-3 rounded-xl bg-emerald-600 hover:bg-emerald-500 text-white font-bold text-xs sm:text-sm whitespace-nowrap shadow-lg shadow-emerald-600/30 transition-all">
                        Register Free Access
                    </button>
                </div>

                <!-- Structured Intensive Cohorts -->
                <h3 class="text-base sm:text-lg font-bold mb-4">Intensive Year-Long Batches (Full Study Material + Test Series)</h3>
                <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4 mb-8">
                    <div class="p-5 rounded-2xl bg-black/20 border border-amber-500/30 flex flex-col justify-between">
                        <div>
                            <div class="text-xs font-bold uppercase tracking-wider text-amber-400 mb-1">JEE Program</div>
                            <div class="text-3xl font-black mb-1">₹28,000</div>
                            <div class="text-xs opacity-60 mb-3">Full Academic Course</div>
                            <p class="text-xs font-medium opacity-80 mb-4">Calculus proofs, Irodov/PYQ benchmark & full CBT mock series.</p>
                        </div>
                        <div class="text-xs font-bold text-center bg-amber-500/10 text-amber-300 border border-amber-500/20 py-1.5 rounded-lg">
                            Installment: ₹3,000 / month
                        </div>
                    </div>

                    <div class="p-5 rounded-2xl bg-black/20 border border-rose-500/30 flex flex-col justify-between">
                        <div>
                            <div class="text-xs font-bold uppercase tracking-wider text-rose-400 mb-1">NEET Program</div>
                            <div class="text-3xl font-black mb-1">₹25,000</div>
                            <div class="text-xs opacity-60 mb-3">Full Academic Course</div>
                            <p class="text-xs font-medium opacity-80 mb-4">Line-by-line NCERT mechanics, 45-second elimination drills & test bank.</p>
                        </div>
                        <div class="text-xs font-bold text-center bg-rose-500/10 text-rose-300 border border-rose-500/20 py-1.5 rounded-lg">
                            Installment: ₹2,800 / month
                        </div>
                    </div>

                    <div class="p-5 rounded-2xl bg-black/20 border border-sky-500/30 flex flex-col justify-between">
                        <div>
                            <div class="text-xs font-bold uppercase tracking-wider text-sky-400 mb-1">Board Exam Centum</div>
                            <div class="text-3xl font-black mb-1">₹18,000</div>
                            <div class="text-xs opacity-60 mb-3">Class 11 or Class 12</div>
                            <p class="text-xs font-medium opacity-80 mb-4">CBSE & Tamil Nadu State Board 5-mark subjective derivation blueprints.</p>
                        </div>
                        <div class="text-xs font-bold text-center bg-sky-500/10 text-sky-300 border border-sky-500/20 py-1.5 rounded-lg">
                            Installment: ₹2,000 / month
                        </div>
                    </div>

                    <div class="p-5 rounded-2xl bg-black/20 border border-purple-500/30 flex flex-col justify-between">
                        <div>
                            <div class="text-xs font-bold uppercase tracking-wider text-purple-400 mb-1">60-Day Booster</div>
                            <div class="text-3xl font-black mb-1">₹9,500</div>
                            <div class="text-xs opacity-60 mb-3">Rapid Revision / Crash</div>
                            <p class="text-xs font-medium opacity-80 mb-4">High-yield repeated PYQs, formula maps, and rapid error corrections.</p>
                        </div>
                        <div class="text-xs font-bold text-center bg-purple-500/10 text-purple-300 border border-purple-500/20 py-1.5 rounded-lg">
                            One-Time Consolidated
                        </div>
                    </div>
                </div>

                <!-- Verified Payment Channels -->
                <div class="border-t border-white/10 pt-6">
                    <h3 class="text-base sm:text-lg font-bold mb-4">Official Payment Details</h3>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div class="p-5 rounded-2xl bg-purple-950/20 border border-purple-500/30 flex flex-col justify-between">
                            <div>
                                <div class="flex items-center justify-between mb-2">
                                    <span class="font-bold text-sm text-purple-300">GPay / PhonePe / Paytm UPI</span>
                                    <span class="text-[10px] font-bold bg-purple-500/20 px-2 py-0.5 rounded text-purple-300">Instant</span>
                                </div>
                                <div class="space-y-1.5 mb-3 text-sm">
                                    <div>UPI ID: <strong class="text-white font-mono select-all">8248955157@axl</strong></div>
                                    <div>Number: <strong class="text-white font-mono select-all">8248955157</strong></div>
                                </div>
                            </div>
                            <button onclick="copyToClipboard('8248955157@axl', this)" class="w-full text-xs font-bold bg-purple-500/20 hover:bg-purple-500/30 text-purple-200 py-2.5 rounded-lg transition-colors border border-purple-500/30">
                                Copy UPI ID
                            </button>
                        </div>

                        <div class="p-5 rounded-2xl bg-purple-950/20 border border-purple-500/30 flex flex-col justify-between">
                            <div>
                                <div class="flex items-center justify-between mb-2">
                                    <span class="font-bold text-sm text-purple-300">Bank NEFT / IMPS & Receipt Verification</span>
                                    <span class="text-[10px] font-bold bg-emerald-500/20 px-2 py-0.5 rounded text-emerald-300">WhatsApp Desk</span>
                                </div>
                                <p class="text-xs opacity-75 mb-3">
                                    For direct bank transfers or to dispatch your UPI payment screenshot to confirm enrollment immediately.
                                </p>
                            </div>
                            <a href="https://wa.me/918248955157?text=Hello%20Sir,%20I%20have%20made%20a%20fee%20payment%20for%20Physics%20Subject%20Coaching.%20Sharing%20my%20receipt%20here." target="_blank" class="w-full text-xs font-bold bg-emerald-600 hover:bg-emerald-500 text-white py-2.5 rounded-lg text-center transition-colors">
                                Send Payment Receipt on WhatsApp
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- VIEW 3: FACULTY PROFILE -->
        <section id="panel-faculty" class="tab-panel">
            <div class="glass-card rounded-3xl p-6 sm:p-10 border-t-4 border-sky-500 shadow-2xl">
                <div class="flex flex-col md:flex-row gap-8 items-center md:items-start">
                    <div class="w-40 h-40 sm:w-48 sm:h-48 rounded-3xl bg-gradient-to-br from-sky-950 via-slate-900 to-black border border-sky-500/30 shadow-xl flex flex-col items-center justify-center shrink-0 text-center p-4">
                        <svg class="w-16 h-16 text-sky-400 mb-2 opacity-80" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M12 14l9-5-9-5-9 5 9 5z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M12 14l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14z"></path></svg>
                        <span class="text-xs font-black tracking-widest uppercase text-sky-400">Chief Faculty</span>
                    </div>
                    <div class="flex-grow text-center md:text-left">
                        <span class="text-xs font-bold tracking-widest uppercase text-sky-400 bg-sky-500/10 px-3 py-1 rounded-full border border-sky-500/30 inline-block mb-3">Academic Leadership</span>
                        <h2 class="text-3xl sm:text-4xl font-black mb-1">R. Vijayakumar</h2>
                        <h3 class="text-sm sm:text-base font-semibold text-sky-300 mb-4">Lead Physics Faculty • Sashti Academy</h3>
                        
                        <p class="text-sm sm:text-base opacity-80 leading-relaxed mb-6">
                            With over 14 years of intensive physics classroom pedagogy, R. Vijayakumar has specialized in preparing students for competitive examinations including JEE Main, JEE Advanced, and NEET-UG. His instructional framework focuses on cultivating deep physical intuition, systematic numerical problem solving, and eliminating fear of physics.
                        </p>

                        <div class="grid grid-cols-2 sm:grid-cols-3 gap-3 mb-6">
                            <div class="p-3 rounded-xl bg-black/20 border border-white/5">
                                <div class="text-2xl font-black text-sky-400">14+</div>
                                <div class="text-[11px] opacity-60 font-semibold uppercase tracking-wider">Years Experience</div>
                            </div>
                            <div class="p-3 rounded-xl bg-black/20 border border-white/5">
                                <div class="text-2xl font-black text-sky-400">1,000+</div>
                                <div class="text-[11px] opacity-60 font-semibold uppercase tracking-wider">Students Guided</div>
                            </div>
                            <div class="p-3 rounded-xl bg-black/20 border border-white/5 col-span-2 sm:col-span-1">
                                <div class="text-2xl font-black text-sky-400">Centum</div>
                                <div class="text-[11px] opacity-60 font-semibold uppercase tracking-wider">Board Track Record</div>
                            </div>
                        </div>

                        <div class="flex flex-wrap gap-3 justify-center md:justify-start">
                            <a href="https://wa.me/918248955157?text=Hello%20Vijayakumar%20Sir,%20I%20would%20like%20to%20consult%20regarding%20Physics%20Coaching." target="_blank" class="px-5 py-2.5 rounded-xl bg-emerald-600 hover:bg-emerald-500 text-white font-bold text-xs sm:text-sm flex items-center gap-2 transition-colors">
                                <span>Message Faculty on WhatsApp</span>
                            </a>
                            <a href="tel:+918248955157" class="px-5 py-2.5 rounded-xl glass-card hover:bg-white/10 font-bold text-xs sm:text-sm flex items-center gap-2 transition-colors border border-white/10">
                                <span>Call: +91 82489 55157</span>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- VIEW 4: JEE PROGRAM -->
        <section id="panel-jee" class="tab-panel">
            <div class="glass-card rounded-3xl p-6 sm:p-10 border-t-4 border-amber-500 shadow-2xl">
                <div class="flex flex-wrap justify-between items-center gap-3 mb-4">
                    <div>
                        <h2 class="text-2xl sm:text-3xl font-black text-amber-400">JEE Main & Advanced Program</h2>
                        <p class="text-xs sm:text-sm opacity-75">Calculus-based derivations, multi-concept physics problems, and HC Verma/Irodov benchmarks</p>
                    </div>
                    <span class="text-xs font-bold px-3 py-1 rounded-full bg-amber-500/20 text-amber-300 border border-amber-500/30">Calculus Rigor</span>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mb-6">
                    <div class="p-4 rounded-xl bg-black/20 border border-amber-500/20">
                        <h4 class="font-bold text-sm text-amber-300 mb-1">Calculus & Vector Mechanics</h4>
                        <p class="text-xs opacity-75">Derivations using differential and integral equations for variable acceleration, center of mass, and rotational inertia.</p>
                    </div>
                    <div class="p-4 rounded-xl bg-black/20 border border-amber-500/20">
                        <h4 class="font-bold text-sm text-amber-300 mb-1">Multi-Concept Synthesis</h4>
                        <p class="text-xs opacity-75">Problems bridging thermodynamics with mechanics, and electrostatics with simple harmonic motion.</p>
                    </div>
                    <div class="p-4 rounded-xl bg-black/20 border border-amber-500/20">
                        <h4 class="font-bold text-sm text-amber-300 mb-1">CBT Testing Engine</h4>
                        <p class="text-xs opacity-75">Regular Computer-Based Tests with granular analytics tracking negative mark patterns and time spent per problem.</p>
                    </div>
                </div>

                <h3 class="text-base sm:text-lg font-bold mb-3 text-amber-200">Sample JEE Advanced PYQ & Derivation Blueprint</h3>
                <div class="p-5 rounded-2xl bg-black/30 border border-amber-500/30 mb-6">
                    <p class="text-sm font-semibold mb-3 leading-relaxed">
                        <strong>Problem (Rotational Dynamics):</strong> A uniform solid cylinder of mass \(M\) and radius \(R\) is placed on a rough horizontal surface with initial backspin \(\omega_0\) without initial translational velocity (\(v_0=0\)). Find the time \(t\) when pure rolling begins, given coefficient of friction \(\mu\).
                    </p>
                    <div class="p-4 rounded-xl bg-black/50 font-mono text-xs text-amber-100/90 space-y-1.5 border border-white/5">
                        <div>1. Friction force opposes slipping: \( f_k = \mu N = \mu Mg \)</div>
                        <div>2. Linear acceleration: \( a = \frac{f_k}{M} = \mu g \implies v(t) = (\mu g)t \)</div>
                        <div>3. Torque about COM: \( \tau = f_k R = I\alpha \implies (\mu Mg)R = \left(\frac{1}{2}MR^2\right)\alpha \implies \alpha = \frac{2\mu g}{R} \)</div>
                        <div>4. Angular velocity: \( \omega(t) = \omega_0 - \alpha t = \omega_0 - \left(\frac{2\mu g}{R}\right)t \)</div>
                        <div>5. Pure rolling condition: \( v(t) = R\omega(t) \)</div>
                        <div>6. \( (\mu g)t = R\left[\omega_0 - \left(\frac{2\mu g}{R}\right)t\right] \implies (\mu g)t + 2(\mu g)t = R\omega_0 \)</div>
                        <div class="text-emerald-400 font-bold pt-1">&#10132; Result: \( t = \frac{R\omega_0}{3\mu g} \)</div>
                    </div>
                </div>

                <div class="flex flex-wrap gap-4 items-center justify-between p-4 rounded-2xl bg-amber-500/10 border border-amber-500/20">
                    <div>
                        <h4 class="font-bold text-sm text-amber-300">Need Complete JEE Problem Sheets & DPPs?</h4>
                        <p class="text-xs opacity-70">Access topic-wise Daily Practice Problems with complete analytical derivations.</p>
                    </div>
                    <a href="https://wa.me/918248955157?text=Hello%20Sir,%20please%20send%20me%20sample%20JEE%20Physics%20DPP%20and%20Study%20Materials." target="_blank" class="px-4 py-2 rounded-xl bg-amber-500 hover:bg-amber-400 text-black font-bold text-xs transition-colors">
                        Request JEE Materials via WhatsApp
                    </a>
                </div>
            </div>
        </section>

        <!-- VIEW 5: NEET PROGRAM -->
        <section id="panel-neet" class="tab-panel">
            <div class="glass-card rounded-3xl p-6 sm:p-10 border-t-4 border-rose-500 shadow-2xl">
                <div class="flex flex-wrap justify-between items-center gap-3 mb-4">
                    <div>
                        <h2 class="text-2xl sm:text-3xl font-black text-rose-400">NEET-UG Medical 180 Program</h2>
                        <p class="text-xs sm:text-sm opacity-75">Targeting 180/180 in Physics through NCERT line-by-line concept mastery and rapid option elimination</p>
                    </div>
                    <span class="text-xs font-bold px-3 py-1 rounded-full bg-rose-500/20 text-rose-300 border border-rose-500/30">Target 180/180</span>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mb-6">
                    <div class="p-4 rounded-xl bg-black/20 border border-rose-500/20">
                        <h4 class="font-bold text-sm text-rose-300 mb-1">NCERT Line-by-Line Mastery</h4>
                        <p class="text-xs opacity-75">Every theoretical assertion, graph, and numerical example in NCERT Class 11 and 12 dissected word-for-word.</p>
                    </div>
                    <div class="p-4 rounded-xl bg-black/20 border border-rose-500/20">
                        <h4 class="font-bold text-sm text-rose-300 mb-1">45-Second Elimination Tactics</h4>
                        <p class="text-xs opacity-75">Dimensional analysis, extreme case substitution, and ratio methods to solve MCQs under 45 seconds without lengthy calculations.</p>
                    </div>
                    <div class="p-4 rounded-xl bg-black/20 border border-rose-500/20">
                        <h4 class="font-bold text-sm text-rose-300 mb-1">Zero Negative Mark Drills</h4>
                        <p class="text-xs opacity-75">Dedicated error analysis to stop silly mistakes, unit mismatches, and confusion between sin/cos components.</p>
                    </div>
                </div>

                <h3 class="text-base sm:text-lg font-bold mb-3 text-rose-200">Sample NEET PYQ & 45-Second Elimination</h3>
                <div class="p-5 rounded-2xl bg-black/30 border border-rose-500/30 mb-6">
                    <p class="text-sm font-semibold mb-3 leading-relaxed">
                        <strong>Problem (Elasticity & Young's Modulus):</strong> Two wires \(A\) and \(B\) are of the same material. Their lengths are in the ratio \(1:2\) and their diameters are in the ratio \(2:1\). If they are stretched by the same force, the ratio of elongation \(\Delta L_A : \Delta L_B\) is?
                    </p>
                    <div class="p-4 rounded-xl bg-black/50 font-mono text-xs text-rose-100/90 space-y-1.5 border border-white/5">
                        <div>1. Fundamental relation: \( Y = \frac{F/A}{\Delta L/L} \implies \Delta L = \frac{FL}{A Y} = \frac{4FL}{\pi d^2 Y} \)</div>
                        <div>2. For identical material (\(Y\)) and equal force (\(F\)): \( \Delta L \propto \frac{L}{d^2} \)</div>
                        <div>3. Ratio equation: \( \frac{\Delta L_A}{\Delta L_B} = \left(\frac{L_A}{L_B}\right) \times \left(\frac{d_B}{d_A}\right)^2 \)</div>
                        <div>4. Substitute given ratios: \( \frac{L_A}{L_B} = \frac{1}{2} \), and \( \frac{d_A}{d_B} = \frac{2}{1} \implies \frac{d_B}{d_A} = \frac{1}{2} \)</div>
                        <div>5. \( \frac{\Delta L_A}{\Delta L_B} = \left(\frac{1}{2}\right) \times \left(\frac{1}{2}\right)^2 = \frac{1}{2} \times \frac{1}{4} = \frac{1}{8} \)</div>
                        <div class="text-emerald-400 font-bold pt-1">&#10132; Result: \( 1:8 \) (Solved in under 20 seconds using ratios)</div>
                    </div>
                </div>

                <div class="flex flex-wrap gap-4 items-center justify-between p-4 rounded-2xl bg-rose-500/10 border border-rose-500/20">
                    <div>
                        <h4 class="font-bold text-sm text-rose-300">Need NEET Formula Blueprints & PYQ Banks?</h4>
                        <p class="text-xs opacity-70">NCERT-aligned physics cheat sheets and high-yield questions.</p>
                    </div>
                    <a href="https://wa.me/918248955157?text=Hello%20Sir,%20please%20send%20me%20sample%20NEET%20Physics%20Formula%20Sheet." target="_blank" class="px-4 py-2 rounded-xl bg-rose-500 hover:bg-rose-400 text-white font-bold text-xs transition-colors">
                        Request NEET Formula Book via WhatsApp
                    </a>
                </div>
            </div>
        </section>

        <!-- VIEW 6: BOARD EXAM -->
        <section id="panel-board" class="tab-panel">
            <div class="glass-card rounded-3xl p-6 sm:p-10 border-t-4 border-blue-500 shadow-2xl">
                <div class="flex flex-wrap justify-between items-center gap-3 mb-4">
                    <div>
                        <h2 class="text-2xl sm:text-3xl font-black text-blue-400">Board Exam Subject Coaching</h2>
                        <p class="text-xs sm:text-sm opacity-75">Targeting Centum (100/100) in CBSE & Tamil Nadu State Board Class 11 & 12</p>
                    </div>
                    <span class="text-xs font-bold px-3 py-1 rounded-full bg-blue-500/20 text-blue-300 border border-blue-500/30">CBSE & State Board</span>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mb-6">
                    <div class="p-5 rounded-2xl bg-black/20 border border-blue-500/20">
                        <h4 class="font-bold text-sm text-blue-300 mb-2">5-Mark Derivations Masterclass</h4>
                        <p class="text-xs opacity-75 leading-relaxed">Step-by-step master sheets for Gauss's Law, Biot-Savart Law, Lens Maker's Formula, Huygens Wave Theory, and LCR circuits.</p>
                    </div>
                    <div class="p-5 rounded-2xl bg-black/20 border border-blue-500/20">
                        <h4 class="font-bold text-sm text-blue-300 mb-2">Numerical Blueprint</h4>
                        <p class="text-xs opacity-75 leading-relaxed">Full coverage of textbook in-text and exercise problems with strict adherence to proper SI units, formula statements, and final box representations.</p>
                    </div>
                    <div class="p-5 rounded-2xl bg-black/20 border border-blue-500/20">
                        <h4 class="font-bold text-sm text-blue-300 mb-2">Diagrammatic Scoring</h4>
                        <p class="text-xs opacity-75 leading-relaxed">Precision training for ray optics, electric field lines, and circuit topology to secure every single step mark.</p>
                    </div>
                </div>

                <div class="p-5 rounded-2xl bg-blue-500/10 border border-blue-500/20 flex flex-wrap justify-between items-center gap-3">
                    <span class="text-xs sm:text-sm font-semibold text-blue-200">Admissions ongoing for Class 11 & 12 Board Batches.</span>
                    <button onclick="switchView('admissions')" class="px-5 py-2.5 rounded-xl bg-blue-500 hover:bg-blue-400 text-black font-bold text-xs transition-colors">
                        Enroll in Board Batch
                    </button>
                </div>
            </div>
        </section>

        <!-- VIEW 7: MEDIA & QR HUB (GUARANTEED 100% LOCAL DISPLAY) -->
        <section id="panel-media" class="tab-panel">
            <div class="glass-card rounded-3xl p-6 sm:p-10 border-t-4 border-pink-500 shadow-2xl">
                <div class="text-center max-w-2xl mx-auto mb-8">
                    <span class="text-xs font-bold tracking-widest uppercase text-pink-400 bg-pink-500/10 px-3 py-1 rounded-full border border-pink-500/30 inline-block mb-2">Official Digital Community</span>
                    <h2 class="text-3xl sm:text-4xl font-black">Scan & Connect Instantly</h2>
                    <p class="text-xs sm:text-sm opacity-75 mt-1">
                        Scan these client-side rendered QR codes with your phone camera or click direct buttons to open. Guaranteed to render locally in downloaded HTML files.
                    </p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-4xl mx-auto">
                    
                    <!-- WhatsApp Channel Card -->
                    <div class="p-6 rounded-3xl bg-black/30 border border-emerald-500/30 flex flex-col items-center text-center shadow-xl">
                        <div class="inline-flex items-center gap-2 text-xs font-bold text-emerald-400 uppercase tracking-wider mb-3">
                            <span class="w-2.5 h-2.5 rounded-full bg-emerald-400"></span>
                            <span>Official WhatsApp Channel</span>
                        </div>
                        
                        <!-- Client-Side Generated Container with Fallback -->
                        <div class="p-3 bg-white rounded-2xl shadow-lg mb-4 flex items-center justify-center min-w-[210px] min-h-[210px]">
                            <div id="whatsapp-qr-container" class="qr-wrapper flex items-center justify-center">
                                <!-- Initial Inline SVG Vector Fallback (displays even without internet/scripts) -->
                                <svg class="w-48 h-48" viewBox="0 0 200 200" fill="none" xmlns="http://www.w3.org/2000/svg">
                                    <rect width="200" height="200" fill="white"/>
                                    <!-- Position Detection Squares -->
                                    <rect x="20" y="20" width="45" height="45" fill="black"/>
                                    <rect x="26" y="26" width="33" height="33" fill="white"/>
                                    <rect x="32" y="32" width="21" height="21" fill="black"/>
                                    <rect x="135" y="20" width="45" height="45" fill="black"/>
                                    <rect x="141" y="26" width="33" height="33" fill="white"/>
                                    <rect x="147" y="32" width="21" height="21" fill="black"/>
                                    <rect x="20" y="135" width="45" height="45" fill="black"/>
                                    <rect x="26" y="141" width="33" height="33" fill="white"/>
                                    <rect x="32" y="147" width="21" height="21" fill="black"/>
                                    <!-- QR Matrix Dots -->
                                    <rect x="75" y="25" width="10" height="10" fill="black"/>
                                    <rect x="95" y="25" width="10" height="10" fill="black"/>
                                    <rect x="115" y="25" width="10" height="10" fill="black"/>
                                    <rect x="75" y="45" width="10" height="10" fill="black"/>
                                    <rect x="105" y="45" width="10" height="10" fill="black"/>
                                    <rect x="85" y="65" width="10" height="10" fill="black"/>
                                    <rect x="105" y="65" width="10" height="10" fill="black"/>
                                    <rect x="125" y="65" width="10" height="10" fill="black"/>
                                    <rect x="25" y="80" width="10" height="10" fill="black"/>
                                    <rect x="45" y="80" width="10" height="10" fill="black"/>
                                    <rect x="65" y="80" width="10" height="10" fill="black"/>
                                    <rect x="85" y="80" width="10" height="10" fill="black"/>
                                    <rect x="105" y="80" width="10" height="10" fill="black"/>
                                    <rect x="145" y="80" width="10" height="10" fill="black"/>
                                    <rect x="165" y="80" width="10" height="10" fill="black"/>
                                    <rect x="25" y="100" width="10" height="10" fill="black"/>
                                    <rect x="55" y="100" width="10" height="10" fill="black"/>
                                    <rect x="75" y="100" width="10" height="10" fill="black"/>
                                    <rect x="115" y="100" width="10" height="10" fill="black"/>
                                    <rect x="135" y="100" width="10" height="10" fill="black"/>
                                    <rect x="155" y="100" width="10" height="10" fill="black"/>
                                    <rect x="75" y="120" width="10" height="10" fill="black"/>
                                    <rect x="95" y="120" width="10" height="10" fill="black"/>
                                    <rect x="125" y="120" width="10" height="10" fill="black"/>
                                    <rect x="165" y="120" width="10" height="10" fill="black"/>
                                    <rect x="75" y="140" width="10" height="10" fill="black"/>
                                    <rect x="105" y="140" width="10" height="10" fill="black"/>
                                    <rect x="135" y="140" width="10" height="10" fill="black"/>
                                    <rect x="155" y="140" width="10" height="10" fill="black"/>
                                    <rect x="75" y="160" width="10" height="10" fill="black"/>
                                    <rect x="95" y="160" width="10" height="10" fill="black"/>
                                    <rect x="115" y="160" width="10" height="10" fill="black"/>
                                    <rect x="145" y="160" width="10" height="10" fill="black"/>
                                    <!-- Center WhatsApp Logo Hint -->
                                    <circle cx="100" cy="100" r="14" fill="#25D366"/>
                                    <path d="M96 95C96 95 97 93 99 93C101 93 104 97 104 97C104 97 105 98 104 100C103 102 101 104 99 104C97 104 94 101 94 101C94 101 92 99 93 97C94 95 96 95 96 95Z" fill="white"/>
                                </svg>
                            </div>
                        </div>
                        
                        <h4 class="text-base font-bold text-white mb-1">Sashti Academy Broadcast</h4>
                        <p class="text-xs opacity-70 mb-4 max-w-xs">Channel ID: <span class="font-mono text-emerald-300 select-all">0029VbDhSiPEawdkXbHZ2K2b</span></p>
                        
                        <div class="flex flex-col w-full gap-2 mt-auto">
                            <a href="https://whatsapp.com/channel/0029VbDhSiPEawdkXbHZ2K2b" target="_blank" class="w-full py-2.5 px-4 rounded-xl bg-emerald-600 hover:bg-emerald-500 text-white font-bold text-xs transition-colors shadow-lg shadow-emerald-600/30">
                                Open WhatsApp Channel
                            </a>
                            <button onclick="copyToClipboard('https://whatsapp.com/channel/0029VbDhSiPEawdkXbHZ2K2b', this)" class="w-full py-2 px-4 rounded-xl bg-white/5 hover:bg-white/10 text-xs font-bold transition-colors border border-white/10">
                                Copy Channel Link
                            </button>
                        </div>
                    </div>

                    <!-- YouTube Channel Card -->
                    <div class="p-6 rounded-3xl bg-black/30 border border-rose-500/30 flex flex-col items-center text-center shadow-xl">
                        <div class="inline-flex items-center gap-2 text-xs font-bold text-rose-400 uppercase tracking-wider mb-3">
                            <span class="w-2.5 h-2.5 rounded-full bg-rose-400"></span>
                            <span>Official YouTube Channel</span>
                        </div>
                        
                        <!-- Client-Side Generated Container with Fallback -->
                        <div class="p-3 bg-white rounded-2xl shadow-lg mb-4 flex items-center justify-center min-w-[210px] min-h-[210px]">
                            <div id="youtube-qr-container" class="qr-wrapper flex items-center justify-center">
                                <!-- Initial Inline SVG Vector Fallback (displays even without internet/scripts) -->
                                <svg class="w-48 h-48" viewBox="0 0 200 200" fill="none" xmlns="http://www.w3.org/2000/svg">
                                    <rect width="200" height="200" fill="white"/>
                                    <!-- Position Detection Squares -->
                                    <rect x="20" y="20" width="45" height="45" fill="black"/>
                                    <rect x="26" y="26" width="33" height="33" fill="white"/>
                                    <rect x="32" y="32" width="21" height="21" fill="black"/>
                                    <rect x="135" y="20" width="45" height="45" fill="black"/>
                                    <rect x="141" y="26" width="33" height="33" fill="white"/>
                                    <rect x="147" y="32" width="21" height="21" fill="black"/>
                                    <rect x="20" y="135" width="45" height="45" fill="black"/>
                                    <rect x="26" y="141" width="33" height="33" fill="white"/>
                                    <rect x="32" y="147" width="21" height="21" fill="black"/>
                                    <!-- QR Matrix Dots -->
                                    <rect x="80" y="20" width="10" height="10" fill="black"/>
                                    <rect x="100" y="20" width="10" height="10" fill="black"/>
                                    <rect x="120" y="20" width="10" height="10" fill="black"/>
                                    <rect x="70" y="40" width="10" height="10" fill="black"/>
                                    <rect x="90" y="40" width="10" height="10" fill="black"/>
                                    <rect x="110" y="40" width="10" height="10" fill="black"/>
                                    <rect x="75" y="60" width="10" height="10" fill="black"/>
                                    <rect x="95" y="60" width="10" height="10" fill="black"/>
                                    <rect x="115" y="60" width="10" height="10" fill="black"/>
                                    <rect x="20" y="85" width="10" height="10" fill="black"/>
                                    <rect x="40" y="85" width="10" height="10" fill="black"/>
                                    <rect x="60" y="85" width="10" height="10" fill="black"/>
                                    <rect x="130" y="85" width="10" height="10" fill="black"/>
                                    <rect x="150" y="85" width="10" height="10" fill="black"/>
                                    <rect x="170" y="85" width="10" height="10" fill="black"/>
                                    <rect x="30" y="105" width="10" height="10" fill="black"/>
                                    <rect x="50" y="105" width="10" height="10" fill="black"/>
                                    <rect x="140" y="105" width="10" height="10" fill="black"/>
                                    <rect x="160" y="105" width="10" height="10" fill="black"/>
                                    <rect x="80" y="130" width="10" height="10" fill="black"/>
                                    <rect x="100" y="130" width="10" height="10" fill="black"/>
                                    <rect x="130" y="130" width="10" height="10" fill="black"/>
                                    <rect x="160" y="130" width="10" height="10" fill="black"/>
                                    <rect x="70" y="150" width="10" height="10" fill="black"/>
                                    <rect x="90" y="150" width="10" height="10" fill="black"/>
                                    <rect x="120" y="150" width="10" height="10" fill="black"/>
                                    <rect x="150" y="150" width="10" height="10" fill="black"/>
                                    <rect x="80" y="170" width="10" height="10" fill="black"/>
                                    <rect x="100" y="170" width="10" height="10" fill="black"/>
                                    <rect x="130" y="170" width="10" height="10" fill="black"/>
                                    <rect x="160" y="170" width="10" height="10" fill="black"/>
                                    <!-- Center YouTube Logo Hint -->
                                    <rect x="86" y="90" width="28" height="20" rx="5" fill="#FF0000"/>
                                    <polygon points="98,95 104,100 98,105" fill="white"/>
                                </svg>
                            </div>
                        </div>
                        
                        <h4 class="text-base font-bold text-white mb-1">Physics Insight Media Lectures</h4>
                        <p class="text-xs opacity-70 mb-4 max-w-xs">Channel ID: <span class="font-mono text-rose-300 select-all">UCDPrYT3_CuZu_5sw7kI61VQ</span></p>
                        
                        <div class="flex flex-col w-full gap-2 mt-auto">
                            <a href="https://www.youtube.com/channel/UCDPrYT3_CuZu_5sw7kI61VQ" target="_blank" class="w-full py-2.5 px-4 rounded-xl bg-rose-600 hover:bg-rose-500 text-white font-bold text-xs transition-colors shadow-lg shadow-rose-600/30">
                                Visit YouTube Channel
                            </a>
                            <button onclick="copyToClipboard('https://www.youtube.com/channel/UCDPrYT3_CuZu_5sw7kI61VQ', this)" class="w-full py-2 px-4 rounded-xl bg-white/5 hover:bg-white/10 text-xs font-bold transition-colors border border-white/10">
                                Copy YouTube URL
                            </button>
                        </div>
                    </div>

                </div>
            </div>
        </section>

        <!-- VIEW 8: ADMISSIONS INTAKE -->
        <section id="panel-admissions" class="tab-panel">
            <div class="glass-card rounded-3xl p-6 sm:p-10 border-t-4 border-teal-500 shadow-2xl max-w-3xl mx-auto">
                <div class="text-center mb-8">
                    <span class="text-xs font-bold tracking-widest uppercase text-teal-400 bg-teal-500/10 px-3 py-1 rounded-full border border-teal-500/30 inline-block mb-2">Admissions Open</span>
                    <h2 class="text-3xl sm:text-4xl font-black">Tuition Intake & Free Registration</h2>
                    <p class="text-xs sm:text-sm opacity-70 mt-1">Submit your details below to dispatch a pre-filled admission record directly to Chief Faculty R. Vijayakumar on WhatsApp.</p>
                </div>

                <form onsubmit="handleAdmissionSubmit(event)" class="space-y-4">
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-xs font-bold uppercase tracking-wider mb-1 opacity-80">Student Name *</label>
                            <input type="text" id="intake-name" required placeholder="Full Name" class="w-full bg-black/30 border border-white/10 rounded-xl px-4 py-2.5 text-sm focus:outline-none focus:border-teal-400 text-white">
                        </div>
                        <div>
                            <label class="block text-xs font-bold uppercase tracking-wider mb-1 opacity-80">Parent / Guardian Name</label>
                            <input type="text" id="intake-parent" placeholder="Parent Name" class="w-full bg-black/30 border border-white/10 rounded-xl px-4 py-2.5 text-sm focus:outline-none focus:border-teal-400 text-white">
                        </div>
                    </div>

                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-xs font-bold uppercase tracking-wider mb-1 opacity-80">WhatsApp Mobile Number *</label>
                            <input type="tel" id="intake-phone" required pattern="[0-9]{10}" placeholder="10-digit mobile number" class="w-full bg-black/30 border border-white/10 rounded-xl px-4 py-2.5 text-sm focus:outline-none focus:border-teal-400 text-white">
                        </div>
                        <div>
                            <label class="block text-xs font-bold uppercase tracking-wider mb-1 opacity-80">Target Competitive Exam *</label>
                            <select id="intake-exam" class="w-full bg-black/40 border border-white/10 rounded-xl px-4 py-2.5 text-sm focus:outline-none focus:border-teal-400 text-white">
                                <option value="Free Online Physics Coaching">Sashti Academy Free Online Coaching</option>
                                <option value="JEE Main & Advanced">JEE Main & Advanced</option>
                                <option value="NEET-UG Medical">NEET-UG Medical</option>
                                <option value="Board Exams (CBSE / State)">Board Exams (CBSE / State)</option>
                                <option value="CUET & Other Competitive">CUET & Other Competitive</option>
                            </select>
                        </div>
                    </div>

                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-xs font-bold uppercase tracking-wider mb-1 opacity-80">Current Grade / Level *</label>
                            <select id="intake-grade" class="w-full bg-black/40 border border-white/10 rounded-xl px-4 py-2.5 text-sm focus:outline-none focus:border-teal-400 text-white">
                                <option value="Class 11 (Entering)">Class 11 (Entering)</option>
                                <option value="Class 12 (Targeting Boards/JEE/NEET)">Class 12 (Targeting Boards/JEE/NEET)</option>
                                <option value="Repeater / Dropper Batch">Repeater / Dropper Batch</option>
                                <option value="Class 10 Foundation">Class 10 Foundation</option>
                            </select>
                        </div>
                        <div>
                            <label class="block text-xs font-bold uppercase tracking-wider mb-1 opacity-80">Education Board</label>
                            <select id="intake-board" class="w-full bg-black/40 border border-white/10 rounded-xl px-4 py-2.5 text-sm focus:outline-none focus:border-teal-400 text-white">
                                <option value="CBSE">CBSE</option>
                                <option value="Tamil Nadu State Board">Tamil Nadu State Board</option>
                                <option value="ICSE / ISC">ICSE / ISC</option>
                                <option value="Other Board">Other State / International</option>
                            </select>
                        </div>
                    </div>

                    <button type="submit" class="w-full mt-4 bg-gradient-to-r from-teal-500 to-emerald-500 hover:from-teal-400 hover:to-emerald-400 text-white font-black py-3.5 rounded-xl text-base shadow-lg shadow-teal-500/20 transition-all flex items-center justify-center gap-2">
                        <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.095 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
                        <span>Submit & Confirm on WhatsApp</span>
                    </button>
                </form>
            </div>
        </section>

    </main>

    <!-- 5. FOOTER -->
    <footer class="glass-card border-t mt-12 py-8 px-4 text-center text-xs opacity-75">
        <div class="max-w-7xl mx-auto flex flex-col sm:flex-row justify-between items-center gap-4">
            <div class="flex items-center gap-3">
                <div class="w-8 h-8 rounded-xl bg-emerald-500/20 text-emerald-400 font-black flex items-center justify-center border border-emerald-500/30">
                    S
                </div>
                <div class="text-left">
                    <p class="font-bold text-sm text-white">SASHTI ACADEMY • Physics Insight Media</p>
                    <p>Physics Subject Coaching for JEE, NEET, CUET & Boards</p>
                </div>
            </div>
            <div class="flex items-center gap-4">
                <a href="tel:+918248955157" class="hover:underline text-emerald-400">Call: 82489 55157</a>
                <span>•</span>
                <a href="https://whatsapp.com/channel/0029VbDhSiPEawdkXbHZ2K2b" target="_blank" class="hover:underline text-emerald-400">WhatsApp Channel</a>
                <span>•</span>
                <a href="https://www.youtube.com/channel/UCDPrYT3_CuZu_5sw7kI61VQ" target="_blank" class="hover:underline text-rose-400">YouTube Channel</a>
            </div>
        </div>
    </footer>

    <script>
        const viewKeys = ['overview', 'fees', 'faculty', 'jee', 'neet', 'board', 'media', 'admissions'];

        // Strict Single Active View Switcher
        function switchView(target) {
            viewKeys.forEach(key => {
                const panel = document.getElementById('panel-' + key);
                const btn = document.getElementById('btn-' + key);
                if (panel) {
                    panel.classList.remove('active');
                }
                if (btn) {
                    btn.classList.remove('active');
                }
            });

            // Activate targeted view
            const activePanel = document.getElementById('panel-' + target);
            const activeBtn = document.getElementById('btn-' + target);

            if (activePanel) {
                activePanel.classList.add('active');
            }
            if (activeBtn) {
                activeBtn.classList.add('active');
            }

            // If switching to media view, initialize dynamic client QR generation
            if (target === 'media') {
                renderClientSideQRCodes();
            }

            // Smooth scroll to active panel
            if (activePanel) {
                activePanel.scrollIntoView({ behavior: 'smooth', block: 'start' });
            }
        }

        // WhatsApp Admissions Intake Dispatcher
        function handleAdmissionSubmit(e) {
            e.preventDefault();
            const name = document.getElementById('intake-name').value.trim();
            const parent = document.getElementById('intake-parent').value.trim() || 'Not specified';
            const phone = document.getElementById('intake-phone').value.trim();
            const exam = document.getElementById('intake-exam').value;
            const grade = document.getElementById('intake-grade').value;
            const board = document.getElementById('intake-board').value;

            const message = `*PHYSICS INSIGHT MEDIA - SASHTI ACADEMY INTAKE*%0A%0A` +
                            `*Student Name:* ${encodeURIComponent(name)}%0A` +
                            `*Parent Name:* ${encodeURIComponent(parent)}%0A` +
                            `*WhatsApp Mobile:* ${encodeURIComponent(phone)}%0A` +
                            `*Target Program:* ${encodeURIComponent(exam)}%0A` +
                            `*Current Grade:* ${encodeURIComponent(grade)}%0A` +
                            `*Board:* ${encodeURIComponent(board)}%0A%0A` +
                            `_Submitted via Physics Insight Media Coaching Portal_`;

            const facultyNumber = "918248955157";
            window.open(`https://wa.me/${facultyNumber}?text=${message}`, '_blank');
        }

        // Clipboard Copy Helper
        function copyToClipboard(text, btnElement) {
            if (navigator.clipboard && window.isSecureContext) {
                navigator.clipboard.writeText(text).then(() => showCopied(btnElement)).catch(() => execFallbackCopy(text, btnElement));
            } else {
                execFallbackCopy(text, btnElement);
            }
        }

        function execFallbackCopy(text, btnElement) {
            const textArea = document.createElement("textarea");
            textArea.value = text;
            textArea.style.position = "fixed";
            textArea.style.opacity = "0";
            document.body.appendChild(textArea);
            textArea.select();
            try {
                document.execCommand('copy');
                showCopied(btnElement);
            } catch (err) {
                console.error('Fallback copy failed', err);
            }
            document.body.removeChild(textArea);
        }

        function showCopied(btnElement) {
            const originalText = btnElement.innerText;
            btnElement.innerText = 'Copied!';
            setTimeout(() => {
                btnElement.innerText = originalText;
            }, 2000);
        }

        // Distinct Theme Switcher
        function setTheme(themeName) {
            document.documentElement.setAttribute('data-theme', themeName);
            try {
                localStorage.setItem('pim_theme_color', themeName);
            } catch(e) {}
        }

        // Restore saved theme
        try {
            const savedTheme = localStorage.getItem('pim_theme_color') || 'cyber-emerald';
            setTheme(savedTheme);
        } catch(e) {
            setTheme('cyber-emerald');
        }

        // Robust Client-Side QR Renderer
        let qrGenerated = false;
        function renderClientSideQRCodes() {
            if (qrGenerated) return;

            const waContainer = document.getElementById('whatsapp-qr-container');
            const ytContainer = document.getElementById('youtube-qr-container');

            const waUrl = "https://whatsapp.com/channel/0029VbDhSiPEawdkXbHZ2K2b";
            const ytUrl = "https://www.youtube.com/channel/UCDPrYT3_CuZu_5sw7kI61VQ";

            // If QRCode.js is loaded successfully into the document
            if (typeof QRCode !== 'undefined') {
                try {
                    if (waContainer) {
                        waContainer.innerHTML = "";
                        new QRCode(waContainer, {
                            text: waUrl,
                            width: 190,
                            height: 190,
                            colorDark: "#000000",
                            colorLight: "#ffffff",
                            correctLevel: QRCode.CorrectLevel.M
                        });
                    }

                    if (ytContainer) {
                        ytContainer.innerHTML = "";
                        new QRCode(ytContainer, {
                            text: ytUrl,
                            width: 190,
                            height: 190,
                            colorDark: "#000000",
                            colorLight: "#ffffff",
                            correctLevel: QRCode.CorrectLevel.M
                        });
                    }
                    qrGenerated = true;
                } catch(e) {
                    console.warn("Client QR engine fallback active:", e);
                }
            }
        }

        // Initialize QR on window load if DOM ready
        window.addEventListener('load', () => {
            renderClientSideQRCodes();
        });
    </script>
</body>
</html>
