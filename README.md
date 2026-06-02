<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Verma Tours & Taxi - Premium Travel Experience</title>
    
    <!-- Google Fonts: Poppins -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    
    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        poppins: ['Poppins', 'sans-serif'],
                    },
                    colors: {
                        brand: {
                            gold: '#fbbf24', // amber-400
                            dark: '#0f172a', // slate-900
                            light: '#f8fafc' // slate-50
                        }
                    }
                }
            }
        }
    </script>

    <style>
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #0f172a;
            color: #f8fafc;
            overflow-x: hidden;
        }

        /* Animated Gradient Background for Hero */
        .hero-bg {
            background: linear-gradient(-45deg, #0f172a, #1e293b, #020617, #1e1b4b);
            background-size: 400% 400%;
            animation: gradientBG 12s ease infinite;
        }

        @keyframes gradientBG {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* Floating Animation */
        .animate-float {
            animation: float 4s ease-in-out infinite;
        }

        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-12px); }
            100% { transform: translateY(0px); }
        }

        /* Glassmorphism Cards */
        .glass-card {
            background: rgba(30, 41, 59, 0.7);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.08);
            position: relative;
            overflow: hidden;
        }

        .glass-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: -100%;
            width: 50%;
            height: 100%;
            background: linear-gradient(120deg, transparent, rgba(255, 255, 255, 0.05), transparent);
            transition: all 0.6s ease;
            transform: skewX(-20deg);
        }

        .glass-card:hover::before {
            left: 150%;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 10px;
        }
        ::-webkit-scrollbar-track {
            background: #0f172a; 
        }
        ::-webkit-scrollbar-thumb {
            background: #334155; 
            border-radius: 5px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #fbbf24; 
        }
    </style>
</head>

