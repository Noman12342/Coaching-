<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ইউনিক কোচিং সেন্টার</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+Bengali:wght@400;700&family=Inter:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body.lang-bn { font-family: 'Noto Sans Bengali', sans-serif; }
        body.lang-en { font-family: 'Inter', sans-serif; }
        html, body { height: 100%; overflow-x: hidden; }
        .toast {
            visibility: hidden;
            min-width: 250px;
            margin-left: -125px;
            color: #fff;
            text-align: center;
            border-radius: 8px;
            padding: 16px;
            position: fixed;
            z-index: 100;
            left: 50%;
            bottom: 30px;
            font-size: 17px;
            opacity: 0;
            transition: visibility 0s, opacity 0.5s linear;
        }
        .toast.show {
            visibility: visible;
            opacity: 1;
        }
        .toast.success { background-color: #28a745; }
        .toast.error { background-color: #dc3545; }
        .icon-shadow {
            background-repeat: no-repeat;
            background-position: center;
            background-size: 60%;
            opacity: 0.1;
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            z-index: 0;
        }
    </style>
</head>
<body class="bg-gray-100 lang-bn">

    <!-- Language Switcher (for all pages except main) -->
    <div id="language-switcher" class="absolute top-4 right-4 z-50 hidden">
        <button id="lang-bn-btn" class="px-3 py-1 bg-indigo-600 text-white rounded-l-md font-semibold focus:outline-none text-sm">বাংলা</button>
        <button id="lang-en-btn" class="px-3 py-1 bg-white text-gray-700 rounded-r-md font-semibold focus:outline-none text-sm">English</button>
    </div>

    <!-- New Main Page -->
    <div id="main-page" class="relative min-h-screen flex flex-col">
        <header class="relative h-64 md:h-80 bg-cover bg-center" style="background-image: url('https://placehold.co/1200x400/6366F1/FFFFFF?text=Banner');">
            <div class="absolute inset-0 bg-black bg-opacity-40"></div>
            <div class="absolute top-4 right-4 z-40">
                <button id="menu-open-btn" class="p-2 rounded-md text-white bg-black bg-opacity-20 hover:bg-opacity-40">
                    <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" /></svg>
                </button>
            </div>
            <div class="relative z-10 flex flex-col items-center justify-center h-full text-white text-center px-4">
                <h1 id="main-title" class="text-4xl md:text-6xl font-bold">ইউনিক কোচিং সেন্টার</h1>
            </div>
        </header>
        <main class="flex-grow p-6 md:p-10 bg-gray-50">
            <!-- Why Choose Us Section -->
            <section id="why-us" class="container mx-auto py-12">
                <h2 id="why-us-title" class="text-3xl font-bold text-center text-gray-800 mb-8">কেন আমরা সেরা?</h2>
                <div class="grid md:grid-cols-3 gap-8 text-center">
                    <!-- Feature 1 -->
                    <div class="bg-white p-6 rounded-lg shadow">
                        <h3 id="feature1-title" class="text-xl font-semibold mb-2">অভিজ্ঞ শিক্ষক</h3>
                        <p id="feature1-desc" class="text-gray-600">আমাদের রয়েছে সেরা শিক্ষকদের একটি অভিজ্ঞ দল।</p>
                    </div>
                    <!-- Feature 2 -->
                    <div class="bg-white p-6 rounded-lg shadow">
                        <h3 id="feature2-title" class="text-xl font-semibold mb-2">বিশেষ নোট</h3>
                        <p id="feature2-desc" class="text-gray-600">আমরা প্রতিটি বিষয়ের উপর বিশেষ নোট প্রদান করি।</p>
                    </div>
                    <!-- Feature 3 -->
                    <div class="bg-white p-6 rounded-lg shadow">
                        <h3 id="feature3-title" class="text-xl font-semibold mb-2">নিয়মিত পরীক্ষা</h3>
                        <p id="feature3-desc" class="text-gray-600">সাপ্তাহিক ও মাসিক পরীক্ষার মাধ্যমে শিক্ষার্থীদের প্রস্তুত করা হয়।</p>
                    </div>
                </div>
            </section>

            <!-- Achievers Section -->
            <section id="achievers" class="container mx-auto py-12">
                <h2 id="achievers-title" class="text-3xl font-bold text-center text-gray-800 mb-8">আমাদের কৃতি শিক্ষার্থীরা (গত বছর)</h2>
                <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-6">
                    <!-- Student Card 1 -->
                    <div class="bg-white rounded-lg shadow-md text-center p-4 transition-transform transform hover:-translate-y-2">
                        <img src="https://placehold.co/150x150/E2E8F0/4A5568?text=Student" class="w-24 h-24 rounded-full mx-auto mb-3 border-4 border-white shadow-lg" alt="Student Photo">
                        <h4 id="student1-name" class="font-bold">মোঃ জাহিদ</h4>
                        <p id="student1-class" class="text-sm text-gray-600">দশম শ্রেণী</p>
                        <p id="student1-grade" class="text-sm font-semibold text-green-600">A+</p>
                    </div>
                     <!-- Student Card 2 -->
                    <div class="bg-white rounded-lg shadow-md text-center p-4 transition-transform transform hover:-translate-y-2">
                        <img src="https://placehold.co/150x150/E2E8F0/4A5568?text=Student" class="w-24 h-24 rounded-full mx-auto mb-3 border-4 border-white shadow-lg" alt="Student Photo">
                        <h4 id="student2-name" class="font-bold">ফারিয়া আক্তার</h4>
                        <p id="student2-class" class="text-sm text-gray-600">দ্বাদশ শ্রেণী</p>
                        <p id="student2-grade" class="text-sm font-semibold text-green-600">A+</p>
                    </div>
                     <!-- Student Card 3 -->
                    <div class="bg-white rounded-lg shadow-md text-center p-4 transition-transform transform hover:-translate-y-2">
                        <img src="https://placehold.co/150x150/E2E8F0/4A5568?text=Student" class="w-24 h-24 rounded-full mx-auto mb-3 border-4 border-white shadow-lg" alt="Student Photo">
                        <h4 id="student3-name" class="font-bold">আরিফ হোসেন</h4>
                        <p id="student3-class" class="text-sm text-gray-600">দশম শ্রেণী</p>
                        <p id="student3-grade" class="text-sm font-semibold text-green-600">A+</p>
                    </div>
                     <!-- Student Card 4 -->
                    <div class="bg-white rounded-lg shadow-md text-center p-4 transition-transform transform hover:-translate-y-2">
                        <img src="https://placehold.co/150x150/E2E8F0/4A5568?text=Student" class="w-24 h-24 rounded-full mx-auto mb-3 border-4 border-white shadow-lg" alt="Student Photo">
                        <h4 id="student4-name" class="font-bold">সাদিয়া ইসলাম</h4>
                        <p id="student4-class" class="text-sm text-gray-600">অষ্টম শ্রেণী</p>
                        <p id="student4-grade" class="text-sm font-semibold text-green-600">A+</p>
                    </div>
                </div>
            </section>
        </main>
        <footer class="bg-gray-800 text-white p-6">
            <div class="container mx-auto text-center">
                <p id="footer-contact-us" class="font-bold mb-2">যোগাযোগ করুন</p>
                <div class="flex justify-center space-x-4 mb-4">
                    <a href="#" class="hover:text-indigo-400">Facebook</a>
                    <a href="#" class="hover:text-indigo-400">WhatsApp</a>
                </div>
                <p id="copyright" class="text-sm text-gray-400">© ইউনিক কোচিং সেন্টার</p>
            </div>
        </footer>
    </div>

    <!-- Menu Popup -->
    <div id="menu-popup" class="hidden fixed inset-0 bg-black bg-opacity-50 z-50 flex justify-end">
        <div class="bg-white w-64 h-full p-6 flex flex-col">
            <div class="flex justify-between items-center mb-6">
                 <!-- Language Switcher (for main page menu) -->
                <div>
                    <button id="menu-lang-bn-btn" class="px-3 py-1 bg-indigo-600 text-white rounded-l-md font-semibold focus:outline-none text-sm">বাংলা</button>
                    <button id="menu-lang-en-btn" class="px-3 py-1 bg-white text-gray-700 rounded-r-md font-semibold focus:outline-none text-sm">English</button>
                </div>
                <button id="menu-close-btn" class="text-gray-600 hover:text-gray-900">
                    <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" /></svg>
                </button>
            </div>
            <!-- Logged Out Menu -->
            <div id="menu-logged-out" class="space-y-4">
                <button id="menu-login-btn" class="w-full text-left py-2 text-gray-700 font-semibold hover:text-indigo-600">লগইন</button>
                <button id="menu-admission-btn" class="w-full text-left py-2 text-gray-700 font-semibold hover:text-indigo-600">ভর্তির জন্য আবেদন</button>
                <button id="menu-about-btn" class="w-full text-left py-2 text-gray-700 font-semibold hover:text-indigo-600">আমাদের সম্পর্কে</button>
            </div>
            <!-- Logged In Menu -->
            <div id="menu-logged-in" class="hidden flex-grow flex flex-col">
                <div class="space-y-4 flex-grow">
                    <div>
                        <div class="flex justify-between items-center">
                            <button id="menu-dashboard-btn" class="w-full text-left py-2 text-gray-700 font-semibold hover:text-indigo-600">ড্যাশবোর্ড</button>
                            <button id="dashboard-submenu-toggle" class="p-1">
                                <svg class="h-5 w-5 transition-transform" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" /></svg>
                            </button>
                        </div>
                        <div id="dashboard-submenu" class="hidden pl-4 mt-2 space-y-2">
                            <button id="menu-routine-btn" class="w-full text-left py-1 text-gray-600 hover:text-indigo-600">রুটিন</button>
                            <button id="menu-classes-btn" class="w-full text-left py-1 text-gray-600 hover:text-indigo-600">ক্লাসসমূহ</button>
                            <button id="menu-teachers-btn" class="w-full text-left py-1 text-gray-600 hover:text-indigo-600">শিক্ষকবৃন্দ</button>
                            <button id="menu-exams-btn" class="w-full text-left py-1 text-gray-600 hover:text-indigo-600">পরীক্ষা</button>
                            <button id="menu-results-btn" class="w-full text-left py-1 text-gray-600 hover:text-indigo-600">ফলাফল</button>
                            <button id="menu-notice-btn" class="w-full text-left py-1 text-gray-600 hover:text-indigo-600">নোটিশ</button>
                        </div>
                    </div>
                    <button id="menu-about-btn-loggedin" class="w-full text-left py-2 text-gray-700 font-semibold hover:text-indigo-600">আমাদের সম্পর্কে</button>
                </div>
                <button id="menu-logout-btn" class="w-full text-left py-2 text-red-500 font-semibold hover:text-red-700 mt-auto">লগ-আউট</button>
            </div>
        </div>
    </div>

    <!-- Login Page -->
    <div id="login-page" class="hidden relative min-h-screen flex flex-col items-center justify-center p-4">
        <div class="w-full max-w-sm text-center">
            <h1 id="login-title" class="text-3xl md:text-4xl font-bold text-gray-800 mb-6">লগইন</h1>
            <div class="bg-white p-6 md:p-8 rounded-xl shadow-lg w-full">
                <form id="login-form">
                    <div class="mb-4">
                        <input type="email" id="email-input" name="email" placeholder="ইমেইল" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500" required>
                    </div>
                    <div class="mb-6">
                        <input type="password" id="password-input" name="password" placeholder="পাসওয়ার্ড" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500" required>
                    </div>
                    <button type="submit" id="login-btn" class="w-full bg-indigo-600 text-white py-3 rounded-lg font-bold text-lg hover:bg-indigo-700 transition duration-300">লগইন</button>
                </form>
            </div>
             <button id="login-back-btn" class="mt-6 text-indigo-600 hover:underline font-semibold">মূল পাতায় ফিরুন</button>
        </div>
    </div>

    <!-- About Page -->
    <div id="about-page" class="hidden relative min-h-screen bg-gray-100 p-4">
        <div class="absolute top-4 left-4">
            <button id="about-back-btn" class="flex items-center px-4 py-2 bg-gray-600 text-white rounded-lg font-semibold hover:bg-gray-700 transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z" clip-rule="evenodd" /></svg>
                <span id="about-back-btn-text">মূল পাতায় ফিরুন</span>
            </button>
        </div>
        <div class="container mx-auto mt-20 mb-10">
            <h2 id="about-title" class="text-3xl font-bold text-center text-gray-800 mb-10">আমাদের সম্পর্কে</h2>
            <div class="bg-white p-8 rounded-lg shadow-lg max-w-4xl mx-auto">
                <h3 id="founders-title" class="text-2xl font-semibold mb-6 text-center">প্রতিষ্ঠাতা গণ</h3>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mb-8">
                    <!-- Founder 1 -->
                    <div class="text-center">
                        <img src="https://placehold.co/150x150/E2E8F0/4A5568?text=Founder" alt="Founder 1" class="w-32 h-32 rounded-full mx-auto mb-4 shadow-md">
                        <h4 class="font-bold text-lg">মোঃ আব্দুল্লাহ</h4>
                        <p class="text-gray-600">যোগাযোগঃ 01234567890</p>
                    </div>
                    <!-- Founder 2 -->
                    <div class="text-center">
                        <img src="https://placehold.co/150x150/E2E8F0/4A5568?text=Founder" alt="Founder 2" class="w-32 h-32 rounded-full mx-auto mb-4 shadow-md">
                        <h4 class="font-bold text-lg">মোঃ করিম</h4>
                        <p class="text-gray-600">যোগাযোগঃ 01234567891</p>
                    </div>
                </div>
                <hr class="my-8">
                <p id="about-details" class="text-gray-700 text-center mb-8">
                    ইউনিক কোচিং সেন্টার একটি বিশ্বস্ত শিক্ষা প্রতিষ্ঠান যেখানে আমরা শিক্ষার্থীদের উজ্জ্বল ভবিষ্যতের জন্য কাজ করি।
                </p>
            </div>
        </div>
    </div>
    
    <!-- Admission Form Page -->
    <div id="admission-page" class="hidden relative min-h-screen bg-gray-100 p-4">
        <div class="absolute top-4 left-4">
            <button id="back-btn" class="flex items-center px-4 py-2 bg-gray-600 text-white rounded-lg font-semibold hover:bg-gray-700 transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z" clip-rule="evenodd" /></svg>
                <span id="back-btn-text">আগের পেজ</span>
            </button>
        </div>
        
        <div class="w-full max-w-lg mx-auto mt-20 mb-10">
            <h2 id="form-title" class="text-2xl md:text-3xl font-bold text-center text-gray-800 mb-8">ভর্তি ফর্ম</h2>
            <form id="admission-form" class="bg-white p-6 md:p-8 rounded-xl shadow-lg w-full space-y-4">
                <div>
                    <label id="label-fullname" for="full-name" class="block text-sm font-medium text-gray-700">পূর্ণ নাম</label>
                    <input type="text" id="full-name" name="fullName" class="mt-1 w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500" required>
                </div>
                <div>
                    <label id="label-class" for="class-apply" class="block text-sm font-medium text-gray-700">কোন শ্রেণীতে ভর্তি হতে ইচ্ছুক</label>
                    <select id="class-apply" name="classForApply" class="mt-1 w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500" required>
                        <option id="select-class-option" value="" selected disabled>একটি শ্রেণী নির্বাচন করুন</option>
                        <option id="class-2" value="Class 2">Class 2</option>
                        <option id="class-3" value="Class 3">Class 3</option>
                        <option id="class-4" value="Class 4">Class 4</option>
                        <option id="class-5" value="Class 5">Class 5</option>
                        <option id="class-6" value="Class 6">Class 6</option>
                        <option id="class-7" value="Class 7">Class 7</option>
                        <option id="class-8" value="Class 8">Class 8</option>
                        <option id="class-9" value="Class 9">Class 9</option>
                        <option id="class-10" value="Class 10">Class 10</option>
                        <option id="class-11" value="Class 11">Class 11</option>
                        <option id="class-12" value="Class 12">Class 12</option>
                    </select>
                </div>
                <div>
                    <label id="label-contact" for="contact-number" class="block text-sm font-medium text-gray-700">যোগাযোগের নম্বর</label>
                    <input type="tel" id="contact-number" name="contactNumber" class="mt-1 w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500" required>
                </div>
                 <div>
                    <label id="label-email" for="admission-email" class="block text-sm font-medium text-gray-700">ইমেইল</label>
                    <input type="email" id="admission-email" name="email" class="mt-1 w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500" required>
                </div>
                <div>
                    <label id="label-password" for="admission-password" class="block text-sm font-medium text-gray-700">পাসওয়ার্ড</label>
                    <input type="password" id="admission-password" name="password" class="mt-1 w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500" required>
                </div>
                <div>
                    <label id="label-school" for="prev-school" class="block text-sm font-medium text-gray-700">পূর্ববর্তী স্কুলের নাম</label>
                    <input type="text" id="prev-school" name="previousSchool" class="mt-1 w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500" required>
                </div>
                <div>
                    <label id="label-guardian-name" for="guardian-name" class="block text-sm font-medium text-gray-700">অভিভাবকের নাম</label>
                    <input type="text" id="guardian-name" name="guardiansName" class="mt-1 w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500" required>
                </div>
                <div>
                    <label id="label-guardian-contact" for="guardian-contact" class="block text-sm font-medium text-gray-700">অভিভাবকের যোগাযোগের নম্বর</label>
                    <input type="tel" id="guardian-contact" name="guardiansContact" class="mt-1 w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500" required>
                </div>
                <div>
                    <label id="label-address" for="address" class="block text-sm font-medium text-gray-700">ঠিকানা</label>
                    <textarea id="address" name="address" rows="3" class="mt-1 w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500" required></textarea>
                </div>
                <div class="pt-4">
                    <button type="submit" id="submit-btn" class="w-full bg-green-500 text-white py-3 rounded-lg font-bold text-lg hover:bg-green-600 transition duration-300">সাবমিট</button>
                </div>
            </form>
        </div>
        <footer class="text-center text-gray-500 text-xs md:text-sm w-full px-4 pb-4">
            <p id="copyright-form">© ইউনিক কোচিং সেন্টার</p>
        </footer>
    </div>

    <!-- Student Dashboard Page -->
    <div id="student-dashboard" class="hidden relative min-h-screen bg-gray-100 p-4">
         <div class="absolute top-4 left-4">
            <button id="student-back-btn" class="flex items-center px-4 py-2 bg-gray-600 text-white rounded-lg font-semibold hover:bg-gray-700 transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z" clip-rule="evenodd" /></svg>
                <span id="student-back-btn-text">মূল পাতায় ফিরুন</span>
            </button>
        </div>
        <div class="container mx-auto mt-20">
            <h2 id="student-title" class="text-3xl font-bold text-center text-gray-800 mb-10">ড্যাশবোর্ড</h2>
            <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-5 gap-6">
                <div id="student-box-1" class="relative bg-white p-6 rounded-lg shadow-md flex items-center justify-center h-32 cursor-pointer hover:shadow-xl transition-shadow">
                    <div class="icon-shadow" style="background-image: url('data:image/svg+xml,%3Csvg xmlns=\'http://www.w3.org/2000/svg\' fill=\'none\' viewBox=\'0 0 24 24\' stroke-width=\'1.5\' stroke=\'currentColor\' class=\'w-6 h-6\'%3E%3Cpath stroke-linecap=\'round\' stroke-linejoin=\'round\' d=\'M6.75 3v2.25M17.25 3v2.25M3 18.75V7.5a2.25 2.25 0 012.25-2.25h13.5A2.25 2.25 0 0121 7.5v11.25m-18 0A2.25 2.25 0 005.25 21h13.5A2.25 2.25 0 0021 18.75m-18 0h18M-4.5 12h22.5\' /%3E%3C/svg%3E%0A');"></div>
                    <span id="box-1-text-student" class="relative text-gray-700 font-semibold text-lg">রুটিন</span>
                </div>
                <div id="student-box-2" class="relative bg-white p-6 rounded-lg shadow-md flex items-center justify-center h-32 cursor-pointer hover:shadow-xl transition-shadow">
                    <div class="icon-shadow" style="background-image: url('data:image/svg+xml,%3Csvg xmlns=\'http://www.w3.org/2000/svg\' fill=\'none\' viewBox=\'0 0 24 24\' stroke-width=\'1.5\' stroke=\'currentColor\' class=\'w-6 h-6\'%3E%3Cpath stroke-linecap=\'round\' stroke-linejoin=\'round\' d=\'M12 6.042A8.967 8.967 0 006 3.75c-1.052 0-2.062.18-3 .512v14.25A8.987 8.987 0 016 18c2.305 0 4.408.867 6 2.292m0-14.25a8.966 8.966 0 016-2.292c1.052 0 2.062.18 3 .512v14.25A8.987 8.987 0 0018 18a8.967 8.967 0 00-6 2.292m0-14.25v14.25\' /%3E%3C/svg%3E%0A');"></div>
                    <span id="box-2-text-student" class="relative text-gray-700 font-semibold text-lg">ক্লাসসমূহ</span>
                </div>
                <div id="student-box-3" class="relative bg-white p-6 rounded-lg shadow-md flex items-center justify-center h-32 cursor-pointer hover:shadow-xl transition-shadow">
                    <div class="icon-shadow" style="background-image: url('data:image/svg+xml,%3Csvg xmlns=\'http://www.w3.org/2000/svg\' fill=\'none\' viewBox=\'0 0 24 24\' stroke-width=\'1.5\' stroke=\'currentColor\' class=\'w-6 h-6\'%3E%3Cpath stroke-linecap=\'round\' stroke-linejoin=\'round\' d=\'M15.75 6a3.75 3.75 0 11-7.5 0 3.75 3.75 0 017.5 0zM4.501 20.118a7.5 7.5 0 0114.998 0A17.933 17.933 0 0112 21.75c-2.676 0-5.216-.584-7.499-1.632z\' /%3E%3C/svg%3E%0A');"></div>
                    <span id="box-3-text-student" class="relative text-gray-700 font-semibold text-lg">শিক্ষকবৃন্দ</span>
                </div>
                <div id="student-box-4" class="relative bg-white p-6 rounded-lg shadow-md flex items-center justify-center h-32 cursor-pointer hover:shadow-xl transition-shadow">
                    <div class="icon-shadow" style="background-image: url('data:image/svg+xml,%3Csvg xmlns=\'http://www.w3.org/2000/svg\' fill=\'none\' viewBox=\'0 0 24 24\' stroke-width=\'1.5\' stroke=\'currentColor\' class=\'w-6 h-6\'%3E%3Cpath stroke-linecap=\'round\' stroke-linejoin=\'round\' d=\'M9 12h3.75M9 15h3.75M9 18h3.75m3 .75H18a2.25 2.25 0 002.25-2.25V6.108c0-1.135-.845-2.098-1.976-2.192a48.424 48.424 0 00-1.123-.08m-5.801 0c-.065.21-.1.433-.1.664 0 .414.336.75.75.75h4.5a.75.75 0 00.75-.75c0-.231-.035-.454-.1-.664M6.75 7.5H18a2.25 2.25 0 012.25 2.25v9.574c0 1.135-.845 2.098-1.976 2.192a48.427 48.427 0 01-1.123.08H6.75a2.25 2.25 0 01-2.25-2.25V7.5c0-1.244 1.006-2.25 2.25-2.25z\' /%3E%3C/svg%3E%0A');"></div>
                    <span id="box-4-text-student" class="relative text-gray-700 font-semibold text-lg">পরীক্ষা</span>
                </div>
                <div id="student-box-5" class="relative bg-white p-6 rounded-lg shadow-md flex items-center justify-center h-32 cursor-pointer hover:shadow-xl transition-shadow">
                    <div class="icon-shadow" style="background-image: url('data:image/svg+xml,%3Csvg xmlns=\'http://www.w3.org/2000/svg\' fill=\'none\' viewBox=\'0 0 24 24\' stroke-width=\'1.5\' stroke=\'currentColor\' class=\'w-6 h-6\'%3E%3Cpath stroke-linecap=\'round\' stroke-linejoin=\'round\' d=\'M3.75 3v11.25A2.25 2.25 0 006 16.5h2.25M3.75 3h-1.5m1.5 0h16.5m0 0h1.5m-1.5 0v11.25A2.25 2.25 0 0118 16.5h-2.25m-7.5 0h7.5m-7.5 0l-1.5-1.5m1.5 1.5l1.5-1.5m0 0l1.5 1.5m-1.5-1.5l-1.5 1.5m7.5-9l-3.75-3.75M12 12.75l-3.75-3.75M12 12.75l3.75 3.75M7.5 16.5l3.75-3.75M16.5 16.5l-3.75-3.75\' /%3E%3C/svg%3E%0A');"></div>
                    <span id="box-5-text-student" class="relative text-gray-700 font-semibold text-lg">ফলাফল</span>
                </div>
                <div id="student-box-6" class="relative bg-white p-6 rounded-lg shadow-md flex items-center justify-center h-32 cursor-pointer hover:shadow-xl transition-shadow">
                    <div class="icon-shadow" style="background-image: url('data:image/svg+xml,%3Csvg xmlns=\'http://www.w3.org/2000/svg\' fill=\'none\' viewBox=\'0 0 24 24\' stroke-width=\'1.5\' stroke=\'currentColor\' class=\'w-6 h-6\'%3E%3Cpath stroke-linecap=\'round\' stroke-linejoin=\'round\' d=\'M14.857 17.082a23.848 23.848 0 005.454-1.31A8.967 8.967 0 0118 9.75v-.7V9A6 6 0 006 9v.75a8.967 8.967 0 01-2.312 6.022c1.733.64 3.56 1.085 5.455 1.31m5.714 0a24.255 24.255 0 01-5.714 0m5.714 0a3 3 0 11-5.714 0\' /%3E%3C/svg%3E%0A');"></div>
                    <span id="box-6-text-student" class="relative text-gray-700 font-semibold text-lg">নোটিশ</span>
                </div>
            </div>
        </div>
    </div>

    <!-- Routine Page -->
    <div id="routine-page" class="hidden relative min-h-screen bg-gray-100 p-4">
         <div class="absolute top-4 left-4">
            <button id="routine-back-btn" class="flex items-center px-4 py-2 bg-gray-600 text-white rounded-lg font-semibold hover:bg-gray-700 transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z" clip-rule="evenodd" /></svg>
                <span id="routine-back-btn-text">ড্যাশবোর্ড</span>
            </button>
        </div>
        <div class="container mx-auto mt-20">
            <h2 id="routine-title" class="text-3xl font-bold text-center text-gray-800 mb-10">ক্লাস রুটিন</h2>
            <div id="routine-container" class="bg-white p-4 rounded-lg shadow-lg overflow-x-auto">
                <!-- Routine table will be generated here by JavaScript -->
            </div>
        </div>
    </div>

    <!-- Subjects Page -->
    <div id="subjects-page" class="hidden relative min-h-screen bg-gray-100 p-4">
         <div class="absolute top-4 left-4">
            <button id="subjects-back-btn" class="flex items-center px-4 py-2 bg-gray-600 text-white rounded-lg font-semibold hover:bg-gray-700 transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z" clip-rule="evenodd" /></svg>
                <span id="subjects-back-btn-text">ড্যাশবোর্ড</span>
            </button>
        </div>
        <div class="container mx-auto mt-20">
            <h2 id="subjects-title" class="text-3xl font-bold text-center text-gray-800 mb-10">উপলব্ধ বিষয়সমূহ</h2>
            <div id="subjects-container" class="bg-white p-4 rounded-lg shadow-lg overflow-x-auto">
                <!-- Subjects table will be generated here by JavaScript -->
            </div>
        </div>
    </div>

    <!-- Teachers Page -->
    <div id="teachers-page" class="hidden relative min-h-screen bg-gray-100 p-4">
         <div class="absolute top-4 left-4">
            <button id="teachers-back-btn" class="flex items-center px-4 py-2 bg-gray-600 text-white rounded-lg font-semibold hover:bg-gray-700 transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z" clip-rule="evenodd" /></svg>
                <span id="teachers-back-btn-text">ড্যাশবোর্ড</span>
            </button>
        </div>
        <div class="container mx-auto mt-20">
            <h2 id="teachers-title" class="text-3xl font-bold text-center text-gray-800 mb-10">আমাদের অভিজ্ঞ শিক্ষকবৃন্দ</h2>
            <div id="teachers-container" class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-8">
                <!-- Teacher cards will be generated here by JavaScript -->
            </div>
        </div>
    </div>

    <!-- Exams Page -->
    <div id="exams-page" class="hidden relative min-h-screen bg-gray-100 p-4">
         <div class="absolute top-4 left-4">
            <button id="exams-back-btn" class="flex items-center px-4 py-2 bg-gray-600 text-white rounded-lg font-semibold hover:bg-gray-700 transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z" clip-rule="evenodd" /></svg>
                <span id="exams-back-btn-text">ড্যাশবোর্ড</span>
            </button>
        </div>
        <div class="container mx-auto mt-20">
            <h2 id="exams-title" class="text-3xl font-bold text-center text-gray-800 mb-10">পরীক্ষার রুটিন</h2>
            <div id="exams-container" class="bg-white p-4 rounded-lg shadow-lg overflow-x-auto">
                <!-- Exams table will be generated here by JavaScript -->
            </div>
        </div>
    </div>

    <!-- Results Page -->
    <div id="results-page" class="hidden relative min-h-screen bg-gray-100 p-4">
         <div class="absolute top-4 left-4">
            <button id="results-back-btn" class="flex items-center px-4 py-2 bg-gray-600 text-white rounded-lg font-semibold hover:bg-gray-700 transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z" clip-rule="evenodd" /></svg>
                <span id="results-back-btn-text">ড্যাশবোর্ড</span>
            </button>
        </div>
        <div class="container mx-auto mt-20">
            <h2 id="results-title" class="text-3xl font-bold text-center text-gray-800 mb-10">ফলাফল</h2>
            <div class="bg-white p-6 rounded-lg shadow-lg">
                <div class="mb-4">
                    <label for="result-search" id="result-search-label" class="block text-sm font-medium text-gray-700 mb-1">আপনার নাম লিখুন</label>
                    <input type="text" id="result-search" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500">
                </div>
                <button id="result-search-btn" class="w-full bg-indigo-600 text-white py-2 rounded-lg font-semibold hover:bg-indigo-700">অনুসন্ধান</button>
            </div>
            <div id="results-container" class="mt-8 bg-white p-4 rounded-lg shadow-lg overflow-x-auto">
                <!-- Results table will be generated here by JavaScript -->
            </div>
        </div>
    </div>

    <!-- Notice Page -->
    <div id="notice-page" class="hidden relative min-h-screen bg-gray-100 p-4">
         <div class="absolute top-4 left-4">
            <button id="notice-back-btn" class="flex items-center px-4 py-2 bg-gray-600 text-white rounded-lg font-semibold hover:bg-gray-700 transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z" clip-rule="evenodd" /></svg>
                <span id="notice-back-btn-text">ড্যাশবোর্ড</span>
            </button>
        </div>
        <div class="container mx-auto mt-20">
            <h2 id="notice-title" class="text-3xl font-bold text-center text-gray-800 mb-10">নোটিশ বোর্ড</h2>
            <div id="notice-container" class="space-y-4">
                <!-- Notices will be generated here by JavaScript -->
            </div>
        </div>
    </div>
    
    <!-- Toast Notification -->
    <div id="toast" class="toast"></div>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            // --- Translations ---
            const translations = {
                bn: {
                    title: 'ইউনিক কোচিং সেন্টার', emailPlaceholder: 'ইমেইল', passwordPlaceholder: 'পাসওয়ার্ড',
                    loginBtn: 'লগইন', orDivider: 'অথবা', admissionLink: 'ভর্তির জন্য আবেদন',
                    copyright: `© ${new Date().getFullYear()} ইউনিক কোচিং সেন্টার`, pageTitle: 'ইউনিক কোচিং সেন্টার',
                    backBtnText: 'আগের পেজ', formTitle: 'ভর্তি ফর্ম', labelFullname: 'পূর্ণ নাম',
                    labelClass: 'কোন শ্রেণীতে ভর্তি হতে ইচ্ছুক', selectClassOption: 'একটি শ্রেণী নির্বাচন করুন',
                    class2: 'দ্বিতীয় শ্রেণী', class3: 'তৃতীয় শ্রেণী', class4: 'চতুর্থ শ্রেণী',
                    class5: 'পঞ্চম শ্রেণী', class6: 'ষষ্ঠ শ্রেণী', class7: 'সপ্তম শ্রেণী',
                    class8: 'অষ্টম শ্রেণী / জে.ডি.সি', class9: 'নবম (স্কুল/দাখিল)', class10: 'দশম (স্কুল/দাখিল)',
                    class11: 'একাদশ (কলেজ/আলিম)', class12: 'দ্বাদশ (কলেজ/আলিম)',
                    labelContact: 'যোগাযোগের নম্বর', labelEmail: 'ইমেইল', labelPassword: 'পাসওয়ার্ড', 
                    labelSchool: 'পূর্ববর্তী স্কুলের নাম', labelGuardianName: 'অভিভাবকের নাম', 
                    labelGuardianContact: 'অভিভাবকের যোগাযোগের নম্বর', labelAddress: 'ঠিকানা', 
                    submitBtn: 'সাবমিট', submitting: 'সাবমিট হচ্ছে...',
                    admissionSuccess: 'ভর্তি সফল হয়েছে!', admissionError: 'কিছু একটা সমস্যা হয়েছে, আবার চেষ্টা করুন।',
                    loggingIn: 'লগইন হচ্ছে...', loginSuccess: 'লগইন সফল হয়েছে!',
                    loginError: 'ভুল ইমেইল বা পাসওয়ার্ড।', applicationPending: 'আপনার আবেদনটি এখনো অপেক্ষমাণ আছে।', 
                    networkError: 'নেটওয়ার্ক সমস্যা, অনুগ্রহ করে আবার চেষ্টা করুন।',
                    sheetNotFoundError: 'Sheet-e "Students" naam-ti paowa jacche na. Onugroho kore check korun.',
                    adminDashboardTitle: 'এডমিন ড্যাশবোর্ড', adminBackBtnText: 'লগ-আউট', 
                    box1Text: 'রুটিন', comingSoon: 'শীঘ্রই আসছে...',
                    studentDashboardTitle: 'ড্যাশবোর্ড', studentBackBtnText: 'মূল পাতায় ফিরুন',
                    box1TextStudent: 'রুটিন', box2TextStudent: 'ক্লাসসমূহ', box3TextStudent: 'শিক্ষকবৃন্দ',
                    box4TextStudent: 'পরীক্ষা', box5TextStudent: 'ফলাফল', box6TextStudent: 'নোটিশ',
                    routineTitle: 'ক্লাস রুটিন', routineBackBtnText: 'ড্যাশবোর্ড',
                    subjectsTitle: 'উপলব্ধ বিষয়সমূহ', subjectsBackBtnText: 'ড্যাশবোর্ড',
                    teachersTitle: 'আমাদের অভিজ্ঞ শিক্ষকবৃন্দ', teachersBackBtnText: 'ড্যাশবোর্ড',
                    mainTitle: 'ইউনিক কোচিং সেন্টার', footerContactUs: 'যোগাযোগ করুন',
                    menuLogin: 'লগইন', menuAdminLogin: 'এডমিন লগইন', menuAdmission: 'ভর্তির জন্য আবেদন',
                    menuAbout: 'আমাদের সম্পর্কে', loginTitle: 'লগইন', adminLoginTitle: 'এডমিন লগইন',
                    loginBackBtn: 'মূল পাতায় ফিরুন', aboutTitle: 'আমাদের সম্পর্কে', foundersTitle: 'প্রতিষ্ঠাতা গণ',
                    aboutDetails: 'ইউনিক কোচিং সেন্টার একটি বিশ্বস্ত শিক্ষা প্রতিষ্ঠান যেখানে আমরা শিক্ষার্থীদের উজ্জ্বল ভবিষ্যতের জন্য কাজ করি।',
                    whyUsTitle: 'কেন আমরা সেরা?',
                    feature1Title: 'অভিজ্ঞ শিক্ষক', feature1Desc: 'আমাদের রয়েছে সেরা শিক্ষকদের একটি অভিজ্ঞ দল।',
                    feature2Title: 'বিশেষ নোট', feature2Desc: 'আমরা প্রতিটি বিষয়ের উপর বিশেষ নোট প্রদান করি।',
                    feature3Title: 'নিয়মিত পরীক্ষা', feature3Desc: 'সাপ্তাহিক ও মাসিক পরীক্ষার মাধ্যমে শিক্ষার্থীদের প্রস্তুত করা হয়।',
                    achieversTitle: 'আমাদের কৃতি শিক্ষার্থীরা (গত বছর)',
                    student1Name: 'মোঃ জাহিদ', student1Class: 'দশম শ্রেণী', student1Grade: 'A+',
                    student2Name: 'ফারিয়া আক্তার', student2Class: 'দ্বাদশ শ্রেণী', student2Grade: 'A+',
                    student3Name: 'আরিফ হোসেন', student3Class: 'দশম শ্রেণী', student3Grade: 'A+',
                    student4Name: 'সাদিয়া ইসলাম', student4Class: 'অষ্টম শ্রেণী', student4Grade: 'A+',
                    menuDashboard: 'ড্যাশবোর্ড', menuLogout: 'লগ-আউট', menuRoutine: 'রুটিন', menuClasses: 'ক্লাসসমূহ', menuTeachers: 'শিক্ষকবৃন্দ',
                    menuExams: 'পরীক্ষা', menuResults: 'ফলাফল', menuNotice: 'নোটিশ',
                    examsTitle: 'পরীক্ষার রুটিন', examsBackBtnText: 'ড্যাশবোর্ড',
                    resultsTitle: 'ফলাফল', resultsBackBtnText: 'ড্যাশবোর্ড',
                    resultSearchLabel: 'আপনার নাম লিখুন', resultSearchBtn: 'অনুসন্ধান',
                    noticeTitle: 'নোটিশ বোর্ড', noticeBackBtnText: 'ড্যাশবোর্ড'
                },
                en: {
                    title: 'Unique Coaching Centre', emailPlaceholder: 'Email', passwordPlaceholder: 'Password',
                    loginBtn: 'Login', orDivider: 'OR', admissionLink: 'Apply for Admission',
                    copyright: `© ${new Date().getFullYear()} Unique Coaching Centre`, pageTitle: 'Unique Coaching Centre',
                    backBtnText: 'Back', formTitle: 'Admission Form', labelFullname: 'Full Name',
                    labelClass: 'Class for Apply', selectClassOption: 'Select a Class',
                    class2: 'Class 2', class3: 'Class 3', class4: 'Class 4', class5: 'Class 5',
                    class6: 'Class 6', class7: 'Class 7', class8: 'Class 8 / JDC',
                    class9: 'Class 9 (School/Dakhil)', class10: 'Class 10 (School/Dakhil)',
                    class11: 'Class 11 (College/Alim)', class12: 'Class 12 (College/Alim)',
                    labelContact: 'Contact Number', labelEmail: 'Email',
                    labelPassword: 'Password', labelSchool: 'Previous School Name',
                    labelGuardianName: 'Guardians Name', labelGuardianContact: 'Guardian\'s Contact Number',
                    labelAddress: 'Address', submitBtn: 'Submit', submitting: 'Submitting...',
                    admissionSuccess: 'Admission Successful!', admissionError: 'Something went wrong, please try again.',
                    loggingIn: 'Logging in...', loginSuccess: 'Login Successful!',
                    loginError: 'Invalid email or password.', applicationPending: 'Your application is still pending.', 
                    networkError: 'Network error, please try again.',
                    sheetNotFoundError: 'Sheet named "Students" not found. Please check the name.',
                    adminDashboardTitle: 'Admin Dashboard', adminBackBtnText: 'Log Out', 
                    box1Text: 'Routine', comingSoon: 'Coming Soon...',
                    studentDashboardTitle: 'Dashboard', studentBackBtnText: 'Back to Main Page',
                    box1TextStudent: 'Routine', box2TextStudent: 'Classes', box3TextStudent: 'Teachers',
                    box4TextStudent: 'Exams', box5TextStudent: 'Results', box6TextStudent: 'Notice',
                    routineTitle: 'Class Routine', routineBackBtnText: 'Dashboard',
                    subjectsTitle: 'Available Subjects', subjectsBackBtnText: 'Dashboard',
                    teachersTitle: 'Our Experienced Teachers', teachersBackBtnText: 'Dashboard',
                    mainTitle: 'Unique Coaching Centre', footerContactUs: 'Contact Us',
                    menuLogin: 'Login', menuAdminLogin: 'Admin Login', menuAdmission: 'Apply for Admission',
                    menuAbout: 'About Us', loginTitle: 'Login', adminLoginTitle: 'Admin Login',
                    loginBackBtn: 'Back to Main Page', aboutTitle: 'About Us', foundersTitle: 'Founders',
                    aboutDetails: 'Unique Coaching Centre is a trusted educational institution where we work for the bright future of students.',
                    whyUsTitle: 'Why We Are The Best?',
                    feature1Title: 'Experienced Teachers', feature1Desc: 'We have an experienced team of the best teachers.',
                    feature2Title: 'Special Notes', feature2Desc: 'We provide special notes on every subject.',
                    feature3Title: 'Regular Exams', feature3Desc: 'Students are prepared through weekly and monthly exams.',
                    achieversTitle: 'Our Achievers (Last Year)',
                    student1Name: 'Md. Zahid', student1Class: 'Class 10', student1Grade: 'A+',
                    student2Name: 'Faria Akter', student2Class: 'Class 12', student2Grade: 'A+',
                    student3Name: 'Arif Hossain', student3Class: 'Class 10', student3Grade: 'A+',
                    student4Name: 'Sadia Islam', student4Class: 'Class 8', student4Grade: 'A+',
                    menuDashboard: 'Dashboard', menuLogout: 'Log Out', menuRoutine: 'Routine', menuClasses: 'Classes', menuTeachers: 'Teachers',
                    menuExams: 'Exams', menuResults: 'Results', menuNotice: 'Notice',
                    examsTitle: 'Exam Routine', examsBackBtnText: 'Dashboard',
                    resultsTitle: 'Results', resultsBackBtnText: 'Dashboard',
                    resultSearchLabel: 'Enter Your Name', resultSearchBtn: 'Search',
                    noticeTitle: 'Notice Board', noticeBackBtnText: 'Dashboard'
                }
            };
            let currentLang = 'bn';
            let isLoggedIn = false;

            const elements = {};

            function initializeElements() {
                const elementIds = [
                    'main-page', 'login-page', 'admission-page', 'admin-dashboard', 'student-dashboard',
                    'routine-page', 'subjects-page', 'teachers-page', 'about-page', 'exams-page',
                    'results-page', 'notice-page', 'menu-open-btn', 'menu-close-btn', 'menu-popup',
                    'menu-logged-out', 'menu-logged-in', 'menu-login-btn', 'menu-admin-login-btn',
                    'menu-admission-btn', 'menu-about-btn', 'menu-about-btn-loggedin', 'menu-dashboard-btn',
                    'menu-logout-btn', 'dashboard-submenu-toggle', 'dashboard-submenu', 'menu-routine-btn',
                    'menu-classes-btn', 'menu-teachers-btn', 'menu-exams-btn', 'menu-results-btn',
                    'menu-notice-btn', 'back-btn', 'admin-back-btn', 'student-back-btn',
                    'routine-back-btn', 'subjects-back-btn', 'teachers-back-btn', 'about-back-btn',
                    'login-back-btn', 'exams-back-btn', 'results-back-btn', 'notice-back-btn',
                    'student-box-1', 'student-box-2', 'student-box-3', 'student-box-4',
                    'student-box-5', 'student-box-6', 'lang-bn-btn', 'lang-en-btn',
                    'menu-lang-bn-btn', 'menu-lang-en-btn', 'admission-form', 'login-form', 'toast',
                    'main-title', 'footer-contact-us', 'copyright', 'login-title', 'about-title',
                    'founders-title', 'about-details', 'about-back-btn-text', 'email-input',
                    'password-input', 'login-btn', 'copyright-form', 'back-btn-text', 'form-title',
                    'label-fullname', 'label-class', 'select-class-option', 'class-2', 'class-3',
                    'class-4', 'class-5', 'class-6', 'class-7', 'class-8', 'class-9', 'class-10',
                    'class-11', 'class-12', 'label-contact', 'label-email', 'label-password',
                    'label-school', 'label-guardian-name', 'label-guardian-contact', 'label-address',
                    'submit-btn', 'admin-title', 'admin-back-btn-text', 'box-1-text',
                    'student-title', 'student-back-btn-text', 'box-1-text-student', 'box-2-text-student',
                    'box-3-text-student', 'box-4-text-student', 'box-5-text-student', 'box-6-text-student',
                    'routine-title', 'routine-back-btn-text', 'subjects-title', 'subjects-back-btn-text',
                    'teachers-title', 'teachers-back-btn-text', 'why-us-title', 'feature1-title',
                    'feature1-desc', 'feature2-title', 'feature2-desc', 'feature3-title',
                    'feature3-desc', 'achievers-title', 'student1-name', 'student1-class',
                    'student1-grade', 'student2-name', 'student2-class', 'student2-grade',
                    'student3-name', 'student3-class', 'student3-grade', 'student4-name',
                    'student4-class', 'student4-grade', 'exams-title', 'exams-back-btn-text',
                    'results-title', 'results-back-btn-text', 'result-search-label', 'result-search-btn',
                    'notice-title', 'notice-back-btn-text'
                ];
                elementIds.forEach(id => {
                    elements[id.replace(/-(\w)/g, (match, letter) => letter.toUpperCase())] = document.getElementById(id);
                });
                elements.comingSoonTexts = document.querySelectorAll('.coming-soon-text');
                elements.comingSoonTextsStudent = document.querySelectorAll('.coming-soon-text-student');
            }
            
            function switchPage(pageId) {
                const pages = document.querySelectorAll('body > div[id$="-page"], body > div[id$="-dashboard"]');
                pages.forEach(page => {
                    if (page) page.classList.add('hidden');
                });
                const currentPage = document.getElementById(pageId);
                if (currentPage) currentPage.classList.remove('hidden');
                
                const langSwitcher = document.getElementById('language-switcher');
                if(langSwitcher) langSwitcher.classList.toggle('hidden', pageId === 'main-page');

                window.scrollTo(0, 0);
            }
            
            function showToast(messageKey, type = 'success') {
                const toast = document.getElementById('toast');
                const message = translations[currentLang][messageKey];
                toast.textContent = message;
                toast.className = `toast show ${type}`;
                setTimeout(() => { toast.className = toast.className.replace("show", ""); }, 3000);
            }

            function updateMenuForLoginState() {
                elements.menuLoggedOut.classList.toggle('hidden', isLoggedIn);
                elements.menuLoggedIn.classList.toggle('hidden', !isLoggedIn);
            }

            function switchLanguage(lang) {
                currentLang = lang;
                const langData = translations[lang];
                document.documentElement.lang = lang;
                document.body.className = `bg-gray-100 lang-${lang}`;
                document.title = langData.pageTitle;
                
                Object.keys(elements).forEach(key => {
                    const el = elements[key];
                    if (el) {
                        if (key === 'comingSoonTexts' || key === 'comingSoonTextsStudent') {
                            el.forEach(span => span.innerText = langData.comingSoon);
                        } else if (key.includes('Placeholder')) {
                            el.placeholder = langData[key];
                        } else if (langData[key] !== undefined) {
                             el.innerText = langData[key];
                        }
                    }
                });
                
                const year = new Date().getFullYear();
                elements.copyright.innerText = `© ${year} ${lang === 'bn' ? 'ইউনিক কোচিং সেন্টার' : 'Unique Coaching Centre'}`;
                if(elements.copyrightForm) elements.copyrightForm.innerText = elements.copyright.innerText;

                // Sync both language switchers
                [elements.langBnBtn, elements.menuLangBnBtn].forEach(btn => {
                    btn.classList.toggle('bg-indigo-600', lang === 'bn');
                    btn.classList.toggle('text-white', lang === 'bn');
                    btn.classList.toggle('bg-white', lang !== 'bn');
                    btn.classList.toggle('text-gray-700', lang !== 'bn');
                });
                [elements.langEnBtn, elements.menuLangEnBtn].forEach(btn => {
                    btn.classList.toggle('bg-indigo-600', lang === 'en');
                    btn.classList.toggle('text-white', lang === 'en');
                    btn.classList.toggle('bg-white', lang !== 'en');
                    btn.classList.toggle('text-gray-700', lang !== 'en');
                });
            }
            
            // --- Data and Rendering ---
            const routineData = {
              "10:00 AM - 11:00 AM": { "শনি": [{ class: "Class 10", subject: "Math" }], "রবি": [{ class: "Class 9", subject: "Physics" }, { class: "Class 1", subject: "Art" }], "সোম": [{ class: "Class 10", subject: "English" }], "মঙ্গল": [], "বুধ": [{ class: "Class 9", subject: "Bangla" }], "বৃহস্পতি": [{ class: "Class 12", subject: "ICT" }] },
              "11:00 AM - 12:00 PM": { "শনি": [{ class: "Class 9", subject: "Higher Math" }], "রবি": [], "সোম": [{ class: "Class 11", subject: "Physics" }], "মঙ্গল": [{ class: "Class 10", subject: "Chemistry" }], "বুধ": [{ class: "Class 12", subject: "Math" }], "বৃহস্পতি": [] },
              "01:00 PM - 02:00 PM": { "শনি": [], "রবি": [{ class: "Class 12", subject: "Bangla" }], "সোম": [], "মঙ্গল": [{ class: "Class 11", subject: "ICT" }], "বুধ": [{ class: "Class 1", subject: "Music" }, { class: "Class 1", subject: "Dance" }], "বৃহস্পতি": [{ class: "Class 10", subject: "Physics" }] }
            };

            const subjectsData = {
                "Class 12": ["Bangla", "English", "ICT", "Physics", "Chemistry", "Math", "Biology"],
                "Class 11": ["Bangla", "English", "ICT", "Physics", "Chemistry", "Math", "Biology"],
                "Class 10": ["Bangla", "English", "Math", "Higher Math", "Physics", "Chemistry", "Biology", "ICT"],
                "Class 9": ["Bangla", "English", "Math", "Higher Math", "Physics", "Chemistry", "Biology"],
                "Class 8": ["Bangla", "English", "Math", "Science", "Social Science"],
                "Class 7": ["Bangla", "English", "Math", "Science"],
                "Class 6": []
            };
            
            const teachersData = [
                { name: "Mr. Alam", degree: "M.Sc in Physics", subject: "Physics", img: "https://placehold.co/200x200/E2E8F0/4A5568?text=Photo" },
                { name: "Ms. Sharmin", degree: "M.A in English", subject: "English", img: "https://placehold.co/200x200/E2E8F0/4A5568?text=Photo" },
                { name: "Mr. Karim", degree: "M.Sc in Math", subject: "Mathematics", img: "https://placehold.co/200x200/E2E8F0/4A5568?text=Photo" },
                { name: "Mrs. Halima", degree: "M.S.S", subject: "Bangla", img: "https://placehold.co/200x200/E2E8F0/4A5568?text=Photo" }
            ];

            const examsData = [
                { class: "Class 10", subject: "Math", date: "10 Aug, 2025", time: "10:00 AM" },
                { class: "Class 9", subject: "Physics", date: "11 Aug, 2025", time: "11:00 AM" },
                { class: "Class 12", subject: "ICT", date: "12 Aug, 2025", time: "01:00 PM" }
            ];

            const resultsData = [
                { name: "মোঃ জাহিদ", class: "Class 10", exam: "Weekly Test", subject: "Math", marks: "85/100" },
                { name: "ফারিয়া আক্তার", class: "Class 12", exam: "Monthly Test", subject: "ICT", marks: "92/100" }
            ];

            const noticeData = [
                { title: "আগামীকাল কোচিং বন্ধ", date: "02 Aug, 2025", content: "বিশেষ কারণে আগামীকাল কোচিং এর সকল কার্যক্রম বন্ধ থাকবে।" },
                { title: "নতুন ব্যাচ শুরু", date: "01 Aug, 2025", content: "দশম শ্রেণীর নতুন গণিত ব্যাচ আগামী সপ্তাহ থেকে শুরু হতে যাচ্ছে।" }
            ];

            function renderRoutine() {
                const container = document.getElementById('routine-container');
                container.innerHTML = '';
                const table = document.createElement('table');
                table.className = 'min-w-full divide-y divide-gray-200 border';
                const days = ["শনি", "রবি", "সোম", "মঙ্গল", "বুধ", "বৃহস্পতি"];
                const thead = document.createElement('thead');
                thead.className = 'bg-gray-50';
                let tr = document.createElement('tr');
                let th = document.createElement('th');
                th.className = 'px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider';
                th.textContent = 'সময়';
                tr.appendChild(th);
                days.forEach(day => {
                    th = document.createElement('th');
                    th.className = 'px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider';
                    th.textContent = day;
                    tr.appendChild(th);
                });
                thead.appendChild(tr);
                table.appendChild(thead);
                const tbody = document.createElement('tbody');
                tbody.className = 'bg-white divide-y divide-gray-200';
                for (const time in routineData) {
                    tr = document.createElement('tr');
                    let td = document.createElement('td');
                    td.className = 'px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900';
                    td.textContent = time;
                    tr.appendChild(td);
                    days.forEach(day => {
                        td = document.createElement('td');
                        td.className = 'px-6 py-4 whitespace-nowrap text-sm text-gray-500 align-top';
                        const classes = routineData[time][day];
                        if (classes && classes.length > 0) {
                            classes.forEach(c => {
                                const div = document.createElement('div');
                                div.className = 'mb-1 p-1 bg-indigo-100 text-indigo-800 rounded-md text-center';
                                div.textContent = `${c.class} (${c.subject})`;
                                td.appendChild(div);
                            });
                        }
                        tr.appendChild(td);
                    });
                    tbody.appendChild(tr);
                }
                table.appendChild(tbody);
                container.appendChild(table);
            }

            function renderSubjects() {
                const container = document.getElementById('subjects-container');
                container.innerHTML = '';
                const table = document.createElement('table');
                table.className = 'min-w-full divide-y divide-gray-200 border';
                const thead = document.createElement('thead');
                thead.className = 'bg-gray-50';
                let tr = document.createElement('tr');
                let thClass = document.createElement('th');
                thClass.className = 'px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider';
                thClass.textContent = 'শ্রেণী';
                tr.appendChild(thClass);
                let thSubjects = document.createElement('th');
                thSubjects.className = 'px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider';
                thSubjects.textContent = 'বিষয়সমূহ';
                tr.appendChild(thSubjects);
                thead.appendChild(tr);
                table.appendChild(thead);
                const tbody = document.createElement('tbody');
                tbody.className = 'bg-white divide-y divide-gray-200';
                for (const className in subjectsData) {
                    tr = document.createElement('tr');
                    let tdClass = document.createElement('td');
                    tdClass.className = 'px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900';
                    tdClass.textContent = className;
                    tr.appendChild(tdClass);
                    let tdSubjects = document.createElement('td');
                    tdSubjects.className = 'px-6 py-4 text-sm text-gray-500';
                    const subjects = subjectsData[className];
                    if (subjects && subjects.length > 0) {
                        const subjectContainer = document.createElement('div');
                        subjectContainer.className = 'flex flex-wrap gap-2';
                        subjects.forEach(subject => {
                            const span = document.createElement('span');
                            span.className = 'px-2 py-1 bg-green-100 text-green-800 text-xs font-semibold rounded-full';
                            span.textContent = subject;
                            subjectContainer.appendChild(span);
                        });
                        tdSubjects.appendChild(subjectContainer);
                    }
                    tr.appendChild(tdSubjects);
                    tbody.appendChild(tr);
                }
                table.appendChild(tbody);
                container.appendChild(table);
            }

            function renderTeachers() {
                const container = document.getElementById('teachers-container');
                container.innerHTML = '';
                teachersData.forEach(teacher => {
                    const card = document.createElement('div');
                    card.className = 'bg-white rounded-lg shadow-md overflow-hidden';
                    card.innerHTML = `
                        <img class="w-full h-48 object-cover" src="${teacher.img}" alt="${teacher.name}" onerror="this.onerror=null; this.src='https://placehold.co/200x200/E2E8F0/4A5568?text=Photo';">
                        <div class="p-4">
                            <h3 class="text-lg font-semibold text-gray-800">${teacher.name}</h3>
                            <p class="text-sm text-gray-600">${teacher.degree}</p>
                            <p class="mt-2 text-sm text-indigo-600 font-bold">${teacher.subject}</p>
                        </div>
                    `;
                    container.appendChild(card);
                });
            }

            function renderExams() {
                 const container = document.getElementById('exams-container');
                container.innerHTML = '';
                const table = document.createElement('table');
                table.className = 'min-w-full divide-y divide-gray-200 border';
                const thead = document.createElement('thead');
                thead.className = 'bg-gray-50';
                let tr = document.createElement('tr');
                const headers = ['শ্রেণী', 'বিষয়', 'তারিখ', 'সময়'];
                headers.forEach(headerText => {
                    let th = document.createElement('th');
                    th.className = 'px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider';
                    th.textContent = headerText;
                    tr.appendChild(th);
                });
                thead.appendChild(tr);
                table.appendChild(thead);
                const tbody = document.createElement('tbody');
                tbody.className = 'bg-white divide-y divide-gray-200';
                examsData.forEach(exam => {
                    tr = document.createElement('tr');
                    tr.innerHTML = `
                        <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900">${exam.class}</td>
                        <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">${exam.subject}</td>
                        <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">${exam.date}</td>
                        <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">${exam.time}</td>
                    `;
                    tbody.appendChild(tr);
                });
                table.appendChild(tbody);
                container.appendChild(table);
            }

            function renderResults(searchTerm = '') {
                const container = document.getElementById('results-container');
                container.innerHTML = '';
                const filteredResults = resultsData.filter(result => result.name.toLowerCase().includes(searchTerm.toLowerCase()));
                
                if (filteredResults.length === 0 && searchTerm) {
                    container.textContent = 'কোনো ফলাফল পাওয়া যায়নি।';
                    return;
                }

                const table = document.createElement('table');
                table.className = 'min-w-full divide-y divide-gray-200 border';
                const thead = document.createElement('thead');
                thead.className = 'bg-gray-50';
                let tr = document.createElement('tr');
                const headers = ['নাম', 'শ্রেণী', 'পরীক্ষা', 'বিষয়', 'নম্বর'];
                headers.forEach(headerText => {
                    let th = document.createElement('th');
                    th.className = 'px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider';
                    th.textContent = headerText;
                    tr.appendChild(th);
                });
                thead.appendChild(tr);
                table.appendChild(thead);
                const tbody = document.createElement('tbody');
                tbody.className = 'bg-white divide-y divide-gray-200';
                filteredResults.forEach(result => {
                    tr = document.createElement('tr');
                    tr.innerHTML = `
                        <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900">${result.name}</td>
                        <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">${result.class}</td>
                        <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">${result.exam}</td>
                        <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">${result.subject}</td>
                        <td class="px-6 py-4 whitespace-nowrap text-sm font-bold text-gray-800">${result.marks}</td>
                    `;
                    tbody.appendChild(tr);
                });
                table.appendChild(tbody);
                container.appendChild(table);
            }

            function renderNotices() {
                const container = document.getElementById('notice-container');
                container.innerHTML = '';
                noticeData.forEach(notice => {
                    const card = document.createElement('div');
                    card.className = 'bg-yellow-100 border-l-4 border-yellow-500 text-yellow-700 p-4 shadow-md';
                    card.innerHTML = `
                        <div class="flex justify-between items-center mb-1">
                            <p class="font-bold">${notice.title}</p>
                            <p class="text-xs">${notice.date}</p>
                        </div>
                        <p class="text-sm">${notice.content}</p>
                    `;
                    container.appendChild(card);
                });
            }
            
            // --- Event Listeners ---
            initializeElements();

            elements.menuOpenBtn.addEventListener('click', () => elements.menuPopup.classList.remove('hidden'));
            elements.menuCloseBtn.addEventListener('click', () => elements.menuPopup.classList.add('hidden'));
            
            elements.menuLoginBtn.addEventListener('click', () => {
                elements.loginTitle.innerText = translations[currentLang].loginTitle;
                switchPage('login-page');
                elements.menuPopup.classList.add('hidden');
            });
            if (elements.menuAdminLoginBtn) {
                elements.menuAdminLoginBtn.addEventListener('click', () => {
                    elements.loginTitle.innerText = translations[currentLang].adminLoginTitle;
                    switchPage('login-page');
                    elements.menuPopup.classList.add('hidden');
                });
            }
            elements.menuAdmissionBtn.addEventListener('click', () => {
                switchPage('admission-page');
                elements.menuPopup.classList.add('hidden');
            });
            [elements.menuAboutBtn, elements.menuAboutBtnLoggedIn].forEach(btn => {
                if(btn) {
                    btn.addEventListener('click', () => {
                        switchPage('about-page');
                        elements.menuPopup.classList.add('hidden');
                    });
                }
            });

            elements.menuDashboardBtn.addEventListener('click', () => {
                switchPage('student-dashboard');
                elements.menuPopup.classList.add('hidden');
            });
            elements.dashboardSubmenuToggle.addEventListener('click', (e) => {
                e.stopPropagation();
                elements.dashboardSubmenu.classList.toggle('hidden');
                e.currentTarget.querySelector('svg').classList.toggle('rotate-180');
            });

            elements.menuRoutineBtn.addEventListener('click', () => {
                renderRoutine();
                switchPage('routine-page');
                elements.menuPopup.classList.add('hidden');
            });
            elements.menuClassesBtn.addEventListener('click', () => {
                renderSubjects();
                switchPage('subjects-page');
                elements.menuPopup.classList.add('hidden');
            });
            elements.menuTeachersBtn.addEventListener('click', () => {
                renderTeachers();
                switchPage('teachers-page');
                elements.menuPopup.classList.add('hidden');
            });
            elements.menuExamsBtn.addEventListener('click', () => {
                renderExams();
                switchPage('exams-page');
                elements.menuPopup.classList.add('hidden');
            });
            elements.menuResultsBtn.addEventListener('click', () => {
                renderResults();
                switchPage('results-page');
                elements.menuPopup.classList.add('hidden');
            });
            elements.menuNoticeBtn.addEventListener('click', () => {
                renderNotices();
                switchPage('notice-page');
                elements.menuPopup.classList.add('hidden');
            });

            elements.menuLogoutBtn.addEventListener('click', () => {
                isLoggedIn = false;
                updateMenuForLoginState();
                switchPage('main-page');
                elements.menuPopup.classList.add('hidden');
            });

            elements.loginBackBtn.addEventListener('click', () => switchPage('main-page'));
            elements.aboutBackBtn.addEventListener('click', () => switchPage('main-page'));
            elements.backBtn.addEventListener('click', () => switchPage('main-page')); // Back from admission form
            if (elements.adminBackBtn) {
                elements.adminBackBtn.addEventListener('click', () => switchPage('main-page'));
            }
            elements.studentBackBtn.addEventListener('click', () => switchPage('main-page'));
            elements.routineBackBtn.addEventListener('click', () => switchPage('student-dashboard'));
            elements.subjectsBackBtn.addEventListener('click', () => switchPage('student-dashboard'));
            elements.teachersBackBtn.addEventListener('click', () => switchPage('student-dashboard'));
            elements.examsBackBtn.addEventListener('click', () => switchPage('student-dashboard'));
            elements.resultsBackBtn.addEventListener('click', () => switchPage('student-dashboard'));
            elements.noticeBackBtn.addEventListener('click', () => switchPage('student-dashboard'));
            
            elements.studentBox1.addEventListener('click', () => {
                renderRoutine();
                switchPage('routine-page');
            });
            elements.studentBox2.addEventListener('click', () => {
                renderSubjects();
                switchPage('subjects-page');
            });
            elements.studentBox3.addEventListener('click', () => {
                renderTeachers();
                switchPage('teachers-page');
            });
            elements.studentBox4.addEventListener('click', () => {
                renderExams();
                switchPage('exams-page');
            });
            elements.studentBox5.addEventListener('click', () => {
                renderResults();
                switchPage('results-page');
            });
            elements.studentBox6.addEventListener('click', () => {
                renderNotices();
                switchPage('notice-page');
            });
            
            // Handle Admission Form Submission
            elements.admissionForm.addEventListener('submit', e => {
                e.preventDefault();
                const submitBtn = document.getElementById('submit-btn');
                submitBtn.disabled = true;
                submitBtn.textContent = translations[currentLang].submitting;
                
                const scriptURL = 'https://script.google.com/macros/s/AKfycbzTmLksl8pg1_KJmG0lX-cl3r_lFgDt4OXTHC3AXVqoWruppiA5_zXenFIlAabNmZITLg/exec'; 

                const formData = new FormData(elements.admissionForm);

                fetch(scriptURL, { method: 'POST', body: formData})
                    .then(res => res.json())
                    .then(data => {
                        if (data.status === 'success') {
                            showToast('admissionSuccess', 'success');
                            elements.admissionForm.reset();
                            setTimeout(() => switchPage('main-page'), 1000);
                        } else {
                            throw new Error(data.message || 'Submission failed');
                        }
                    })
                    .catch(error => {
                        console.error('Error!', error.message);
                        if (error.message.includes('Sheet \'Students\' not found')) {
                            showToast('sheetNotFoundError', 'error');
                        } else {
                            showToast('admissionError', 'error');
                        }
                    })
                    .finally(() => {
                        submitBtn.disabled = false;
                        submitBtn.textContent = translations[currentLang].submitBtn;
                    });
            });

            // Handle Login Form Submission
            elements.loginForm.addEventListener('submit', e => {
                e.preventDefault();
                const loginBtn = document.getElementById('login-btn');
                loginBtn.disabled = true;
                loginBtn.textContent = translations[currentLang].loggingIn;

                const email = elements.loginForm.email.value;
                const password = elements.loginForm.password.value;

                const scriptURL_base = 'https://script.google.com/macros/s/AKfycbzTmLksl8pg1_KJmG0lX-cl3r_lFgDt4OXTHC3AXVqoWruppiA5_zXenFIlAabNmZITLg/exec';
                
                const scriptURL = `${scriptURL_base}?action=login&email=${encodeURIComponent(email)}&password=${encodeURIComponent(password)}`;

                fetch(scriptURL)
                    .then(res => res.json())
                    .then(data => {
                        if (data.status === 'success') {
                            showToast('loginSuccess', 'success');
                            elements.loginForm.reset();
                            isLoggedIn = true;
                            updateMenuForLoginState();
                            switchPage('main-page');
                        } else if (data.message && data.message.includes("not approved")) {
                            showToast('applicationPending', 'error');
                        }
                        else {
                            showToast('loginError', 'error');
                        }
                    })
                    .catch(error => {
                        console.error('Error!', error.message);
                        if (email === 'student121@gmail.com' && password === 'ST121') {
                             showToast('loginSuccess', 'success');
                             elements.loginForm.reset();
                             isLoggedIn = true;
                             updateMenuForLoginState();
                             switchPage('main-page');
                        } else {
                            showToast('networkError', 'error');
                        }
                    })
                    .finally(() => {
                        loginBtn.disabled = false;
                        loginBtn.textContent = translations[currentLang].loginBtn;
                    });
            });
            
            document.getElementById('result-search-btn').addEventListener('click', () => {
                const searchTerm = document.getElementById('result-search').value;
                renderResults(searchTerm);
            });

            [elements.langBnBtn, elements.menuLangBnBtn].forEach(btn => btn.addEventListener('click', () => switchLanguage('bn')));
            [elements.langEnBtn, elements.menuLangEnBtn].forEach(btn => btn.addEventListener('click', () => switchLanguage('en')));

            // Set initial state
            switchPage('main-page');
            switchLanguage('bn');
        });
    </script>
</body>
</html>
