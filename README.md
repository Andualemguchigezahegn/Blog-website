<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>TechBlog - Complete Website</title>
    
    <style>
        /* ============================================
           ALL CSS STYLES - Everything in one place
           ============================================ */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f8f9fa;
        }

        a {
            text-decoration: none;
            color: #2563eb;
        }

        a:hover {
            color: #1a4f9e;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* ===== HEADER & NAVIGATION ===== */
        header {
            background: #fff;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        header .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 20px;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo img {
            height: 40px;
            width: auto;
        }

        .logo h1 {
            font-size: 24px;
            color: #2563eb;
        }

        nav {
            display: flex;
            gap: 25px;
        }

        nav a {
            color: #333;
            font-weight: 500;
            padding: 8px 12px;
            border-radius: 5px;
            transition: all 0.3s ease;
        }

        nav a:hover,
        nav a.active {
            background: #2563eb;
            color: #fff;
        }

        /* ===== HERO SECTION ===== */
        .hero {
            background: linear-gradient(135deg, #2563eb, #7c3aed);
            color: #fff;
            padding: 80px 0;
            text-align: center;
        }

        .hero h2 {
            font-size: 48px;
            margin-bottom: 20px;
        }

        .hero p {
            font-size: 20px;
            margin-bottom: 30px;
            opacity: 0.9;
        }

        .btn {
            display: inline-block;
            background: #fff;
            color: #2563eb;
            padding: 12px 30px;
            border-radius: 30px;
            font-weight: 600;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
        }

        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
            color: #2563eb;
        }

        /* ===== POST GRID ===== */
        .featured-posts,
        .blog-grid {
            padding: 60px 0;
        }

        .featured-posts h2 {
            text-align: center;
            font-size: 32px;
            margin-bottom: 40px;
            color: #1e293b;
        }

        .post-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
        }

        .post-card {
            background: #fff;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.08);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .post-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 25px rgba(0, 0, 0, 0.12);
        }

        .post-card img {
            width: 100%;
            height: 220px;
            object-fit: cover;
        }

        .post-content {
            padding: 20px;
        }

        .post-content .category {
            display: inline-block;
            background: #2563eb;
            color: #fff;
            font-size: 12px;
            font-weight: 600;
            padding: 4px 12px;
            border-radius: 20px;
            margin-bottom: 10px;
        }

        .post-content h3 {
            font-size: 20px;
            margin-bottom: 10px;
        }

        .post-content h3 a {
            color: #1e293b;
            transition: color 0.3s ease;
        }

        .post-content h3 a:hover {
            color: #2563eb;
        }

        .post-content p {
            color: #64748b;
            margin-bottom: 15px;
        }

        .post-meta {
            display: flex;
            gap: 15px;
            font-size: 14px;
            color: #94a3b8;
        }

        .post-meta span {
            display: flex;
            align-items: center;
            gap: 5px;
        }

        /* ===== NEWSLETTER ===== */
        .newsletter {
            background: #1e293b;
            color: #fff;
            padding: 60px 0;
            text-align: center;
        }

        .newsletter h2 {
            font-size: 28px;
            margin-bottom: 10px;
        }

        .newsletter p {
            margin-bottom: 25px;
            opacity: 0.8;
        }

        .newsletter form {
            display: flex;
            justify-content: center;
            gap: 10px;
            flex-wrap: wrap;
        }

        .newsletter input {
            padding: 12px 20px;
            border: none;
            border-radius: 30px;
            width: 300px;
            font-size: 16px;
        }

        .newsletter button {
            padding: 12px 30px;
            border: none;
            border-radius: 30px;
            background: #2563eb;
            color: #fff;
            font-weight: 600;
            cursor: pointer;
            transition: background 0.3s ease;
        }

        .newsletter button:hover {
            background: #1a4f9e;
        }

        /* ===== FOOTER ===== */
        footer {
            background: #0f172a;
            color: #94a3b8;
            padding: 40px 0 20px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 30px;
        }

        .footer-section h3,
        .footer-section h4 {
            color: #fff;
            margin-bottom: 15px;
        }

        .footer-section p {
            opacity: 0.7;
        }

        .footer-section a {
            display: block;
            color: #94a3b8;
            margin-bottom: 8px;
            transition: color 0.3s ease;
        }

        .footer-section a:hover {
            color: #fff;
        }

        .footer-bottom {
            border-top: 1px solid #1e293b;
            padding-top: 20px;
            text-align: center;
            font-size: 14px;
            opacity: 0.7;
        }

        /* ===== PAGE HEADERS ===== */
        .page-header {
            background: linear-gradient(135deg, #1e293b, #0f172a);
            color: #fff;
            padding: 60px 0;
            text-align: center;
        }

        .page-header h1 {
            font-size: 40px;
            margin-bottom: 10px;
        }

        .page-header p {
            font-size: 18px;
            opacity: 0.8;
        }

        /* ===== BLOG FILTERS ===== */
        .blog-filters {
            padding: 30px 0;
            background: #fff;
            border-bottom: 1px solid #e2e8f0;
        }

        .blog-filters .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 15px;
        }

        .filter-buttons {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }

        .filter-btn {
            padding: 8px 18px;
            border: 2px solid #e2e8f0;
            border-radius: 25px;
            background: transparent;
            cursor: pointer;
            font-weight: 500;
            transition: all 0.3s ease;
        }

        .filter-btn:hover {
            border-color: #2563eb;
            color: #2563eb;
        }

        .filter-btn.active {
            background: #2563eb;
            color: #fff;
            border-color: #2563eb;
        }

        .search-box {
            display: flex;
            gap: 5px;
        }

        .search-box input {
            padding: 8px 15px;
            border: 2px solid #e2e8f0;
            border-radius: 25px;
            font-size: 14px;
            width: 200px;
        }

        .search-box button {
            padding: 8px 15px;
            border: none;
            border-radius: 25px;
            background: #2563eb;
            color: #fff;
            cursor: pointer;
        }

        /* ===== PAGINATION ===== */
        .pagination {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-top: 40px;
        }

        .pagination a {
            padding: 8px 16px;
            border: 1px solid #e2e8f0;
            border-radius: 5px;
            color: #333;
            transition: all 0.3s ease;
        }

        .pagination a:hover,
        .pagination a.active {
            background: #2563eb;
            color: #fff;
            border-color: #2563eb;
        }

        /* ===== ABOUT PAGE ===== */
        .about-content {
            padding: 60px 0;
        }

        .about-grid {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 40px;
            align-items: start;
        }

        .about-text h2 {
            font-size: 28px;
            color: #1e293b;
            margin-top: 25px;
            margin-bottom: 15px;
        }

        .about-text h2:first-child {
            margin-top: 0;
        }

        .about-text ul {
            list-style: none;
            padding: 0;
        }

        .about-text ul li {
            padding: 8px 0;
            padding-left: 25px;
            position: relative;
        }

        .about-text ul li::before {
            content: "▸";
            position: absolute;
            left: 0;
            color: #2563eb;
            font-weight: bold;
        }

        .about-image img {
            width: 100%;
            border-radius: 12px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
        }

        /* ===== TEAM SECTION ===== */
        .team-section {
            padding: 60px 0;
            background: #fff;
        }

        .team-section h2 {
            text-align: center;
            font-size: 32px;
            margin-bottom: 40px;
            color: #1e293b;
        }

        .team-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .team-member {
            text-align: center;
            padding: 20px;
        }

        .team-member img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            margin-bottom: 15px;
            border: 3px solid #2563eb;
        }

        .team-member h3 {
            font-size: 20px;
            color: #1e293b;
        }

        .team-member p {
            color: #64748b;
        }

        /* ===== CONTACT PAGE ===== */
        .contact-section {
            padding: 60px 0;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: 3fr 2fr;
            gap: 50px;
        }

        .contact-form h2 {
            font-size: 28px;
            color: #1e293b;
            margin-bottom: 30px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            font-weight: 600;
            margin-bottom: 5px;
            color: #1e293b;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px 15px;
            border: 2px solid #e2e8f0;
            border-radius: 8px;
            font-size: 16px;
            transition: border-color 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #2563eb;
        }

        .contact-form .btn {
            background: #2563eb;
            color: #fff;
            border: none;
            cursor: pointer;
            font-size: 16px;
        }

        .contact-form .btn:hover {
            background: #1a4f9e;
        }

        .contact-info h2 {
            font-size: 28px;
            color: #1e293b;
            margin-bottom: 30px;
        }

        .info-item {
            display: flex;
            gap: 15px;
            margin-bottom: 25px;
            align-items: flex-start;
        }

        .info-item .icon {
            font-size: 24px;
            min-width: 40px;
        }

        .info-item h4 {
            color: #1e293b;
            margin-bottom: 3px;
        }

        .info-item p {
            color: #64748b;
        }

        .info-item a {
            color: #2563eb;
        }

        /* ===== SINGLE POST ===== */
        .breadcrumb {
            background: #f1f5f9;
            padding: 15px 0;
            font-size: 14px;
        }

        .breadcrumb a {
            color: #2563eb;
        }

        .breadcrumb span {
            color: #64748b;
        }

        .single-post {
            padding: 60px 0;
        }

        .post-header {
            margin-bottom: 30px;
        }

        .post-header .category {
            display: inline-block;
            background: #2563eb;
            color: #fff;
            font-size: 14px;
            font-weight: 600;
            padding: 4px 14px;
            border-radius: 20px;
            margin-bottom: 10px;
        }

        .post-header h1 {
            font-size: 36px;
            color: #1e293b;
            margin-bottom: 15px;
        }

        .post-header .post-meta {
            font-size: 16px;
        }

        .featured-image {
            width: 100%;
            max-height: 500px;
            object-fit: cover;
            border-radius: 12px;
            margin-bottom: 30px;
        }

        .post-body {
            max-width: 800px;
            margin: 0 auto;
        }

        .post-body h2 {
            font-size: 28px;
            color: #1e293b;
            margin: 30px 0 15px;
        }

        .post-body p {
            margin-bottom: 20px;
            font-size: 18px;
            color: #334155;
        }

        .post-body ul {
            margin: 20px 0;
            padding-left: 25px;
        }

        .post-body ul li {
            margin-bottom: 10px;
            font-size: 18px;
            color: #334155;
        }

        .post-footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 30px 0;
            border-top: 1px solid #e2e8f0;
            margin-top: 40px;
        }

        .tags {
            display: flex;
            gap: 10px;
            align-items: center;
        }

        .tags span {
            font-weight: 600;
            color: #1e293b;
        }

        .tags a {
            background: #f1f5f9;
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 14px;
            color: #64748b;
            transition: all 0.3s ease;
        }

        .tags a:hover {
            background: #2563eb;
            color: #fff;
        }

        .share {
            display: flex;
            gap: 10px;
            align-items: center;
        }

        .share span {
            font-weight: 600;
            color: #1e293b;
        }

        .share a {
            color: #64748b;
            transition: color 0.3s ease;
        }

        .share a:hover {
            color: #2563eb;
        }

        .related-posts {
            margin-top: 50px;
            padding-top: 40px;
            border-top: 1px solid #e2e8f0;
        }

        .related-posts h3 {
            font-size: 24px;
            color: #1e293b;
            margin-bottom: 25px;
        }

        .related-posts .post-grid {
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
        }

        .related-posts .post-card img {
            height: 180px;
        }

        /* ===== PAGE SECTIONS (Hidden by default) ===== */
        .page-section {
            display: none;
        }

        .page-section.active {
            display: block;
        }

        /* ===== RESPONSIVE DESIGN ===== */
        @media (max-width: 992px) {
            .about-grid,
            .contact-grid {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 768px) {
            header .container {
                flex-direction: column;
                gap: 15px;
            }

            nav {
                flex-wrap: wrap;
                justify-content: center;
            }

            .hero h2 {
                font-size: 32px;
            }

            .post-grid {
                grid-template-columns: 1fr;
            }

            .blog-filters .container {
                flex-direction: column;
            }

            .search-box input {
                width: 100%;
            }

            .post-header h1 {
                font-size: 28px;
            }

            .post-footer {
                flex-direction: column;
                gap: 15px;
                align-items: flex-start;
            }
        }

        @media (max-width: 480px) {
            .hero h2 {
                font-size: 24px;
            }

            .hero p {
                font-size: 16px;
            }

            .newsletter input {
                width: 100%;
            }

            .footer-content {
                grid-template-columns: 1fr;
            }

            .filter-buttons {
                justify-content: center;
            }
        }

        /* ===== ANIMATIONS ===== */
        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateY(-10px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* ===== BACK TO TOP ===== */
        #backToTop {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 50px;
            height: 50px;
            border: none;
            border-radius: 50%;
            background: #2563eb;
            color: #fff;
            font-size: 24px;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(37, 99, 235, 0.4);
            display: none;
            transition: all 0.3s ease;
            z-index: 999;
        }

        #backToTop:hover {
            transform: scale(1.1);
        }
    </style>
