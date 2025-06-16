<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Orange Chemist - Your Neighborhood Health Partner</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: #333;
            background: #f8fafc;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        /* Mobile-First Header */
        .header {
            background: white;
            color: #333;
            padding: 12px 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 15px rgba(0,0,0,0.08);
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        /* Mobile-optimized Logo */
        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .cross-container {
            position: relative;
            width: 40px;
            height: 40px;
            background: #00A859;
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 15px rgba(0, 168, 89, 0.25);
        }

        .medical-cross {
            width: 24px;
            height: 24px;
            position: relative;
        }

        .medical-cross::before,
        .medical-cross::after {
            content: '';
            position: absolute;
            background: white;
            border-radius: 1px;
        }

        .medical-cross::before {
            width: 5px;
            height: 24px;
            left: 50%;
            top: 0;
            transform: translateX(-50%);
        }

        .medical-cross::after {
            width: 24px;
            height: 5px;
            top: 50%;
            left: 0;
            transform: translateY(-50%);
        }

        .orange-accent {
            position: absolute;
            top: -4px;
            right: -4px;
            width: 16px;
            height: 16px;
            background: #F56A0A;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            font-size: 9px;
            color: white;
            box-shadow: 0 2px 8px rgba(245, 106, 10, 0.3);
            border: 2px solid white;
        }

        .leaf-element {
            position: absolute;
            top: -3px;
            right: 6px;
            width: 5px;
            height: 8px;
            background: #1BA94C;
            border-radius: 0 100% 0 100%;
            transform: rotate(45deg);
            box-shadow: 0 1px 4px rgba(27, 169, 76, 0.2);
        }

        .brand-text h1 {
            font-size: 1.3rem;
            font-weight: 700;
            margin: 0;
            color: #1e293b;
        }

        .brand-text .orange-text {
            color: #F56A0A;
        }

        .brand-text .tagline {
            font-size: 0.75rem;
            color: #64748b;
            font-weight: 400;
            margin-top: 1px;
        }

        /* Mobile Menu Button */
        .menu-toggle {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            color: #333;
            cursor: pointer;
            padding: 8px;
            flex-shrink: 0;
        }

        /* Mobile-First Navigation - Fixed */
        .nav {
            background: rgba(248, 250, 252, 0.98);
            backdrop-filter: blur(10px);
            padding: 8px 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: sticky;
            top: 65px;
            z-index: 99;
            width: 100%;
            overflow: hidden;
        }

        .nav-links {
            display: flex;
            justify-content: flex-start;
            gap: 8px;
            list-style: none;
            overflow-x: auto;
            padding: 5px 0;
            -webkit-overflow-scrolling: touch;
            scrollbar-width: none;
            -ms-overflow-style: none;
            width: 100%;
        }

        .nav-links::-webkit-scrollbar {
            display: none;
        }

        .nav-links li {
            flex-shrink: 0;
        }

        .nav-links a {
            text-decoration: none;
            color: #1e293b;
            font-weight: 500;
            padding: 8px 14px;
            border-radius: 20px;
            transition: all 0.3s ease;
            white-space: nowrap;
            font-size: 0.85rem;
            display: block;
        }

        .nav-links a:hover,
        .nav-links a.active {
            background: #00A859;
            color: white;
        }

        /* Mobile-optimized Hero - Fixed text overflow */
        .hero {
            background: linear-gradient(135deg, #e8f5e8 0%, #f0f8ff 100%);
            padding: 2rem 0;
            text-align: center;
            width: 100%;
            overflow: hidden;
        }

        .hero h2 {
            font-size: 1.5rem;
            color: #00A859;
            margin-bottom: 1rem;
            font-weight: 700;
            line-height: 1.3;
            padding: 0 10px;
            word-wrap: break-word;
        }

        .hero p {
            font-size: 0.9rem;
            color: #64748b;
            margin-bottom: 2rem;
            line-height: 1.5;
            padding: 0 10px;
            word-wrap: break-word;
        }

        .cta-buttons {
            display: flex;
            flex-direction: column;
            gap: 12px;
            align-items: center;
            padding: 0 15px;
        }

        .btn {
            padding: 12px 20px;
            border-radius: 25px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            width: 100%;
            max-width: 260px;
            font-size: 0.9rem;
            text-align: center;
        }

        .btn i {
            font-size: 1em;
            flex-shrink: 0;
        }

        .btn-primary {
            background: linear-gradient(135deg, #25d366 0%, #128c7e 100%);
            color: white;
        }

        .btn-secondary {
            background: #F56A0A;
            color: white;
        }

        .btn:hover {
            transform: translateY(-1px);
            box-shadow: 0 6px 20px rgba(0,0,0,0.15);
        }

        /* Mobile-optimized Prescription Upload - Fixed */
        .prescription-hero {
            background: linear-gradient(135deg, #F56A0A, #ff8c42);
            color: white;
            padding: 2rem 0;
            margin: 1.5rem 0;
            border-radius: 15px;
            text-align: center;
            width: 100%;
            overflow: hidden;
        }

        .prescription-content {
            max-width: 100%;
            padding: 0 15px;
        }

        .prescription-content h2 {
            font-size: 1.4rem;
            margin-bottom: 1rem;
            word-wrap: break-word;
        }

        .prescription-content p {
            font-size: 0.9rem;
            margin-bottom: 1.5rem;
            word-wrap: break-word;
        }

        .prescription-upload {
            background: rgba(255,255,255,0.15);
            backdrop-filter: blur(10px);
            border: 2px dashed rgba(255,255,255,0.5);
            border-radius: 12px;
            padding: 1.2rem;
            margin: 1.2rem 0;
            cursor: pointer;
            transition: all 0.3s ease;
            touch-action: manipulation;
        }

        .prescription-upload:hover,
        .prescription-upload.dragover {
            background: rgba(255,255,255,0.25);
            border-color: white;
        }

        .upload-icon {
            font-size: 2rem;
            margin-bottom: 0.8rem;
            opacity: 0.9;
        }

        .prescription-upload h3 {
            font-size: 1rem;
            margin-bottom: 0.5rem;
            word-wrap: break-word;
        }

        .prescription-upload p {
            font-size: 0.8rem;
            word-wrap: break-word;
        }

        /* Mobile-optimized Categories Grid - Fixed */
        .categories {
            padding: 2.5rem 0;
            background: white;
            width: 100%;
        }

        .section-title {
            text-align: center;
            font-size: 1.4rem;
            color: #00A859;
            margin-bottom: 1.5rem;
            font-weight: 700;
            padding: 0 15px;
            word-wrap: break-word;
        }

        .categories-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
            gap: 12px;
            margin-bottom: 2rem;
            padding: 0 5px;
        }

        .category-card {
            background: white;
            border-radius: 12px;
            padding: 1.2rem 0.8rem;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0,0,0,0.08);
            transition: all 0.3s ease;
            border: 2px solid transparent;
            cursor: pointer;
            text-decoration: none;
            color: inherit;
            touch-action: manipulation;
            width: 100%;
            min-height: 140px;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .category-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.15);
            border-color: #F56A0A;
            text-decoration: none;
            color: inherit;
        }

        .category-icon {
            width: 40px;
            height: 40px;
            margin: 0 auto 0.8rem;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            background: linear-gradient(135deg, rgba(245, 106, 10, 0.1), rgba(255, 140, 66, 0.1));
            border: 2px solid #F56A0A;
            color: #F56A0A;
            font-size: 16px;
            flex-shrink: 0;
        }

        .category-card:hover .category-icon {
            background: linear-gradient(135deg, #F56A0A, #ff8c42);
            color: white;
            border-color: #F56A0A;
        }

        .category-card h3 {
            color: #00A859;
            margin-bottom: 0.4rem;
            font-weight: 600;
            font-size: 0.85rem;
            line-height: 1.2;
            word-wrap: break-word;
            hyphens: auto;
        }

        .category-card p {
            color: #64748b;
            font-size: 0.7rem;
            line-height: 1.3;
            word-wrap: break-word;
            hyphens: auto;
        }

        /* Mobile-optimized Store Locator - Fixed */
        .store-locator {
            padding: 2.5rem 0;
            background: linear-gradient(135deg, #f0f8ff 0%, #e8f5e8 100%);
            width: 100%;
        }

        .stores-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 1.2rem;
        }

        .store-card {
            background: white;
            border-radius: 12px;
            padding: 1.2rem;
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
            width: 100%;
        }

        .store-header {
            display: flex;
            align-items: flex-start;
            gap: 10px;
            margin-bottom: 1rem;
        }

        .store-icon {
            width: 35px;
            height: 35px;
            background: #00A859;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 14px;
            flex-shrink: 0;
        }

        .store-details {
            flex: 1;
            min-width: 0;
        }

        .store-details h3 {
            color: #00A859;
            margin-bottom: 0.2rem;
            font-size: 1rem;
            word-wrap: break-word;
            line-height: 1.2;
        }

        .store-details p {
            color: #F56A0A;
            font-weight: 600;
            font-size: 0.8rem;
            word-wrap: break-word;
        }

        .store-info {
            margin-bottom: 1rem;
        }

        .store-info p {
            margin-bottom: 0.5rem;
            color: #64748b;
            font-size: 0.85rem;
            line-height: 1.3;
            word-wrap: break-word;
        }

        .store-actions {
            display: flex;
            gap: 6px;
            flex-wrap: wrap;
        }

        .btn-small {
            padding: 8px 12px;
            font-size: 0.75rem;
            border-radius: 16px;
            flex: 1;
            min-width: 100px;
            text-align: center;
        }

        /* Mobile-optimized Service Info - Fixed */
        .service-info {
            padding: 2.5rem 0;
            background: linear-gradient(135deg, #00A859 0%, #1BA94C 100%);
            color: white;
            width: 100%;
        }

        .service-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 1.2rem;
        }

        .service-card {
            text-align: center;
            padding: 1rem;
        }

        .service-icon {
            width: 40px;
            height: 40px;
            background: #F56A0A;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 0.8rem;
            font-size: 16px;
            flex-shrink: 0;
        }

        .service-card h3 {
            font-size: 0.9rem;
            margin-bottom: 0.4rem;
            word-wrap: break-word;
            line-height: 1.2;
        }

        .service-card p {
            font-size: 0.75rem;
            line-height: 1.3;
            word-wrap: break-word;
        }

        /* Mobile-optimized Footer - Fixed */
        .footer {
            background: #1e293b;
            color: white;
            padding: 2rem 0 1.2rem;
            width: 100%;
        }

        .footer-content {
            display: grid;
            grid-template-columns: 1fr;
            gap: 1.2rem;
            margin-bottom: 1.2rem;
        }

        .footer-section h3 {
            color: #F56A0A;
            margin-bottom: 0.6rem;
            font-size: 1rem;
            word-wrap: break-word;
        }

        .footer-section p,
        .footer-section a {
            color: #94a3b8;
            text-decoration: none;
            margin-bottom: 0.3rem;
            display: block;
            font-size: 0.85rem;
            word-wrap: break-word;
            line-height: 1.3;
        }

        .footer-section a:hover {
            color: white;
        }

                /* Floating WhatsApp - Updated to right side with bounce animation */
        .whatsapp-float {
            position: fixed;
            width: 60px;
            height: 60px;
            bottom: 40px;
            right: 40px;
            background: #25d366;
            color: white;
            border-radius: 50px;
            text-align: center;
            font-size: 30px;
            box-shadow: 2px 2px 3px #999;
            z-index: 100;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            animation: bounce 2s infinite;
            transition: all 0.3s ease;
        }

        .whatsapp-float:hover {
            transform: scale(1.1);
            box-shadow: 0 6px 25px rgba(37, 211, 102, 0.6);
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {
                transform: translateY(0);
            }
            40% {
                transform: translateY(-10px);
            }
            60% {
                transform: translateY(-5px);
            }
        }

        /* Enhanced Mobile WhatsApp Button - Fixed */
        .whatsapp-float {
            position: fixed;
            width: 50px;
            height: 50px;
            bottom: 15px;
            right: 15px;
            background: #25d366;
            color: white;
            border-radius: 50%;
            text-align: center;
            font-size: 20px;
            box-shadow: 0 4px 20px rgba(37, 211, 102, 0.4);
            z-index: 1000;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            animation: bounce 2s infinite;
            transition: all 0.3s ease;
            touch-action: manipulation;
        }

        .whatsapp-float:hover {
            transform: scale(1.05);
            box-shadow: 0 6px 25px rgba(37, 211, 102, 0.6);
        }

        .whatsapp-float i {
            font-size: 22px;
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-6px); }
            60% { transform: translateY(-3px); }
        }

        /* Tablet Responsive (768px+) */
        @media (min-width: 768px) {
            .container { padding: 0 25px; }
            
            .cross-container {
                width: 45px;
                height: 45px;
            }
            
            .medical-cross {
                width: 28px;
                height: 28px;
            }
            
            .brand-text h1 { 
                font-size: 1.5rem; 
                white-space: normal;
            }
            .brand-text .tagline { 
                font-size: 0.8rem; 
                white-space: normal;
            }
            
            .nav-links {
                justify-content: center;
                gap: 20px;
            }
            
            .hero h2 { font-size: 2.2rem; }
            .hero p { font-size: 1.1rem; }
            
            .cta-buttons {
                flex-direction: row;
                justify-content: center;
                gap: 16px;
            }
            
            .btn {
                width: auto;
                max-width: none;
                padding: 14px 28px;
            }
            
            .categories-grid {
                grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
                gap: 20px;
            }
            
            .stores-grid {
                grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
                gap: 2rem;
            }
            
            .service-grid {
                grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            }
            
            .footer-content {
                grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
                gap: 2rem;
            }
        }

        /* Desktop Responsive (1024px+) */
        @media (min-width: 1024px) {
            .cross-container {
                width: 50px;
                height: 50px;
            }
            
            .medical-cross {
                width: 30px;
                height: 30px;
            }
            
            .brand-text h1 { font-size: 1.6rem; }
            .brand-text .tagline { font-size: 0.85rem; }
            
            .nav-links {
                gap: 35px;
            }
            
            .nav-links a {
                padding: 10px 18px;
                font-size: 1rem;
            }
            
            .hero {
                padding: 4rem 0;
            }
            
            .hero h2 { font-size: 2.5rem; }
            .hero p { font-size: 1.2rem; }
            
            .prescription-hero {
                padding: 3rem 0;
                margin: 2rem 0;
            }
            
            .categories {
                padding: 4rem 0;
            }
            
            .section-title { font-size: 2rem; }
            
            .categories-grid {
                grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
                gap: 2rem;
            }
            
            .category-card {
                padding: 2rem;
            }
            
            .category-icon {
                width: 70px;
                height: 70px;
                font-size: 28px;
            }
            
            .category-card h3 { font-size: 1.1rem; }
            .category-card p { font-size: 0.9rem; }
            
            .whatsapp-float {
                width: 60px;
                height: 60px;
                bottom: 30px;
                right: 30px;
            }
        }

        /* Landscape Phone Optimization */
        @media (max-height: 500px) and (orientation: landscape) {
            .hero {
                padding: 1.5rem 0;
            }
            
            .hero h2 { font-size: 1.4rem; }
            .hero p { font-size: 0.85rem; }
            
            .prescription-hero {
                padding: 1.5rem 0;
            }
            
            .categories {
                padding: 2rem 0;
            }
            
            .store-locator {
                padding: 2rem 0;
            }
            
            .service-info {
                padding: 2rem 0;
            }
        }

        /* Touch improvements */
        @media (hover: none) and (pointer: coarse) {
            .btn:hover,
            .category-card:hover,
            .whatsapp-float:hover {
                transform: none;
            }
            
            .btn:active {
                transform: scale(0.98);
            }
            
            .category-card:active {
                transform: scale(0.97);
            }
        }

        /* Hidden file input */
        input[type="file"] { display: none; }

        /* Scroll indicator for nav */
        .nav::after {
            content: '';
            position: absolute;
            right: 15px;
            top: 50%;
            transform: translateY(-50%);
            width: 6px;
            height: 6px;
            background: #F56A0A;
            border-radius: 50%;
            opacity: 0.6;
        }

        @media (min-width: 768px) {
            .nav::after {
                display: none;
            }
        }

        /* Additional mobile fixes */
        .container {
            overflow-x: hidden;
        }

        /* Ensure all text fits within screen */
        h1, h2, h3, h4, h5, h6, p, span, div {
            word-wrap: break-word;
            overflow-wrap: break-word;
        }

        /* Fix any potential horizontal scroll */
        html, body {
            overflow-x: hidden;
            width: 100%;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <div class="cross-container">
                        <div class="medical-cross"></div>
                        <div class="orange-accent">O</div>
                        <div class="leaf-element"></div>
                    </div>
                    <div class="brand-text">
                        <h1><span class="orange-text">Orange</span> Chemist</h1>
                        <p class="tagline">Your Neighborhood Health Partner</p>
                    </div>
                </div>
                <button class="menu-toggle" id="menuToggle">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
        </div>
    </header>

    <!-- Navigation -->
    <nav class="nav">
        <div class="container">
            <ul class="nav-links" id="navLinks">
                <li><a href="#home" class="active">Home</a></li>
                <li><a href="#store-locator">Stores</a></li>
                <li><a href="#categories">Products</a></li>
                <li><a href="#prescription">Prescription</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h2>Healthcare Made Simple & Convenient</h2>
            <p>Your trusted neighborhood pharmacy in Kharghar, Navi Mumbai. From medicines to ice creams, baby care to pet supplies - we deliver quality products right to your doorstep.</p>
            <div class="cta-buttons">
                <a href="https://wa.me/919820796184?text=Hi! I'd like to place an order" class="btn btn-primary">
                    <i class="fab fa-whatsapp"></i> Order on WhatsApp
                </a>
                <a href="#categories" class="btn btn-secondary">
                    <i class="fas fa-th-large"></i> Browse Products
                </a>
            </div>
        </div>
    </section>

    <!-- Prescription Upload -->
    <section class="prescription-hero" id="prescription">
        <div class="container">
            <div class="prescription-content">
                <h2>Upload Your Prescription</h2>
                <p>Fast, secure, and convenient prescription service</p>
                
                <div class="prescription-upload" onclick="document.getElementById('prescription-file').click()">
                    <div class="upload-icon">
                        <i class="fas fa-cloud-upload-alt"></i>
                    </div>
                    <h3>Click to upload or drag & drop</h3>
                    <p>Supported formats: JPG, PNG, PDF (Max 5MB)</p>
                    <input type="file" id="prescription-file" accept=".jpg,.jpeg,.png,.pdf" multiple>
                </div>
                
                <div class="cta-buttons">
                    <a href="https://wa.me/919820796184?text=Hi! I'd like to upload my prescription and place an order" class="btn" style="background: white; color: #F56A0A;">
                        <i class="fab fa-whatsapp"></i> Send via WhatsApp
                    </a>
                </div>
                
                <p style="margin-top: 1rem; opacity: 0.9; font-size: 0.85rem;">
                    <i class="fas fa-user-md"></i> Our licensed pharmacists will review and contact you within 30 minutes
                </p>
            </div>
        </div>
    </section>

   <!-- Product Categories -->
    <section class="categories" id="categories">
        <div class="container">
            <h2 class="section-title">Our Product Categories</h2>
            <div class="categories-grid">
                <a href="products.html?category=medicines" class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-pills"></i>
                    </div>
                    <h3>Medicines</h3>
                    <p>Prescription & OTC medicines, generics, branded drugs</p>
                </a>
                
                <a href="products.html?category=icecream-frozen" class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-ice-cream"></i>
                    </div>
                    <h3>Ice Creams & Frozen Food</h3>
                    <p>Premium ice creams, frozen meals, cold storage items</p>
                </a>
                
                <a href="products.html?category=baby-care" class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-baby"></i>
                    </div>
                    <h3>Baby Care</h3>
                    <p>Diapers, formula, baby food, care essentials</p>
                </a>
                
                <a href="products.html?category=skincare" class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-spa"></i>
                    </div>
                    <h3>Skin, Hair, Body Care</h3>
                    <p>Skincare, haircare, cosmetics, personal hygiene</p>
                </a>
                
                <a href="products.html?category=ayurvedic" class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-leaf"></i>
                    </div>
                    <h3>Ayurvedic</h3>
                    <p>Traditional medicines, herbal products, natural remedies</p>
                </a>
                
                <a href="products.html?category=groceries" class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-cookie-bite"></i>
                    </div>
                    <h3>Groceries - Snacks, Biscuits</h3>
                    <p>Daily essentials, snacks, beverages, packaged foods</p>
                </a>
                
                <a href="products.html?category=nutrition" class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-dumbbell"></i>
                    </div>
                    <h3>Nutrition & Supplements</h3>
                    <p>Vitamins, protein powders, health supplements</p>
                </a>
                
                <a href="products.html?category=pet-supplies" class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-paw"></i>
                    </div>
                    <h3>Pet Supplies</h3>
                    <p>Pet medicines, food, care products, accessories</p>
                </a>
                
                <a href="products.html?category=medical-devices" class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-stethoscope"></i>
                    </div>
                    <h3>Medical Devices & More</h3>
                    <p>BP monitors, thermometers, first aid, medical equipment</p>
                </a>
            </div>
        </div>
    </section>

  <!-- Store Locator -->
    <section class="store-locator" id="store-locator">
        <div class="container">
            <h2 class="section-title">Our Store Locations</h2>
            <div class="stores-grid">
                <div class="store-card">
                    <div class="store-header">
                        <div class="store-icon">
                            <i class="fas fa-store"></i>
                        </div>
                        <div class="store-details">
                            <h3>Orange Chemist - Sai Spring</h3>
                            <p style="color: #F56A0A; font-weight: 600;">Main Store</p>
                        </div>
                    </div>
                    <div class="store-info">
                        <p><i class="fas fa-map-marker-alt" style="color: #F56A0A; width: 16px;"></i> 35G Sai Spring Apartment, 2&3, Utsav Chowk - CISF Rd, Kharghar, Navi Mumbai, Maharashtra 410210</p>
                        <p><i class="fas fa-clock" style="color: #F56A0A; width: 16px;"></i> Daily: 8:00 AM - 11:00 PM</p>
                        <p><i class="fas fa-truck" style="color: #F56A0A; width: 16px;"></i> Delivery: 10:00 AM - 10:00 PM</p>
                    </div>
                    <div class="store-actions">
                        <a href="https://g.co/kgs/vfRQ3s9" target="_blank" class="btn btn-primary btn-small">
                            <i class="fas fa-directions"></i> Get Directions
                        </a>
                        <a href="https://wa.me/919820796184?text=Hi! I want to visit your Sai Spring store" class="btn btn-secondary btn-small">
                            <i class="fab fa-whatsapp"></i> Contact Store
                        </a>
                    </div>
                </div>

                <div class="store-card">
                    <div class="store-header">
                        <div class="store-icon">
                            <i class="fas fa-store"></i>
                        </div>
                        <div class="store-details">
                            <h3>Orange Chemist - Greenwoods</h3>
                            <p style="color: #F56A0A; font-weight: 600;">Metro Station Store</p>
                        </div>
                    </div>
                    <div class="store-info">
                        <p><i class="fas fa-map-marker-alt" style="color: #F56A0A; width: 16px;"></i> Shop No 25/26 Greenwoods CHS Plot 9,13,13A,13B, Metro Road, near Pethpada Metro Station, Sector 35E, Kharghar, Navi Mumbai, Maharashtra 410210</p>
                        <p><i class="fas fa-clock" style="color: #F56A0A; width: 16px;"></i> Daily: 8:00 AM - 11:00 PM</p>
                        <p><i class="fas fa-train" style="color: #F56A0A; width: 16px;"></i> Near Pethpada Metro Station</p>
                    </div>
                    <div class="store-actions">
                        <a href="https://g.co/kgs/tneNGyd" target="_blank" class="btn btn-primary btn-small">
                            <i class="fas fa-directions"></i> Get Directions
                        </a>
                        <a href="https://wa.me/919820796184?text=Hi! I want to visit your Greenwoods store" class="btn btn-secondary btn-small">
                            <i class="fab fa-whatsapp"></i> Contact Store
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Service Information -->
    <section class="service-info">
        <div class="container">
            <h2 class="section-title" style="color: white;">Why Choose Orange Chemist?</h2>
            <div class="service-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-truck"></i>
                    </div>
                    <h3>Free Home Delivery</h3>
                    <p>Free delivery on orders above ₹100 in Kharghar<br>Delivery Time: 10 AM - 10 PM</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-clock"></i>
                    </div>
                    <h3>Extended Hours</h3>
                    <p>Open Daily: 8:00 AM - 11:00 PM<br>Monday to Sunday<br>Consistent service</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3>Licensed & Trusted</h3>
                    <p>Certified pharmacists<br>100% genuine products<br>Quality guaranteed</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <h3>Easy Ordering</h3>
                    <p>WhatsApp ordering<br>Prescription upload<br>Quick delivery</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer" id="contact">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>Orange Chemist</h3>
                    <p>Your trusted neighborhood pharmacy in Kharghar, Navi Mumbai. From healthcare essentials to daily needs, we're here to serve you with quality and care.</p>
                </div>
                <div class="footer-section">
                    <h3>Quick Links</h3>
                    <a href="#categories">Browse Products</a>
                    <a href="#prescription">Upload Prescription</a>
                    <a href="#store-locator">Store Locations</a>
                    <a href="https://wa.me/919820796184">WhatsApp Order</a>
                </div>
                <div class="footer-section">
                    <h3>Contact Information</h3>
                    <p><i class="fab fa-whatsapp"></i> +91 98207 96184</p>
                    <p><i class="fas fa-envelope"></i> info@orangechemist.com</p>
                    <p><i class="fas fa-clock"></i> Daily: 8:00 AM - 11:00 PM</p>
                </div>
            </div>
            <div style="text-align: center; padding-top: 2rem; border-top: 1px solid #475569;">
                <p>&copy; 2024 Orange Chemist. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <!-- Floating WhatsApp Button - Right Side with Bounce -->
    <a href="https://wa.me/919820796184?text=Hi! I'd like to place an order" class="whatsapp-float" target="_blank">
        <i class="fab fa-whatsapp"></i>
    </a>

    <script>
        // Prescription file upload handling
        document.getElementById('prescription-file').addEventListener('change', function(e) {
            const files = e.
