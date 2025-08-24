# my-website

   

[Uploading 666index.html…]()
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>فنون الرقمية | تصميم شعارك الإحترافي خلال 48 ساعة</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #4e54c8;
            --secondary: #8f94fb;
            --accent: #ff6b6b;
            --light: #f8f9fa;
            --dark: #2d3436;
            --success: #00b894;
            --gradient: linear-gradient(to right, var(--primary), var(--secondary));
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Cairo', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            color: var(--dark);
            line-height: 1.6;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background: var(--gradient);
            color: white;
            padding: 1.2rem 0;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.15);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1.8rem;
            font-weight: bold;
        }
        
        .logo i {
            color: var(--accent);
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            padding: 5px 10px;
            border-radius: 4px;
            position: relative;
        }
        
        nav a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: 0;
            left: 0;
            background-color: var(--accent);
            transition: width 0.3s ease;
        }
        
        nav a:hover::after {
            width: 100%;
        }
        
        /* Hero Section */
        .hero {
            padding: 5rem 0;
            text-align: center;
            background: url('https://images.unsplash.com/photo-1626785774573-4b799315345d?ixlib=rb-4.0.3') center/cover no-repeat;
            color: white;
            position: relative;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: var(--gradient);
            opacity: 0.9;
        }
        
        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 800px;
            margin: 0 auto;
            animation: fadeIn 1s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .hero h1 {
            font-size: 3.2rem;
            margin-bottom: 1.5rem;
            line-height: 1.2;
        }
        
        .hero p {
            font-size: 1.4rem;
            margin-bottom: 2.5rem;
        }
        
        .highlight {
            color: var(--accent);
            font-weight: bold;
        }
        
        /* Features Section */
        .features {
            padding: 5rem 0;
            background: white;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            font-size: 2.3rem;
            color: var(--primary);
            position: relative;
            padding-bottom: 15px;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--accent);
            border-radius: 2px;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .feature-card {
            background: var(--light);
            padding: 2rem;
            border-radius: 12px;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .feature-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: var(--gradient);
            transition: width 0.3s ease;
        }
        
        .feature-card:hover::before {
            width: 100%;
            opacity: 0.1;
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
        }
        
        .feature-icon {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
            position: relative;
            z-index: 1;
        }
        
        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--dark);
            position: relative;
            z-index: 1;
        }
        
        .feature-card p {
            position: relative;
            z-index: 1;
        }
        
        /* Portfolio Section */
        .portfolio {
            padding: 5rem 0;
            background: #f8f9fa;
        }
        
        .logo-gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .logo-item {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
            position: relative;
        }
        
        .logo-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
        }
        
        .logo-img {
            height: 200px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
        }
        
        .logo-img i {
            font-size: 5rem;
            color: var(--primary);
            transition: all 0.3s ease;
        }
        
        .logo-item:hover .logo-img i {
            transform: scale(1.1);
        }
        
        .logo-name {
            padding: 1.5rem;
            text-align: center;
            font-weight: bold;
            font-size: 1.2rem;
            color: var(--dark);
        }
        
        /* Services Section */
        .services {
            padding: 5rem 0;
            background: white;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .service-card {
            background: var(--light);
            padding: 2.5rem;
            border-radius: 12px;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: var(--gradient);
            transition: height 0.3s ease;
        }
        
        .service-card:hover::before {
            height: 100%;
            opacity: 0.05;
        }
        
        .service-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
        }
        
        .service-icon {
            font-size: 3.5rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
            position: relative;
            z-index: 1;
        }
        
        .service-card h3 {
            font-size: 1.8rem;
            margin-bottom: 1rem;
            color: var(--dark);
            position: relative;
            z-index: 1;
        }
        
        .service-card p {
            margin-bottom: 1.5rem;
            color: #666;
            position: relative;
            z-index: 1;
        }
        
        .service-price {
            font-size: 1.8rem;
            color: var(--primary);
            font-weight: bold;
            margin-bottom: 1.5rem;
            position: relative;
            z-index: 1;
        }
        
        /* Contact Section */
        .contact {
            padding: 5rem 0;
            background: #f8f9fa;
        }
        
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 3rem;
            margin-top: 2rem;
        }
        
        .contact-info {
            background: var(--gradient);
            padding: 2.5rem;
            border-radius: 12px;
            color: white;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
            position: relative;
            overflow: hidden;
        }
        
        .contact-info::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 100%;
            height: 100%;
            background: rgba(255, 255, 255, 0.1);
            transform: rotate(30deg);
            transition: all 0.3s ease;
        }
        
        .contact-info:hover::before {
            transform: rotate(0deg);
            top: 0;
            right: 0;
        }
        
        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            position: relative;
            padding-bottom: 10px;
            z-index: 1;
        }
        
        .contact-info h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 3px;
            background: var(--accent);
        }
        
        .contact-details {
            margin-top: 2rem;
            position: relative;
            z-index: 1;
        }
        
        .contact-details p {
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .contact-details i {
            color: var(--accent);
            font-size: 1.2rem;
        }
        
        .contact-form {
            background: white;
            padding: 2.5rem;
            border-radius: 12px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
            color: var(--dark);
        }
        
        .form-control {
            width: 100%;
            padding: 0.8rem 1rem;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
            transition: all 0.3s ease;
        }
        
        .form-control:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(78, 84, 200, 0.1);
        }
        
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        .btn {
            display: inline-block;
            padding: 0.8rem 2rem;
            background: var(--accent);
            color: white;
            border: none;
            border-radius: 30px;
            font-size: 1rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            position: relative;
            overflow: hidden;
        }
        
        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            transition: all 0.5s ease;
        }
        
        .btn:hover::before {
            left: 100%;
        }
        
        .btn:hover {
            background: #ff5252;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(255, 107, 107, 0.3);
        }
        
        .btn-block {
            display: block;
            width: 100%;
            text-align: center;
        }
        
        /* FAQ Section */
        .faq {
            padding: 5rem 0;
            background: white;
        }
        
        .accordion {
            margin-top: 2rem;
        }
        
        .accordion-item {
            margin-bottom: 1rem;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        
        .accordion-header {
            background: var(--light);
            padding: 1.5rem;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-weight: 500;
        }
        
        .accordion-header i {
            transition: transform 0.3s ease;
        }
        
        .accordion-content {
            padding: 0;
            max-height: 0;
            overflow: hidden;
            transition: all 0.3s ease;
        }
        
        .accordion-content.active {
            padding: 1.5rem;
            max-height: 300px;
        }
        
        .accordion-header.active i {
            transform: rotate(180deg);
        }
        
        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            text-align: center;
            padding: 2rem 0;
            margin-top: 3rem;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin: 1.5rem 0;
        }
        
        .social-links a {
            color: white;
            font-size: 1.5rem;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            color: var(--accent);
            transform: translateY(-3px);
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 1rem;
            }
            
            nav ul {
                gap: 1rem;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.2rem;
            }
            
            .contact-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <i class="fas fa-paint-brush"></i>
                    <span>فنون الرقمية</span>
                </div>
                <nav>
                    <ul>
                        <li><a href="#home">الرئيسية</a></li>
                        <li><a href="#features">خدماتنا</a></li>
                        <li><a href="#portfolio">معرض الأعمال</a></li>
                        <li><a href="#services">الباقات</a></li>
                        <li><a href="#contact">اتصل بنا</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1>شعار <span class="highlight">إبداعي</span> يعبر عن هوية علامتك التجارية</h1>
                <p>نحن نصنع هويات بصرية مؤثرة تترك انطباعاً لا ينسى</p>
                <a href="#contact" class="btn">اطلب تصميمك الآن</a>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features" id="features">
        <div class="container">
            <h2 class="section-title">لماذا تختار فنون الرقمية؟</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-rocket"></i>
                    </div>
                    <h3>تصميم سريع</h3>
                    <p>احصل على شعارك خلال 48 ساعة فقط مع الحفاظ على أعلى معايير الجودة</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-palette"></i>
                    </div>
                    <h3>تصاميم فريدة</h3>
                    <p>نقدم لك 3 تصاميم مختلفة لشعارك حتى تجد التصميم المثالي لعلامتك التجارية</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-headset"></i>
                    </div>
                    <h3>دعم متكامل</h3>
                    <p>خدمة عملاء على مدار الساعة لتلبية جميع احتياجاتك واستفساراتك</p>
                </div>
            </div>
        </div>
    </section>

   

    <!-- Portfolio Section -->
    <section class="portfolio" id="portfolio">
        <div class="container">
            <h2 class="section-title">معرض أعمالنا</h2>
            <div class="logo-gallery">
                <div class="logo-item">
                    <div class="logo-img">
                        <i class="fas fa-gem"></i>
                    </div>
                    <div class="logo-name">شعار الماس</div>
                </div>
                <div class="logo-item">
                    <div class="logo-img">
                        <i class="fas fa-dragon"></i>
                    </div>
                    <div class="logo-name">شعار التنين</div>
                </div>
                <div class="logo-item">
                    <div class="logo-img">
                        <i class="fas fa-infinity"></i>
                    </div>
                    <div class="logo-name">شعار اللانهاية</div>
                </div>
                <div class="logo-item">
                    <div class="logo-img">
                        <i class="fas fa-feather-alt"></i>
                    </div>
                    <div class="logo-name">شعار الريشة</div>
                </div>
            </div>
        </div>
    </section>

    <!-- FAQ Section -->
    <section class="faq">
        <div class="container">
            <h2 class="section-title">أسئلة شائعة</h2>
            <div class="accordion">
                <div class="accordion-item">
                    <div class="accordion-header">
                        <span>كم من الوقت يستغرق تصميم الشعار؟</span>
                        <i class="fas fa-chevron-down"></i>
                    </div>
                    <div class="accordion-content">
                        <p>نحن نقدم تصميم سريع للشعار خلال 48 ساعة فقط. ومع ذلك، قد تستغرق العملية وقتاً أطول قليلاً إذا كانت هناك مراجعات أو تعديلات إضافية.</p>
                    </div>
                </div>
                <div class="accordion-item">
                    <div class="accordion-header">
                        <span>هل يمكنني طلب تعديلات على التصميم؟</span>
                        <i class="fas fa-chevron-down"></i>
                    </div>
                    <div class="accordion-content">
                        <p>نعم، نقدم عدد غير محدود من التعديلات حتى تحصل على الشعار الذي تحلم به وتتوافق مع رؤيتك لعلامتك التجارية.</p>
                    </div>
                </div>
                <div class="accordion-item">
                    <div class="accordion-header">
                        <span>ما هي طرق الدفع المتاحة؟</span>
                        <i class="fas fa-chevron-down"></i>
                    </div>
                    <div class="accordion-content">
                        <p>نحن نقبل الدفع عبر التحويل البنكي، وبطاقات الائتمان، والدفع عبر PayPal، بالإضافة إلى الدفع نقداً عند الاستلام في بعض المناطق.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <h2 class="section-title">تواصل معنا</h2>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>معلومات التواصل</h3>
                    <p>تواصل معنا عبر القنوات التالية لطلب خدمة أو للاستفسار</p>
                    <div class="contact-details">
                        <p>
                            <i class="fab fa-whatsapp"></i>
                            <span>+97471350115</span>
                        </p>
                        <p>
                            <i class="fas fa-envelope"></i>
                            <span>smarwebstudio8@gmail.com</span>
                        </p>
                        <p>
                            <i class="fas fa-phone"></i>
                            <span>+97471350115</span>
                        </p>
                        <p>
                            <i class="fas fa-map-marker-alt"></i>
                            <span>Doha -QATAR</span>
                        </p>
                    </div>
                </div>
                <div class="contact-form">
                    <form id="projectForm">
                        <div class="form-group">
                            <label for="name">الاسم بالكامل</label>
                            <input type="text" id="name" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="email">البريد الإلكتروني</label>
                            <input type="email" id="email" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="phone">رقم الهاتف / واتساب</label>
                            <input type="tel" id="phone" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="service">الخدمة المطلوبة</label>
                            <select id="service" class="form-control" required>
                                <option value="">اختر الخدمة</option>
                                <option value="logo">تصميم شعار</option>
                                <option value="website">تصميم موقع</option>
                                <option value="branding">هوية بصرية متكاملة</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <label for="details">تفاصيل عن مشروعك</label>
                            <textarea id="details" class="form-control" required></textarea>
                        </div>
                        <button type="submit" class="btn btn-block">إرسال الطلب</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="logo">
                <i class="fas fa-paint-brush"></i>
                <span>فنون الرقمية</span>
            </div>
            <p>نحو بصرة بصرية استثنائية لعلامتك التجارية</p>
            <div class="social-links">
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="fab fa-snapchat-ghost"></i></a>
                <a href="#"><i class="fab fa-linkedin-in"></i></a>
            </div>
            <p>جميع الحقوق محفوظة &copy; 2023 فنون الرقمية</p>
        </div>
    </footer>

    <script>
        // كود JavaScript لإدارة عملية إرسال الطلب
        document.getElementById('projectForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const formData = {
                name: document.getElementById('name').value,
                email: document.getElementById('email').value,
                phone: document.getElementById('phone').value,
                service: document.getElementById('service').value,
                details: document.getElementById('details').value
            };
            
            alert(`شكراً ${formData.name}! تم استلام طلبك بنجاح وسنتواصل معك خلال 24 ساعة.`);
            
            document.getElementById('projectForm').reset();
        });

        // كود JavaScript للأسئلة الشائعة
        const accordionHeaders = document.querySelectorAll('.accordion-header');
        accordionHeaders.forEach(header => {
            header.addEventListener('click', function() {
                this.classList.toggle('active');
                const content = this.nextElementSibling;
                content.classList.toggle('active');
            });
        });
    </script>
</body>
</html>
