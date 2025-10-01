<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مدرسة عكرمة الثانوية - الأردن</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #1a5276;
            --secondary: #2e86c1;
            --accent: #e74c3c;
            --gold: #f39c12;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --green: #27ae60;
        }

        body {
            font-family: 'Cairo', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #333;
            line-height: 1.8;
            scroll-behavior: smooth;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            padding: 1rem 0;
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            transition: all 0.3s ease;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo-img {
            width: 60px;
            height: 60px;
            background: var(--primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
            border: 3px solid var(--gold);
        }

        .logo-text {
            color: var(--primary);
        }

        .logo-text h1 {
            font-size: 1.4rem;
            margin-bottom: 5px;
        }

        .logo-text p {
            font-size: 0.9rem;
            color: var(--secondary);
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 600;
            transition: color 0.3s;
            padding: 0.5rem 1rem;
            border-radius: 25px;
            font-size: 1rem;
        }

        .nav-links a:hover,
        .nav-links a.active {
            color: var(--secondary);
            background: rgba(52, 152, 219, 0.1);
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), 
                        url('https://images.unsplash.com/photo-1523050854058-8df90110c9f1?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            padding: 0 20px;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        .hero-content p {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .cta-button {
            display: inline-block;
            background: var(--gold);
            color: white;
            padding: 1rem 2.5rem;
            text-decoration: none;
            border-radius: 50px;
            font-size: 1.2rem;
            font-weight: bold;
            transition: all 0.3s ease;
            border: 2px solid var(--gold);
        }

        .cta-button:hover {
            background: transparent;
            color: var(--gold);
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(243, 156, 18, 0.3);
        }

        /* Sections */
        .section {
            padding: 5rem 0;
            background: white;
        }

        .section:nth-child(even) {
            background: #f8f9fa;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: var(--primary);
            position: relative;
        }

        .section-title:after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: var(--gold);
            border-radius: 2px;
        }

        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .about-text {
            font-size: 1.1rem;
        }

        .about-stats {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 2rem;
            margin-top: 2rem;
        }

        .stat-item {
            text-align: center;
            padding: 1.5rem;
            background: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            color: var(--primary);
            display: block;
        }

        .stat-label {
            color: var(--dark);
            font-weight: 600;
        }

        /* Programs Section */
        .programs-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .program-card {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            text-align: center;
            transition: transform 0.3s ease;
            border-top: 4px solid var(--secondary);
        }

        .program-card:hover {
            transform: translateY(-10px);
        }

        .program-icon {
            font-size: 3rem;
            color: var(--secondary);
            margin-bottom: 1rem;
        }

        .program-card h3 {
            color: var(--primary);
            margin-bottom: 1rem;
            font-size: 1.5rem;
        }

        /* Staff Section */
        .staff-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .staff-card {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .staff-avatar {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            background: var(--light);
            margin: 0 auto 1rem;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.5rem;
            color: var(--primary);
            border: 3px solid var(--gold);
        }

        /* Gallery */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1rem;
        }

        .gallery-item {
            height: 250px;
            background: var(--light);
            border-radius: 10px;
            overflow: hidden;
            position: relative;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s ease;
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        /* Contact Section */
        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            padding: 1rem;
            background: white;
            border-radius: 10px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
        }

        .contact-icon {
            width: 50px;
            height: 50px;
            background: var(--primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.2rem;
        }

        .contact-form {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: var(--dark);
            font-weight: 600;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 1rem;
            border: 2px solid #e0e0e0;
            border-radius: 10px;
            font-size: 1rem;
            font-family: 'Cairo', sans-serif;
            transition: border-color 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--secondary);
        }

        .submit-btn {
            background: var(--primary);
            color: white;
            padding: 1rem 2rem;
            border: none;
            border-radius: 10px;
            font-size: 1.1rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            width: 100%;
        }

        .submit-btn:hover {
            background: var(--secondary);
            transform: translateY(-2px);
        }

        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 3rem 0 1rem;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-section h3 {
            color: var(--gold);
            margin-bottom: 1.5rem;
            font-size: 1.3rem;
        }

        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }

        .social-links a {
            width: 40px;
            height: 40px;
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            background: var(--gold);
            transform: translateY(-3px);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255,255,255,0.1);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero-content h1 {
                font-size: 2.5rem;
            }
            
            .about-content,
            .contact-content {
                grid-template-columns: 1fr;
            }
            
            .about-stats {
                grid-template-columns: 1fr;
            }
        }

        /* Scroll to top */
        .scroll-top {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 50px;
            height: 50px;
            background: var(--gold);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            font-size: 1.2rem;
            box-shadow: 0 3px 15px rgba(0,0,0,0.2);
            transition: all 0.3s ease;
            z-index: 1000;
        }

        .scroll-top:hover {
            background: var(--primary);
            transform: translateY(-3px);
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header id="header">
        <div class="container">
            <div class="nav-container">
                <div class="logo">
                    <div class="logo-img">
                        <i class="fas fa-graduation-cap"></i>
                    </div>
                    <div class="logo-text">
                        <h1>مدرسة عكرمة الثانوية</h1>
                        <p>عمان - الأردن</p>
                    </div>
                </div>
                <ul class="nav-links">
                    <li><a href="#home" class="active">الرئيسية</a></li>
                    <li><a href="#about">عن المدرسة</a></li>
                    <li><a href="#programs">البرامج</a></li>
                    <li><a href="#staff">الهيئة التدريسية</a></li>
                    <li><a href="#gallery">معرض الصور</a></li>
                    <li><a href="#contact">اتصل بنا</a></li>
                </ul>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>مدرسة عكرمة الثانوية</h1>
            <p>نحو مستقبل مشرق بجيل واعد</p>
            <p>تأسست عام 1985 - عمان، الأردن</p>
            <a href="#about" class="cta-button">اكتشف المزيد <i class="fas fa-arrow-down"></i></a>
        </div>
    </section>

    <!-- About Section -->
    <section class="section" id="about">
        <div class="container">
            <h2 class="section-title">عن مدرستنا</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>مدرسة عكرمة الثانوية مؤسسة تعليمية رائدة في العاصمة عمان، تأسست عام 1985 بهدف تقديم تعليم متميز يجمع بين الأصالة والحداثة. نحن نؤمن بأن التعليم هو أساس تقدم الأمم وسر ازدهارها.</p>
                    
                    <p>تضم المدرسة أحدث المرافق التعليمية والمختبرات العلمية المتطورة، ونسعى دائماً لتوفير بيئة تعليمية محفزة للإبداع والتميز، حيث نعمل على بناء شخصية الطالب المتكاملة علمياً وثقافياً واجتماعياً.</p>

                    <div class="about-stats">
                        <div class="stat-item">
                            <span class="stat-number">1,200+</span>
                            <span class="stat-label">طالب وطالبة</span>
                        </div>
                        <div class="stat-item">
                            <span class="stat-number">85+</span>
                            <span class="stat-label">معلم ومعلمة</span>
                        </div>
                        <div class="stat-item">
                            <span class="stat-number">98%</span>
                            <span class="stat-label">نسبة النجاح</span>
                        </div>
                        <div class="stat-item">
                            <span class="stat-number">35+</span>
                            <span class="stat-label">عاماً من العطاء</span>
                        </div>
                    </div>
                </div>
                <div class="about-image">
                    <div style="background: #f0f0f0; height: 400px; border-radius: 15px; display: flex; align-items: center; justify-content: center; color: #666;">
                        <i class="fas fa-school" style="font-size: 4rem;"></i>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Programs Section -->
    <section class="section" id="programs">
        <div class="container">
            <h2 class="section-title">برامجنا الأكاديمية</h2>
            <div class="programs-grid">
                <div class="program-card">
                    <div class="program-icon">
                        <i class="fas fa-flask"></i>
                    </div>
                    <h3>القسم العلمي</h3>
                    <p>برنامج متكامل في العلوم والرياضيات يؤهل الطلاب للتخصصات العلمية والطبية والهندسية في الجامعات.</p>
                </div>
                <div class="program-card">
                    <div class="program-icon">
                        <i class="fas fa-book"></i>
                    </div>
                    <h3>القسم الأدبي</h3>
                    <p>يركز على العلوم الإنسانية واللغات والدراسات الاجتماعية، ويؤهل للعديد من التخصصات الجامعية.</p>
                </div>
                <div class="program-card">
                    <div class="program-icon">
                        <i class="fas fa-laptop-code"></i>
                    </div>
                    <h3>تكنولوجيا المعلومات</h3>
                    <p>برنامج متخصص في الحاسوب وتكنولوجيا المعلومات يواكب متطلبات العصر الرقمي.</p>
                </div>
                <div class="program-card">
                    <div class="program-icon">
                        <i class="fas fa-futbol"></i>
                    </div>
                    <h3>الأنشطة الطلابية</h3>
                    <p>برامج رياضية وفنية وثقافية متنوعة لتنمية مواهب الطلاب وصقل شخصياتهم.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Staff Section -->
    <section class="section" id="staff">
        <div class="container">
            <h2 class="section-title">الهيئة التدريسية</h2>
            <div class="staff-grid">
                <div class="staff-card">
                    <div class="staff-avatar">
                        <i class="fas fa-user-tie"></i>
                    </div>
                    <h3>د. أحمد السعدون</h3>
                    <p>مدير المدرسة</p>
                    <p>دكتوراه في الإدارة التربوية</p>
                </div>
                <div class="staff-card">
                    <div class="staff-avatar">
                        <i class="fas fa-user-graduate"></i>
                    </div>
                    <h3>أ. فاطمة الزعبي</h3>
                    <p>نائب المدير للشؤون الأكاديمية</p>
                    <p>ماجستير في المناهج وطرق التدريس</p>
                </div>
                <div class="staff-card">
                    <div class="staff-avatar">
                        <i class="fas fa-atom"></i>
                    </div>
                    <h3>أ. محمد الحسين</h3>
                    <p>رئيس قسم العلوم</p>
                    <p>ماجستير في الكيمياء</p>
                </div>
                <div class="staff-card">
                    <div class="staff-avatar">
                        <i class="fas fa-language"></i>
                    </div>
                    <h3>أ. سارة العبداللات</h3>
                    <p>رئيسة قسم اللغات</p>
                    <p>ماجستير في اللغة العربية</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section class="section" id="gallery">
        <div class="container">
            <h2 class="section-title">معرض الصور</h2>
            <div class="gallery-grid">
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1523050854058-8df90110c9f1?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=500&q=80" alt="المدرسة">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1546410531-bb4caa6b424d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=500&q=80" alt="الفصول الدراسية">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1588072432836-e10032774350?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=500&q=80" alt="المختبرات">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1541336032412-2048a678540d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=500&q=80" alt="الأنشطة">
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="section" id="contact">
        <div class="container">
            <h2 class="section-title">اتصل بنا</h2>
            <div class="contact-content">
                <div class="contact-info">
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div>
                            <h3>عنوان المدرسة</h3>
                            <p>عمان - جبل عمان - شارع المدينة المنورة</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone"></i>
                        </div>
                        <div>
                            <h3>هاتف المدرسة</h3>
                            <p>+962 6 555 1234</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div>
                            <h3>البريد الإلكتروني</h3>
                            <p>info@ikrima-school.edu.jo</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-clock"></i>
                        </div>
                        <div>
                            <h3>ساعات الدوام</h3>
                            <p>الأحد - الخميس: 7:30 صباحاً - 2:30 مساءً</p>
                        </div>
                    </div>
                </div>
                <div class="contact-form">
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="name">الاسم الكامل</label>
                            <input type="text" id="name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">البريد الإلكتروني</label>
                            <input type="email" id="email" required>
                        </div>
                        <div class="form-group">
                            <label for="phone">رقم الهاتف</label>
                            <input type="tel" id="phone">
                        </div>
                        <div class="form-group">
                            <label for="message">الرسالة</label>
                            <textarea id="message" rows="5" required></textarea>
                        </div>
                        <button type="submit" class="submit-btn">إرسال الرسالة</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>مدرسة عكرمة الثانوية</h3>
                    <p>مؤسسة تعليمية تلتزم بتقديم تعليم متميز يواكب متطلبات العصر، ويساهم في بناء جيل قادر على مواجهة تحديات المستقبل.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                <div class="footer-section">
                    <h3>روابط سريعة</h3>
                    <p><a href="#home" style="color: #ccc;">الرئيسية</a></p>
                    <p><a href="#about" style="color: #ccc;">عن المدرسة</a></p>
                    <p><a href="#programs" style="color: #ccc;">البرامج</a></p>
                    <p><a href="#contact" style="color: #ccc;">اتصل بنا</a></p>
                </div>
                <div class="footer-section">
                    <h3>خريطة الموقع</h3>
                    <div style="background: rgba(255,255,255,0.1); height: 150px; border-radius: 10px; display: flex; align-items: center; justify-content: center; color: #ccc;">
                        <i class="fas fa-map" style="font-size: 2rem;"></i>
                    </div>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2024 مدرسة عكرمة الثانوية - عمان، الأردن. جميع الحقوق محفوظة.</p>
            </div>
        </div>
    </footer>

    <!-- Scroll to Top -->
    <a href="#home" class="scroll-top">
        <i class="fas fa-arrow-up"></i>
    </a>

    <script>
        // Scroll effect for header
        window.addEventListener('scroll', function() {
            const header = document.getElementById('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(255, 255, 255, 0.98)';
                header.style.padding = '0.5rem 0';
            } else {
                header.style.background = 'rgba(255, 255, 255, 0.95)';
                header.style.padding = '1rem 0';
            }
        });

        // Active nav link
        const sections = document.querySelectorAll('section');
        const navLinks = document.querySelectorAll('.nav-links a');

        window.addEventListener('scroll', function() {
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if (scrollY >= (sectionTop - 200)) {
                    current = section.getAttribute('id');
                }
            });

            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href').substring(1) === current) {
                    link.classList.add('active');
                }
            });
        });

        // Form submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('شكراً لتواصلكم معنا! سنرد على رسالتكم في أقرب وقت ممكن.');
            this.reset();
        });

        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });
    </script>
</body>
</html>
