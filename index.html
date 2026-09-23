<html lang="vi" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Trần Anh Khoa (SPK) - Bio Link</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        brand: {
                            50: '#f0f9ff',
                            500: '#0ea5e9',
                            600: '#0284c7',
                            700: '#0369a1',
                        }
                    },
                    animation: {
                        'pulse-slow': 'pulse 4s cubic-bezier(0.4, 0, 0.6, 1) infinite',
                        'float': 'float 6s ease-in-out infinite',
                    },
                    keyframes: {
                        float: {
                            '0%, 100%': { transform: 'translateY(0px)' },
                            '50%': { transform: 'translateY(-6px)' },
                        }
                    }
                }
            }
        }
    </script>

    <!-- FontAwesome Icons & Google Fonts -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <!-- QR Code Generator Library -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>

    <style>
        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            -webkit-tap-highlight-color: transparent;
        }

        /* Glassmorphism Styles */
        .glass-panel {
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.5);
        }

        .dark .glass-panel {
            background: rgba(15, 23, 42, 0.85);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.08);
        }

        .glass-card {
            background: rgba(255, 255, 255, 0.7);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(229, 231, 235, 0.8);
            transition: all 0.25s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .dark .glass-card {
            background: rgba(30, 41, 59, 0.7);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.06);
        }

        .glass-card:active, .glass-card:hover {
            transform: translateY(-2px) scale(1.005);
            box-shadow: 0 8px 20px -6px rgba(0, 0, 0, 0.12);
        }

        .dark .glass-card:active, .dark .glass-card:hover {
            box-shadow: 0 8px 20px -6px rgba(0, 0, 0, 0.4);
            border-color: rgba(56, 189, 248, 0.3);
        }

        /* Toast Popup Animation */
        @keyframes slideUp {
            from { transform: translateY(100%) translateX(-50%); opacity: 0; }
            to { transform: translateY(0) translateX(-50%); opacity: 1; }
        }

        .toast-animate {
            animation: slideUp 0.3s cubic-bezier(0.18, 0.89, 0.32, 1.28) forwards;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 4px;
        }
        ::-webkit-scrollbar-track {
            background: transparent;
        }
        ::-webkit-scrollbar-thumb {
            background: rgba(156, 163, 175, 0.4);
            border-radius: 20px;
        }
    </style>
