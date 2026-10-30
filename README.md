<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DANIELWEALTH | Modern Wealth & Private Banking</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=Playfair+Display:ital,wght@0,600;0,700;1,400&display=swap" rel="stylesheet">
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        navy: {
                            800: '#0B132B',
                            900: '#0B1120',
                            950: '#050811',
                        },
                        gold: {
                            400: '#F3C663',
                            500: '#D4AF37',
                            600: '#AA820A',
                        },
                        tealAccent: '#00E5FF'
                    },
                    fontFamily: {
                        sans: ['"Plus Jakarta Sans"', 'sans-serif'],
                        serif: ['"Playfair Display"', 'serif'],
                    }
                }
            }
        }
    </script>
    <style>
        .glass-panel {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.08);
        }
        .glass-card {
            background: linear-gradient(135deg, rgba(255, 255, 255, 0.07) 0%, rgba(255, 255, 255, 0.02) 100%);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(212, 175, 55, 0.2);
        }
        .gold-gradient-text {
            background: linear-gradient(135deg, #FFF099 0%, #D4AF37 50%, #997A15 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .gold-button-gradient {
            background: linear-gradient(135deg, #E6C251 0%, #C49D28 100%);
        }
        .gold-button-gradient:hover {
            background: linear-gradient(135deg, #F0CE62 0%, #D4AF37 100%);
        }
    </style>
</head>
<body class="bg-navy-950 text-slate-100 font-sans antialiased overflow-x-hidden selection:bg-gold-500 selection:text-navy-950">

    <!-- Fictional Disclaimer Banner -->
    <div class="bg-gradient-to-r from-amber-600 via-gold-500 to-amber-600 text-navy-950 text-xs sm:text-sm font-semibold py-2 px-4 text-center sticky top-0 z-50 shadow-md">
        <div class="max-w-7xl mx-auto flex items-center justify-center gap-2">
            <i data-lucide="alert-triangle" class="w-4 h-4 flex-shrink-0"></i>
            <span>DEMONSTRATION ONLY: DANIELWEALTH is a fictional bank conceptual mockup created for preview purposes.</span>
        </div>
    </div>

    <!-- Navigation Header -->
    <header class="sticky top-[33px] z-40 bg-navy-950/80 backdrop-blur-md border-b border-slate-800/60 transition-all">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            <!-- Brand Logo -->
            <a href="#" class="flex items-center gap-3 group">
                <div class="w-10 h-10 rounded-xl bg-gradient-to-br from-gold-400 to-gold-600 flex items-center justify-center text-navy-950 font-bold text-xl shadow-lg shadow-gold-500/10 group-hover:scale-105 transition-transform">
                    DW
                </div>
                <div class="flex flex-col">
                    <span class="font-bold text-xl tracking-wider text-white font-serif">DANIEL<span class="gold-gradient-text">WEALTH</span></span>
                    <span class="text-[9px] tracking-[0.2em] text-slate-400 uppercase -mt-1">Private Banking</span>
                </div>
            </a>

            <!-- Desktop Nav Links -->
            <nav class="hidden md:flex items-center space-x-8 text-sm font-medium text-slate-300">
                <a href="#wealth" class="hover:text-gold-400 transition-colors">Private Wealth</a>
                <a href="#solutions" class="hover:text-gold-400 transition-colors">Smart Solutions</a>
                <a href="#dashboard" class="hover:text-gold-400 transition-colors">Digital Platform</a>
                <a href="#security" class="hover:text-gold-400 transition-colors">Security</a>
            </nav>

            <!-- Header Action Buttons -->
            <div class="hidden md:flex items-center gap-4">
                <button onclick="toggleModal('login-modal')" class="text-sm font-semibold text-slate-200 hover:text-gold-400 px-4 py-2 rounded-lg transition-colors flex items-center gap-2">
                    <i data-lucide="lock" class="w-4 h-4"></i> Secure Login
                </button>
                <a href="#dashboard" class="gold-button-gradient text-navy-950 font-bold text-sm px-5 py-2.5 rounded-lg shadow-lg shadow-gold-500/20 hover:shadow-gold-500/30 transition-all transform hover:-translate-y-0.5">
                    Become a Client
                </a>
            </div>

            <!-- Mobile Menu Button -->
            <button id="menu-btn" class="md:hidden text-slate-300 hover:text-white p-2" aria-label="Toggle Navigation">
                <i data-lucide="menu" class="w-6 h-6"></i>
            </button>
        </div>

        <!-- Mobile Navigation Drawer -->
        <div id="mobile-menu" class="hidden md:hidden bg-navy-900 border-b border-slate-800 px-6 py-6 space-y-4">
            <a href="#wealth" class="block text-slate-200 hover:text-gold-400 py-2">Private Wealth</a>
            <a href="#solutions" class="block text-slate-200 hover:text-gold-400 py-2">Smart Solutions</a>
            <a href="#dashboard" class="block text-slate-200 hover:text-gold-400 py-2">Digital Platform</a>
            <a href="#security" class="block text-slate-200 hover:text-gold-400 py-2">Security</a>
            <div class="pt-4 border-t border-slate-800 flex flex-col gap-3">
                <button onclick="toggleModal('login-modal')" class="w-full text-center text-slate-200 font-semibold py-2.5 border border-slate-700 rounded-lg">
                    Client Login
                </button>
                <a href="#dashboard" class="w-full text-center gold-button-gradient text-navy-950 font-bold py-2.5 rounded-lg">
                    Open an Account
                </a>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="relative pt-12 pb-24 lg:pt-20 lg:pb-32 overflow-hidden">
        <!-- Background Glows -->
        <div class="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[600px] h-[600px] bg-gold-500/10 rounded-full blur-[140px] pointer-events-none"></div>
        <div class="absolute top-1/3 right-10 w-[400px] h-[400px] bg-teal-500/10 rounded-full blur-[120px] pointer-events-none"></div>

        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="grid lg:grid-cols-12 gap-12 lg:gap-8 items-center">
                <!-- Hero Left Column -->
                <div class="lg:col-span-7 space-y-8 text-center lg:text-left">
                    <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full bg-slate-900/80 border border-gold-500/30 text-gold-400 text-xs font-semibold tracking-wide">
                        <span class="w-2 h-2 rounded-full bg-gold-400 animate-pulse"></span>
                        Next-Generation Private Banking
                    </div>
                    
                    <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold tracking-tight text-white leading-[1.15] font-serif">
                        Architecting Your <br class="hidden sm:inline">
                        <span class="gold-gradient-text">Financial Legacy</span>
                    </h1>

                    <p class="text-slate-400 text-base sm:text-lg max-w-2xl mx-auto lg:mx-0 leading-relaxed">
                        Experience bespoke wealth management, intelligent automated portfolios, and premier global banking services tailored exclusively for high-net-worth individuals and visionaries.
                    </p>

                    <!-- Hero Call to Actions -->
                    <div class="flex flex-col sm:flex-row items-center justify-center lg:justify-start gap-4 pt-2">
                        <a href="#dashboard" class="w-full sm:w-auto gold-button-gradient text-navy-950 font-bold px-8 py-4 rounded-xl shadow-xl shadow-gold-500/20 hover:shadow-gold-500/30 transition-all flex items-center justify-center gap-2 text-base">
                            Explore Client Platform <i data-lucide="arrow-right" class="w-5 h-5"></i>
                        </a>
                        <button onclick="toggleModal('login-modal')" class="w-full sm:w-auto glass-panel text-slate-200 hover:text-white hover:bg-white/10 px-8 py-4 rounded-xl font-semibold transition-all flex items-center justify-center gap-2 text-base border border-slate-700/60">
                            Access Portal
                        </button>
                    </div>

                    <!-- Trust Stats -->
                    <div class="pt-8 grid grid-cols-3 gap-6 border-t border-slate-800/80 max-w-xl mx-auto lg:mx-0">
                        <div>
                            <div class="text-2xl sm:text-3xl font-bold text-white font-serif">$24B+</div>
                            <div class="text-xs text-slate-400 mt-1">Assets Managed</div>
                        </div>
                        <div>
                            <div class="text-2xl sm:text-3xl font-bold text-white font-serif">99.99%</div>
                            <div class="text-xs text-slate-400 mt-1">Platform Uptime</div>
                        </div>
                        <div>
                            <div class="text-2xl sm:text-3xl font-bold text-white font-serif">140+</div>
                            <div class="text-xs text-slate-400 mt-1">Global Markets</div>
                        </div>
                    </div>
                </div>

                <!-- Hero Right Column: Card Showcase Graphic -->
                <div class="lg:col-span-5 relative flex justify-center">
                    <div class="relative w-full max-w-md">
                        <!-- Premium Metal Card Mockup -->
                        <div class="w-full h-56 sm:h-64 rounded-2xl glass-card p-6 flex flex-col justify-between shadow-2xl relative z-20 border border-gold-500/30 transform hover:rotate-1 transition-transform duration-500">
                            <div class="flex justify-between items-start">
                                <div>
                                    <span class="text-xs text-gold-400 font-semibold tracking-widest uppercase">BLACK EDITION</span>
                                    <h3 class="text-xl font-bold text-white font-serif tracking-wide mt-1">DANIELWEALTH</h3>
                                </div>
                                <i data-lucide="wifi" class="w-6 h-6 text-slate-400 rotate-90"></i>
                            </div>

                            <div class="my-auto pt-4">
                                <div class="w-12 h-9 bg-gradient-to-r from-amber-200 to-yellow-400 rounded-md opacity-90 shadow-inner flex items-center justify-center">
                                    <div class="w-8 h-6 border border-navy-950/40 rounded-sm"></div>
                                </div>
                            </div>

                            <div>
                                <div class="font-mono text-lg sm:text-xl tracking-widest text-slate-200 mb-2">
                                    •••• •••• •••• 8892
                                </div>
                                <div class="flex justify-between items-end text-xs text-slate-400">
                                    <div>
                                        <div class="text-[9px] uppercase tracking-wider text-slate-500">Card Holder</div>
                                        <div class="font-semibold text-slate-200">DANIEL V. ARCHER</div>
                                    </div>
                                    <div>
                                        <div class="text-[9px] uppercase tracking-wider text-slate-500">Expires</div>
                                        <div class="font-semibold text-slate-200">12/28</div>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <!-- Secondary Glass Card behind -->
                        <div class="absolute -bottom-8 -right-4 sm:-right-6 w-full h-56 bg-slate-900/90 rounded-2xl p-6 border border-slate-800 shadow-xl z-10 hidden sm:flex flex-col justify-between backdrop-blur-md">
                            <div class="flex justify-between items-center text-xs text-slate-400 border-b border-slate-800 pb-3">
                                <span class="flex items-center gap-2"><span class="w-2 h-2 rounded-full bg-emerald-400"></span> Live Portfolio Index</span>
                                <span class="text-emerald-400 font-semibold">+14.2% YTD</span>
                            </div>
                            <div class="space-y-2 my-2">
                                <div class="flex justify-between text-sm">
                                    <span class="text-slate-300">Global Tech Equity</span>
                                    <span class="font-semibold text-white">$1,420,500</span>
                                </div>
                                <div class="w-full bg-slate-800 h-1.5 rounded-full overflow-hidden">
                                    <div class="bg-gold-500 h-full w-[75%] rounded-full"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Key Features Section -->
    <section id="solutions" class="py-20 bg-navy-900/50 border-y border-slate-800/80 relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <h2 class="text-xs uppercase tracking-[0.2em] font-bold text-gold-400 mb-3">Superior Banking Capabilities</h2>
                <p class="text-3xl sm:text-4xl font-bold text-white font-serif">Engineered for Sophisticated Investors</p>
            </div>

            <div class="grid md:grid-cols-3 gap-8">
                <!-- Feature 1 -->
                <div class="glass-panel p-8 rounded-2xl border border-slate-800 hover:border-gold-500/40 transition-all group">
                    <div class="w-14 h-14 rounded-xl bg-gold-500/10 border border-gold-500/20 flex items-center justify-center text-gold-400 mb-6 group-hover:scale-110 transition-transform">
                        <i data-lucide="shield-check" class="w-7 h-7"></i>
                    </div>
                    <h3 class="text-xl font-bold text-white mb-3">Institutional Security</h3>
                    <p class="text-slate-400 text-sm leading-relaxed">
                        Multi-layer military grade encryption, biometric authentication, and end-to-end asset vaulting guarantee your wealth remains fortress-protected.
                    </p>
                </div>

                <!-- Feature 2 -->
                <div class="glass-panel p-8 rounded-2xl border border-slate-800 hover:border-gold-500/40 transition-all group">
                    <div class="w-14 h-14 rounded-xl bg-gold-500/10 border border-gold-500/20 flex items-center justify-center text-gold-400 mb-6 group-hover:scale-110 transition-transform">
                        <i data-lucide="trending-up" class="w-7 h-7"></i>
                    </div>
                    <h3 class="text-xl font-bold text-white mb-3">AI Smart Portfolio</h3>
                    <p class="text-slate-400 text-sm leading-relaxed">
                        Algorithmic rebalancing and quantitative investment strategies optimized in real-time to align with your tailored risk profile and goals.
                    </p>
                </div>

                <!-- Feature 3 -->
                <div class="glass-panel p-8 rounded-2xl border border-slate-800 hover:border-gold-500/40 transition-all group">
                    <div class="w-14 h-14 rounded-xl bg-gold-500/10 border border-gold-500/20 flex items-center justify-center text-gold-400 mb-6 group-hover:scale-110 transition-transform">
                        <i data-lucide="headphone-off" class="w-7 h-7"></i>
                    </div>
                    <h3 class="text-xl font-bold text-white mb-3">Dedicated Concierge</h3>
                    <p class="text-slate-400 text-sm leading-relaxed">
                        Direct 24/7 access to your personal Private Wealth Advisor and concierge team. No queues, automated phone trees, or delays.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Interactive Dashboard Preview Section -->
    <section id="dashboard" class="py-24 relative overflow-hidden">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-12">
                <h2 class="text-xs uppercase tracking-[0.2em] font-bold text-gold-400 mb-3">Digital Control Center</h2>
                <p class="text-3xl sm:text-4xl font-bold text-white font-serif">Intuitive. Instant. Omnipresent.</p>
                <p class="text-slate-400 mt-4 text-sm">Interactive Preview — Explore the DANIELWEALTH client interface below.</p>
            </div>

            <!-- Mock Dashboard Frame -->
            <div class="glass-panel rounded-3xl border border-slate-800 overflow-hidden shadow-2xl bg-navy-900/80">
                <!-- Dashboard Top Navigation Bar -->
                <div class="bg-navy-950 px-6 py-4 border-b border-slate-800 flex flex-wrap items-center justify-between gap-4">
                    <div class="flex items-center gap-3">
                        <div class="w-3 h-3 rounded-full bg-red-500/80"></div>
                        <div class="w-3 h-3 rounded-full bg-yellow-500/80"></div>
                        <div class="w-3 h-3 rounded-full bg-green-500/80"></div>
                        <span class="text-xs text-slate-500 font-mono ml-2">portal.danielwealth.com/dashboard</span>
                    </div>
                    <div class="flex items-center gap-4 text-xs">
                        <span class="text-slate-400">Welcome, <strong class="text-white">Alexander Daniel</strong></span>
                        <div class="w-8 h-8 rounded-full bg-gold-500/20 text-gold-400 font-bold flex items-center justify-center border border-gold-500/40">
                            AD
                        </div>
                    </div>
                </div>

                <!-- Dashboard Content Area -->
                <div class="p-6 lg:p-8 space-y-8">
                    <!-- Top Balance Cards -->
                    <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-4">
                        <div class="bg-navy-950 p-5 rounded-xl border border-slate-800">
                            <span class="text-xs text-slate-400">Total Net Worth</span>
                            <div class="text-2xl font-bold text-white font-serif mt-1">$4,852,190.00</div>
                            <span class="text-xs text-emerald-400 flex items-center gap-1 mt-2">
                                <i data-lucide="arrow-up-right" class="w-3.5 h-3.5"></i> +2.4% this month
                            </span>
                        </div>
                        <div class="bg-navy-950 p-5 rounded-xl border border-slate-800">
                            <span class="text-xs text-slate-400">Liquid Savings</span>
                            <div class="text-2xl font-bold text-white font-serif mt-1">$1,120,400.50</div>
                            <span class="text-xs text-slate-400 mt-2 block">4.85% APY Yield</span>
                        </div>
                        <div class="bg-navy-950 p-5 rounded-xl border border-slate-800">
                            <span class="text-xs text-slate-400">Investment Portfolio</span>
                            <div class="text-2xl font-bold text-white font-serif mt-1">$3,481,789.50</div>
                            <span class="text-xs text-emerald-400 flex items-center gap-1 mt-2">
                                <i data-lucide="arrow-up-right" class="w-3.5 h-3.5"></i> +12.8% YTD
                            </span>
                        </div>
                        <div class="bg-navy-950 p-5 rounded-xl border border-slate-800">
                            <span class="text-xs text-slate-400">Credit Facility</span>
                            <div class="text-2xl font-bold text-white font-serif mt-1">$250,000.00</div>
                            <span class="text-xs text-slate-400 mt-2 block">Available Liquidity</span>
                        </div>
                    </div>

                    <!-- Main Grid: Transfers & Activity -->
                    <div class="grid lg:grid-cols-3 gap-8">
                        <!-- Quick Transfer Interactive Widget -->
                        <div class="bg-navy-950 p-6 rounded-2xl border border-slate-800 flex flex-col justify-between">
                            <div>
                                <h4 class="text-base font-bold text-white mb-4 flex items-center gap-2">
                                    <i data-lucide="send" class="w-4 h-4 text-gold-400"></i> Instant Wealth Transfer
                                </h4>
                                <form id="transfer-form" onsubmit="handleTransfer(event)" class="space-y-4">
                                    <div>
                                        <label class="block text-xs text-slate-400 mb-1">Recipient Account</label>
                                        <input type="text" required placeholder="DW-9082-XXXX" class="w-full bg-navy-900 border border-slate-700 rounded-lg px-3 py-2 text-sm text-white focus:outline-none focus:border-gold-500">
                                    </div>
                                    <div>
                                        <label class="block text-xs text-slate-400 mb-1">Amount ($)</label>
                                        <input type="number" required min="1" placeholder="50,000" class="w-full bg-navy-900 border border-slate-700 rounded-lg px-3 py-2 text-sm text-white focus:outline-none focus:border-gold-500">
                                    </div>
                                    <div>
                                        <label class="block text-xs text-slate-400 mb-1">Transfer Type</label>
                                        <select class="w-full bg-navy-900 border border-slate-700 rounded-lg px-3 py-2 text-sm text-white focus:outline-none focus:border-gold-500">
                                            <option>Wire Transfer (Domestic/Global)</option>
                                            <option>Internal Liquidity Move</option>
                                            <option>Vault Deposit</option>
                                        </select>
                                    </div>
                                    <button type="submit" class="w-full gold-button-gradient text-navy-950 font-bold py-2.5 rounded-lg text-sm transition-all mt-2">
                                        Authorize Transfer
                                    </button>
                                </form>
                                <div id="transfer-status" class="hidden mt-3 p-3 rounded-lg bg-emerald-500/10 border border-emerald-500/30 text-emerald-400 text-xs text-center">
                                    Transfer Request Encrypted & Sent Successfully!
                                </div>
                            </div>
                        </div>

                        <!-- Recent Transactions -->
                        <div class="lg:col-span-2 bg-navy-950 p-6 rounded-2xl border border-slate-800">
                            <div class="flex justify-between items-center mb-6">
                                <h4 class="text-base font-bold text-white flex items-center gap-2">
                                    <i data-lucide="activity" class="w-4 h-4 text-gold-400"></i> Recent Activity
                                </h4>
                                <button class="text-xs text-gold-400 hover:underline">View All</button>
                            </div>

                            <div class="space-y-4">
                                <div class="flex items-center justify-between p-3 rounded-lg hover:bg-slate-900/60 transition-colors border border-transparent hover:border-slate-800">
                                    <div class="flex items-center gap-3">
                                        <div class="w-10 h-10 rounded-lg bg-emerald-500/10 border border-emerald-500/20 text-emerald-400 flex items-center justify-center">
                                            <i data-lucide="arrow-down-left" class="w-5 h-5"></i>
                                        </div>
                                        <div>
                                            <div class="text-sm font-semibold text-white">Dividend Yield Credit</div>
                                            <div class="text-xs text-slate-500">Today, 09:42 AM • Global ETF Fund</div>
                                        </div>
                                    </div>
                                    <div class="text-right">
                                        <div class="text-sm font-bold text-emerald-400">+$14,250.00</div>
                                        <div class="text-[10px] text-slate-500">Completed</div>
                                    </div>
                                </div>

                                <div class="flex items-center justify-between p-3 rounded-lg hover:bg-slate-900/60 transition-colors border border-transparent hover:border-slate-800">
                                    <div class="flex items-center gap-3">
                                        <div class="w-10 h-10 rounded-lg bg-slate-800 text-slate-300 flex items-center justify-center">
                                            <i data-lucide="shopping-bag" class="w-5 h-5"></i>
                                        </div>
                                        <div>
                                            <div class="text-sm font-semibold text-white">Aviation Charter Services</div>
                                            <div class="text-xs text-slate-500">Yesterday • Card ending in 8892</div>
                                        </div>
                                    </div>
                                    <div class="text-right">
                                        <div class="text-sm font-bold text-white">-$18,400.00</div>
                                        <div class="text-[10px] text-slate-500">Cleared</div>
                                    </div>
                                </div>

                                <div class="flex items-center justify-between p-3 rounded-lg hover:bg-slate-900/60 transition-colors border border-transparent hover:border-slate-800">
                                    <div class="flex items-center gap-3">
                                        <div class="w-10 h-10 rounded-lg bg-gold-500/10 border border-gold-500/20 text-gold-400 flex items-center justify-center">
                                            <i data-lucide="refresh-cw" class="w-5 h-5"></i>
                                        </div>
                                        <div>
                                            <div class="text-sm font-semibold text-white">Automated Portfolio Rebalance</div>
                                            <div class="text-xs text-slate-500">Oct 28, 2026 • AI Wealth Engine</div>
                                        </div>
                                    </div>
                                    <div class="text-right">
                                        <div class="text-sm font-bold text-slate-300">$120,000.00</div>
                                        <div class="text-[10px] text-slate-500">Internal</div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Client Testimonial / Quote Section -->
    <section class="py-20 bg-navy-900/40 border-t border-slate-800">
        <div class="max-w-5xl mx-auto px-4 text-center">
            <i data-lucide="quote" class="w-12 h-12 text-gold-500/30 mx-auto mb-6"></i>
            <blockquote class="text-2xl sm:text-3xl font-serif text-slate-200 italic leading-relaxed">
                "DANIELWEALTH transformed how our family manages multi-generational assets. Their private digital platform matches the excellence of their personal advisors."
            </blockquote>
            <div class="mt-6 font-semibold text-gold-400">Elena Rostova</div>
            <div class="text-xs text-slate-500 uppercase tracking-widest mt-1">Managing Director, Rostova Global Capital</div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-navy-950 border-t border-slate-800/80 pt-16 pb-12 text-slate-400 text-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-2 md:grid-cols-5 gap-8 mb-12">
                <!-- Brand Column -->
                <div class="col-span-2">
                    <div class="flex items-center gap-3 mb-4">
                        <div class="w-8 h-8 rounded-lg bg-gold-500 flex items-center justify-center text-navy-950 font-bold text-lg">
                            DW
                        </div>
                        <span class="font-bold text-lg text-white font-serif">DANIEL<span class="gold-gradient-text">WEALTH</span></span>
                    </div>
                    <p class="text-xs text-slate-500 max-w-sm mb-4 leading-relaxed">
                        Redefining modern wealth stewardship. Providing secure, sophisticated, and seamless financial architecture to individuals and institutions worldwide.
                    </p>
                    <div class="text-xs text-slate-600">
                        © 2026 DANIELWEALTH Financial Inc. All rights reserved.
                    </div>
                </div>

                <!-- Navigation Columns -->
                <div>
                    <h5 class="text-white font-semibold mb-3 text-xs uppercase tracking-wider">Solutions</h5>
                    <ul class="space-y-2 text-xs">
                        <li><a href="#" class="hover:text-gold-400 transition-colors">Private Banking</a></li>
                        <li><a href="#" class="hover:text-gold-400 transition-colors">Wealth Planning</a></li>
                        <li><a href="#" class="hover:text-gold-400 transition-colors">Smart Investment</a></li>
                        <li><a href="#" class="hover:text-gold-400 transition-colors">Global Vaults</a></li>
                    </ul>
                </div>

                <div>
                    <h5 class="text-white font-semibold mb-3 text-xs uppercase tracking-wider">Company</h5>
                    <ul class="space-y-2 text-xs">
                        <li><a href="#" class="hover:text-gold-400 transition-colors">About Us</a></li>
                        <li><a href="#" class="hover:text-gold-400 transition-colors">Leadership</a></li>
                        <li><a href="#" class="hover:text-gold-400 transition-colors">Careers</a></li>
                        <li><a href="#" class="hover:text-gold-400 transition-colors">Press & Media</a></li>
                    </ul>
                </div>

                <div>
                    <h5 class="text-white font-semibold mb-3 text-xs uppercase tracking-wider">Legal & Safety</h5>
                    <ul class="space-y-2 text-xs">
                        <li><a href="#" class="hover:text-gold-400 transition-colors">Privacy Policy</a></li>
                        <li><a href="#" class="hover:text-gold-400 transition-colors">Terms of Service</a></li>
                        <li><a href="#" class="hover:text-gold-400 transition-colors">Security Overview</a></li>
                        <li><a href="#" class="hover:text-gold-400 transition-colors">Regulatory Compliance</a></li>
                    </ul>
                </div>
            </div>

            <!-- Fictional Disclaimer Footer Note -->
            <div class="pt-8 border-t border-slate-900 text-center text-[11px] text-slate-600 leading-relaxed">
                <p><strong>Disclaimer:</strong> This website is a fictional concept created solely for demonstration purposes under the brand name "DANIELWEALTH". It does not offer real financial services, take deposits, or manage assets. Do not submit sensitive financial or personal information.</p>
            </div>
        </div>
    </footer>

    <!-- Modal for Mock Secure Login -->
    <div id="login-modal" class="fixed inset-0 bg-navy-950/80 backdrop-blur-sm z-50 flex items-center justify-center p-4 hidden">
        <div class="bg-navy-900 border border-slate-700 rounded-2xl w-full max-w-md p-6 relative shadow-2xl">
            <button onclick="toggleModal('login-modal')" class="absolute top-4 right-4 text-slate-400 hover:text-white">
                <i data-lucide="x" class="w-5 h-5"></i>
            </button>
            
            <div class="text-center mb-6">
                <div class="w-12 h-12 bg-gold-500/10 border border-gold-500/20 text-gold-400 rounded-xl flex items-center justify-center mx-auto mb-3">
                    <i data-lucide="lock" class="w-6 h-6"></i>
                </div>
                <h3 class="text-xl font-bold text-white font-serif">Client Portal Login</h3>
                <p class="text-xs text-slate-400 mt-1">Enter your DANIELWEALTH private credentials</p>
            </div>

            <form onsubmit="handleLogin(event)" class="space-y-4">
                <div>
                    <label class="block text-xs text-slate-300 mb-1">Client ID / Username</label>
                    <input type="text" required placeholder="DW-Client-ID" class="w-full bg-navy-950 border border-slate-700 rounded-lg px-4 py-2.5 text-sm text-white focus:outline-none focus:border-gold-500">
                </div>
                <div>
                    <label class="block text-xs text-slate-300 mb-1">Passcode / Token</label>
                    <input type="password" required placeholder="••••••••••••" class="w-full bg-navy-950 border border-slate-700 rounded-lg px-4 py-2.5 text-sm text-white focus:outline-none focus:border-gold-500">
                </div>
                <div class="flex items-center justify-between text-xs text-slate-400">
                    <label class="flex items-center gap-2 cursor-pointer">
                        <input type="checkbox" class="rounded bg-navy-950 border-slate-700 text-gold-500 focus:ring-0">
                        <span>Remember Hardware ID</span>
                    </label>
                    <a href="#" class="text-gold-400 hover:underline">Forgot Key?</a>
                </div>
                <button type="submit" class="w-full gold-button-gradient text-navy-950 font-bold py-3 rounded-lg text-sm shadow-lg shadow-gold-500/20">
                    Authenticate Session
                </button>
            </form>
            
            <div id="login-feedback" class="hidden mt-4 p-3 rounded bg-gold-500/10 border border-gold-500/30 text-gold-400 text-xs text-center">
                Demo Mode: Login sequence initialized! (Mock behavior)
            </div>
        </div>
    </div>

    <!-- Scripts -->
    <script>
        // Initialize Lucide Icons
        lucide.createIcons();

        // Mobile menu toggle
        const menuBtn = document.getElementById('menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');

        menuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // Toggle Modal helper
        function toggleModal(modalId) {
            const modal = document.getElementById(modalId);
            modal.classList.toggle('hidden');
        }

        // Mock Transfer Event
        function handleTransfer(e) {
            e.preventDefault();
            const status = document.getElementById('transfer-status');
            status.classList.remove('hidden');
            setTimeout(() => {
                status.classList.add('hidden');
                e.target.reset();
            }, 3000);
        }

        // Mock Login Event
        function handleLogin(e) {
            e.preventDefault();
            const feedback = document.getElementById('login-feedback');
            feedback.classList.remove('hidden');
            setTimeout(() => {
                feedback.classList.add('hidden');
                toggleModal('login-modal');
            }, 2000);
        }
    </script>
</body>
</html>