<body class="antialiased selection:bg-brand-gold selection:text-brand-dark">

    <!-- HEADER / NAVIGATION -->
    <nav id="navbar" class="fixed w-full z-50 top-0 transition-all duration-300 backdrop-blur-md bg-slate-900/80 border-b border-slate-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <!-- Logo -->
                <a href="#" class="flex items-center gap-3 cursor-pointer">
                    <div class="w-10 h-10 bg-brand-gold/15 rounded-lg flex items-center justify-center border border-brand-gold/35">
                        <i class="fa-solid fa-taxi text-brand-gold text-xl"></i>
                    </div>
                    <span class="font-bold text-2xl tracking-tight text-white">Verma<span class="text-brand-gold">Tours</span></span>
                </a>
                
                <!-- Desktop Links -->
                <div class="hidden md:flex space-x-8 items-center">
                    <a href="#services" class="text-slate-300 hover:text-brand-gold transition-colors font-medium text-sm">Services</a>
                    <a href="#fleet" class="text-slate-300 hover:text-brand-gold transition-colors font-medium text-sm">Our Fleet</a>
                    <a href="#destinations" class="text-slate-300 hover:text-brand-gold transition-colors font-medium text-sm">Destinations</a>
                    <a href="#faq" class="text-slate-300 hover:text-brand-gold transition-colors font-medium text-sm">FAQs</a>
                    <a href="#contact" class="text-slate-300 hover:text-brand-gold transition-colors font-medium text-sm">Contact</a>
                    <a href="https://wa.me/919991650628" target="_blank" class="bg-green-500 hover:bg-green-400 text-white px-5 py-2.5 rounded-full font-semibold transition-all shadow-lg shadow-green-500/30 flex items-center gap-2 hover:-translate-y-1">
                        <i class="fa-brands fa-whatsapp text-lg"></i> Book Now
                    </a>
                </div>

                <!-- Hamburger Menu Button -->
                <div class="md:hidden">
                    <button id="menu-btn" class="text-slate-300 hover:text-brand-gold focus:outline-none p-2">
                        <i class="fa-solid fa-bars text-2xl"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Side Navigation Drawer -->
        <div id="mobile-menu" class="hidden md:hidden bg-slate-950/95 border-b border-slate-800 transition-all duration-300 ease-in-out">
            <div class="px-4 pt-4 pb-6 space-y-3 flex flex-col">
                <a href="#services" class="mobile-nav-link text-slate-300 hover:text-brand-gold py-2 border-b border-slate-900 transition-colors">Our Services</a>
                <a href="#fleet" class="mobile-nav-link text-slate-300 hover:text-brand-gold py-2 border-b border-slate-900 transition-colors">Our Fleet</a>
                <a href="#destinations" class="mobile-nav-link text-slate-300 hover:text-brand-gold py-2 border-b border-slate-900 transition-colors">Destinations</a>
                <a href="#faq" class="mobile-nav-link text-slate-300 hover:text-brand-gold py-2 border-b border-slate-900 transition-colors">FAQs</a>
                <a href="#contact" class="mobile-nav-link text-slate-300 hover:text-brand-gold py-2 transition-colors">Contact</a>
                <a href="https://wa.me/919991650628" target="_blank" class="bg-green-500 hover:bg-green-400 text-white py-3 rounded-full font-semibold text-center shadow-lg flex items-center justify-center gap-2">
                    <i class="fa-brands fa-whatsapp text-lg"></i> Instant WhatsApp Booking
                </a>
            </div>
        </div>
    </nav>

    <!-- HERO SECTION -->
    <section class="hero-bg min-h-screen flex flex-col justify-center items-center text-center px-4 relative pt-24 pb-16">
        <!-- Grid overlay pattern -->
        <div class="absolute inset-0 bg-[url('data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjAiIGhlaWdodD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PGNpcmNsZSBjeD0iMSIgY3k9IjEiIHI9IjEiIGZpbGw9InJnYmEoMjU1LDI1NSwyNTUsMC4wNSkiLz48L3N2Zz4=')] opacity-50"></div>
        
        <div class="z-10 max-w-4xl mx-auto">
            <div class="inline-block mb-6 px-4 py-1.5 rounded-full border border-brand-gold/30 bg-brand-gold/10 text-brand-gold text-xs sm:text-sm font-semibold tracking-wide backdrop-blur-sm">
                🌟 PREMIUM OUTSTATION & LOCAL TRAVEL EXPERTS
            </div>
            <h1 class="text-4xl sm:text-6xl md:text-7xl font-extrabold mb-6 leading-tight animate-float">
                Verma Tours & <span class="text-transparent bg-clip-text bg-gradient-to-r from-brand-gold to-yellow-200">Taxi</span>
            </h1>
            <p class="text-base sm:text-xl md:text-2xl text-slate-300 mb-10 font-light max-w-2xl mx-auto px-4">
                Luxury Feel <span class="text-brand-gold">•</span> Budget Price <span class="text-brand-gold">•</span> Safe Travel
            </p>
            
            <div class="flex flex-col sm:flex-row gap-4 justify-center items-center px-4">
                <a href="https://wa.me/919991650628" target="_blank" class="w-full sm:w-auto px-8 py-4 bg-green-500 text-white rounded-full font-bold text-lg shadow-xl shadow-green-500/20 transition-all hover:bg-green-400 hover:-translate-y-1 flex items-center justify-center gap-2">
                    <i class="fa-brands fa-whatsapp text-xl"></i> WhatsApp Booking
                </a>
                <a href="#contact" class="w-full sm:w-auto px-8 py-4 bg-slate-800 hover:bg-slate-700 text-white rounded-full font-bold text-lg transition-all hover:-translate-y-1 flex items-center justify-center gap-2">
                    <i class="fa-solid fa-phone"></i> Contact Us
                </a>
            </div>

            <!-- Trust Badges -->
            <div class="grid grid-cols-3 gap-4 mt-16 max-w-xl mx-auto border-t border-slate-800/60 pt-8 text-center px-4">
                <div>
                    <div class="text-brand-gold text-2xl sm:text-3xl font-bold">100%</div>
                    <div class="text-[10px] sm:text-xs text-slate-400 uppercase tracking-widest mt-1">Safe & Reliable</div>
                </div>
                <div class="border-x border-slate-800/60">
                    <div class="text-brand-gold text-2xl sm:text-3xl font-bold">5.0 ★</div>
                    <div class="text-[10px] sm:text-xs text-slate-400 uppercase tracking-widest mt-1">Highest Rating</div>
                </div>
                <div>
                    <div class="text-brand-gold text-2xl sm:text-3xl font-bold">24/7</div>
                    <div class="text-[10px] sm:text-xs text-slate-400 uppercase tracking-widest mt-1">Active Support</div>
                </div>
            </div>
        </div>
        
        <!-- Scroll indicator -->
        <div class="absolute bottom-6 left-1/2 transform -translate-x-1/2 animate-bounce text-slate-400">
            <i class="fa-solid fa-chevron-down text-xl"></i>
        </div>
    </section>

    <!-- PREMIUM FLEET SHOWCASE -->
    <section id="fleet" class="py-24 px-4 bg-slate-900 relative">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-16">
                <span class="text-brand-gold text-sm font-semibold tracking-wider uppercase">Our Premium Ride</span>
                <h2 class="text-3xl md:text-4xl font-bold text-white mt-2">Our Featured <span class="text-brand-gold">Vehicle</span></h2>
                <div class="w-16 h-1 bg-brand-gold mx-auto rounded-full mt-4"></div>
                <p class="mt-4 text-slate-400 text-sm md:text-base max-w-xl mx-auto">Impeccably clean, fully air-conditioned Maruti Suzuki Ertiga ready for your comfort.</p>
            </div>

            <!-- Single Fleet Centered Grid -->
            <div class="max-w-3xl mx-auto">
                <!-- Vehicle: Ertiga Only -->
                <div class="glass-card rounded-3xl overflow-hidden border border-slate-800 grid grid-cols-1 md:grid-cols-2 shadow-2xl">
                    <div class="h-64 md:h-auto overflow-hidden bg-slate-950 relative">
                        <img src="https://images.unsplash.com/photo-1533473359331-0135ef1b58bf?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Maruti Ertiga" class="w-full h-full object-cover">
                        <span class="absolute top-4 right-4 bg-brand-gold text-slate-900 text-xs font-bold px-3 py-1 rounded-full">Primary Vehicle</span>
                    </div>
                    <div class="p-8 flex flex-col justify-between">
                        <div>
                            <div class="flex items-center gap-2 mb-2">
                                <h3 class="text-2xl font-bold text-white">Maruti Suzuki Ertiga</h3>
                                <span class="bg-slate-800 text-brand-gold text-xs font-semibold px-2.5 py-0.5 rounded-full border border-brand-gold/20">SUV Comfort</span>
                            </div>
                            <p class="text-slate-400 text-sm mb-6 leading-relaxed">The perfect choice for families, tourist groups, and long-distance outstation travel. Exceptionally spacious, dual AC vents, smooth highway suspension, and deep luggage capacity.</p>
                            
                            <div class="grid grid-cols-3 gap-4 border-y border-slate-800/80 py-4 mb-6 text-center text-xs text-slate-300">
                                <div>
                                    <i class="fa-solid fa-user-group text-brand-gold text-lg mb-1 block"></i>
                                    <span>6+1 Seats</span>
                                </div>
                                <div>
                                    <i class="fa-solid fa-snowflake text-brand-gold text-lg mb-1 block"></i>
                                    <span>Dual AC</span>
                                </div>
                                <div>
                                    <i class="fa-solid fa-suitcase text-brand-gold text-lg mb-1 block"></i>
                                    <span>Heavy Boot</span>
                                </div>
                            </div>
                        </div>
                        
                        <div class="flex items-center justify-between">
                            <div>
                                <span class="text-xs text-slate-500 font-medium">Estimated Pricing Range</span>
                                <div class="text-xl font-bold text-brand-gold">Flexible Fares</div>
                                <span class="text-[10px] text-slate-400 block mt-0.5">*Varies with route & demands</span>
                            </div>
                            <a href="https://wa.me/919991650628?text=Hello%2C%20I'm%20interested%20in%20booking%20your%207-seater%20Ertiga%20for%20a%20tour%20trip!" target="_blank" class="bg-green-500 hover:bg-green-400 text-white text-xs font-bold px-5 py-3 rounded-xl transition-all shadow-md shadow-green-500/10 flex items-center gap-1.5 hover:scale-105">
                                <i class="fa-brands fa-whatsapp text-sm"></i> Book on WhatsApp
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- POPULAR DESTINATIONS -->
    <section id="destinations" class="py-24 px-4 bg-slate-850">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-16">
                <span class="text-brand-gold text-sm font-semibold tracking-wider uppercase">Fascinating Trips</span>
                <h2 class="text-3xl md:text-4xl font-bold text-white mt-2">Popular <span class="text-brand-gold">Destinations</span></h2>
                <div class="w-16 h-1 bg-brand-gold mx-auto rounded-full mt-4"></div>
                <p class="mt-4 text-slate-400 text-sm md:text-base">Explore the absolute best travel hot-spots with our certified mountain drivers.</p>
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
                <!-- Dest 1 -->
                <a href="https://wa.me/919991650628?text=Hello%20Verma%20Tours%2C%20I'm%20inquiring%20about%20a%20flexible%20Ertiga%20tour%20package%20to%20Rishikesh%20from%20Barwala." target="_blank" class="group relative h-72 rounded-2xl overflow-hidden cursor-pointer shadow-lg block">
                    <img src="https://images.unsplash.com/photo-1626082929543-6c70b2401614?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Rishikesh" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                    <div class="absolute inset-0 bg-gradient-to-t from-slate-950 via-slate-900/40 to-transparent"></div>
                    <div class="absolute bottom-0 left-0 p-6">
                        <h3 class="text-2xl font-bold text-white mb-1">Rishikesh</h3>
                        <p class="text-slate-400 text-xs mb-2">Yoga Capital & White-Water River Rafting</p>
                        <p class="text-brand-gold text-sm font-semibold opacity-0 group-hover:opacity-100 transition-opacity duration-300 transform translate-y-2 group-hover:translate-y-0 flex items-center gap-1">Inquire Quote on WhatsApp <i class="fa-solid fa-arrow-right text-xs"></i></p>
                    </div>
                </a>
                <!-- Dest 2 -->
                <a href="https://wa.me/919991650628?text=Hello%20Verma%20Tours%2C%20I'm%20inquiring%20about%20a%20flexible%20Ertiga%20tour%20package%20to%20Manali%20from%20Barwala." target="_blank" class="group relative h-72 rounded-2xl overflow-hidden cursor-pointer shadow-lg block">
                    <img src="https://images.unsplash.com/photo-1605640840605-14ac1855827b?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Manali" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                    <div class="absolute inset-0 bg-gradient-to-t from-slate-950 via-slate-900/40 to-transparent"></div>
                    <div class="absolute bottom-0 left-0 p-6">
                        <h3 class="text-2xl font-bold text-white mb-1">Manali</h3>
                        <p class="text-slate-400 text-xs mb-2">Snowy Valleys, Rohtang Pass, & Solang Valley</p>
                        <p class="text-brand-gold text-sm font-semibold opacity-0 group-hover:opacity-100 transition-opacity duration-300 transform translate-y-2 group-hover:translate-y-0 flex items-center gap-1">Inquire Quote on WhatsApp <i class="fa-solid fa-arrow-right text-xs"></i></p>
                    </div>
                </a>
                <!-- Dest 3 -->
                <a href="https://wa.me/919991650628?text=Hello%20Verma%20Tours%2C%20I'm%20inquiring%20about%20a%20flexible%20Ertiga%20tour%20package%20to%20Shimla%20from%20Barwala." target="_blank" class="group relative h-72 rounded-2xl overflow-hidden cursor-pointer shadow-lg block">
                    <img src="https://images.unsplash.com/photo-1596895111956-bf5705315225?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Shimla" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                    <div class="absolute inset-0 bg-gradient-to-t from-slate-950 via-slate-900/40 to-transparent"></div>
                    <div class="absolute bottom-0 left-0 p-6">
                        <h3 class="text-2xl font-bold text-white mb-1">Shimla</h3>
                        <p class="text-slate-400 text-xs mb-2">The Mall Road, Ridge, & Pine Forests</p>
                        <p class="text-brand-gold text-sm font-semibold opacity-0 group-hover:opacity-100 transition-opacity duration-300 transform translate-y-2 group-hover:translate-y-0 flex items-center gap-1">Inquire Quote on WhatsApp <i class="fa-solid fa-arrow-right text-xs"></i></p>
                    </div>
                </a>
                <!-- Dest 4 -->
                <a href="https://wa.me/919991650628?text=Hello%20Verma%20Tours%2C%20I'm%20inquiring%20about%20an%20Ertiga%20airport%20transfer%20trip%20to%20or%20from%20Delhi%20Airport." target="_blank" class="group relative h-72 rounded-2xl overflow-hidden cursor-pointer shadow-lg block">
                    <img src="https://images.unsplash.com/photo-1587474260580-c5e3d7a8e833?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Delhi" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-# Verma-tour-travel-