</head>
<body class="bg-slate-100 dark:bg-slate-950 text-slate-800 dark:text-slate-100 min-h-screen transition-colors duration-300 flex justify-center items-start sm:py-6 selection:bg-sky-500 selection:text-white">

    <!-- Toast Notification -->
    <div id="toast" class="hidden fixed bottom-5 left-1/2 -translate-x-1/2 z-50 bg-slate-900/90 dark:bg-white/95 text-white dark:text-slate-900 px-4 py-2.5 rounded-xl shadow-2xl backdrop-blur-md text-xs font-semibold flex items-center gap-2 toast-animate">
        <i class="fa-solid fa-circle-check text-emerald-400 dark:text-emerald-600 text-sm"></i>
        <span id="toast-message">Đã sao chép vào bộ nhớ tạm!</span>
    </div>

    <!-- Main Mobile Container -->
    <div class="w-full max-w-sm sm:max-w-md min-h-screen sm:min-h-0 sm:rounded-3xl flex flex-col relative overflow-hidden shadow-xl sm:shadow-2xl bg-white/70 dark:bg-slate-900/70 backdrop-blur-3xl border-0 sm:border border-slate-200/60 dark:border-slate-800/60">
        
        <!-- Action Buttons -->
        <div class="absolute top-3 right-3 left-3 z-20 flex justify-between items-center">
            <button id="theme-toggle" onclick="toggleTheme()" class="w-8 h-8 rounded-full glass-panel flex items-center justify-center text-slate-700 dark:text-slate-200 active:scale-90 transition-all shadow-md" title="Đổi giao diện">
                <i class="fa-solid fa-moon dark:hidden text-xs"></i>
                <i class="fa-solid fa-sun hidden dark:block text-amber-400 text-xs"></i>
            </button>

            <div class="flex gap-2">
                <button onclick="openQRModal()" class="w-8 h-8 rounded-full glass-panel flex items-center justify-center text-slate-700 dark:text-slate-200 active:scale-90 transition-all shadow-md" title="Mã QR">
                    <i class="fa-solid fa-qrcode text-xs"></i>
                </button>
                <button onclick="shareProfile()" class="w-8 h-8 rounded-full glass-panel flex items-center justify-center text-slate-700 dark:text-slate-200 active:scale-90 transition-all shadow-md" title="Chia sẻ">
                    <i class="fa-solid fa-share-nodes text-xs"></i>
                </button>
            </div>
        </div>

        <!-- Cover Photo -->
        <div class="h-44 w-full relative overflow-hidden bg-slate-800 flex-shrink-0">
            <img id="cover-img" 
                 src="https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=1200&q=80" 
                 alt="Cover Photo Lighthouse" 
                 class="w-full h-full object-cover object-center filter brightness-95 dark:brightness-90 transition-transform duration-700 hover:scale-105">
            <div class="absolute inset-0 bg-gradient-to-b from-black/20 via-transparent to-white dark:to-slate-900"></div>
        </div>

        <!-- Main Content -->
        <div class="px-4 sm:px-5 relative flex-1 flex flex-col -mt-14 z-10">
            
            <!-- Avatar Section -->
            <div class="flex flex-col items-center mb-3">
                <div class="relative group">
                    <div class="absolute -inset-0.5 bg-gradient-to-r from-sky-400 to-blue-600 rounded-full blur opacity-60 group-hover:opacity-100 transition duration-500 animate-pulse-slow"></div>
                    <div class="relative w-24 h-24 rounded-full p-0.5 bg-white dark:bg-slate-900 shadow-xl">
                        <img id="avatar-img" 
                             src="https://scontent.fdad3-8.fna.fbcdn.net/v/t39.30808-6/814999473_2832030020509538_2916820980541575312_n.jpg?stp=dst-jpg_tt6&cstp=mx800x800&ctp=s800x800&_nc_cat=100&ccb=1-7&_nc_sid=6ee11a&_nc_ohc=b66FVPJ1GuwQ7kNvwFEoIpN&_nc_oc=AdrY5oOGxegWO0NH_lYMTs7G-mEy25pF6lHYG11RQywD75sJ0o7z8cswN2fs9DIj4cY&_nc_zt=23&_nc_ht=scontent.fdad3-8.fna&_nc_gid=ywyp8MN02jYBRUK7qQX77w&_nc_ss=7b289&oh=00_AQIEj48jNvvnPM8VMjPqSsN1m1SJrADF-mM4zr8gyDna7g&oe=6AB91C12" 
                             alt="Trần Anh Khoa" 
                             class="w-full h-full object-cover rounded-full transition duration-300">
                    </div>
                    <!-- Verified Badge -->
                    <div class="absolute bottom-1 right-1 bg-sky-500 text-white rounded-full w-5 h-5 flex items-center justify-center text-[10px] shadow-md border-2 border-white dark:border-slate-900" title="Xác minh chính chủ">
                        <i class="fa-solid fa-check"></i>
                    </div>
                </div>

                <!-- Name & Title -->
                <div class="text-center mt-2">
                    <h1 class="text-lg font-bold text-slate-900 dark:text-white tracking-tight flex items-center justify-center gap-1.5">
                        Trần Anh Khoa 
                        <span class="text-[11px] font-semibold text-sky-600 dark:text-sky-400 bg-sky-100 dark:bg-sky-950/80 px-2 py-0.2 rounded-full border border-sky-200 dark:border-sky-800/80">(SPK)</span>
                    </h1>
                    <p class="text-[12px] font-medium text-slate-600 dark:text-slate-300 mt-0.5 max-w-[280px] leading-snug">
                        Nhân viên Hành chính tổng hợp, Trung tâm Dịch vụ sự nghiệp công phường An Cựu
                    </p>
                </div>
            </div>

            <!-- Certificates Badges -->
            <div class="space-y-1.5 mb-4">
                <div class="glass-card p-2.5 rounded-xl flex items-center gap-2.5">
                    <div class="w-6 h-6 rounded-lg bg-amber-500/10 text-amber-600 dark:text-amber-400 flex items-center justify-center flex-shrink-0 text-xs">
                        <i class="fa-solid fa-award"></i>
                    </div>
                    <span class="text-[11px] font-medium text-slate-700 dark:text-slate-200 leading-snug">
                        Giấy chứng nhận của Khoa Quản trị Kinh doanh
                    </span>
                </div>

                <div class="glass-card p-2.5 rounded-xl flex items-center gap-2.5">
                    <div class="w-6 h-6 rounded-lg bg-blue-500/10 text-blue-600 dark:text-blue-400 flex items-center justify-center flex-shrink-0 text-xs">
                        <i class="fa-solid fa-laptop-code"></i>
                    </div>
                    <span class="text-[11px] font-medium text-slate-700 dark:text-slate-200 leading-snug">
                        Giấy chứng nhận dự án H&M Study Buddy - Nền tảng học tập trực tuyến
                    </span>
                </div>

                <div class="glass-card p-2.5 rounded-xl flex items-center gap-2.5">
                    <div class="w-6 h-6 rounded-lg bg-emerald-500/10 text-emerald-600 dark:text-emerald-400 flex items-center justify-center flex-shrink-0 text-xs">
                        <i class="fa-solid fa-chart-line"></i>
                    </div>
                    <span class="text-[11px] font-medium text-slate-700 dark:text-slate-200 leading-snug">
                        Giấy chứng nhận Quản lý năng suất và chất lượng của Học viện Tài Chính
                    </span>
                </div>

                <div class="glass-card p-2.5 rounded-xl flex items-center gap-2.5">
                    <div class="w-6 h-6 rounded-lg bg-purple-500/10 text-purple-600 dark:text-purple-400 flex items-center justify-center flex-shrink-0 text-xs">
                        <i class="fa-solid fa-graduation-cap"></i>
                    </div>
                    <span class="text-[11px] font-medium text-slate-700 dark:text-slate-200 leading-snug">
                        Giấy chứng nhận Bồi dưỡng, tập huấn kỹ năng số cơ bản cho cán bộ, viên chức
                    </span>
                </div>
            </div>

            <!-- Social Links Grid -->
            <div class="grid grid-cols-4 gap-2 mb-4">
                <a href="https://facebook.com" target="_blank" class="glass-card py-2.5 rounded-xl flex flex-col items-center justify-center text-slate-700 dark:text-slate-200 hover:text-blue-600 dark:hover:text-blue-400">
                    <i class="fa-brands fa-facebook text-lg"></i>
                    <span class="text-[9px] font-bold mt-0.5">Facebook</span>
                </a>
                <a href="https://instagram.com" target="_blank" class="glass-card py-2.5 rounded-xl flex flex-col items-center justify-center text-slate-700 dark:text-slate-200 hover:text-pink-600 dark:hover:text-pink-400">
                    <i class="fa-brands fa-instagram text-lg"></i>
                    <span class="text-[9px] font-bold mt-0.5">Instagram</span>
                </a>
                <a href="https://youtube.com" target="_blank" class="glass-card py-2.5 rounded-xl flex flex-col items-center justify-center text-slate-700 dark:text-slate-200 hover:text-red-600 dark:hover:text-red-400">
                    <i class="fa-brands fa-youtube text-lg"></i>
                    <span class="text-[9px] font-bold mt-0.5">YouTube</span>
                </a>
                <a href="https://tiktok.com" target="_blank" class="glass-card py-2.5 rounded-xl flex flex-col items-center justify-center text-slate-700 dark:text-slate-200 hover:text-slate-900 dark:hover:text-white">
                    <i class="fa-brands fa-tiktok text-lg"></i>
                    <span class="text-[9px] font-bold mt-0.5">TikTok</span>
                </a>
            </div>

            <!-- Contact Actions -->
            <div class="space-y-2 mb-6">
                
                <!-- Email -->
                <div class="glass-card p-2.5 rounded-xl flex items-center justify-between group">
                    <a href="mailto:anhkhoat363@gmail.com" class="flex items-center gap-2.5 flex-1 min-w-0">
                        <div class="w-8 h-8 rounded-lg bg-red-500/10 text-red-500 flex items-center justify-center flex-shrink-0 text-sm">
                            <i class="fa-solid fa-envelope"></i>
                        </div>
                        <div class="min-w-0">
                            <div class="text-[9px] font-bold text-slate-400 dark:text-slate-500 uppercase tracking-wider">Gmail</div>
                            <div class="text-[12px] font-bold text-slate-800 dark:text-slate-100 truncate">anhkhoat363@gmail.com</div>
                        </div>
                    </a>
                    <button onclick="copyText('anhkhoat363@gmail.com', 'Gmail')" class="w-7 h-7 rounded-lg glass-panel flex items-center justify-center text-slate-400 hover:text-slate-700 dark:hover:text-slate-200 active:scale-90 transition-all ml-1" title="Sao chép">
                        <i class="fa-regular fa-copy text-xs"></i>
                    </button>
                </div>

                <!-- Phone -->
                <div class="glass-card p-2.5 rounded-xl flex items-center justify-between group">
                    <a href="tel:0899997781" class="flex items-center gap-2.5 flex-1 min-w-0">
                        <div class="w-8 h-8 rounded-lg bg-emerald-500/10 text-emerald-500 flex items-center justify-center flex-shrink-0 text-sm">
                            <i class="fa-solid fa-phone"></i>
                        </div>
                        <div class="min-w-0">
                            <div class="text-[9px] font-bold text-slate-400 dark:text-slate-500 uppercase tracking-wider">Điện thoại</div>
                            <div class="text-[12px] font-bold text-slate-800 dark:text-slate-100 truncate">0899997781</div>
                        </div>
                    </a>
                    <button onclick="copyText('0899997781', 'Số điện thoại')" class="w-7 h-7 rounded-lg glass-panel flex items-center justify-center text-slate-400 hover:text-slate-700 dark:hover:text-slate-200 active:scale-90 transition-all ml-1" title="Sao chép">
                        <i class="fa-regular fa-copy text-xs"></i>
                    </button>
                </div>

                <!-- Zalo -->
                <div class="glass-card p-2.5 rounded-xl flex items-center justify-between group">
                    <a href="https://zalo.me/0562242242" target="_blank" class="flex items-center gap-2.5 flex-1 min-w-0">
                        <div class="w-8 h-8 rounded-lg bg-blue-500/10 text-blue-500 flex items-center justify-center flex-shrink-0 text-[11px] font-black">
                            Zalo
                        </div>
                        <div class="min-w-0">
                            <div class="text-[9px] font-bold text-slate-400 dark:text-slate-500 uppercase tracking-wider">Zalo</div>
                            <div class="text-[12px] font-bold text-slate-800 dark:text-slate-100 truncate">0562242242</div>
                        </div>
                    </a>
                    <button onclick="copyText('0562242242', 'Zalo')" class="w-7 h-7 rounded-lg glass-panel flex items-center justify-center text-slate-400 hover:text-slate-700 dark:hover:text-slate-200 active:scale-90 transition-all ml-1" title="Sao chép">
                        <i class="fa-regular fa-copy text-xs"></i>
                    </button>
                </div>

                <!-- Website -->
                <div class="glass-card p-2.5 rounded-xl flex items-center justify-between group">
                    <a href="https://soaiem333666.github.io/TranAnhKhoa_/index.html#home" target="_blank" class="flex items-center gap-2.5 flex-1 min-w-0">
                        <div class="w-8 h-8 rounded-lg bg-purple-500/10 text-purple-500 flex items-center justify-center flex-shrink-0 text-sm">
                            <i class="fa-solid fa-globe"></i>
                        </div>
                        <div class="min-w-0">
                            <div class="text-[9px] font-bold text-slate-400 dark:text-slate-500 uppercase tracking-wider">Website</div>
                            <div class="text-[12px] font-bold text-slate-800 dark:text-slate-100 truncate">soaiem333666.github.io/TranAnhKhoa_</div>
                        </div>
                    </a>
                    <button onclick="copyText('https://soaiem333666.github.io/TranAnhKhoa_/index.html#home', 'Website')" class="w-7 h-7 rounded-lg glass-panel flex items-center justify-center text-slate-400 hover:text-slate-700 dark:hover:text-slate-200 active:scale-90 transition-all ml-1" title="Sao chép">
                        <i class="fa-regular fa-copy text-xs"></i>
                    </button>
                </div>

            </div>

            <!-- Footer -->
            <div class="mt-auto pb-5 text-center">
                <div class="w-full border-b border-dashed border-slate-300 dark:border-slate-800/80 mb-4"></div>
                <p class="text-[10px] font-medium text-slate-400 dark:text-slate-500">
                    © <span id="year"></span> Trần Anh Khoa. Tất cả quyền được bảo lưu.
                </p>
            </div>

        </div>
    </div>

    <!-- QR Modal -->
    <div id="qr-modal" class="hidden fixed inset-0 z-50 bg-slate-900/60 backdrop-blur-md flex items-center justify-center p-4 transition-all duration-300">
        <div class="glass-panel p-5 rounded-2xl max-w-xs w-full bg-white dark:bg-slate-900 text-center shadow-2xl relative border border-slate-200 dark:border-slate-800">
            <button onclick="closeQRModal()" class="absolute top-3 right-3 w-7 h-7 rounded-full bg-slate-100 dark:bg-slate-800 text-slate-500 hover:text-slate-900 dark:hover:text-white flex items-center justify-center text-xs">
                <i class="fa-solid fa-xmark"></i>
            </button>
            <h3 class="text-sm font-bold text-slate-900 dark:text-white mb-0.5">Mã QR Liên Hệ</h3>
            <p class="text-[10px] text-slate-500 mb-3">Quét mã để kết nối với Trần Anh Khoa</p>
            
            <div class="bg-white p-3 rounded-xl inline-block shadow-inner mb-3">
                <div id="qrcode"></div>
            </div>

            <button onclick="closeQRModal()" class="w-full py-2 bg-sky-500 hover:bg-sky-600 text-white rounded-lg font-bold text-xs transition shadow-md shadow-sky-500/20">
                Đóng
            </button>
        </div>
    </div>

    <!-- Scripts -->
    <script>
        document.getElementById('year').textContent = new Date().getFullYear();

        function toggleTheme() {
            const html = document.documentElement;
            if (html.classList.contains('dark')) {
                html.classList.remove('dark');
                localStorage.setItem('theme', 'light');
            } else {
                html.classList.add('dark');
                localStorage.setItem('theme', 'dark');
            }
        }

        if (localStorage.getItem('theme') === 'light') {
            document.documentElement.classList.remove('dark');
        }

        function copyText(text, label) {
            navigator.clipboard.writeText(text).then(() => {
                showToast(`Đã sao chép ${label}!`);
            }).catch(err => {
                showToast('Không thể sao chép!');
            });
        }

        function showToast(message) {
            const toast = document.getElementById('toast');
            const toastMsg = document.getElementById('toast-message');
            toastMsg.textContent = message;
            toast.classList.remove('hidden');

            setTimeout(() => {
                toast.classList.add('hidden');
            }, 2500);
        }

        let qrGenerated = false;
        function openQRModal() {
            const modal = document.getElementById('qr-modal');
            modal.classList.remove('hidden');

            if (!qrGenerated) {
                new QRCode(document.getElementById("qrcode"), {
                    text: window.location.href,
                    width: 160,
                    height: 160,
                    colorDark: "#0f172a",
                    colorLight: "#ffffff",
                    correctLevel: QRCode.CorrectLevel.H
                });
                qrGenerated = true;
            }
        }

        function closeQRModal() {
            document.getElementById('qr-modal').classList.add('hidden');
        }

        function shareProfile() {
            if (navigator.share) {
                navigator.share({
                    title: 'Trần Anh Khoa (SPK) - Bio Link',
                    text: 'Thông tin cá nhân và liên hệ của Trần Anh Khoa',
                    url: window.location.href,
                }).catch(err => {});
            } else {
                copyText(window.location.href, 'Liên kết trang web');
            }
        }
    </script>
</body>
</html>