</head>
<body>

    <!-- ============================================
    HEADER - Same on all pages
    ============================================ -->
    <header>
        <div class="container">
            <div class="logo">
                <img src="https://via.placeholder.com/40x40/2563eb/ffffff?text=T" alt="TechBlog Logo" />
                <h1>TechBlog</h1>
            </div>
            <nav>
                <a href="#" onclick="showPage('home')" id="nav-home" class="active">Home</a>
                <a href="#" onclick="showPage('blog')" id="nav-blog">Blog</a>
                <a href="#" onclick="showPage('about')" id="nav-about">About</a>
                <a href="#" onclick="showPage('contact')" id="nav-contact">Contact</a>
            </nav>
        </div>
    </header>

    <!-- ============================================
    PAGE: HOME
    ============================================ -->
    <div id="page-home" class="page-section active">
        <!-- Hero Section -->
        <section class="hero">
            <div class="container">
                <h2>Welcome to TechBlog</h2>
                <p>Discover the latest in technology, programming, and innovation</p>
                <a href="#" onclick="showPage('blog')" class="btn">Read Our Blog</a>
            </div>
        </section>

        <!-- Featured Posts -->
        <section class="featured-posts">
            <div class="container">
                <h2>Featured Posts</h2>
                <div class="post-grid">
                    <article class="post-card">
                        <img src="https://picsum.photos/800/500?random=1" alt="Post 1" />
                        <div class="post-content">
                            <span class="category">Technology</span>
                            <h3><a href="#" onclick="showPage('single')">The Future of AI in 2026</a></h3>
                            <p>Explore how artificial intelligence is transforming industries...</p>
                            <div class="post-meta">
                                <span>By John Doe</span>
                                <span>Jan 15, 2026</span>
                            </div>
                        </div>
                    </article>

                    <article class="post-card">
                        <img src="https://picsum.photos/800/500?random=2" alt="Post 2" />
                        <div class="post-content">
                            <span class="category">Web Development</span>
                            <h3><a href="#" onclick="showPage('single')">Modern Web Development Trends</a></h3>
                            <p>Stay updated with the latest web technologies and frameworks...</p>
                            <div class="post-meta">
                                <span>By Jane Smith</span>
                                <span>Jan 12, 2026</span>
                            </div>
                        </div>
                    </article>

                    <article class="post-card">
                        <img src="https://picsum.photos/800/500?random=3" alt="Post 3" />
                        <div class="post-content">
                            <span class="category">Programming</span>
                            <h3><a href="#" onclick="showPage('single')">Top 10 Programming Languages 2026</a></h3>
                            <p>Discover which programming languages are dominating the job market...</p>
                            <div class="post-meta">
                                <span>By Alex Johnson</span>
                                <span>Jan 10, 2026</span>
                            </div>
                        </div>
                    </article>
                </div>
            </div>
        </section>
    </div>

    <!-- ============================================
    PAGE: BLOG
    ============================================ -->
    <div id="page-blog" class="page-section">
        <section class="page-header">
            <div class="container">
                <h1>All Blog Posts</h1>
                <p>Explore our collection of technology articles and tutorials</p>
            </div>
        </section>

        <section class="blog-filters">
            <div class="container">
                <div class="filter-buttons">
                    <button class="filter-btn active" data-filter="all">All</button>
                    <button class="filter-btn" data-filter="technology">Technology</button>
                    <button class="filter-btn" data-filter="webdev">Web Development</button>
                    <button class="filter-btn" data-filter="programming">Programming</button>
                    <button class="filter-btn" data-filter="ai">AI & ML</button>
                </div>
                <div class="search-box">
                    <input type="text" id="searchInput" placeholder="Search posts..." />
                    <button onclick="performSearch()">🔍</button>
                </div>
            </div>
        </section>

        <section class="blog-grid">
            <div class="container">
                <div class="post-grid" id="blogPosts">
                    <article class="post-card" data-category="technology">
                        <img src="https://picsum.photos/800/500?random=1" alt="Post 1" />
                        <div class="post-content">
                            <span class="category">Technology</span>
                            <h3><a href="#" onclick="showPage('single')">The Future of AI in 2026</a></h3>
                            <p>Explore how artificial intelligence is transforming industries...</p>
                            <div class="post-meta">
                                <span>By John Doe</span>
                                <span>Jan 15, 2026</span>
                                <span>5 min read</span>
                            </div>
                        </div>
                    </article>

                    <article class="post-card" data-category="webdev">
                        <img src="https://picsum.photos/800/500?random=2" alt="Post 2" />
                        <div class="post-content">
                            <span class="category">Web Development</span>
                            <h3><a href="#" onclick="showPage('single')">Modern Web Development Trends</a></h3>
                            <p>Stay updated with the latest web technologies and frameworks...</p>
                            <div class="post-meta">
                                <span>By Jane Smith</span>
                                <span>Jan 12, 2026</span>
                                <span>4 min read</span>
                            </div>
                        </div>
                    </article>

                    <article class="post-card" data-category="programming">
                        <img src="https://picsum.photos/800/500?random=3" alt="Post 3" />
                        <div class="post-content">
                            <span class="category">Programming</span>
                            <h3><a href="#" onclick="showPage('single')">Top 10 Programming Languages 2026</a></h3>
                            <p>Discover which programming languages are in high demand...</p>
                            <div class="post-meta">
                                <span>By Alex Johnson</span>
                                <span>Jan 10, 2026</span>
                                <span>6 min read</span>
                            </div>
                        </div>
                    </article>

                    <article class="post-card" data-category="ai">
                        <img src="https://picsum.photos/800/500?random=4" alt="Post 4" />
                        <div class="post-content">
                            <span class="category">AI & ML</span>
                            <h3><a href="#" onclick="showPage('single')">Machine Learning for Beginners</a></h3>
                            <p>Understanding the fundamentals of machine learning...</p>
                            <div class="post-meta">
                                <span>By Sarah Wilson</span>
                                <span>Jan 8, 2026</span>
                                <span>8 min read</span>
                            </div>
                        </div>
                    </article>

                    <article class="post-card" data-category="technology">
                        <img src="https://picsum.photos/800/500?random=5" alt="Post 5" />
                        <div class="post-content">
                            <span class="category">Technology</span>
                            <h3><a href="#" onclick="showPage('single')">5G Technology: What You Need to Know</a></h3>
                            <p>Exploring the impact of 5G on mobile connectivity...</p>
                            <div class="post-meta">
                                <span>By Mike Chen</span>
                                <span>Jan 5, 2026</span>
                                <span>4 min read</span>
                            </div>
                        </div>
                    </article>

                    <article class="post-card" data-category="webdev">
                        <img src="https://picsum.photos/800/500?random=6" alt="Post 6" />
                        <div class="post-content">
                            <span class="category">Web Development</span>
                            <h3><a href="#" onclick="showPage('single')">CSS Grid vs Flexbox Guide</a></h3>
                            <p>A complete guide to choosing between CSS Grid and Flexbox...</p>
                            <div class="post-meta">
                                <span>By Lisa Zhang</span>
                                <span>Jan 3, 2026</span>
                                <span>3 min read</span>
                            </div>
                        </div>
                    </article>
                </div>

                <div class="pagination">
                    <a href="#" class="prev">← Previous</a>
                    <a href="#" class="active">1</a>
                    <a href="#">2</a>
                    <a href="#">3</a>
                    <a href="#" class="next">Next →</a>
                </div>
            </div>
        </section>
    </div>

    <!-- ============================================
    PAGE: ABOUT
    ============================================ -->
    <div id="page-about" class="page-section">
        <section class="page-header">
            <div class="container">
                <h1>About TechBlog</h1>
                <p>Learn more about our mission and team</p>
            </div>
        </section>

        <section class="about-content">
            <div class="container">
                <div class="about-grid">
                    <div class="about-text">
                        <h2>Our Mission</h2>
                        <p>TechBlog was founded in 2025 with a simple mission: to make technology knowledge accessible to everyone. We believe that understanding technology is essential in today's digital world.</p>

                        <h2>What We Do</h2>
                        <p>We publish in-depth articles, tutorials, and guides on the latest technology trends. Our content covers:</p>
                        <ul>
                            <li>Artificial Intelligence and Machine Learning</li>
                            <li>Web Development and Programming</li>
                            <li>Cybersecurity and Privacy</li>
                            <li>Cloud Computing and DevOps</li>
                            <li>Data Science and Analytics</li>
                        </ul>

                        <h2>Our Team</h2>
                        <p>We are a team of passionate technology enthusiasts, developers, and writers dedicated to providing high-quality content.</p>
                    </div>
                    <div class="about-image">
                        <img src="https://via.placeholder.com/400x400/2563eb/ffffff?text=Team" alt="TechBlog Team" />
                    </div>
                </div>
            </div>
        </section>

        <section class="team-section">
            <div class="container">
                <h2>Meet Our Team</h2>
                <div class="team-grid">
                    <div class="team-member">
                        <img src="https://via.placeholder.com/150x150/2563eb/ffffff?text=JD" alt="John Doe" />
                        <h3>John Doe</h3>
                        <p>Founder & CEO</p>
                    </div>
                    <div class="team-member">
                        <img src="https://via.placeholder.com/150x150/2563eb/ffffff?text=JS" alt="Jane Smith" />
                        <h3>Jane Smith</h3>
                        <p>Lead Developer</p>
                    </div>
                    <div class="team-member">
                        <img src="https://via.placeholder.com/150x150/2563eb/ffffff?text=AJ" alt="Alex Johnson" />
                        <h3>Alex Johnson</h3>
                        <p>Content Manager</p>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- ============================================
    PAGE: CONTACT
    ============================================ -->
    <div id="page-contact" class="page-section">
        <section class="page-header">
            <div class="container">
                <h1>Contact Us</h1>
                <p>We'd love to hear from you!</p>
            </div>
        </section>

        <section class="contact-section">
            <div class="container">
                <div class="contact-grid">
                    <div class="contact-form">
                        <h2>Send Us a Message</h2>
                        <form id="contactForm">
                            <div class="form-group">
                                <label for="name">Full Name *</label>
                                <input type="text" id="name" placeholder="Enter your full name" required />
                            </div>
                            <div class="form-group">
                                <label for="email">Email Address *</label>
                                <input type="email" id="email" placeholder="Enter your email address" required />
                            </div>
                            <div class="form-group">
                                <label for="subject">Subject *</label>
                                <input type="text" id="subject" placeholder="Enter the subject" required />
                            </div>
                            <div class="form-group">
                                <label for="message">Message *</label>
                                <textarea id="message" placeholder="Write your message here..." rows="5" required></textarea>
                            </div>
                            <button type="submit" class="btn">Send Message</button>
                        </form>
                        <div id="formMessage" style="display:none;"></div>
                    </div>
                    <div class="contact-info">
                        <h2>Get in Touch</h2>
                        <div class="info-item">
                            <span class="icon">📍</span>
                            <div>
                                <h4>Address</h4>
                                <p>123 Tech Street, Silicon Valley, CA 94025</p>
                            </div>
                        </div>
                        <div class="info-item">
                            <span class="icon">📧</span>
                            <div>
                                <h4>Email</h4>
                                <p><a href="mailto:contact@techblog.com">contact@techblog.com</a></p>
                            </div>
                        </div>
                        <div class="info-item">
                            <span class="icon">📞</span>
                            <div>
                                <h4>Phone</h4>
                                <p><a href="tel:+1234567890">+1 (234) 567-890</a></p>
                            </div>
                        </div>
                        <div class="info-item">
                            <span class="icon">🕐</span>
                            <div>
                                <h4>Working Hours</h4>
                                <p>Monday - Friday: 9:00 AM - 6:00 PM</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- ============================================
    PAGE: SINGLE POST
    ============================================ -->
    <div id="page-single" class="page-section">
        <div class="breadcrumb">
            <div class="container">
                <a href="#" onclick="showPage('home')">Home</a> &gt; 
                <a href="#" onclick="showPage('blog')">Blog</a> &gt; 
                <span>The Future of AI in 2026</span>
            </div>
        </div>

        <section class="single-post">
            <div class="container">
                <article>
                    <div class="post-header">
                        <span class="category">Technology</span>
                        <h1>The Future of AI in 2026</h1>
                        <div class="post-meta">
                            <span>By John Doe</span>
                            <span>Jan 15, 2026</span>
                            <span>5 min read</span>
                        </div>
                    </div>

                    <img src="https://picsum.photos/800/500?random=1" alt="AI Future" class="featured-image" />

                    <div class="post-body">
                        <p><strong>Artificial Intelligence has come a long way in the past decade, and 2026 is shaping up to be a pivotal year for the technology.</strong></p>

                        <h2>The Current State of AI</h2>
                        <p>As we enter 2026, AI has become an integral part of our daily lives. From voice assistants to recommendation algorithms, AI is everywhere. But what does the future hold?</p>

                        <h2>Key Trends to Watch</h2>
                        <p>Several key trends are shaping the future of AI:</p>
                        <ul>
                            <li><strong>Generative AI:</strong> AI models that can create content, images, and even code are becoming more sophisticated.</li>
                            <li><strong>AI in Healthcare:</strong> AI is revolutionizing diagnosis, drug discovery, and personalized medicine.</li>
                            <li><strong>Autonomous Systems:</strong> Self-driving cars, drones, and robotic systems are becoming more capable.</li>
                            <li><strong>AI Ethics:</strong> There's a growing focus on making AI fair, transparent, and accountable.</li>
                        </ul>

                        <h2>AI in the Workplace</h2>
                        <p>By 2026, AI is expected to augment human capabilities rather than replace them. New roles will emerge, and existing jobs will be transformed. Workers will need to adapt by developing skills in AI literacy and human-AI collaboration.</p>

                        <h2>Challenges Ahead</h2>
                        <p>Despite the progress, there are challenges to overcome:</p>
                        <ul>
                            <li>Data privacy and security</li>
                            <li>AI bias and fairness</li>
                            <li>Regulatory frameworks</li>
                            <li>Energy consumption and sustainability</li>
                        </ul>

                        <h2>Conclusion</h2>
                        <p>The future of AI in 2026 is bright and full of possibilities. As the technology continues to evolve, it will open new opportunities for innovation and human progress.</p>
                    </div>

                    <div class="post-footer">
                        <div class="tags">
                            <span>Tags:</span>
                            <a href="#">AI</a>
                            <a href="#">Technology</a>
                            <a href="#">Future</a>
                            <a href="#">Innovation</a>
                        </div>
                        <div class="share">
                            <span>Share:</span>
                            <a href="#">Twitter</a>
                            <a href="#">LinkedIn</a>
                            <a href="#">Facebook</a>
                        </div>
                    </div>
                </article>

                <div class="related-posts">
                    <h3>Related Posts</h3>
                    <div class="post-grid">
                        <article class="post-card">
                            <img src="https://picsum.photos/800/500?random=4" alt="Related Post" />
                            <div class="post-content">
                                <h4><a href="#" onclick="showPage('single')">Machine Learning for Beginners</a></h4>
                                <div class="post-meta">
                                    <span>Jan 8, 2026</span>
                                </div>
                            </div>
                        </article>
                        <article class="post-card">
                            <img src="https://picsum.photos/800/500?random=5" alt="Related Post" />
                            <div class="post-content">
                                <h4><a href="#" onclick="showPage('single')">5G Technology: What You Need to Know</a></h4>
                                <div class="post-meta">
                                    <span>Jan 5, 2026</span>
                                </div>
                            </div>
                        </article>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- ============================================
    NEWSLETTER SECTION (Shows on all pages)
    ============================================ -->
    <section class="newsletter">
        <div class="container">
            <h2>Subscribe to Our Newsletter</h2>
            <p>Get the latest tech updates directly in your inbox</p>
            <form id="newsletterForm">
                <input type="email" placeholder="Enter your email" required />
                <button type="submit">Subscribe</button>
            </form>
        </div>
    </section>

    <!-- ============================================
    FOOTER (Same on all pages)
    ============================================ -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>TechBlog</h3>
                    <p>Your source for technology news and insights</p>
                </div>
                <div class="footer-section">
                    <h4>Quick Links</h4>
                    <a href="#" onclick="showPage('home')">Home</a>
                    <a href="#" onclick="showPage('blog')">Blog</a>
                    <a href="#" onclick="showPage('about')">About</a>
                    <a href="#" onclick="showPage('contact')">Contact</a>
                </div>
                <div class="footer-section">
                    <h4>Categories</h4>
                    <a href="#">Technology</a>
                    <a href="#">Web Development</a>
                    <a href="#">Programming</a>
                    <a href="#">AI & ML</a>
                </div>
                <div class="footer-section">
                    <h4>Connect</h4>
                    <a href="#">Twitter</a>
                    <a href="#">LinkedIn</a>
                    <a href="#">GitHub</a>
                    <a href="#">YouTube</a>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; <span id="currentYear">2026</span> TechBlog. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <!-- ============================================
    BACK TO TOP BUTTON
    ============================================ -->
    <button id="backToTop" onclick="scrollToTop()">↑</button>

    <!-- ============================================
    ALL JAVASCRIPT - Everything in one place
    ============================================ -->
    <script>
        // ============================================
        // PAGE NAVIGATION
        // ============================================
        function showPage(page) {
            // Hide all pages
            document.querySelectorAll('.page-section').forEach(function(section) {
                section.classList.remove('active');
            });

            // Show selected page
            var targetPage = document.getElementById('page-' + page);
            if (targetPage) {
                targetPage.classList.add('active');
            }

            // Update navigation
            document.querySelectorAll('nav a').forEach(function(link) {
                link.classList.remove('active');
            });

            var navLink = document.getElementById('nav-' + page);
            if (navLink) {
                navLink.classList.add('active');
            }

            // Scroll to top
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // ============================================
        // BLOG FILTER FUNCTIONALITY
        // ============================================
        document.querySelectorAll('.filter-btn').forEach(function(btn) {
            btn.addEventListener('click', function() {
                // Remove active class from all buttons
                document.querySelectorAll('.filter-btn').forEach(function(b) {
                    b.classList.remove('active');
                });
                this.classList.add('active');

                var filter = this.dataset.filter;

                document.querySelectorAll('#blogPosts .post-card').forEach(function(card) {
                    var category = card.dataset.category;
                    if (filter === 'all' || category === filter) {
                        card.style.display = 'block';
                        card.style.animation = 'fadeIn 0.5s ease';
                    } else {
                        card.style.display = 'none';
                    }
                });
            });
        });

        // ============================================
        // SEARCH FUNCTIONALITY
        // ============================================
        function performSearch() {
            var query = document.getElementById('searchInput').value.toLowerCase().trim();
            var posts = document.querySelectorAll('#blogPosts .post-card');

            posts.forEach(function(post) {
                var title = post.querySelector('h3 a')?.textContent.toLowerCase() || '';
                var content = post.querySelector('p')?.textContent.toLowerCase() || '';
                var category = post.querySelector('.category')?.textContent.toLowerCase() || '';

                if (title.includes(query) || content.includes(query) || category.includes(query)) {
                    post.style.display = 'block';
                } else {
                    post.style.display = 'none';
                }
            });
        }

        document.getElementById('searchInput').addEventListener('keyup', function(e) {
            if (e.key === 'Enter') {
                performSearch();
            }
        });

        // ============================================
        // CONTACT FORM HANDLING
        // ============================================
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();

            var name = document.getElementById('name').value.trim();
            var email = document.getElementById('email').value.trim();
            var subject = document.getElementById('subject').value.trim();
            var message = document.getElementById('message').value.trim();
            var formMessage = document.getElementById('formMessage');

            if (!name || !email || !subject || !message) {
                showFormMessage('Please fill in all required fields.', 'error');
                return;
            }

            var emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            if (!emailRegex.test(email)) {
                showFormMessage('Please enter a valid email address.', 'error');
                return;
            }

            showFormMessage('Message sent successfully! We\'ll get back to you soon.', 'success');
            this.reset();
        });

        function showFormMessage(message, type) {
            var formMessage = document.getElementById('formMessage');
            formMessage.style.display = 'block';
            formMessage.textContent = message;
            formMessage.style.padding = '15px 20px';
            formMessage.style.borderRadius = '8px';
            formMessage.style.marginTop = '20px';

            if (type === 'success') {
                formMessage.style.backgroundColor = '#d1fae5';
                formMessage.style.color = '#065f46';
                formMessage.style.border = '1px solid #a7f3d0';
            } else {
                formMessage.style.backgroundColor = '#fee2e2';
                formMessage.style.color = '#991b1b';
                formMessage.style.border = '1px solid #fca5a5';
            }

            setTimeout(function() {
                formMessage.style.display = 'none';
            }, 5000);
        }

        // ============================================
        // NEWSLETTER FORM
        // ============================================
        document.getElementById('newsletterForm').addEventListener('submit', function(e) {
            e.preventDefault();
            var email = this.querySelector('input[type="email"]').value.trim();
            if (email) {
                alert('Thank you for subscribing to our newsletter!');
                this.reset();
            }
        });

        // ============================================
        // BACK TO TOP BUTTON
        // ============================================
        var backToTopBtn = document.getElementById('backToTop');

        window.addEventListener('scroll', function() {
            if (window.scrollY > 300) {
                backToTopBtn.style.display = 'block';
            } else {
                backToTopBtn.style.display = 'none';
            }
        });

        function scrollToTop() {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // ============================================
        // DYNAMIC YEAR IN FOOTER
        // ============================================
        document.getElementById('currentYear').textContent = new Date().getFullYear();

        // ============================================
        // CONSOLE MESSAGE
        // ============================================
        console.log('🚀 TechBlog Website Loaded Successfully!');
        console.log('📝 Built with ❤️ using HTML, CSS, and JavaScript');
        console.log('📱 All pages in one file!');
    </script>

</body>
</html>
