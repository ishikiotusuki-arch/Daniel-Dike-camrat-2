# Daniel-Dike-camrat-2<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CAMRT Exam Hub | Dedicated to Daniel Dike by Yamoskipo</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=Space+Grotesk:wght@500;700&family=Crimson+Text:ital,wght@0,400;0,600;1,400&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        display: ['Space Grotesk', 'sans-serif'],
                        serif: ['Crimson Text', 'serif'],
                    },
                    colors: {
                        medical: {
                            50: '#f0f9ff',
                            100: '#e0f2fe',
                            500: '#0ea5e9',
                            600: '#0284c7',
                            700: '#0369a1',
                            800: '#075985',
                            900: '#0c4a6e',
                        },
                        dedication: {
                            gold: '#d4af37',
                            deep: '#1e3a8a',
                            purple: '#6b21a8'
                        }
                    },
                    animation: {
                        'float': 'float 6s ease-in-out infinite',
                        'pulse-slow': 'pulse 4s cubic-bezier(0.4, 0, 0.6, 1) infinite',
                        'shimmer': 'shimmer 2s linear infinite',
                        'fade-in': 'fadeIn 1s ease-in',
                    },
                    keyframes: {
                        float: {
                            '0%, 100%': { transform: 'translateY(0)' },
                            '50%': { transform: 'translateY(-20px)' },
                        },
                        fadeIn: {
                            '0%': { opacity: '0', transform: 'translateY(20px)' },
                            '100%': { opacity: '1', transform: 'translateY(0)' },
                        }
                    }
                }
            }
        }
    </script>
    <style>
        body {
            background: linear-gradient(135deg, #f0f9ff 0%, #e0f2fe 100%);
            overflow-x: hidden;
        }
        .glass-panel {
            background: rgba(255, 255, 255, 0.7);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.5);
        }
        .gradient-text {
            background: linear-gradient(135deg, #0284c7 0%, #14b8a6 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .hover-lift {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .hover-lift:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px -15px rgba(0, 0, 0, 0.1);
        }
        .dedication-banner {
            background: linear-gradient(135deg, #1e3a8a 0%, #312e81 50%, #6b21a8 100%);
        }
        .flashcard {
            perspective: 1000px;
            height: 400px;
        }
        .flashcard-inner {
            position: relative;
            width: 100%;
            height: 100%;
            transition: transform 0.6s;
            transform-style: preserve-3d;
        }
        .flashcard.flipped .flashcard-inner {
            transform: rotateY(180deg);
        }
        .flashcard-front, .flashcard-back {
            position: absolute;
            width: 100%;
            height: 100%;
            backface-visibility: hidden;
            border-radius: 1.5rem;
        }
        .flashcard-back {
            transform: rotateY(180deg);
        }
        .formula-card {
            background: linear-gradient(145deg, #ffffff 0%, #f0f9ff 100%);
            border-left: 4px solid #0284c7;
        }
        .morph-blob {
            position: absolute;
            filter: blur(80px);
            opacity: 0.4;
            z-index: -1;
        }
        .study-tab-active {
            background: linear-gradient(135deg, #0284c7 0%, #0369a1 100%);
            color: white;
        }
        .anatomy-hotspot {
            position: absolute;
            width: 20px;
            height: 20px;
            background: #f43f5e;
            border: 3px solid white;
            border-radius: 50%;
            cursor: pointer;
            animation: pulse 2s infinite;
            box-shadow: 0 0 0 0 rgba(244, 63, 94, 0.7);
        }
        .anatomy-hotspot:hover::after {
            content: attr(data-label);
            position: absolute;
            bottom: 25px;
            left: 50%;
            transform: translateX(-50%);
            background: rgba(0,0,0,0.8);
            color: white;
            padding: 4px 8px;
            border-radius: 4px;
            font-size: 12px;
            white-space: nowrap;
        }
        .calculation-input {
            background: linear-gradient(135deg, #f8fafc 0%, #f1f5f9 100%);
            border: 2px solid #e2e8f0;
            transition: all 0.3s;
        }
        .calculation-input:focus {
            border-color: #0284c7;
            box-shadow: 0 0 0 3px rgba(2, 132, 199, 0.1);
            outline: none;
        }
    </style>
</head>
<body class="text-slate-800 antialiased">

    <!-- Animated Background -->
    <div class="morph-blob bg-medical-400 w-96 h-96 rounded-full top-0 left-0 animate-float"></div>
    <div class="morph-blob bg-teal-400 w-80 h-80 rounded-full bottom-0 right-0 animate-float" style="animation-delay: -3s;"></div>
    <div class="morph-blob bg-purple-400 w-64 h-64 rounded-full top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 animate-pulse-slow"></div>

    <!-- Dedication Banner -->
    <div class="dedication-banner text-white py-3 px-4 relative overflow-hidden">
        <div class="absolute inset-0 opacity-20">
            <div class="absolute inset-0 bg-[url('data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNjAiIGhlaWdodD0iNjAiIHZpZXdCb3g9IjAgMCA2MCA2MCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48ZyBmaWxsPSJub25lIiBmaWxsLXJ1bGU9ImV2ZW5vZGQiPjxnIGZpbGw9IiNmZmZmZmYiIGZpbGwtb3BhY2l0eT0iMC4xIj48cGF0aCBkPSJNMzYgMzRoLTJ2LTRoMnY0em0wLTZ2LTRoLTJ2NGgyem0tNiA2aC00djJoNHYtMnptMC02di00aC00djRoNHptLTYgNmgtNHYyaDR2LTJ6bTAtNnYtNGgtNHY0aDR6Ii8+PC9nPjwvZz48L3N2Zz4=')]"></div>
        </div>
        <div class="max-w-7xl mx-auto flex flex-col md:flex-row items-center justify-center gap-4 relative z-10">
            <div class="flex items-center gap-3">
                <i class="fa-solid fa-star text-yellow-400 text-xl animate-pulse"></i>
                <span class="font-serif italic text-lg">Dedicated to</span>
                <span class="font-display font-bold text-2xl text-yellow-300">Daniel Dike</span>
                <span class="font-serif italic text-lg">by</span>
                <span class="font-display font-bold text-xl text-purple-300">Yamoskipo</span>
                <i class="fa-solid fa-heart text-rose-400 text-xl animate-pulse"></i>
            </div>
            <div class="hidden md:block w-px h-6 bg-white/30"></div>
            <p class="text-sm text-blue-100 text-center md:text-left">Inspiring excellence in Medical Radiation Technology</p>
        </div>
    </div>

    <!-- Navigation -->
    <nav class="fixed w-full z-50 glass-panel border-b border-white/20 top-14 md:top-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-20 items-center">
                <div class="flex items-center space-x-3">
                    <div class="w-12 h-12 bg-gradient-to-br from-medical-600 to-teal-500 rounded-xl flex items-center justify-center text-white font-bold text-xl shadow-lg">
                        <i class="fa-solid fa-user-doctor"></i>
                    </div>
                    <div>
                        <h1 class="font-display font-bold text-2xl text-slate-900">CAMRT<span class="text-medical-600">Hub</span></h1>
                        <p class="text-xs text-slate-500 font-medium">Daniel Dike Study Center</p>
                    </div>
                </div>
                <div class="hidden md:flex space-x-6">
                    <button onclick="scrollToSection('overview')" class="nav-link text-slate-600 hover:text-medical-600 font-medium transition-colors">Overview</button>
                    <button onclick="scrollToSection('materials')" class="nav-link text-slate-600 hover:text-medical-600 font-medium transition-colors">Study Materials</button>
                    <button onclick="scrollToSection('flashcards')" class="nav-link text-slate-600 hover:text-medical-600 font-medium transition-colors">Flashcards</button>
                    <button onclick="scrollToSection('calculations')" class="nav-link text-slate-600 hover:text-medical-600 font-medium transition-colors">Calculations</button>
                    <button onclick="scrollToSection('anatomy')" class="nav-link text-slate-600 hover:text-medical-600 font-medium transition-colors">Anatomy</button>
                    <button onclick="scrollToSection('practice')" class="nav-link text-slate-600 hover:text-medical-600 font-medium transition-colors">Practice</button>
                </div>
                <button onclick="toggleMobileMenu()" class="md:hidden text-slate-600 text-2xl">
                    <i class="fa-solid fa-bars"></i>
                </button>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="relative pt-40 pb-20 px-4 sm:px-6 lg:px-8 overflow-hidden">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-16 animate-fade-in">
                <div class="inline-flex items-center px-6 py-3 rounded-full bg-gradient-to-r from-blue-100 to-purple-100 text-blue-800 text-sm font-bold border border-blue-200 mb-6 shadow-sm">
                    <i class="fa-solid fa-graduation-cap mr-2"></i>
                    Comprehensive CAMRT Certification Preparation
                </div>
                <h1 class="font-display text-6xl lg:text-7xl font-bold leading-tight text-slate-900 mb-6">
                    Master Your <span class="gradient-text">CAMRT</span> Journey
                </h1>
                <p class="text-xl text-slate-600 leading-relaxed max-w-3xl mx-auto mb-8 font-serif italic">
                    "Excellence is not a destination but a continuous journey. Dedicated to all aspiring MRTs, with special dedication to Daniel Dike."
                </p>
                <div class="flex flex-wrap justify-center gap-4">
                    <button onclick="scrollToSection('materials')" class="px-8 py-4 bg-gradient-to-r from-medical-600 to-medical-700 text-white rounded-2xl font-semibold shadow-lg hover:shadow-xl hover:scale-105 transition-all flex items-center gap-2">
                        <span>Access Study Materials</span>
                        <i class="fa-solid fa-book-open"></i>
                    </button>
                    <button onclick="scrollToSection('flashcards')" class="px-8 py-4 bg-white text-medical-700 border-2 border-medical-200 rounded-2xl font-semibold hover:bg-medical-50 transition-all flex items-center gap-2">
                        <i class="fa-solid fa-layer-group"></i>
                        <span>Review Flashcards</span>
                    </button>
                </div>
            </div>

            <!-- Stats Grid -->
            <div class="grid grid-cols-2 md:grid-cols-4 gap-6 max-w-4xl mx-auto mb-16">
                <div class="glass-panel rounded-2xl p-6 text-center hover-lift">
                    <div class="text-3xl font-bold text-medical-600 mb-1">500+</div>
                    <div class="text-sm text-slate-600">Study Questions</div>
                </div>
                <div class="glass-panel rounded-2xl p-6 text-center hover-lift">
                    <div class="text-3xl font-bold text-purple-600 mb-1">200+</div>
                    <div class="text-sm text-slate-600">Flashcards</div>
                </div>
                <div class="glass-panel rounded-2xl p-6 text-center hover-lift">
                    <div class="text-3xl font-bold text-teal-600 mb-1">50+</div>
                    <div class="text-sm text-slate-600">Formulas</div>
                </div>
                <div class="glass-panel rounded-2xl p-6 text-center hover-lift">
                    <div class="text-3xl font-bold text-rose-600 mb-1">4</div>
                    <div class="text-sm text-slate-600">Disciplines</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Comprehensive Study Materials Hub -->
    <section id="materials" class="py-20 px-4 sm:px-6 lg:px-8 bg-white/30">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-12">
                <h2 class="font-display text-4xl font-bold text-slate-900 mb-4">Comprehensive Study Materials</h2>
                <p class="text-lg text-slate-600">Curated resources for Daniel Dike and all CAMRT candidates</p>
            </div>

            <!-- Material Categories Tabs -->
            <div class="flex flex-wrap justify-center gap-2 mb-8">
                <button onclick="switchMaterialTab('guides')" id="mat-tab-guides" class="mat-tab px-6 py-3 rounded-full font-semibold transition-all bg-medical-600 text-white shadow-lg">
                    <i class="fa-solid fa-book mr-2"></i>Study Guides
                </button>
                <button onclick="switchMaterialTab('formulas')" id="mat-tab-formulas" class="mat-tab px-6 py-3 rounded-full font-semibold transition-all bg-white text-slate-600 hover:bg-slate-100">
                    <i class="fa-solid fa-calculator mr-2"></i>Formulas
                </button>
                <button onclick="switchMaterialTab('protocols')" id="mat-tab-protocols" class="mat-tab px-6 py-3 rounded-full font-semibold transition-all bg-white text-slate-600 hover:bg-slate-100">
                    <i class="fa-solid fa-clipboard-list mr-2"></i>Protocols
                </button>
                <button onclick="switchMaterialTab('safety')" id="mat-tab-safety" class="mat-tab px-6 py-3 rounded-full font-semibold transition-all bg-white text-slate-600 hover:bg-slate-100">
                    <i class="fa-solid fa-shield-halved mr-2"></i>Safety & QC
                </button>
            </div>

            <!-- Content Container -->
            <div id="materials-content" class="space-y-6">
                <!-- Populated by JavaScript -->
            </div>
        </div>
    </section>

    <!-- Interactive Flashcards Section -->
    <section id="flashcards" class="py-20 px-4 sm:px-6 lg:px-8">
        <div class="max-w-6xl mx-auto">
            <div class="text-center mb-12">
                <h2 class="font-display text-4xl font-bold text-slate-900 mb-4">Interactive Flashcards</h2>
                <p class="text-lg text-slate-600 mb-6">Click cards to flip • Use arrows to navigate</p>
                
                <!-- Flashcard Filters -->
                <div class="flex flex-wrap justify-center gap-2 mb-8">
                    <button onclick="filterFlashcards('all')" class="fc-filter px-4 py-2 rounded-full bg-medical-600 text-white text-sm font-semibold">All</button>
                    <button onclick="filterFlashcards('anatomy')" class="fc-filter px-4 py-2 rounded-full bg-white text-slate-600 text-sm font-semibold hover:bg-slate-100">Anatomy</button>
                    <button onclick="filterFlashcards('physics')" class="fc-filter px-4 py-2 rounded-full bg-white text-slate-600 text-sm font-semibold hover:bg-slate-100">Physics</button>
                    <button onclick="filterFlashcards('procedures')" class="fc-filter px-4 py-2 rounded-full bg-white text-slate-600 text-sm font-semibold hover:bg-slate-100">Procedures</button>
                    <button onclick="filterFlashcards('safety')" class="fc-filter px-4 py-2 rounded-full bg-white text-slate-600 text-sm font-semibold hover:bg-slate-100">Safety</button>
                </div>
            </div>

            <div class="relative max-w-2xl mx-auto">
                <div id="flashcard-container" class="flashcard cursor-pointer" onclick="flipCard()">
                    <div class="flashcard-inner">
                        <div class="flashcard-front glass-panel flex flex-col items-center justify-center p-8 text-center border-2 border-medical-200">
                            <div class="w-16 h-16 bg-medical-100 rounded-full flex items-center justify-center text-medical-600 text-2xl mb-4">
                                <i class="fa-solid fa-question"></i>
                            </div>
                            <h3 id="fc-front-title" class="text-sm font-bold text-medical-600 uppercase tracking-wider mb-2">Category</h3>
                            <p id="fc-front-content" class="text-2xl font-bold text-slate-900">Click to view question</p>
                            <p class="text-sm text-slate-400 mt-8">Click to flip</p>
                        </div>
                        <div class="flashcard-back bg-gradient-to-br from-medical-600 to-medical-800 flex flex-col items-center justify-center p-8 text-center text-white">
                            <div class="w-16 h-16 bg-white/20 rounded-full flex items-center justify-center text-2xl mb-4">
                                <i class="fa-solid fa-lightbulb"></i>
                            </div>
                            <h3 class="text-sm font-bold text-blue-200 uppercase tracking-wider mb-2">Answer</h3>
                            <p id="fc-back-content" class="text-xl font-medium leading-relaxed">Answer content</p>
                            <div id="fc-back-extra" class="mt-6 text-sm text-blue-100 bg-white/10 rounded-lg p-3"></div>
                        </div>
                    </div>
                </div>

                <!-- Navigation -->
                <div class="flex justify-center items-center gap-4 mt-8">
                    <button onclick="prevCard()" class="w-12 h-12 rounded-full bg-white shadow-lg flex items-center justify-center text-slate-600 hover:text-medical-600 hover:scale-110 transition-all">
                        <i class="fa-solid fa-chevron-left"></i>
                    </button>
                    <span id="fc-counter" class="font-bold text-slate-600">1 / 20</span>
                    <button onclick="nextCard()" class="w-12 h-12 rounded-full bg-white shadow-lg flex items-center justify-center text-slate-600 hover:text-medical-600 hover:scale-110 transition-all">
                        <i class="fa-solid fa-chevron-right"></i>
                    </button>
                </div>

                <div class="text-center mt-6">
                    <button onclick="shuffleCards()" class="px-6 py-2 bg-white border border-slate-200 rounded-full text-sm font-semibold text-slate-600 hover:bg-slate-50 transition-all">
                        <i class="fa-solid fa-shuffle mr-2"></i>Shuffle Deck
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Calculations & Formulas Lab -->
    <section id="calculations" class="py-20 px-4 sm:px-6 lg:px-8 bg-white/30">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-12">
                <h2 class="font-display text-4xl font-bold text-slate-900 mb-4">Calculations Laboratory</h2>
                <p class="text-lg text-slate-600">Interactive formula calculators for exam preparation</p>
            </div>

            <div class="grid lg:grid-cols-2 gap-8">
                <!-- Calculator 1: Exposure Time -->
                <div class="glass-panel rounded-3xl p-8">
                    <h3 class="font-bold text-xl text-slate-900 mb-6 flex items-center gap-3">
                        <i class="fa-solid fa-clock text-medical-600"></i>
                        Exposure Time Calculator (mAs)
                    </h3>
                    <div class="space-y-4">
                        <div>
                            <label class="block text-sm font-semibold text-slate-700 mb-2">Tube Current (mA)</label>
                            <input type="number" id="calc-ma" class="calculation-input w-full px-4 py-3 rounded-xl" placeholder="e.g., 400" oninput="calculateMas()">
                        </div>
                        <div>
                            <label class="block text-sm font-semibold text-slate-700 mb-2">Time (seconds)</label>
                            <input type="number" id="calc-time" class="calculation-input w-full px-4 py-3 rounded-xl" placeholder="e.g., 0.05" step="0.001" oninput="calculateMas()">
                        </div>
                        <div class="bg-medical-50 rounded-xl p-4 border border-medical-200">
                            <div class="text-sm text-medical-700 mb-1">Result (mAs)</div>
                            <div id="result-mas" class="text-3xl font-bold text-medical-900">0</div>
                            <div class="text-xs text-medical-600 mt-1">Formula: mA × Time = mAs</div>
                        </div>
                    </div>
                </div>

                <!-- Calculator 2: Density Maintenance -->
                <div class="glass-panel rounded-3xl p-8">
                    <h3 class="font-bold text-xl text-slate-900 mb-6 flex items-center gap-3">
                        <i class="fa-solid fa-scale-balanced text-purple-600"></i>
                        15% Rule Calculator
                    </h3>
                    <div class="space-y-4">
                        <div>
                            <label class="block text-sm font-semibold text-slate-700 mb-2">Original kVp</label>
                            <input type="number" id="calc-kvp-orig" class="calculation-input w-full px-4 py-3 rounded-xl" placeholder="e.g., 70" oninput="calculate15Rule()">
                        </div>
                        <div>
                            <label class="block text-sm font-semibold text-slate-700 mb-2">Direction</label>
                            <select id="calc-direction" class="calculation-input w-full px-4 py-3 rounded-xl" onchange="calculate15Rule()">
                                <option value="increase">Increase kVp by 15%</option>
                                <option value="decrease">Decrease kVp by 15%</option>
                            </select>
                        </div>
                        <div class="bg-purple-50 rounded-xl p-4 border border-purple-200">
                            <div class="text-sm text-purple-700 mb-1">New kVp</div>
                            <div id="result-kvp" class="text-3xl font-bold text-purple-900">0</div>
                            <div class="text-xs text-purple-600 mt-1">Doubles or halves exposure</div>
                        </div>
                    </div>
                </div>

                <!-- Calculator 3: SFD (Tech Factor) -->
                <div class="glass-panel rounded-3xl p-8">
                    <h3 class="font-bold text-xl text-slate-900 mb-6 flex items-center gap-3">
                        <i class="fa-solid fa-ruler-horizontal text-teal-600"></i>
                        SID Compensation (SFD)
                    </h3>
                    <div class="space-y-4">
                        <div>
                            <label class="block text-sm font-semibold text-slate-700 mb-2">Original mAs</label>
                            <input type="number" id="calc-mas-orig" class="calculation-input w-full px-4 py-3 rounded-xl" placeholder="e.g., 10" oninput="calculateSfd()">
                        </div>
                        <div class="grid grid-cols-2 gap-4">
                            <div>
                                <label class="block text-sm font-semibold text-slate-700 mb-2">Original SID (cm)</label>
                                <input type="number" id="calc-sid-orig" class="calculation-input w-full px-4 py-3 rounded-xl" placeholder="100" oninput="calculateSfd()">
                            </div>
                            <div>
                                <label class="block text-sm font-semibold text-slate-700 mb-2">New SID (cm)</label>
                                <input type="number" id="calc-sid-new" class="calculation-input w-full px-4 py-3 rounded-xl" placeholder="180" oninput="calculateSfd()">
                            </div>
                        </div>
                        <div class="bg-teal-50 rounded-xl p-4 border border-teal-200">
                            <div class="text-sm text-teal-700 mb-1">New mAs Required</div>
                            <div id="result-sfd" class="text-3xl font-bold text-teal-900">0</div>
                            <div class="text-xs text-teal-600 mt-1">Formula: mAs₁/mAs₂ = (SID₁)²/(SID₂)²</div>
                        </div>
                    </div>
                </div>

                <!-- Calculator 4: Grid Ratio -->
                <div class="glass-panel rounded-3xl p-8">
                    <h3 class="font-bold text-xl text-slate-900 mb-6 flex items-center gap-3">
                        <i class="fa-solid fa-filter text-amber-600"></i>
                        Grid Conversion (Bucky Factor)
                    </h3>
                    <div class="space-y-4">
                        <div>
                            <label class="block text-sm font-semibold text-slate-700 mb-2">Non-grid mAs</label>
                            <input type="number" id="calc-nogrid" class="calculation-input w-full px-4 py-3 rounded-xl" placeholder="e.g., 5" oninput="calculateGrid()">
                        </div>
                        <div>
                            <label class="block text-sm font-semibold text-slate-700 mb-2">Grid Ratio</label>
                            <select id="calc-grid-ratio" class="calculation-input w-full px-4 py-3 rounded-xl" onchange="calculateGrid()">
                                <option value="5">5:1</option>
                                <option value="6">6:1</option>
                                <option value="8">8:1</option>
                                <option value="10">10:1</option>
                                <option value="12">12:1</option>
                                <option value="16">16:1</option>
                            </select>
                        </div>
                        <div class="bg-amber-50 rounded-xl p-4 border border-amber-200">
                            <div class="text-sm text-amber-700 mb-1">Required mAs with Grid</div>
                            <div id="result-grid" class="text-3xl font-bold text-amber-900">0</div>
                            <div class="text-xs text-amber-600 mt-1">Accounts for lead strip absorption</div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Formula Reference Sheet -->
            <div class="mt-12 glass-panel rounded-3xl p-8">
                <h3 class="font-bold text-2xl text-slate-900 mb-6 text-center">Quick Formula Reference</h3>
                <div class="grid md:grid-cols-3 gap-6 text-sm">
                    <div class="formula-card p-4 rounded-xl">
                        <h4 class="font-bold text-medical-700 mb-2">Image Receptor Exposure</h4>
                        <code class="bg-slate-100 px-2 py-1 rounded">E = kVp⁴ × mAs</code>
                        <p class="text-slate-600 mt-2">Exposure proportional to kVp to the fourth power</p>
                    </div>
                    <div class="formula-card p-4 rounded-xl">
                        <h4 class="font-bold text-medical-700 mb-2">Heat Unit (HU)</h4>
                        <code class="bg-slate-100 px-2 py-1 rounded">HU = kVp × mAs × Generator Factor</code>
                        <p class="text-slate-600 mt-2">Single phase: ×1, Three phase: ×1.35, HF: ×1.41</p>
                    </div>
                    <div class="formula-card p-4 rounded-xl">
                        <h4 class="font-bold text-medical-700 mb-2">Half Value Layer</h4>
                        <code class="bg-slate-100 px-2 py-1 rounded">HVL = 0.693/μ</code>
                        <p class="text-slate-600 mt-2">Thickness reducing intensity by 50%</p>
                    </div>
                    <div class="formula-card p-4 rounded-xl">
                        <h4 class="font-bold text-medical-700 mb-2">Dose (Gy)</h4>
                        <code class="bg-slate-100 px-2 py-1 rounded">D = E/m (J/kg)</code>
                        <p class="text-slate-600 mt-2">Absorbed energy per unit mass</p>
                    </div>
                    <div class="formula-card p-4 rounded-xl">
                        <h4 class="font-bold text-medical-700 mb-2">Effective Dose</h4>
                        <code class="bg-slate-100 px-2 py-1 rounded">E = Σ(wT × HT)</code>
                        <p class="text-slate-600 mt-2">Sum of equivalent doses × tissue weights</p>
                    </div>
                    <div class="formula-card p-4 rounded-xl">
                        <h4 class="font-bold text-medical-700 mb-2">Decay Factor</h4>
                        <code class="bg-slate-100 px-2 py-1 rounded">A = A₀ × (1/2)^(t/t½)</code>
                        <p class="text-slate-600 mt-2">Radioactivity remaining after time t</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Anatomy Atlas -->
    <section id="anatomy" class="py-20 px-4 sm:px-6 lg:px-8">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-12">
                <h2 class="font-display text-4xl font-bold text-slate-900 mb-4">Cross-Sectional Anatomy Atlas</h2>
                <p class="text-lg text-slate-600">Essential anatomy for MRI and CT interpretation</p>
            </div>

            <div class="grid lg:grid-cols-3 gap-8">
                <!-- Anatomy Selector -->
                <div class="lg:col-span-1 space-y-4">
                    <button onclick="showAnatomy('brain')" class="anatomy-btn w-full p-4 rounded-xl bg-white border-2 border-slate-200 hover:border-medical-500 hover:bg-medical-50 transition-all text-left flex items-center gap-3">
                        <i class="fa-solid fa-brain text-purple-500 text-xl"></i>
                        <div>
                            <div class="font-bold text-slate-900">Brain</div>
                            <div class="text-xs text-slate-500">Cerebrum, cerebellum, brainstem</div>
                        </div>
                    </button>
                    <button onclick="showAnatomy('spine')" class="anatomy-btn w-full p-4 rounded-xl bg-white border-2 border-slate-200 hover:border-medical-500 hover:bg-medical-50 transition-all text-left flex items-center gap-3">
                        <i class="fa-solid fa-bone text-teal-500 text-xl"></i>
                        <div>
                            <div class="font-bold text-slate-900">Spine</div>
                            <div class="text-xs text-slate-500">Vertebrae, cord, discs</div>
                        </div>
                    </button>
                    <button onclick="showAnatomy('thorax')" class="anatomy-btn w-full p-4 rounded-xl bg-white border-2 border-slate-200 hover:border-medical-500 hover:bg-medical-50 transition-all text-left flex items-center gap-3">
                        <i class="fa-solid fa-lungs text-rose-500 text-xl"></i>
                        <div>
                            <div class="font-bold text-slate-900">Thorax</div>
                            <div class="text-xs text-slate-500">Heart, lungs, mediastinum</div>
                        </div>
                    </button>
                    <button onclick="showAnatomy('abdomen')" class="anatomy-btn w-full p-4 rounded-xl bg-white border-2 border-slate-200 hover:border-medical-500 hover:bg-medical-50 transition-all text-left flex items-center gap-3">
                        <i class="fa-solid fa-kidney text-amber-500 text-xl"></i>
                        <div>
                            <div class="font-bold text-slate-900">Abdomen</div>
                            <div class="text-xs text-slate-500">Liver, kidneys, GI tract</div>
                        </div>
                    </button>
                    <button onclick="showAnatomy('pelvis')" class="anatomy-btn w-full p-4 rounded-xl bg-white border-2 border-slate-200 hover:border-medical-500 hover:bg-medical-50 transition-all text-left flex items-center gap-3">
                        <i class="fa-solid fa-person text-blue-500 text-xl"></i>
                        <div>
                            <div class="font-bold text-slate-900">Pelvis</div>
                            <div class="text-xs text-slate-500">Hip, bladder, reproductive</div>
                        </div>
                    </button>
                </div>

                <!-- Anatomy Display -->
                <div class="lg:col-span-2">
                    <div id="anatomy-display" class="glass-panel rounded-3xl p-8 min-h-[500px] relative overflow-hidden">
                        <div class="absolute inset-0 flex items-center justify-center text-slate-400">
                            <div class="text-center">
                                <i class="fa-solid fa-hand-pointer text-4xl mb-4"></i>
                                <p>Select an anatomical region to explore</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Anatomy Tables -->
            <div class="mt-12 grid md:grid-cols-2 gap-8">
                <div class="glass-panel rounded-3xl p-6">
                    <h3 class="font-bold text-xl text-slate-900 mb-4">Cranial Nerves (Quick Reference)</h3>
                    <div class="overflow-x-auto">
                        <table class="w-full text-sm">
                            <thead class="bg-medical-50 text-medical-900">
                                <tr>
                                    <th class="px-3 py-2 text-left rounded-tl-lg">#</th>
                                    <th class="px-3 py-2 text-left">Name</th>
                                    <th class="px-3 py-2 text-left rounded-tr-lg">Function</th>
                                </tr>
                            </thead>
                            <tbody class="divide-y divide-slate-200">
                                <tr><td class="px-3 py-2 font-mono">I</td><td class="px-3 py-2">Olfactory</td><td class="px-3 py-2">Smell</td></tr>
                                <tr><td class="px-3 py-2 font-mono">II</td><td class="px-3 py-2">Optic</td><td class="px-3 py-2">Vision</td></tr>
                                <tr><td class="px-3 py-2 font-mono">III</td><td class="px-3 py-2">Oculomotor</td><td class="px-3 py-2">Eye movement, pupil</td></tr>
                                <tr><td class="px-3 py-2 font-mono">V</td><td class="px-3 py-2">Trigeminal</td><td class="px-3 py-2">Facial sensation</td></tr>
                                <tr><td class="px-3 py-2 font-mono">VII</td><td class="px-3 py-2">Facial</td><td class="px-3 py-2">Facial expression</td></tr>
                                <tr><td class="px-3 py-2 font-mono">X</td><td class="px-3 py-2">Vagus</td><td class="px-3 py-2">Parasympathetic</td></tr>
                            </tbody>
                        </table>
                    </div>
                </div>

                <div class="glass-panel rounded-3xl p-6">
                    <h3 class="font-bold text-xl text-slate-900 mb-4">Spinal Cord Segments</h3>
                    <div class="space-y-3">
                        <div class="flex items-center gap-4 p-3 bg-cervical-50 rounded-lg border-l-4 border-cervical-500" style="border-color: #f59e0b;">
                            <div class="font-bold text-amber-700 w-20">Cervical</div>
                            <div class="text-sm text-slate-600">C1-C8 (8 pairs) - Neck, arms, diaphragm (C3-C5)</div>
                        </div>
                        <div class="flex items-center gap-4 p-3 bg-thoracic-50 rounded-lg border-l-4 border-thoracic-500" style="border-color: #3b82f6;">
                            <div class="font-bold text-blue-700 w-20">Thoracic</div>
                            <div class="text-sm text-slate-600">T1-T12 - Trunk, abdominal muscles</div>
                        </div>
                        <div class="flex items-center gap-4 p-3 bg-lumbar-50 rounded-lg border-l-4 border-lumbar-500" style="border-color: #10b981;">
                            <div class="font-bold text-emerald-700 w-20">Lumbar</div>
                            <div class="text-sm text-slate-600">L1-L5 - Legs, bowel/bladder</div>
                        </div>
                        <div class="flex items-center gap-4 p-3 bg-sacral-50 rounded-lg border-l-4 border-sacral-500" style="border-color: #8b5cf6;">
                            <div class="font-bold text-purple-700 w-20">Sacral</div>
                            <div class="text-sm text-slate-600">S1-S5 - Bowel, bladder, sexual function</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Enhanced Practice Section -->
    <section id="practice" class="py-20 px-4 sm:px-6 lg:px-8 bg-white/30">
        <div class="max-w-6xl mx-auto">
            <div class="text-center mb-12">
                <h2 class="font-display text-4xl font-bold text-slate-900 mb-4">Comprehensive Practice Bank</h2>
                <p class="text-lg text-slate-600">500+ questions covering all CAMRT competencies</p>
            </div>

            <!-- Practice Filters -->
            <div class="flex flex-wrap justify-center gap-3 mb-8">
                <select id="practice-discipline" class="px-4 py-2 rounded-full border border-slate-200 bg-white text-slate-700 focus:border-medical-500 outline-none" onchange="loadPracticeQuestion()">
                    <option value="all">All Disciplines</option>
                    <option value="radiography">Radiography</option>
                    <option value="mri">MRI</option>
                    <option value="nuclear">Nuclear Medicine</option>
                    <option value="therapy">Radiation Therapy</option>
                </select>
                <select id="practice-category" class="px-4 py-2 rounded-full border border-slate-200 bg-white text-slate-700 focus:border-medical-500 outline-none" onchange="loadPracticeQuestion()">
                    <option value="all">All Categories</option>
                    <option value="patient-care">Patient Care</option>
                    <option value="physics">Physics</option>
                    <option value="anatomy">Anatomy</option>
                    <option value="procedures">Procedures</option>
                    <option value="safety">Radiation Safety</option>
                </select>
                <select id="practice-difficulty" class="px-4 py-2 rounded-full border border-slate-200 bg-white text-slate-700 focus:border-medical-500 outline-none" onchange="loadPracticeQuestion()">
                    <option value="all">All Levels</option>
                    <option value="easy">Easy</option>
                    <option value="medium">Medium</option>
                    <option value="hard">Hard</option>
                </select>
            </div>

            <!-- Question Card -->
            <div class="glass-panel rounded-3xl p-8 shadow-2xl mb-8">
                <div class="flex justify-between items-start mb-6">
                    <div class="flex gap-2 flex-wrap">
                        <span id="q-discipline" class="px-3 py-1 bg-blue-100 text-blue-700 rounded-full text-xs font-bold">Radiography</span>
                        <span id="q-category" class="px-3 py-1 bg-purple-100 text-purple-700 rounded-full text-xs font-bold">Physics</span>
                        <span id="q-difficulty" class="px-3 py-1 bg-green-100 text-green-700 rounded-full text-xs font-bold">Medium</span>
                    </div>
                    <div class="text-right">
                        <div class="text-2xl font-bold text-medical-600" id="q-score">0/0</div>
                        <div class="text-xs text-slate-500">Score</div>
                    </div>
                </div>

                <div class="mb-8">
                    <h3 id="q-text" class="text-xl font-semibold text-slate-900 mb-6 leading-relaxed"></h3>
                    <div id="q-options" class="space-y-3">
                        <!-- Options populated by JS -->
                    </div>
                </div>

                <div id="q-explanation" class="hidden mb-6 p-6 bg-gradient-to-r from-green-50 to-emerald-50 border border-green-200 rounded-xl">
                    <div class="flex items-start gap-3">
                        <div class="w-10 h-10 bg-green-500 rounded-full flex items-center justify-center text-white flex-shrink-0">
                            <i class="fa-solid fa-check"></i>
                        </div>
                        <div>
                            <h4 class="font-bold text-green-900 mb-2">Explanation</h4>
                            <p id="q-explanation-text" class="text-green-800 text-sm leading-relaxed"></p>
                            <div id="q-reference" class="mt-3 text-xs text-green-700 font-semibold"></div>
                        </div>
                    </div>
                </div>

                <div class="flex justify-between items-center pt-6 border-t border-slate-200">
                    <button onclick="prevQuestion()" class="px-6 py-3 text-slate-600 hover:text-medical-600 font-medium transition-colors">
                        <i class="fa-solid fa-arrow-left mr-2"></i>Previous
                    </button>
                    <div class="flex gap-3">
                        <button onclick="flagQuestion()" class="px-4 py-3 text-amber-600 hover:bg-amber-50 rounded-xl transition-colors" title="Flag for review">
                            <i class="fa-solid fa-flag"></i>
                        </button>
                        <button onclick="checkPracticeAnswer()" id="q-check-btn" class="px-8 py-3 bg-medical-600 text-white rounded-xl font-semibold hover:bg-medical-700 transition-all shadow-lg">
                            Check Answer
                        </button>
                    </div>
                    <button onclick="nextQuestion()" class="px-6 py-3 text-medical-600 hover:text-medical-700 font-medium transition-colors">
                        Next<i class="fa-solid fa-arrow-right ml-2"></i>
                    </button>
                </div>
            </div>

            <!-- Progress Stats -->
            <div class="grid grid-cols-3 gap-4 max-w-2xl mx-auto">
                <div class="text-center p-4 bg-white rounded-2xl shadow-sm">
                    <div class="text-2xl font-bold text-medical-600" id="stat-attempted">0</div>
                    <div class="text-xs text-slate-500">Attempted</div>
                </div>
                <div class="text-center p-4 bg-white rounded-2xl shadow-sm">
                    <div class="text-2xl font-bold text-green-600" id="stat-correct">0</div>
                    <div class="text-xs text-slate-500">Correct</div>
                </div>
                <div class="text-center p-4 bg-white rounded-2xl shadow-sm">
                    <div class="text-2xl font-bold text-purple-600" id="stat-accuracy">0%</div>
                    <div class="text-xs text-slate-500">Accuracy</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Dedicated Study Schedule -->
    <section class="py-20 px-4 sm:px-6 lg:px-8 bg-gradient-to-br from-slate-900 to-slate-800 text-white">
        <div class="max-w-5xl mx-auto">
            <div class="text-center mb-12">
                <h2 class="font-display text-4xl font-bold mb-4">Daniel Dike's 12-Week Mastery Plan</h2>
                <p class="text-slate-300 text-lg">A structured approach to CAMRT certification success</p>
            </div>

            <div class="space-y-4">
                <!-- Phase 1 -->
                <div class="bg-white/10 backdrop-blur rounded-2xl p-6 border border-white/20">
                    <div class="flex items-center gap-4 mb-4">
                        <div class="w-12 h-12 bg-blue-500 rounded-full flex items-center justify-center font-bold text-xl">1</div>
                        <div>
                            <h3 class="font-bold text-xl">Foundation Phase (Weeks 1-3)</h3>
                            <p class="text-blue-300 text-sm">Core Concepts & Physics</p>
                        </div>
                    </div>
                    <div class="grid md:grid-cols-3 gap-4 text-sm">
                        <div class="bg-white/5 rounded-lg p-3">
                            <i class="fa-solid fa-atom text-blue-400 mb-2"></i>
                            <div class="font-semibold">Radiation Physics</div>
                            <div class="text-slate-400">Interactions, attenuation, production</div>
                        </div>
                        <div class="bg-white/5 rounded-lg p-3">
                            <i class="fa-solid fa-shield-virus text-green-400 mb-2"></i>
                            <div class="font-semibold">Protection</div>
                            <div class="text-slate-400">ALARA, shielding, dosimetry</div>
                        </div>
                        <div class="bg-white/5 rounded-lg p-3">
                            <i class="fa-solid fa-book-medical text-purple-400 mb-2"></i>
                            <div class="font-semibold">Anatomy Review</div>
                            <div class="text-slate-400">Cross-sectional, topographic</div>
                        </div>
                    </div>
                </div>

                <!-- Phase 2 -->
                <div class="bg-white/10 backdrop-blur rounded-2xl p-6 border border-white/20">
                    <div class="flex items-center gap-4 mb-4">
                        <div class="w-12 h-12 bg-purple-500 rounded-full flex items-center justify-center font-bold text-xl">2</div>
                        <div>
                            <h3 class="font-bold text-xl">Application Phase (Weeks 4-7)</h3>
                            <p class="text-purple-300 text-sm">Procedures & Pathology</p>
                        </div>
                    </div>
                    <div class="grid md:grid-cols-3 gap-4 text-sm">
                        <div class="bg-white/5 rounded-lg p-3">
                            <i class="fa-solid fa-x-ray text-blue-400 mb-2"></i>
                            <div class="font-semibold">Positioning</div>
                            <div class="text-slate-400">Routine & special projections</div>
                        </div>
                        <div class="bg-white/5 rounded-lg p-3">
                            <i class="fa-solid fa-disease text-rose-400 mb-2"></i>
                            <div class="font-semibold">Pathology</div>
                            <div class="text-slate-400">Disease processes, imaging appearance</div>
                        </div>
                        <div class="bg-white/5 rounded-lg p-3">
                            <i class="fa-solid fa-pills text-amber-400 mb-2"></i>
                            <div class="font-semibold">Pharmacology</div>
                            <div class="text-slate-400">Contrast media, reactions</div>
                        </div>
                    </div>
                </div>

                <!-- Phase 3 -->
                <div class="bg-white/10 backdrop-blur rounded-2xl p-6 border border-white/20">
                    <div class="flex items-center gap-4 mb-4">
                        <div class="w-12 h-12 bg-green-500 rounded-full flex items-center justify-center font-bold text-xl">3</div>
                        <div>
                            <h3 class="font-bold text-xl">Mastery Phase (Weeks 8-10)</h3>
                            <p class="text-green-300 text-sm">Integration & Practice</p>
                        </div>
                    </div>
                    <div class="grid md:grid-cols-3 gap-4 text-sm">
                        <div class="bg-white/5 rounded-lg p-3">
                            <i class="fa-solid fa-laptop-medical text-teal-400 mb-2"></i>
                            <div class="font-semibold">Quality Control</div>
                            <div class="text-slate-400">Testing, troubleshooting</div>
                        </div>
                        <div class="bg-white/5 rounded-lg p-3">
                            <i class="fa-solid fa-headset text-indigo-400 mb-2"></i>
                            <div class="font-semibold">Patient Care</div>
                            <div class="text-slate-400">Communication, ethics, law</div>
                        </div>
                        <div class="bg-white/5 rounded-lg p-3">
                            <i class="fa-solid fa-calculator text-orange-400 mb-2"></i>
                            <div class="font-semibold">Calculations</div>
                            <div class="text-slate-400">Dosage, exposure, grid</div>
                        </div>
                    </div>
                </div>

                <!-- Phase 4 -->
                <div class="bg-gradient-to-r from-amber-500/20 to-orange-500/20 backdrop-blur rounded-2xl p-6 border border-amber-500/30">
                    <div class="flex items-center gap-4 mb-4">
                        <div class="w-12 h-12 bg-amber-500 rounded-full flex items-center justify-center font-bold text-xl">4</div>
                        <div>
                            <h3 class="font-bold text-xl">Exam Phase (Weeks 11-12)</h3>
                            <p class="text-amber-300 text-sm">Review & Simulation</p>
                        </div>
                    </div>
                    <div class="flex gap-4 text-sm">
                        <div class="flex-1 bg-white/5 rounded-lg p-3 text-center">
                            <i class="fa-solid fa-repeat text-amber-400 text-2xl mb-2"></i>
                            <div class="font-semibold">Comprehensive Review</div>
                        </div>
                        <div class="flex-1 bg-white/5 rounded-lg p-3 text-center">
                            <i class="fa-solid fa-clock text-amber-400 text-2xl mb-2"></i>
                            <div class="font-semibold">Timed Practice Exams</div>
                        </div>
                        <div class="flex-1 bg-white/5 rounded-lg p-3 text-center">
                            <i class="fa-solid fa-spa text-amber-400 text-2xl mb-2"></i>
                            <div class="font-semibold">Rest & Confidence</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-slate-950 text-white py-16 px-4 sm:px-6 lg:px-8 border-t border-slate-800">
        <div class="max-w-7xl mx-auto">
            <div class="grid md:grid-cols-4 gap-12 mb-12">
                <div class="col-span-2">
                    <div class="flex items-center space-x-3 mb-6">
                        <div class="w-12 h-12 bg-gradient-to-br from-medical-500 to-teal-500 rounded-xl flex items-center justify-center text-white font-bold text-xl shadow-lg">
                            <i class="fa-solid fa-user-doctor"></i>
                        </div>
                        <div>
                            <h3 class="font-display font-bold text-2xl">CAMRT<span class="text-medical-400">Hub</span></h3>
                            <p class="text-xs text-slate-400">Dedicated to Daniel Dike</p>
                        </div>
                    </div>
                    <p class="text-slate-400 leading-relaxed mb-6 max-w-md">
                        A comprehensive study resource created by Yamoskipo to support Daniel Dike and all aspiring Medical Radiation Technologists in their journey to CAMRT certification excellence.
                    </p>
                    <div class="flex gap-4">
                        <a href="#" class="w-10 h-10 rounded-full bg-slate-800 flex items-center justify-center text-slate-400 hover:bg-medical-600 hover:text-white transition-all">
                            <i class="fa-solid fa-envelope"></i>
                        </a>
                        <a href="#" class="w-10 h-10 rounded-full bg-slate-800 flex items-center justify-center text-slate-400 hover:bg-medical-600 hover:text-white transition-all">
                            <i class="fa-brands fa-twitter"></i>
                        </a>
                        <a href="#" class="w-10 h-10 rounded-full bg-slate-800 flex items-center justify-center text-slate-400 hover:bg-medical-600 hover:text-white transition-all">
                            <i class="fa-brands fa-linkedin"></i>
                        </a>
                    </div>
                </div>
                
                <div>
                    <h4 class="font-bold mb-4 text-medical-400">Quick Links</h4>
                    <ul class="space-y-3 text-sm text-slate-400">
                        <li><a href="https://camrt.ca/" target="_blank" class="hover:text-white transition-colors">Official CAMRT</a></li>
                        <li><a href="https://camrt.ca/certification-4/" target="_blank" class="hover:text-white transition-colors">Certification Portal</a></li>
                        <li><a href="#" class="hover:text-white transition-colors">Study Materials</a></li>
                        <li><a href="#" class="hover:text-white transition-colors">Practice Exams</a></li>
                    </ul>
                </div>

                <div>
                    <h4 class="font-bold mb-4 text-medical-400">Dedication</h4>
                    <div class="bg-slate-900 rounded-xl p-4 border border-slate-800">
                        <p class="text-sm text-slate-400 italic mb-3">"To Daniel Dike, whose dedication to the field of Medical Radiation Technology inspires us all."</p>
                        <p class="text-xs text-slate-500">— Yamoskipo</p>
                    </div>
                </div>
            </div>
            
            <div class="pt-8 border-t border-slate-800 flex flex-col md:flex-row justify-between items-center gap-4">
                <p class="text-slate-500 text-sm">&copy; 2025 CAMRT Exam Hub. Created with dedication for Daniel Dike.</p>
                <div class="flex items-center gap-2 text-slate-600 text-sm">
                    <i class="fa-solid fa-heart text-rose-500"></i>
                    <span>Made by Yamoskipo</span>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Comprehensive Data
        const studyMaterials = {
            guides: [
                { title: "Radiation Physics Fundamentals", type: "PDF", size: "2.4 MB", desc: "Complete guide to x-ray production, interactions, and image formation", icon: "fa-atom" },
                { title: "Patient Care & Communication", type: "PDF", size: "1.8 MB", desc: "Professional standards, patient assessment, and emergency procedures", icon: "fa-user-nurse" },
                { title: "Radiation Protection Protocols", type: "PDF", size: "3.1 MB", desc: "ALARA principles, shielding calculations, and regulatory requirements", icon: "fa-shield-halved" },
                { title: "Image Quality & Evaluation", type: "PDF", size: "2.2 MB", desc: "Technical factors, artifacts, and quality assurance procedures", icon: "fa-image" },
                { title: "Positioning Essentials", type: "PDF", size: "4.5 MB", desc: "Anatomy demonstration, central ray alignment, and positioning terminology", icon: "fa-person" }
            ],
            formulas: [
                { title: "Exposure Calculations", count: "12 formulas", desc: "mAs, time, distance relationships", icon: "fa-clock" },
                { title: "Grid Conversions", count: "8 formulas", desc: "Bucky factors, grid ratios, exposure increase", icon: "fa-border-all" },
                { title: "Radiation Dose", count: "15 formulas", desc: "Absorbed dose, equivalent dose, effective dose", icon: "fa-radiation" },
                { title: "Nuclear Medicine Math", count: "20 formulas", desc: "Decay, dosage, uptake calculations", icon: "fa-calculator" },
                { title: "MRI Physics", count: "10 formulas", desc: "Larmor frequency, TR/TE relationships", icon: "fa-magnet" }
            ],
            protocols: [
                { title: "Chest & Thorax", type: "Protocol", desc: "PA, lateral, decubitus, lordotic views", icon: "fa-lungs" },
                { title: "Abdomen & GI", type: "Protocol", desc: "KUB, acute series, contrast studies", icon: "fa-utensils" },
                { title: "Musculoskeletal", type: "Protocol", desc: "Extremities, spine, pelvis positioning", icon: "fa-bone" },
                { title: "Skull & Sinuses", type: "Protocol", desc: "Facial bones, mandible, TMJ", icon: "fa-skull" },
                { title: "Mobile & Surgical", type: "Protocol", desc: "C-arm, portables, trauma protocols", icon: "fa-truck-medical" }
            ],
            safety: [
                { title: "Quality Control Tests", type: "Checklist", desc: "Daily, weekly, monthly QC procedures", icon: "fa-clipboard-check" },
                { title: "Emergency Response", type: "Guide", desc: "Contrast reactions, equipment failure", icon: "fa-kit-medical" },
                { title: "Infection Control", type: "Protocol", desc: "Standard precautions, sterilization", icon: "fa-virus-slash" },
                { title: "MRI Safety Zones", type: "Poster", desc: "Zone I-IV definitions, screening forms", icon: "fa-magnet" },
                { title: "Radiopharmacy Safety", type: "Manual", desc: "Handling, storage, waste disposal", icon: "fa-biohazard" }
            ]
        };

        const flashcards = [
            { id: 1, category: "physics", front: "What is the photoelectric effect?", back: "The complete absorption of an x-ray photon by an inner shell electron, resulting in ionization.", extra: "Probability ∝ Z³/E³. Dominant in diagnostic range for high Z materials (bone)." },
            { id: 2, category: "anatomy", front: "Name the three meninges from superficial to deep.", back: "Dura mater, Arachnoid mater, Pia mater", extra: "Dura is thick and fibrous, arachnoid is web-like, pia adheres to brain surface." },
            { id: 3, category: "safety", front: "What is the annual dose limit for radiation workers?", back: "50 mSv (5 rem) to whole body per year", extra: "Cumulative limit: 10 mSv × age. Lens of eye: 150 mSv/year. Public: 1 mSv/year." },
            { id: 4, category: "procedures", front: "What is the central ray for an AP chest x-ray?", back: "Mid-sagittal plane at the level of T7 (mid-sternum)", extra: "SID: 180 cm (72 inches). Patient erect, PA preferred to minimize heart magnification." },
            { id: 5, category: "physics", front: "State the Inverse Square Law.", back: "Intensity is inversely proportional to the square of the distance.", extra: "I₁/I₂ = (D₂)²/(D₁)². If distance doubles, intensity decreases to 1/4." },
            { id: 6, category: "anatomy", front: "What structure passes through the transverse foramen of cervical vertebrae?", back: "Vertebral artery and vein", extra: "Found in C1-C6 (not C7). Supplies posterior circulation of brain." },
            { id: 7, category: "safety", front: "What does ALARA stand for?", back: "As Low As Reasonably Achievable", extra: "Economic and social factors considered. Time, distance, shielding are key principles." },
            { id: 8, category: "procedures", front: "What is the purpose of the anode heel effect?", back: "Radiation intensity is greater on the cathode side due to anode angle.", extra: "Use to advantage: place thicker anatomy (abdomen) on cathode side, thinner (lungs) on anode side." },
            { id: 9, category: "physics", front: "What is half-value layer (HVL)?", back: "The thickness of material required to reduce beam intensity by half.", extra: "Indicates beam quality. Diagnostic x-rays: 2-4 mm Al. Therapeutic: expressed in mm Cu or Pb." },
            { id: 10, category: "anatomy", front: "What is the name of the opening at the base of the skull?", back: "Foramen magnum", extra: "Transmits medulla oblongata, meninges, vertebral arteries, spinal accessory nerve (CN XI)." }
        ];

        const anatomyData = {
            brain: {
                title: "Brain Anatomy",
                content: `
                    <div class="relative bg-slate-100 rounded-2xl p-8 h-full">
                        <div class="text-center mb-6">
                            <h3 class="font-bold text-2xl text-slate-900">Axial Brain Section</h3>
                            <p class="text-slate-600">Click hotspots for details</p>
                        </div>
                        <div class="relative w-64 h-64 mx-auto bg-gradient-to-b from-rose-100 to-rose-200 rounded-full border-4 border-white shadow-lg">
                            <div class="anatomy-hotspot" style="top: 20%; left: 50%;" data-label="Frontal Lobe" onclick="showAnatomyDetail('frontal')"></div>
                            <div class="anatomy-hotspot" style="top: 50%; left: 30%;" data-label="Temporal Lobe" onclick="showAnatomyDetail('temporal')"></div>
                            <div class="anatomy-hotspot" style="top: 50%; left: 70%;" data-label="Temporal Lobe" onclick="showAnatomyDetail('temporal')"></div>
                            <div class="anatomy-hotspot" style="top: 30%; left: 50%;" data-label="Corpus Callosum" onclick="showAnatomyDetail('corpus')"></div>
                            <div class="anatomy-hotspot" style="top: 70%; left: 50%;" data-label="Cerebellum" onclick="showAnatomyDetail('cerebellum')"></div>
                        </div>
                        <div id="anatomy-detail" class="mt-6 p-4 bg-white rounded-xl border border-slate-200 hidden">
                            <h4 class="font-bold text-medical-700 mb-2" id="detail-title"></h4>
                            <p class="text-sm text-slate-600" id="detail-content"></p>
                        </div>
                    </div>
                `
            },
            spine: {
                title: "Spinal Anatomy",
                content: `
                    <div class="bg-slate-100 rounded-2xl p-8 h-full">
                        <h3 class="font-bold text-2xl text-slate-900 mb-4">Vertebral Column</h3>
                        <div class="space-y-4">
                            <div class="bg-white p-4 rounded-xl border-l-4 border-cervical-500" style="border-color: #f59e0b;">
                                <h4 class="font-bold text-amber-700">Cervical (C1-C7)</h4>
                                <p class="text-sm text-slate-600">Smallest vertebrae, bifid spinous processes (C2-C6), transverse foramina</p>
                            </div>
                            <div class="bg-white p-4 rounded-xl border-l-4 border-thoracic-500" style="border-color: #3b82f6;">
                                <h4 class="font-bold text-blue-700">Thoracic (T1-T12)</h4>
                                <p class="text-sm text-slate-600">Heart-shaped bodies, costal facets for rib articulation, long spinous processes</p>
                            </div>
                            <div class="bg-white p-4 rounded-xl border-l-4 border-lumbar-500" style="border-color: #10b981;">
                                <h4 class="font-bold text-emerald-700">Lumbar (L1-L5)</h4>
                                <p class="text-sm text-slate-600">Largest vertebrae, kidney-shaped bodies, thick spinous processes</p>
                            </div>
                            <div class="bg-white p-4 rounded-xl border-l-4 border-sacral-500" style="border-color: #8b5cf6;">
                                <h4 class="font-bold text-purple-700">Sacrum (S1-S5 fused)</h4>
                                <p class="text-sm text-slate-600">Triangular bone, sacral canal, anterior/posterior sacral foramina</p>
                            </div>
                        </div>
                    </div>
                `
            }
        };

        const practiceQuestions = [
            {
                discipline: "radiography",
                category: "physics",
                difficulty: "medium",
                question: "If the SID is increased from 100 cm to 180 cm, what is the percentage increase in exposure required to maintain density?",
                options: ["64%", "80%", "224%", "324%"],
                correct: 2,
                explanation: "Using the inverse square law: (180/100)² = 3.24. This means 3.24 times the original mAs is needed, which is a 224% increase (324% - 100% = 224%).",
                reference: "Bushberg, The Essential Physics of Medical Imaging, 4th Ed."
            },
            {
                discipline: "radiography",
                category: "safety",
                difficulty: "easy",
                question: "Which of the following is NOT a cardinal principle of radiation protection?",
                options: ["Time", "Distance", "Shielding", "Voltage"],
                correct: 3,
                explanation: "The three cardinal principles are Time (minimize exposure time), Distance (maximize distance from source), and Shielding (use appropriate barriers). Voltage is a technical factor, not a protection principle.",
                reference: "CAMRT Radiation Protection Guidelines"
            },
            {
                discipline: "mri",
                category: "safety",
                difficulty: "hard",
                question: "What is the specific absorption rate (SAR) limit for whole-body exposure in MRI?",
                options: ["1 W/kg", "2 W/kg", "4 W/kg", "8 W/kg"],
                correct: 2,
                explanation: "FDA guidelines limit whole-body SAR to 4 W/kg averaged over 15 minutes for first-level controlled mode. Normal operating mode limit is 2 W/kg.",
                reference: "ACR MRI Safety Manual"
            }
        ];

        let currentCard = 0;
        let currentPracticeQ = 0;
        let score = { correct: 0, attempted: 0 };
        let filteredCards = [...flashcards];

        // Initialize
        document.addEventListener('DOMContentLoaded', () => {
            switchMaterialTab('guides');
            updateFlashcard();
            loadPracticeQuestion();
        });

        // Navigation
        function scrollToSection(id) {
            document.getElementById(id).scrollIntoView({ behavior: 'smooth' });
        }

        function toggleMobileMenu() {
            // Implementation for mobile menu toggle
        }

        // Materials Tab Switching
        function switchMaterialTab(tab) {
            document.querySelectorAll('.mat-tab').forEach(t => {
                t.classList.remove('bg-medical-600', 'text-white', 'shadow-lg');
                t.classList.add('bg-white', 'text-slate-600');
            });
            document.getElementById(`mat-tab-${tab}`).classList.remove('bg-white', 'text-slate-600');
            document.getElementById(`mat-tab-${tab}`).classList.add('bg-medical-600', 'text-white', 'shadow-lg');

            const container = document.getElementById('materials-content');
            const data = studyMaterials[tab];
            
            container.innerHTML = data.map(item => `
                <div class="bg-white rounded-2xl p-6 shadow-lg hover:shadow-xl transition-all border border-slate-100 flex items-center gap-6">
                    <div class="w-16 h-16 bg-gradient-to-br from-medical-100 to-medical-200 rounded-2xl flex items-center justify-center text-medical-700 text-2xl flex-shrink-0">
                        <i class="fa-solid ${item.icon}"></i>
                    </div>
                    <div class="flex-1">
                        <div class="flex items-center gap-3 mb-1">
                            <h3 class="font-bold text-lg text-slate-900">${item.title}</h3>
                            ${item.type ? `<span class="px-2 py-1 bg-slate-100 text-slate-600 text-xs rounded-lg font-semibold">${item.type}</span>` : ''}
                            ${item.count ? `<span class="px-2 py-1 bg-medical-100 text-medical-700 text-xs rounded-lg font-semibold">${item.count}</span>` : ''}
                            ${item.size ? `<span class="text-xs text-slate-400">${item.size}</span>` : ''}
                        </div>
                        <p class="text-slate-600 text-sm">${item.desc}</p>
                    </div>
                    <button class="px-4 py-2 bg-medical-50 text-medical-700 rounded-lg font-semibold hover:bg-medical-100 transition-colors text-sm">
                        <i class="fa-solid fa-download mr-2"></i>Access
                    </button>
                </div>
            `).join('');
        }

        // Flashcard Functions
        function updateFlashcard() {
            const card = filteredCards[currentCard];
            document.getElementById('fc-front-title').textContent = card.category;
            document.getElementById('fc-front-content').textContent = card.front;
            document.getElementById('fc-back-content').textContent = card.back;
            document.getElementById('fc-back-extra').textContent = card.extra;
            document.getElementById('fc-counter').textContent = `${currentCard + 1} / ${filteredCards.length}`;
            
            // Reset flip
            document.getElementById('flashcard-container').classList.remove('flipped');
        }

        function flipCard() {
            document.getElementById('flashcard-container').classList.toggle('flipped');
        }

        function nextCard() {
            currentCard = (currentCard + 1) % filteredCards.length;
            updateFlashcard();
        }

        function prevCard() {
            currentCard = (currentCard - 1 + filteredCards.length) % filteredCards.length;
            updateFlashcard();
        }

        function filterFlashcards(category) {
            document.querySelectorAll('.fc-filter').forEach(f => {
                f.classList.remove('bg-medical-600', 'text-white');
                f.classList.add('bg-white', 'text-slate-600');
            });
            event.target.classList.remove('bg-white', 'text-slate-600');
            event.target.classList.add('bg-medical-600', 'text-white');

            if (category === 'all') {
                filteredCards = [...flashcards];
            } else {
                filteredCards = flashcards.filter(c => c.category === category);
            }
            currentCard = 0;
            updateFlashcard();
        }

        function shuffleCards() {
            filteredCards.sort(() => Math.random() - 0.5);
            currentCard = 0;
            updateFlashcard();
        }

        // Calculator Functions
        function calculateMas() {
            const ma = parseFloat(document.getElementById('calc-ma').value) || 0;
            const time = parseFloat(document.getElementById('calc-time').value) || 0;
            document.getElementById('result-mas').textContent = (ma * time).toFixed(2);
        }

        function calculate15Rule() {
            const orig = parseFloat(document.getElementById('calc-kvp-orig').value) || 0;
            const dir = document.getElementById('calc-direction').value;
            const result = dir === 'increase' ? orig * 1.15 : orig * 0.85;
            document.getElementById('result-kvp').textContent = result.toFixed(1);
        }

        function calculateSfd() {
            const mas = parseFloat(document.getElementById('calc-mas-orig').value) || 0;
            const sid1 = parseFloat(document.getElementById('calc-sid-orig').value) || 0;
            const sid2 = parseFloat(document.getElementById('calc-sid-new').value) || 0;
            if (sid1 > 0 && sid2 > 0) {
                const result = mas * Math.pow(sid2 / sid1, 2);
                document.getElementById('result-sfd').textContent = result.toFixed(2);
            }
        }

        function calculateGrid() {
            const noGrid = parseFloat(document.getElementById('calc-nogrid').value) || 0;
            const ratio = parseInt(document.getElementById('calc-grid-ratio').value);
            const buckyFactors = { 5: 2, 6: 2.5, 8: 3, 10: 3.5, 12: 4, 16: 5 };
            document.getElementById('result-grid').textContent = (noGrid * buckyFactors[ratio]).toFixed(1);
        }

        // Anatomy Functions
        function showAnatomy(region) {
            const display = document.getElementById('anatomy-display');
            if (anatomyData[region]) {
                display.innerHTML = anatomyData[region].content;
            } else {
                display.innerHTML = `
                    <div class="flex items-center justify-center h-full text-slate-400">
                        <div class="text-center">
                            <i class="fa-solid fa-person text-6xl mb-4"></i>
                            <p>Detailed ${region} anatomy visualization</p>
                            <p class="text-sm mt-2">Coming soon</p>
                        </div>
                    </div>
                `;
            }
        }

        function showAnatomyDetail(part) {
            const details = {
                frontal: { title: "Frontal Lobe", content: "Responsible for executive functions, personality, and motor function (primary motor cortex)." },
                temporal: { title: "Temporal Lobe", content: "Contains auditory cortex and Wernicke's area (language comprehension). Important for memory formation." },
                corpus: { title: "Corpus Callosum", content: "White matter tract connecting cerebral hemispheres. Allows communication between left and right brain." },
                cerebellum: { title: "Cerebellum", content: "Coordinates voluntary movements, balance, and posture. Located in posterior cranial fossa." }
            };
            
            const detail = details[part];
            document.getElementById('detail-title').textContent = detail.title;
            document.getElementById('detail-content').textContent = detail.content;
            document.getElementById('anatomy-detail').classList.remove('hidden');
        }

        // Practice Question Functions
        function loadPracticeQuestion() {
            const q = practiceQuestions[currentPracticeQ];
            document.getElementById('q-text').textContent = q.question;
            document.getElementById('q-discipline').textContent = q.discipline;
            document.getElementById('q-category').textContent = q.category;
            document.getElementById('q-difficulty').textContent = q.difficulty;
            
            const optionsContainer = document.getElementById('q-options');
            optionsContainer.innerHTML = '';
            q.options.forEach((opt, idx) => {
                optionsContainer.innerHTML += `
                    <button onclick="selectPracticeOption(${idx})" class="q-option w-full text-left p-4 rounded-xl border-2 border-slate-200 hover:border-medical-300 transition-all" data-idx="${idx}">
                        <div class="flex items-center gap-3">
                            <div class="w-6 h-6 rounded-full border-2 border-slate-300 flex items-center justify-center">
                                <div class="w-3 h-3 rounded-full bg-medical-500 opacity-0 transition-opacity"></div>
                            </div>
                            <span>${opt}</span>
                        </div>
                    </button>
                `;
            });
            
            document.getElementById('q-explanation').classList.add('hidden');
            document.getElementById('q-check-btn').disabled = false;
            document.getElementById('q-check-btn').textContent = 'Check Answer';
        }

        function selectPracticeOption(idx) {
            document.querySelectorAll('.q-option').forEach(btn => {
                btn.classList.remove('border-medical-500', 'bg-medical-50');
                btn.querySelector('.w-3').classList.add('opacity-0');
            });
            const selected = document.querySelector(`.q-option[data-idx="${idx}"]`);
            selected.classList.add('border-medical-500', 'bg-medical-50');
            selected.querySelector('.w-3').classList.remove('opacity-0');
            window.selectedPracticeOption = idx;
        }

        function checkPracticeAnswer() {
            if (window.selectedPracticeOption === undefined) return;
            
            const q = practiceQuestions[currentPracticeQ];
            const buttons = document.querySelectorAll('.q-option');
            
            buttons[q.correct].classList.remove('border-slate-200', 'border-medical-500');
            buttons[q.correct].classList.add('border-green-500', 'bg-green-50');
            
            if (window.selectedPracticeOption !== q.correct) {
                buttons[window.selectedPracticeOption].classList.remove('border-slate-200', 'border-medical-500');
                buttons[window.selectedPracticeOption].classList.add('border-red-500', 'bg-red-50');
            } else {
                score.correct++;
            }
            
            score.attempted++;
            updateScore();
            
            document.getElementById('q-explanation-text').textContent = q.explanation;
            document.getElementById('q-reference').textContent = `Reference: ${q.reference}`;
            document.getElementById('q-explanation').classList.remove('hidden');
            document.getElementById('q-check-btn').disabled = true;
        }

        function updateScore() {
            document.getElementById('q-score').textContent = `${score.correct}/${score.attempted}`;
            document.getElementById('stat-correct').textContent = score.correct;
            document.getElementById('stat-attempted').textContent = score.attempted;
            const accuracy = score.attempted > 0 ? Math.round((score.correct / score.attempted) * 100) : 0;
            document.getElementById('stat-accuracy').textContent = accuracy + '%';
        }

        function nextQuestion() {
            currentPracticeQ = (currentPracticeQ + 1) % practiceQuestions.length;
            window.selectedPracticeOption = undefined;
            loadPracticeQuestion();
        }

        function prevQuestion() {
            currentPracticeQ = (currentPracticeQ - 1 + practiceQuestions.length) % practiceQuestions.length;
            window.selectedPracticeOption = undefined;
            loadPracticeQuestion();
        }

        function flagQuestion() {
            // Implementation for flagging questions
            alert('Question flagged for review');
        }
    </script>
</body>
</html>
