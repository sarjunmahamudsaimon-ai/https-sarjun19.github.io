<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Sarjun Mahamud - Saymon. | Professional Portfolio</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://unpkg.com/lucide@latest"></script>
    <!-- Font Awesome for better social icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap');
        
        :root {
            --bg-dark: #020617;
            --accent-blue: #3b82f6;
            --accent-purple: #a855f7;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: var(--bg-dark);
            color: #f8fafc;
            overflow-x: hidden;
        }

        .bg-mesh {
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: radial-gradient(circle at 10% 20%, rgba(59, 130, 246, 0.05) 0%, transparent 40%),
                        radial-gradient(circle at 90% 80%, rgba(168, 85, 247, 0.05) 0%, transparent 40%);
            z-index: -1;
        }

        .glass-card {
            background: rgba(15, 23, 42, 0.6);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.05);
            transition: all 0.3s ease;
        }
        
        .glass-card:hover {
            border-color: rgba(59, 130, 246, 0.3);
            transform: translateY(-5px);
        }

        .gradient-text {
            background: linear-gradient(135deg, #60a5fa 0%, #a855f7 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        /* Profile Background Animation (Kept as requested) */
        .profile-container {
            position: relative;
            width: 200px;
            height: 200px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .profile-bg-glow {
            position: absolute;
            width: 100%;
            height: 100%;
            border-radius: 50%;
            background: linear-gradient(45deg, var(--accent-blue), var(--accent-purple));
            filter: blur(25px);
            opacity: 0.6;
            animation: rotate-glow 5s linear infinite;
            z-index: 0;
        }

        @keyframes rotate-glow {
            0% { transform: rotate(0deg) scale(0.95); opacity: 0.4; }
            50% { transform: rotate(180deg) scale(1.1); opacity: 0.7; }
            100% { transform: rotate(360deg) scale(0.95); opacity: 0.4; }
        }

        .profile-img-inner {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            position: relative;
            z-index: 10;
            border: 2px solid rgba(255, 255, 255, 0.1);
            background: var(--bg-dark);
            padding: 2px;
            overflow: hidden;
        }

        .profile-img-inner img {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            object-fit: cover;
        }

        .social-btn {
            width: 38px;
            height: 38px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.05);
            transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            cursor: pointer;
            font-size: 1.1rem;
        }
        
        .social-btn:hover {
            transform: scale(1.2) rotate(8deg);
            color: white;
        }

        /* Original Brand Colors on Hover */
        .social-btn.whatsapp:hover { background-color: #25D366; }
        .social-btn.facebook:hover { background-color: #1877F2; }
        .social-btn.linkedin:hover { background-color: #0077B5; }
        .social-btn.youtube:hover { background-color: #FF0000; }
        .social-btn.instagram:hover { background: linear-gradient(45deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%); }

        .custom-scrollbar::-webkit-scrollbar {
            width: 4px;
        }
        .custom-scrollbar::-webkit-scrollbar-thumb {
            background: #1e293b;
            border-radius: 10px;
        }
    </style>
</head>
<body class="antialiased">

    <div class="bg-mesh"></div>

    <!-- Navigation -->
    <nav class="fixed w-full z-[100] bg-slate-950/80 backdrop-blur-md border-b border-white/5">
        <div class="max-w-7xl mx-auto px-6 h-16 flex items-center justify-between">
            <div class="flex items-center space-x-2 cursor-pointer" onclick="window.scrollTo({top: 0, behavior: 'smooth'})">
                <img src="https://i.ibb.co/9m6B8CXD/sarjun19-logo-at-your-service-png.png" alt="logo" class="h-8">
                <span class="text-lg font-bold">sarjun19.com</span>
            </div>
            <div class="hidden md:flex space-x-6 text-xs font-bold uppercase tracking-widest text-slate-400">
                <a href="#home" class="hover:text-white transition">Home</a>
                <a href="#services" class="hover:text-white transition">Services</a>
                <a href="#contact" class="hover:text-white transition">Contact</a>
                <a href="#reviews" class="hover:text-white transition">Reviews</a>
            </div>
            <div class="flex items-center space-x-2">
                <a href="https://linkedin.com/in/sarjun-mahamud" target="_blank" class="social-btn linkedin"><i class="fa-brands fa-linkedin-in"></i></a>
                <a href="https://facebook.com/sarjun.mahamud" target="_blank" class="social-btn facebook"><i class="fa-brands fa-facebook-f"></i></a>
                <a href="https://wa.me/8801601058174" target="_blank" class="social-btn whatsapp text-green-500 hover:text-white"><i class="fa-brands fa-whatsapp"></i></a>
                <a href="#contact" class="bg-blue-600 text-white px-4 py-2 rounded-lg text-xs font-bold transition hover:bg-blue-500 ml-2">Hire Me</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="pt-32 pb-16 px-6 text-center">
        <div class="max-w-4xl mx-auto">
            <div class="flex justify-center mb-8">
                <div class="profile-container">
                    <div class="profile-bg-glow"></div>
                    <div class="profile-img-inner">
                        <img src="https://i.ibb.co/gZCSJXFF/f12e0fa2-7deb-4f30-b71f-89f3aa86c88a.png" alt="Sarjun Mahamud">
                    </div>
                </div>
            </div>
            <h1 class="text-4xl md:text-6xl font-extrabold mb-4 gradient-text">Sarjun Mahamud - Saymon.</h1>
            <p class="text-slate-400 text-lg mb-8">Professional IT Specialist & Digital Growth Expert</p>
            <div class="flex justify-center gap-4">
                <button onclick="document.getElementById('services').scrollIntoView({behavior: 'smooth'})" class="bg-white text-black px-6 py-3 rounded-xl font-bold hover:bg-slate-200 transition">View Services</button>
                <button onclick="document.getElementById('contact').scrollIntoView({behavior: 'smooth'})" class="glass-card px-6 py-3 rounded-xl font-bold hover:bg-white/10 transition">Contact Me</button>
            </div>
        </div>
    </section>

    <!-- Expert Services Section -->
    <section id="services" class="py-20 px-6">
        <div class="max-w-7xl mx-auto">
            <h2 class="text-2xl font-bold mb-12 text-center uppercase tracking-widest text-slate-400">Expert Services</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                <!-- Service Cards -->
                <div class="glass-card p-6 rounded-2xl group cursor-pointer" onclick="orderService('Cyber Security', 'Full Security Audit & Protection')">
                    <div class="bg-blue-500/20 w-12 h-12 flex items-center justify-center rounded-xl mb-4 group-hover:scale-110 transition">
                        <i data-lucide="shield-check" class="text-blue-500"></i>
                    </div>
                    <h3 class="font-bold mb-2 group-hover:text-blue-400">Cyber Security</h3>
                    <p class="text-slate-400 text-sm mb-4">Ethical Hacking, Website Audit, and Data Protection solutions.</p>
                    <span class="text-blue-400 text-xs font-bold tracking-widest">ORDER NOW →</span>
                </div>
                
                <div class="glass-card p-6 rounded-2xl group cursor-pointer" onclick="orderService('AI Development', 'AI Tools & Automation Integration')">
                    <div class="bg-purple-500/20 w-12 h-12 flex items-center justify-center rounded-xl mb-4 group-hover:scale-110 transition">
                        <i data-lucide="brain-circuit" class="text-purple-500"></i>
                    </div>
                    <h3 class="font-bold mb-2 group-hover:text-purple-400">AI Development</h3>
                    <p class="text-slate-400 text-sm mb-4">Prompt Engineering, AI-based Content Creation & Automation.</p>
                    <span class="text-purple-400 text-xs font-bold tracking-widest">ORDER NOW →</span>
                </div>

                <div class="glass-card p-6 rounded-2xl group cursor-pointer" onclick="orderService('Digital Marketing', 'Growth Hacking & Social Media Ads')">
                    <div class="bg-amber-500/20 w-12 h-12 flex items-center justify-center rounded-xl mb-4 group-hover:scale-110 transition">
                        <i data-lucide="trending-up" class="text-amber-500"></i>
                    </div>
                    <h3 class="font-bold mb-2 group-hover:text-amber-400">Digital Marketing</h3>
                    <p class="text-slate-400 text-sm mb-4">SEO Optimization, Affiliate Marketing, and Social Brand Growth.</p>
                    <span class="text-amber-400 text-xs font-bold tracking-widest">ORDER NOW →</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact & Social Section -->
    <section id="contact" class="py-20 px-6 bg-slate-900/30">
        <div class="max-w-4xl mx-auto">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
                <div>
                    <h2 class="text-3xl font-bold mb-4">Send Message</h2>
                    <form onsubmit="handleContact(event)" class="space-y-4">
                        <input type="text" id="contact-name" placeholder="Full Name" required class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-sm focus:border-blue-500 outline-none">
                        <select id="service-select" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-sm focus:border-blue-500 outline-none">
                            <option value="">Select Category</option>
                            <option value="Cyber Security">Cyber Security</option>
                            <option value="AI Development">AI Development</option>
                            <option value="Digital Marketing">Digital Marketing</option>
                            <option value="Office Applications">MS Applications</option>
                        </select>
                        <textarea id="message-box" rows="4" placeholder="Briefly describe your requirements..." required class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-sm focus:border-blue-500 outline-none"></textarea>
                        <button type="submit" class="w-full py-3 bg-blue-600 text-white font-bold rounded-xl hover:bg-blue-500 transition shadow-lg shadow-blue-900/20">Send Inquiry</button>
                    </form>
                </div>

                <div class="glass-card p-8 rounded-2xl flex flex-col justify-between">
                    <div>
                        <h3 class="text-xl font-bold mb-6">Quick Connectivity</h3>
                        <div class="space-y-5">
                            <a href="https://wa.me/8801601058174" target="_blank" class="flex items-center space-x-3 text-slate-400 hover:text-green-500 transition">
                                <i class="fa-brands fa-whatsapp text-xl w-6"></i>
                                <span class="text-sm">+880 1601 058174</span>
                            </a>
                            <a href="mailto:sarjunmahamudsaimon@gmail.com" class="flex items-center space-x-3 text-slate-400 hover:text-red-400 transition">
                                <i class="fa-regular fa-envelope text-xl w-6"></i>
                                <span class="text-sm">sarjunmahamudsaimon@gmail.com</span>
                            </a>
                        </div>
                    </div>
                    
                    <div class="pt-10">
                        <p class="text-[10px] uppercase tracking-[3px] text-slate-500 mb-4">Follow Me On</p>
                        <div class="flex gap-4">
                            <a href="https://facebook.com/sarjun.mahamud" target="_blank" class="social-btn facebook"><i class="fa-brands fa-facebook-f"></i></a>
                            <a href="https://linkedin.com/in/sarjun-mahamud" target="_blank" class="social-btn linkedin"><i class="fa-brands fa-linkedin-in"></i></a>
                            <a href="https://instagram.com/sarjun_saymon" target="_blank" class="social-btn instagram"><i class="fa-brands fa-instagram"></i></a>
                            <!-- YouTube Icon added next to Instagram -->
                            <a href="https://youtube.com/@sarjunmahamud" target="_blank" class="social-btn youtube"><i class="fa-brands fa-youtube"></i></a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Reviews Section -->
    <section id="reviews" class="py-20 px-6 border-t border-white/5">
        <div class="max-w-4xl mx-auto text-center">
            <h2 class="text-xl font-bold mb-10 text-slate-400 uppercase tracking-widest">Client Feedback</h2>
            <div id="reviews-container" class="grid grid-cols-1 md:grid-cols-2 gap-4 text-left">
                <div class="glass-card p-4 rounded-xl border-l-2 border-blue-500">
                    <div class="flex justify-between items-center mb-2">
                        <span class="font-bold text-xs">Ariful Islam</span>
                        <div class="flex text-amber-400"><i data-lucide="star" class="w-3 h-3 fill-current"></i><i data-lucide="star" class="w-3 h-3 fill-current"></i><i data-lucide="star" class="w-3 h-3 fill-current"></i><i data-lucide="star" class="w-3 h-3 fill-current"></i><i data-lucide="star" class="w-3 h-3 fill-current"></i></div>
                    </div>
                    <p class="text-slate-400 text-xs italic">"Great experience working with Saymon. His technical skills are outstanding!"</p>
                </div>
            </div>
        </div>
    </section>

    <footer class="py-10 px-6 border-t border-white/5 text-center">
        <p class="text-[10px] text-slate-600 tracking-widest uppercase">© 2024 Sarjun Mahamud - Saymon. All Rights Reserved.</p>
    </footer>

    <script>
        lucide.createIcons();

        // Optimized Service Order Logic
        function orderService(category, details) {
            const select = document.getElementById('service-select');
            const message = document.getElementById('message-box');
            const contactSection = document.getElementById('contact');
            
            if(select) select.value = category;
            if(message) message.value = "I'm looking for " + category + " service specifically: " + details;
            
            contactSection.scrollIntoView({ behavior: 'smooth' });
        }

        // Contact Form Handling
        function handleContact(e) {
            e.preventDefault();
            const name = document.getElementById('contact-name').value;
            alert("Dhonnobad " + name + "! Apnar message-ti Sarjun-er kache pouchano hoyeche. Khub shiggory jogajog kora hobe.");
            e.target.reset();
        }

        // Smooth Scroll for Navigation Links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const targetId = this.getAttribute('href').slice(1);
                const targetElement = document.getElementById(targetId);
                if (targetElement) {
                    targetElement.scrollIntoView({
                        behavior: 'smooth'
                    });
                }
            });
        });
    </script>
</body>
</html>
