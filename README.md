<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Trần Anh Khoa (SPK) - Bio Link</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        .cert-badge {
            background-color: #f1f3f5;
            color: #495057;
            transition: all 0.2s ease;
        }
        .cert-badge:hover {
            background-color: #e9ecef;
            color: #212529;
            transform: translateY(-1px);
        }
        .contact-card {
            transition: all 0.2s ease;
            box-shadow: 0 2px 8px rgba(0,0,0,0.04);
        }
        .contact-card:hover {
            box-shadow: 0 4px 12px rgba(0,0,0,0.08);
            transform: translateY(-2px);
        }
        .social-icon {
            transition: all 0.2s ease;
        }
        .social-icon:hover {
            transform: scale(1.15);
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 min-h-screen pb-12 flex justify-center">

    <div class="w-full max-w-md bg-white min-h-screen shadow-xl flex flex-col relative overflow-hidden">
        
        <!-- Header / Banner Image -->
        <div class="h-48 w-full relative bg-slate-200">
            <img src="https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=1200&q=80" 
                 alt="Cover Photo" 
                 class="w-full h-full object-cover">
        </div>

        <!-- Profile Content Container -->
        <div class="px-6 relative flex-1 flex flex-col">
            
            <!-- Avatar -->
            <div class="relative -mt-16 mb-3 inline-block w-fit">
                <div class="w-28 h-28 rounded-full border-4 border-white shadow-lg overflow-hidden bg-white">
                    <img src="https://scontent.fdad3-8.fna.fbcdn.net/v/t39.30808-6/814999473_2832030020509538_2916820980541575312_n.jpg?stp=dst-jpg_tt6&cstp=mx800x800&ctp=s800x800&_nc_cat=100&ccb=1-7&_nc_sid=6ee11a&_nc_ohc=b66FVPJ1GuwQ7kNvwFEoIpN&_nc_oc=AdrY5oOGxegWO0NH_lYMTs7G-mEy25pF6lHYG11RQywD75sJ0o7z8cswN2fs9DIj4cY&_nc_zt=23&_nc_ht=scontent.fdad3-8.fna&_nc_gid=ywyp8MN02jYBRUK7qQX77w&_nc_ss=7b289&oh=00_AQIEj48jNvvnPM8VMjPqSsN1m1SJrADF-mM4zr8gyDna7g&oe=6AB91C12" 
                         alt="Trần Anh Khoa Avatar" 
                         class="w-full h-full object-cover">
                </div>
                <!-- Verified Badge -->
                <div class="absolute bottom-1 right-1 bg-blue-500 text-white rounded-full w-6 h-6 flex items-center justify-center text-xs shadow-md">
                    <i class="fa-solid fa-check"></i>
                </div>
            </div>

            <!-- Profile Info -->
            <div class="mb-4">
                <h1 class="text-2xl font-bold text-slate-900 flex items-center gap-2">
                    Trần Anh Khoa <span class="text-sm font-normal text-slate-500">(SPK)</span>
                </h1>
                <p class="text-sm font-medium text-slate-700 mt-1 leading-snug">
                    Nhân viên Hành chính tổng hợp, Trung tâm Dịch vụ sự nghiệp công phường An Cựu
                </p>
            </div>

            <!-- Certificates List -->
            <div class="flex flex-col gap-2 mb-6">
                <div class="cert-badge text-xs px-3 py-2 rounded-lg leading-relaxed flex items-center gap-2">
                    <i class="fa-solid fa-certificate text-slate-400"></i>
                    <span>Giấy chứng nhận của Khoa Quản trị Kinh doanh</span>
                </div>
                <div class="cert-badge text-xs px-3 py-2 rounded-lg leading-relaxed flex items-center gap-2">
                    <i class="fa-solid fa-certificate text-slate-400"></i>
                    <span>Giấy chứng nhận dự án H&M Study Buddy - Nền tảng học tập trực tuyến</span>
                </div>
                <div class="cert-badge text-xs px-3 py-2 rounded-lg leading-relaxed flex items-center gap-2">
                    <i class="fa-solid fa-certificate text-slate-400"></i>
                    <span>Giấy chứng nhận Quản lý năng suất và chất lượng của Học viện Tài Chính</span>
                </div>
                <div class="cert-badge text-xs px-3 py-2 rounded-lg leading-relaxed flex items-center gap-2">
                    <i class="fa-solid fa-certificate text-slate-400"></i>
                    <span>Giấy chứng nhận Bồi dưỡng, tập huấn kỹ năng số cơ bản cho cán bộ, viên chức</span>
                </div>
            </div>

            <!-- Social Media Links -->
            <div class="flex justify-center items-center gap-6 py-2 mb-6">
                <a href="#" target="_blank" class="social-icon text-2xl text-slate-800 hover:text-black">
                    <i class="fa-brands fa-facebook"></i>
                </a>
                <a href="#" target="_blank" class="social-icon text-2xl text-slate-800 hover:text-black">
                    <i class="fa-brands fa-instagram"></i>
                </a>
                <a href="#" target="_blank" class="social-icon text-2xl text-slate-800 hover:text-red-600">
                    <i class="fa-brands fa-youtube"></i>
                </a>
                <a href="#" target="_blank" class="social-icon text-2xl text-slate-800 hover:text-black">
                    <i class="fa-brands fa-tiktok"></i>
                </a>
            </div>

            <!-- Contact List Section -->
            <div class="flex flex-col gap-3 mb-8">
                
                <!-- Gmail -->
                <a href="mailto:anhkhoat363@gmail.com" class="contact-card flex items-center gap-4 p-3 bg-white border border-slate-100 rounded-xl">
                    <div class="w-10 h-10 rounded-full bg-slate-900 text-white flex items-center justify-center flex-shrink-0">
                        <i class="fa-solid fa-envelope"></i>
                    </div>
                    <div class="overflow-hidden">
                        <div class="text-xs text-slate-500 font-medium">Gmail</div>
                        <div class="text-sm font-semibold text-slate-800 truncate">anhkhoat363@gmail.com</div>
                    </div>
                </a>

                <!-- Phone -->
                <a href="tel:0899997781" class="contact-card flex items-center gap-4 p-3 bg-white border border-slate-100 rounded-xl">
                    <div class="w-10 h-10 rounded-full bg-slate-900 text-white flex items-center justify-center flex-shrink-0">
                        <i class="fa-solid fa-phone"></i>
                    </div>
                    <div>
                        <div class="text-xs text-slate-500 font-medium">Điện thoại</div>
                        <div class="text-sm font-semibold text-slate-800">0899997781</div>
                    </div>
                </a>

                <!-- Zalo -->
                <a href="https://zalo.me/0562242242" target="_blank" class="contact-card flex items-center gap-4 p-3 bg-white border border-slate-100 rounded-xl">
                    <div class="w-10 h-10 rounded-full bg-slate-900 text-white flex items-center justify-center flex-shrink-0 font-bold text-xs">
                        Zalo
                    </div>
                    <div>
                        <div class="text-xs text-slate-500 font-medium">Zalo</div>
                        <div class="text-sm font-semibold text-slate-800">0562242242</div>
                    </div>
                </a>

                <!-- Website -->
                <a href="https://soaiem333666.github.io/TranAnhKhoa_/index.html#home" target="_blank" class="contact-card flex items-center gap-4 p-3 bg-white border border-slate-100 rounded-xl">
                    <div class="w-10 h-10 rounded-full bg-slate-900 text-white flex items-center justify-center flex-shrink-0">
                        <i class="fa-solid fa-globe"></i>
                    </div>
                    <div class="overflow-hidden">
                        <div class="text-xs text-slate-500 font-medium">Website</div>
                        <div class="text-sm font-semibold text-slate-800 truncate">soaiem333666.github.io/TranAnhKhoa_/index.html#home</div>
                    </div>
                </a>

            </div>

            <!-- Footer / Dashed Divider -->
            <div class="mt-auto pb-6">
                <div class="border-b-2 border-dashed border-slate-300 w-full mb-4"></div>
                <div class="text-center text-xs text-slate-400">
                    © Trần Anh Khoa - All rights reserved
                </div>
            </div>

        </div>
    </div>

</body>
</html>
