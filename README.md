<html lang="vi" class="light">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Trần Anh Khoa (SPK) - Trang cá nhân & Liên hệ</title>
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
                            100: '#e0f2fe',
                            500: '#0284c7',
                            600: '#0369a1',
                            700: '#075985',
                        }
                    },
                    fontFamily: {
                        sans: ['Inter', 'system-ui', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    
    <style>
        body {
            font-family: 'Inter', sans-serif;
            -webkit-tap-highlight-color: transparent;
        }

        /* Glassmorphism effects */
        .glass-card {
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
        }
        .dark .glass-card {
            background: rgba(15, 23, 42, 0.85);
        }

        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 6px;
        }
        ::-webkit-scrollbar-track {
            background: transparent;
        }
        ::-webkit-scrollbar-thumb {
            background: #cbd5e1;
            border-radius: 9999px;
        }
        .dark ::-webkit-scrollbar-thumb {
            background: #334155;
        }

        /* Toast animation */
        @keyframes slideUp {
            from { transform: translate(-50%, 100%); opacity: 0; }
            to { transform: translate(-50%, 0); opacity: 1; }
        }
        .animate-toast {
            animation: slideUp 0.3s ease-out forwards;
        }

        /* Pulse aura for verified badge */
        .badge-pulse::after {
            content: '';
            position: absolute;
            inset: -2px;
            border-radius: 9999px;
            background: #3b82f6;
            opacity: 0.4;
            z-index: -1;
            animation: pulse-ring 2s cubic-bezier(0.4, 0, 0.6, 1) infinite;
        }
        @keyframes pulse-ring {
            0% { transform: scale(0.95); opacity: 0.8; }
            50% { transform: scale(1.3); opacity: 0; }
            100% { transform: scale(0.95); opacity: 0; }
        }
    </style>
</head>
<body class="bg-slate-100 dark:bg-slate-950 text-slate-800 dark:text-slate-100 min-h-screen flex items-center justify-center p-0 sm:p-4 md:p-6 transition-colors duration-300">

    <!-- Toast Notification -->
    <div id="toast" class="fixed bottom-6 left-1/2 -translate-x-1/2 z-50 hidden bg-slate-900/90 dark:bg-white/90 text-white dark:text-slate-900 px-5 py-3 rounded-full text-sm font-semibold shadow-2xl backdrop-blur-md flex items-center gap-2 border border-slate-700/30">
        <i class="fa-solid fa-circle-check text-emerald-400 dark:text-emerald-600 text-base"></i>
        <span id="toast-msg">Đã sao chép vào bộ nhớ tạm!</span>
    </div>

    <!-- QR Code Modal -->
    <div id="qr-modal" class="fixed inset-0 z-50 bg-black/60 backdrop-blur-sm hidden items-center justify-center p-4 transition-opacity">
        <div class="bg-white dark:bg-slate-900 rounded-3xl p-6 max-w-xs w-full text-center shadow-2xl border border-slate-200 dark:border-slate-800 transform transition-all scale-95 opacity-0 modal-content">
            <div class="flex justify-between items-center mb-4">
                <h3 class="font-bold text-lg text-slate-900 dark:text-white">Mã QR Trang Cá Nhân</h3>
                <button onclick="toggleQRModal(false)" class="text-slate-400 hover:text-slate-600 dark:hover:text-slate-200 p-1">
                    <i class="fa-solid fa-xmark text-xl"></i>
                </button>
            </div>
            <div class="bg-white p-4 rounded-2xl shadow-inner inline-block border border-slate-100 my-2">
                <img id="qr-img" src="https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=https://soaiem333666.github.io/TranAnhKhoa_/index.html%23home" alt="QR Code" class="w-48 h-48 mx-auto">
            </div>
            <p class="text-xs text-slate-500 dark:text-slate-400 mt-3">Quét mã bằng camera hoặc Zalo để mở nhanh trang web này</p>
        </div>
    </div>

    <!-- Main Card Container -->
    <div class="w-full max-w-md bg-white dark:bg-slate-900 min-h-screen sm:min-h-0 sm:rounded-[2.5rem] shadow-2xl overflow-hidden relative pb-10 border border-slate-200/60 dark:border-slate-800/80 my-0 sm:my-4 transition-all duration-300">

        <!-- Top Quick Controls (Theme Toggle & Share) -->
        <div class="absolute top-4 right-4 z-20 flex gap-2">
            <button onclick="toggleDarkMode()" aria-label="Đổi giao diện" class="w-10 h-10 rounded-full bg-black/30 backdrop-blur-md text-white hover:bg-black/50 transition-all flex items-center justify-center shadow-lg active:scale-95">
                <i id="theme-icon" class="fa-solid fa-moon text-sm"></i>
            </button>
            <button onclick="toggleQRModal(true)" aria-label="Xem mã QR" class="w-10 h-10 rounded-full bg-black/30 backdrop-blur-md text-white hover:bg-black/50 transition-all flex items-center justify-center shadow-lg active:scale-95">
                <i class="fa-solid fa-qrcode text-sm"></i>
            </button>
            <button onclick="shareProfile()" aria-label="Chia sẻ trang" class="w-10 h-10 rounded-full bg-black/30 backdrop-blur-md text-white hover:bg-black/50 transition-all flex items-center justify-center shadow-lg active:scale-95">
                <i class="fa-solid fa-share-nodes text-sm"></i>
            </button>
        </div>

        <!-- Banner / Cover Photo -->
        <div class="relative h-52 sm:h-60 w-full overflow-hidden bg-slate-200 dark:bg-slate-800">
            <img 
                src="178971697000053089.jpg" 
                alt="Ảnh bìa Hải đăng & Biển" 
                class="w-full h-full object-cover object-center transform hover:scale-105 transition-transform duration-700"
                onerror="this.onerror=null; this.src='https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=1200&q=80';"
            />
            <!-- Gradient Overlay for smooth contrast -->
            <div class="absolute inset-0 bg-gradient-to-t from-black/40 via-transparent to-black/20"></div>
        </div>

        <!-- Avatar & Name Header -->
        <div class="px-6 relative flex flex-col items-start -mt-16 mb-5">
            <!-- Profile Picture Box -->
            <div class="relative group">
                <div class="w-28 h-28 sm:w-32 sm:h-32 rounded-full border-4 border-white dark:border-slate-900 overflow-hidden shadow-xl bg-slate-100 dark:bg-slate-800 transition-transform group-hover:scale-105 duration-300">
                    <img 
                        src="178971449400070618.jpg" 
                        alt="Trần Anh Khoa Avatar" 
                        class="w-full h-full object-cover"
                        onerror="this.onerror=null; this.src='https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&w=500&q=80';"
                    />
                </div>
                <!-- Verified Badge -->
                <div class="absolute bottom-1 right-1 bg-blue-500 text-white rounded-full w-8 h-8 flex items-center justify-center border-2 border-white dark:border-slate-900 shadow-lg badge-pulse" title="Tài khoản chính thức đã xác minh">
                    <i class="fa-solid fa-check text-xs font-black"></i>
                </div>
            </div>

            <!-- Full Name & Title -->
            <div class="mt-4">
                <h1 class="text-2xl font-extrabold text-slate-900 dark:text-white tracking-tight flex items-center gap-2">
                    Trần Anh Khoa 
                    <span class="text-slate-500 dark:text-slate-400 font-normal text-base">(SPK)</span>
                </h1>
                <p class="text-sm font-medium text-slate-700 dark:text-slate-300 leading-snug mt-1.5 flex items-start gap-2">
                    <i class="fa-solid fa-briefcase text-blue-500 mt-1 shrink-0"></i>
                    <span>Nhân viên Hành chính tổng hợp, Trung tâm Dịch vụ sự nghiệp công phường An Cựu</span>
                </p>
            </div>
        </div>

        <!-- Certificate Badges Section -->
        <div class="px-6 mb-6">
            <h2 class="text-xs font-bold uppercase tracking-wider text-slate-400 dark:text-slate-500 mb-2.5 flex items-center gap-1.5">
                <i class="fa-solid fa-award text-amber-500"></i> Chứng chỉ & Thành tựu
            </h2>
            <div class="flex flex-col gap-2">
                <div class="bg-slate-100/90 dark:bg-slate-800/60 hover:bg-slate-200/80 dark:hover:bg-slate-800 transition-all rounded-2xl px-4 py-2.5 text-xs text-slate-700 dark:text-slate-300 font-medium leading-relaxed border border-slate-200/60 dark:border-slate-700/50 flex items-start gap-2.5 shadow-sm">
                    <i class="fa-solid fa-certificate text-blue-500 text-sm mt-0.5 shrink-0"></i>
                    <span>Giấy chứng nhận của Khoa Quản trị Kinh doanh</span>
                </div>
                <div class="bg-slate-100/90 dark:bg-slate-800/60 hover:bg-slate-200/80 dark:hover:bg-slate-800 transition-all rounded-2xl px-4 py-2.5 text-xs text-slate-700 dark:text-slate-300 font-medium leading-relaxed border border-slate-200/60 dark:border-slate-700/50 flex items-start gap-2.5 shadow-sm">
                    <i class="fa-solid fa-graduation-cap text-emerald-500 text-sm mt-0.5 shrink-0"></i>
                    <span>Giấy chứng nhận dự án H&M Study Buddy - Nền tảng học tập trực tuyến</span>
                </div>
                <div class="bg-slate-100/90 dark:bg-slate-800/60 hover:bg-slate-200/80 dark:hover:bg-slate-800 transition-all rounded-2xl px-4 py-2.5 text-xs text-slate-700 dark:text-slate-300 font-medium leading-relaxed border border-slate-200/60 dark:border-slate-700/50 flex items-start gap-2.5 shadow-sm">
                    <i class="fa-solid fa-chart-line text-purple-500 text-sm mt-0.5 shrink-0"></i>
                    <span>Giấy chứng nhận Quản lý năng suất và chất lượng của Học viện Tài Chính</span>
                </div>
                <div class="bg-slate-100/90 dark:bg-slate-800/60 hover:bg-slate-200/80 dark:hover:bg-slate-800 transition-all rounded-2xl px-4 py-2.5 text-xs text-slate-700 dark:text-slate-300 font-medium leading-relaxed border border-slate-200/60 dark:border-slate-700/50 flex items-start gap-2.5 shadow-sm">
                    <i class="fa-solid fa-laptop-code text-indigo-500 text-sm mt-0.5 shrink-0"></i>
                    <span>Giấy chứng nhận Bồi dưỡng, tập huấn kỹ năng số cơ bản cho cán bộ, viên chức</span>
                </div>
            </div>
        </div>

        <!-- Social Networks Bar -->
        <div class="px-6 mb-7">
            <h2 class="text-xs font-bold uppercase tracking-wider text-slate-400 dark:text-slate-500 mb-3 flex items-center gap-1.5">
                <i class="fa-solid fa-hashtag text-sky-500"></i> Mạng xã hội
            </h2>
            <div class="flex justify-around items-center bg-slate-50 dark:bg-slate-800/40 p-3.5 rounded-2xl border border-slate-100 dark:border-slate-800 shadow-inner">
                <a href="https://facebook.com" target="_blank" rel="noopener noreferrer" aria-label="Facebook" class="text-slate-800 dark:text-slate-200 hover:text-blue-600 dark:hover:text-blue-400 transition-all transform hover:scale-125">
                    <i class="fa-brands fa-facebook text-3xl"></i>
                </a>
                <a href="https://instagram.com" target="_blank" rel="noopener noreferrer" aria-label="Instagram" class="text-slate-800 dark:text-slate-200 hover:text-pink-600 dark:hover:text-pink-400 transition-all transform hover:scale-125">
                    <i class="fa-brands fa-instagram text-3xl"></i>
                </a>
                <a href="https://youtube.com" target="_blank" rel="noopener noreferrer" aria-label="YouTube" class="text-slate-800 dark:text-slate-200 hover:text-red-600 dark:hover:text-red-400 transition-all transform hover:scale-125">
                    <i class="fa-brands fa-youtube text-3xl"></i>
                </a>
                <a href="https://tiktok.com" target="_blank" rel="noopener noreferrer" aria-label="TikTok" class="text-slate-800 dark:text-slate-200 hover:text-cyan-500 dark:hover:text-cyan-400 transition-all transform hover:scale-125">
                    <i class="fa-brands fa-tiktok text-3xl"></i>
                </a>
            </div>
        </div>

        <!-- Contact Methods Section -->
        <div class="px-6 space-y-3">
            <h2 class="text-xs font-bold uppercase tracking-wider text-slate-400 dark:text-slate-500 mb-2 flex items-center gap-1.5">
                <i class="fa-solid fa-address-book text-emerald-500"></i> Thông tin liên hệ
            </h2>

            <!-- Gmail -->
            <div class="flex items-center justify-between p-3 rounded-2xl bg-slate-50 dark:bg-slate-800/50 hover:bg-slate-100 dark:hover:bg-slate-800 transition-all border border-slate-200/60 dark:border-slate-800 group shadow-sm">
                <a href="mailto:anhkhoat363@gmail.com" class="flex items-center gap-3.5 flex-1 min-w-0">
                    <div class="w-11 h-11 rounded-xl bg-slate-900 dark:bg-slate-100 text-white dark:text-slate-900 flex items-center justify-center shrink-0 shadow-sm group-hover:scale-105 transition-transform">
                        <i class="fa-solid fa-envelope text-lg"></i>
                    </div>
                    <div class="truncate">
                        <div class="text-sm font-bold text-slate-900 dark:text-white">Gmail</div>
                        <div class="text-xs text-slate-500 dark:text-slate-400 truncate">anhkhoat363@gmail.com</div>
                    </div>
                </a>
                <button onclick="copyToClipboard('anhkhoat363@gmail.com', 'Email')" class="p-2.5 text-slate-400 hover:text-slate-900 dark:hover:text-white transition-colors rounded-xl hover:bg-white dark:hover:bg-slate-700" title="Sao chép Email">
                    <i class="fa-regular fa-copy text-base"></i>
                </button>
            </div>

            <!-- Điện thoại -->
            <div class="flex items-center justify-between p-3 rounded-2xl bg-slate-50 dark:bg-slate-800/50 hover:bg-slate-100 dark:hover:bg-slate-800 transition-all border border-slate-200/60 dark:border-slate-800 group shadow-sm">
                <a href="tel:0899997781" class="flex items-center gap-3.5 flex-1 min-w-0">
                    <div class="w-11 h-11 rounded-xl bg-slate-900 dark:bg-slate-100 text-white dark:text-slate-900 flex items-center justify-center shrink-0 shadow-sm group-hover:scale-105 transition-transform">
                        <i class="fa-solid fa-phone text-base"></i>
                    </div>
                    <div>
                        <div class="text-sm font-bold text-slate-900 dark:text-white">Điện thoại</div>
                        <div class="text-xs text-slate-500 dark:text-slate-400">0899997781</div>
                    </div>
                </a>
                <button onclick="copyToClipboard('0899997781', 'Số điện thoại')" class="p-2.5 text-slate-400 hover:text-slate-900 dark:hover:text-white transition-colors rounded-xl hover:bg-white dark:hover:bg-slate-700" title="Sao chép Số điện thoại">
                    <i class="fa-regular fa-copy text-base"></i>
                </button>
            </div>

            <!-- Zalo -->
            <div class="flex items-center justify-between p-3 rounded-2xl bg-slate-50 dark:bg-slate-800/50 hover:bg-slate-100 dark:hover:bg-slate-800 transition-all border border-slate-200/60 dark:border-slate-800 group shadow-sm">
                <a href="https://zalo.me/0562242242" target="_blank" rel="noopener noreferrer" class="flex items-center gap-3.5 flex-1 min-w-0">
                    <div class="w-11 h-11 rounded-xl bg-slate-900 dark:bg-slate-100 text-white dark:text-slate-900 flex items-center justify-center shrink-0 shadow-sm font-extrabold text-xs group-hover:scale-105 transition-transform">
                        Zalo
                    </div>
                    <div>
                        <div class="text-sm font-bold text-slate-900 dark:text-white">Zalo</div>
                        <div class="text-xs text-slate-500 dark:text-slate-400">0562242242</div>
                    </div>
                </a>
                <button onclick="copyToClipboard('0562242242', 'Số Zalo')" class="p-2.5 text-slate-400 hover:text-slate-900 dark:hover:text-white transition-colors rounded-xl hover:bg-white dark:hover:bg-slate-700" title="Sao chép Số Zalo">
                    <i class="fa-regular fa-copy text-base"></i>
                </button>
            </div>

            <!-- Website -->
            <div class="flex items-center justify-between p-3 rounded-2xl bg-slate-50 dark:bg-slate-800/50 hover:bg-slate-100 dark:hover:bg-slate-800 transition-all border border-slate-200/60 dark:border-slate-800 group shadow-sm">
                <a href="https://soaiem333666.github.io/TranAnhKhoa_/index.html#home" target="_blank" rel="noopener noreferrer" class="flex items-center gap-3.5 flex-1 min-w-0">
                    <div class="w-11 h-11 rounded-xl bg-slate-900 dark:bg-slate-100 text-white dark:text-slate-900 flex items-center justify-center shrink-0 shadow-sm group-hover:scale-105 transition-transform">
                        <i class="fa-solid fa-globe text-base"></i>
                    </div>
                    <div class="truncate">
                        <div class="text-sm font-bold text-slate-900 dark:text-white">Website</div>
                        <div class="text-xs text-slate-500 dark:text-slate-400 truncate">soaiem333666.github.io/TranAnhKhoa_/index.html#home</div>
                    </div>
                </a>
                <button onclick="copyToClipboard('https://soaiem333666.github.io/TranAnhKhoa_/index.html#home', 'Đường dẫn Website')" class="p-2.5 text-slate-400 hover:text-slate-900 dark:hover:text-white transition-colors rounded-xl hover:bg-white dark:hover:bg-slate-700" title="Sao chép Website">
                    <i class="fa-regular fa-copy text-base"></i>
                </button>
            </div>

        </div>

        <!-- Footer Divider -->
        <div class="mt-8 pt-6 border-t border-dashed border-slate-300 dark:border-slate-800 mx-6 text-center text-xs text-slate-400 dark:text-slate-500">
            <p>© 2026 Trần Anh Khoa. Tất cả quyền được bảo lưu.</p>
        </div>

    </div>

    <script>
        // Copy to clipboard with iframe safety fallback
        function copyToClipboard(text, label) {
            const textarea = document.createElement('textarea');
            textarea.value = text;
            textarea.style.position = 'fixed';
            textarea.style.opacity = '0';
            document.body.appendChild(textarea);
            textarea.select();
            
            try {
                document.execCommand('copy');
                showToast(`Đã sao chép ${label || 'thông tin'}!`);
            } catch (err) {
                showToast("Không thể sao chép tự động!");
            }
            
            document.body.removeChild(textarea);
        }

        // Display toast message
        function showToast(message) {
            const toast = document.getElementById('toast');
            const msgSpan = document.getElementById('toast-msg');
            msgSpan.innerText = message;
            
            toast.classList.remove('hidden');
            toast.classList.add('animate-toast');

            setTimeout(() => {
                toast.classList.add('hidden');
                toast.classList.remove('animate-toast');
            }, 2500);
        }

        // Toggle Dark Mode
        function toggleDarkMode() {
            const html = document.documentElement;
            const themeIcon = document.getElementById('theme-icon');
            
            if (html.classList.contains('dark')) {
                html.classList.remove('dark');
                html.classList.add('light');
                themeIcon.className = "fa-solid fa-moon text-sm";
                showToast("Đã chuyển sang giao diện Sáng");
            } else {
                html.classList.remove('light');
                html.classList.add('dark');
                themeIcon.className = "fa-solid fa-sun text-sm";
                showToast("Đã chuyển sang giao diện Tối");
            }
        }

        // Toggle QR Modal
        function toggleQRModal(show) {
            const modal = document.getElementById('qr-modal');
            const modalContent = modal.querySelector('.modal-content');
            
            if (show) {
                modal.classList.remove('hidden');
                modal.classList.add('flex');
                setTimeout(() => {
                    modalContent.classList.remove('scale-95', 'opacity-0');
                    modalContent.classList.add('scale-100', 'opacity-100');
                }, 10);
            } else {
                modalContent.classList.remove('scale-100', 'opacity-100');
                modalContent.classList.add('scale-95', 'opacity-0');
                setTimeout(() => {
                    modal.classList.remove('flex');
                    modal.classList.add('hidden');
                }, 200);
            }
        }

        // Native Share or fallback copy
        function shareProfile() {
            const shareData = {
                title: 'Trần Anh Khoa - Trang cá nhân',
                text: 'Trần Anh Khoa (SPK) - Nhân viên Hành chính tổng hợp, Trung tâm Dịch vụ sự nghiệp công phường An Cựu',
                url: window.location.href
            };

            if (navigator.share) {
                navigator.share(shareData).catch(() => {});
            } else {
                copyToClipboard(window.location.href, 'Liên kết trang');
            }
        }
    </script>
</body>
</html>
