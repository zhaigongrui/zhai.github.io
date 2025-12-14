<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>翟公瑞的个人博客</title>
    <!-- 引入Tailwind CSS简化样式开发 -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- 引入Font Awesome图标 -->
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    <!-- 自定义Tailwind配置 -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#2563eb',
                        secondary: '#475569',
                        accent: '#f97316',
                        light: '#f8fafc',
                        dark: '#0f172a'
                    },
                    fontFamily: {
                        sans: ['Inter', 'system-ui', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    <style type="text/tailwindcss">
        @layer utilities {
            .content-auto {
                content-visibility: auto;
            }
            .blog-card-hover {
                @apply transition-all duration-300 hover:shadow-lg hover:-translate-y-1;
            }
            .nav-link {
                @apply px-4 py-2 rounded-md hover:bg-primary/10 transition-colors duration-200;
            }
        }
    </style>
</head>
<body class="bg-gray-50 text-dark">
    <!-- 导航栏 -->
    <header class="sticky top-0 z-50 bg-white shadow-sm">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <!-- 左侧logo/名称 -->
                <div class="flex items-center space-x-2">
                    <i class="fa fa-book text-primary text-2xl"></i>
                    <div>
                        <h1 class="text-xl font-bold text-primary">翟公瑞的博客</h1>
                        <p class="text-xs text-gray-500">学号：20242800005</p>
                    </div>
                </div>
                
                <!-- 桌面端导航 -->
                <nav class="hidden md:flex space-x-1">
                    <a href="#home" class="nav-link text-primary font-medium">首页</a>
                    <a href="#blogs" class="nav-link text-secondary">博客列表</a>
                    <a href="#categories" class="nav-link text-secondary">分类</a>
                    <a href="#about" class="nav-link text-secondary">关于我</a>
                </nav>
                
                <!-- 移动端菜单按钮 -->
                <button id="menuBtn" class="md:hidden text-secondary hover:text-primary">
                    <i class="fa fa-bars text-xl"></i>
                </button>
            </div>
        </div>
        
        <!-- 移动端导航菜单 -->
        <div id="mobileMenu" class="md:hidden hidden bg-white border-t border-gray-100">
            <div class="container mx-auto px-4 py-2 flex flex-col space-y-1">
                <a href="#home" class="nav-link text-primary font-medium">首页</a>
                <a href="#blogs" class="nav-link text-secondary">博客列表</a>
                <a href="#categories" class="nav-link text-secondary">分类</a>
                <a href="#about" class="nav-link text-secondary">关于我</a>
            </div>
        </div>
    </header>

    <main>
        <!-- 首页横幅 -->
        <section id="home" class="bg-gradient-to-r from-primary to-blue-700 text-white py-16 md:py-24">
            <div class="container mx-auto px-4 sm:px-6 lg:px-8">
                <div class="max-w-3xl mx-auto text-center">
                    <h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-4">
                        欢迎来到翟公瑞的个人博客
                    </h2>
                    <p class="text-lg md:text-xl opacity-90 mb-8">
                        记录学习历程，分享技术心得，探索编程世界
                    </p>
                    <a href="#blogs" class="inline-block bg-white text-primary font-medium px-6 py-3 rounded-lg shadow-md hover:shadow-lg transition-shadow">
                        浏览博客 <i class="fa fa-arrow-right ml-2"></i>
                    </a>
                </div>
            </div>
        </section>

        <!-- 博客列表 -->
        <section id="blogs" class="py-16 bg-white">
            <div class="container mx-auto px-4 sm:px-6 lg:px-8">
                <div class="max-w-5xl mx-auto">
                    <div class="text-center mb-12">
                        <h2 class="text-3xl font-bold text-dark mb-2">最新博客</h2>
                        <p class="text-gray-600">分享我的学习与思考</p>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                        <!-- 博客卡片1 -->
                        <div class="bg-light rounded-lg overflow-hidden shadow blog-card-hover">
                            <img src="https://picsum.photos/600/400?random=1" alt="博客封面" class="w-full h-48 object-cover">
                            <div class="p-6">
                                <div class="flex items-center text-sm text-gray-500 mb-2">
                                    <span><i class="fa fa-calendar-o mr-1"></i> 2025-01-15</span>
                                    <span class="ml-4"><i class="fa fa-folder-o mr-1"></i> 前端开发</span>
                                </div>
                                <h3 class="text-xl font-bold mb-3 hover:text-primary transition-colors">
                                    <a href="#">Tailwind CSS快速上手与实战技巧</a>
                                </h3>
                                <p class="text-gray-600 mb-4 line-clamp-3">
                                    Tailwind CSS是一个功能优先的CSS框架，本文将介绍如何快速上手Tailwind，并分享一些在实际项目中常用的技巧和最佳实践，帮助你更高效地开发前端界面。
                                </p>
                                <a href="#" class="text-primary font-medium hover:underline">
                                    阅读更多 <i class="fa fa-angle-right ml-1"></i>
                                </a>
                            </div>
                        </div>

                        <!-- 博客卡片2 -->
                        <div class="bg-light rounded-lg overflow-hidden shadow blog-card-hover">
                            <img src="https://picsum.photos/600/400?random=2" alt="博客封面" class="w-full h-48 object-cover">
                            <div class="p-6">
                                <div class="flex items-center text-sm text-gray-500 mb-2">
                                    <span><i class="fa fa-calendar-o mr-1"></i> 2025-01-10</span>
                                    <span class="ml-4"><i class="fa fa-folder-o mr-1"></i> JavaScript</span>
                                </div>
                                <h3 class="text-xl font-bold mb-3 hover:text-primary transition-colors">
                                    <a href="#">JavaScript异步编程全解析</a>
                                </h3>
                                <p class="text-gray-600 mb-4 line-clamp-3">
                                    从回调函数到Promise，再到async/await，本文详细解析JavaScript异步编程的发展历程和各种实现方式，帮助你彻底理解异步编程的核心思想。
                                </p>
                                <a href="#" class="text-primary font-medium hover:underline">
                                    阅读更多 <i class="fa fa-angle-right ml-1"></i>
                                </a>
                            </div>
                        </div>

                        <!-- 博客卡片3 -->
                        <div class="bg-light rounded-lg overflow-hidden shadow blog-card-hover">
                            <img src="https://picsum.photos/600/400?random=3" alt="博客封面" class="w-full h-48 object-cover">
                            <div class="p-6">
                                <div class="flex items-center text-sm text-gray-500 mb-2">
                                    <span><i class="fa fa-calendar-o mr-1"></i> 2025-01-05</span>
                                    <span class="ml-4"><i class="fa fa-folder-o mr-1"></i> 学习心得</span>
                                </div>
                                <h3 class="text-xl font-bold mb-3 hover:text-primary transition-colors">
                                    <a href="#">计算机专业入门学习路线分享</a>
                                </h3>
                                <p class="text-gray-600 mb-4 line-clamp-3">
                                    作为一名计算机专业的新生，结合自己的学习经验，整理了一份从入门到进阶的学习路线，涵盖编程语言、算法、计算机基础等多个方面，希望能帮助到同专业的同学。
                                </p>
                                <a href="#" class="text-primary font-medium hover:underline">
                                    阅读更多 <i class="fa fa-angle-right ml-1"></i>
                                </a>
                            </div>
                        </div>

                        <!-- 博客卡片4 -->
                        <div class="bg-light rounded-lg overflow-hidden shadow blog-card-hover">
                            <img src="https://picsum.photos/600/400?random=4" alt="博客封面" class="w-full h-48 object-cover">
                            <div class="p-6">
                                <div class="flex items-center text-sm text-gray-500 mb-2">
                                    <span><i class="fa fa-calendar-o mr-1"></i> 2025-01-01</span>
                                    <span class="ml-4"><i class="fa fa-folder-o mr-1"></i> 工具使用</span>
                                </div>
                                <h3 class="text-xl font-bold mb-3 hover:text-primary transition-colors">
                                    <a href="#">Git与GitHub常用操作指南</a>
                                </h3>
                                <p class="text-gray-600 mb-4 line-clamp-3">
                                    本文总结了Git和GitHub的常用操作命令和使用技巧，包括版本控制、分支管理、提交规范、远程仓库操作等，适合初学者快速掌握版本控制工具的使用。
                                </p>
                                <a href="#" class="text-primary font-medium hover:underline">
                                    阅读更多 <i class="fa fa-angle-right ml-1"></i>
                                </a>
                            </div>
                        </div>
                    </div>

                    <div class="text-center mt-10">
                        <button class="px-6 py-2 border border-primary text-primary rounded-lg hover:bg-primary hover:text-white transition-colors">
                            加载更多 <i class="fa fa-refresh ml-1"></i>
                        </button>
                    </div>
                </div>
            </div>
        </section>

        <!-- 分类板块 -->
        <section id="categories" class="py-16 bg-gray-50">
            <div class="container mx-auto px-4 sm:px-6 lg:px-8">
                <div class="max-w-5xl mx-auto">
                    <div class="text-center mb-12">
                        <h2 class="text-3xl font-bold text-dark mb-2">博客分类</h2>
                        <p class="text-gray-600">按主题浏览我的博客内容</p>
                    </div>

                    <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-6">
                        <!-- 分类卡片1 -->
                        <div class="bg-white rounded-lg p-6 text-center shadow hover:shadow-md transition-shadow">
                            <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center mx-auto mb-4">
                                <i class="fa fa-code text-primary text-xl"></i>
                            </div>
                            <h3 class="font-bold mb-2">前端开发</h3>
                            <p class="text-gray-600 text-sm">12篇文章</p>
                        </div>

                        <!-- 分类卡片2 -->
                        <div class="bg-white rounded-lg p-6 text-center shadow hover:shadow-md transition-shadow">
                            <div class="w-12 h-12 bg-green-100 rounded-full flex items-center justify-center mx-auto mb-4">
                                <i class="fa fa-server text-green-600 text-xl"></i>
                            </div>
                            <h3 class="font-bold mb-2">后端开发</h3>
                            <p class="text-gray-600 text-sm">8篇文章</p>
                        </div>

                        <!-- 分类卡片3 -->
                        <div class="bg-white rounded-lg p-6 text-center shadow hover:shadow-md transition-shadow">
                            <div class="w-12 h-12 bg-purple-100 rounded-full flex items-center justify-center mx-auto mb-4">
                                <i class="fa fa-book text-purple-600 text-xl"></i>
                            </div>
                            <h3 class="font-bold mb-2">学习心得</h3>
                            <p class="text-gray-600 text-sm">15篇文章</p>
                        </div>

                        <!-- 分类卡片4 -->
                        <div class="bg-white rounded-lg p-6 text-center shadow hover:shadow-md transition-shadow">
                            <div class="w-12 h-12 bg-orange-100 rounded-full flex items-center justify-center mx-auto mb-4">
                                <i class="fa fa-wrench text-accent text-xl"></i>
                            </div>
                            <h3 class="font-bold mb-2">工具使用</h3>
                            <p class="text-gray-600 text-sm">6篇文章</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 关于我 -->
        <section id="about" class="py-16 bg-white">
            <div class="container mx-auto px-4 sm:px-6 lg:px-8">
                <div class="max-w-4xl mx-auto">
                    <div class="text-center mb-12">
                        <h2 class="text-3xl font-bold text-dark mb-2">关于我</h2>
                        <p class="text-gray-600">认识一个真实的翟公瑞</p>
                    </div>

                    <div class="flex flex-col md:flex-row items-center gap-8">
                        <div class="w-full md:w-1/3">
                            <div class="relative">
                                <img src="https://picsum.photos/400/400?random=10" alt="个人头像" class="w-64 h-64 object-cover rounded-full mx-auto border-4 border-primary/20">
                                <div class="absolute -bottom-4 -right-4 bg-accent text-white w-16 h-16 rounded-full flex items-center justify-center text-xl font-bold">
                                    2024
                                </div>
                            </div>
                        </div>

                        <div class="w-full md:w-2/3">
                            <div class="bg-light p-8 rounded-lg shadow">
                                <h3 class="text-2xl font-bold mb-4">翟公瑞</h3>
                                <p class="text-gray-700 mb-2"><span class="font-medium">学号：</span>20242800005</p>
                                <p class="text-gray-700 mb-4"><span class="font-medium">专业：</span>计算机科学与技术</p>
                                
                                <p class="text-gray-600 mb-6">
                                    大家好，我是翟公瑞，一名计算机专业的学生，热爱编程和技术探索。
                                    我创建这个博客的初衷是记录自己的学习历程，分享所学的知识和遇到的问题，
                                    同时也希望能和更多的技术爱好者交流学习，共同进步。
                                </p>

                                <div class="flex flex-wrap gap-4 mb-6">
                                    <span class="px-3 py-1 bg-blue-100 text-primary rounded-full text-sm">HTML/CSS</span>
                                    <span class="px-3 py-1 bg-yellow-100 text-yellow-700 rounded-full text-sm">JavaScript</span>
                                    <span class="px-3 py-1 bg-green-100 text-green-700 rounded-full text-sm">Python</span>
                                    <span class="px-3 py-1 bg-purple-100 text-purple-700 rounded-full text-sm">Git</span>
                                </div>

                                <div class="flex space-x-4">
                                    <a href="#" class="w-10 h-10 rounded-full bg-primary text-white flex items-center justify-center hover:bg-blue-700 transition-colors">
                                        <i class="fa fa-github"></i>
                                    </a>
                                    <a href="#" class="w-10 h-10 rounded-full bg-red-500 text-white flex items-center justify-center hover:bg-red-600 transition-colors">
                                        <i class="fa fa-weibo"></i>
                                    </a>
                                    <a href="#" class="w-10 h-10 rounded-full bg-green-500 text-white flex items-center justify-center hover:bg-green-600 transition-colors">
                                        <i class="fa fa-wechat"></i>
                                    </a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- 页脚 -->
    <footer class="bg-dark text-white py-12">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
            <div class="max-w-5xl mx-auto">
                <div class="flex flex-col md:flex-row justify-between items-center mb-8">
                    <div class="mb-6 md:mb-0">
                        <div class="flex items-center space-x-2">
                            <i class="fa fa-book text-primary text-2xl"></i>
                            <span class="text-xl font-bold">翟公瑞的博客</span>
                        </div>
                        <p class="text-gray-400 mt-2">学号：20242800005</p>
                    </div>
                    <div class="flex space-x-6">
                        <a href="#home" class="text-gray-400 hover:text-white transition-colors">首页</a>
                        <a href="#blogs" class="text-gray-400 hover:text-white transition-colors">博客</a>
                        <a href="#categories" class="text-gray-400 hover:text-white transition-colors">分类</a>
                        <a href="#about" class="text-gray-400 hover:text-white transition-colors">关于我</a>
                    </div>
                </div>
                <div class="border-t border-gray-800 pt-8 text-center text-gray-400">
                    <p>© 2025 翟公瑞的个人博客. 保留所有权利.</p>
                </div>
            </div>
        </div>
    </footer>

    <!-- JavaScript -->
    <script>
        // 移动端菜单切换
        const menuBtn = document.getElementById('menuBtn');
        const mobileMenu = document.getElementById('mobileMenu');
        
        menuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // 平滑滚动
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // 关闭移动端菜单
                    if (!mobileMenu.classList.contains('hidden')) {
                        mobileMenu.classList.add('hidden');
                    }
                }
            });
        });

        // 滚动时导航栏样式变化
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 50) {
                header.classList.add('shadow');
            } else {
                header.classList.remove('shadow');
            }
        });
    </script>
</body>
</html>