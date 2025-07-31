<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Дубайский и Аббая - Интернет магазин</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #8B4513;
            --secondary: #D2691E;
            --accent: #FFD700;
            --light: #F5F5DC;
            --dark: #2F4F4F;
            --text: #333;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            color: var(--text);
            background-color: #f8f5f0;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 15px rgba(0,0,0,0.1);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1.8rem;
            font-weight: 700;
            font-family: 'Playfair Display', serif;
        }
        
        .logo-icon {
            font-size: 2rem;
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
            position: relative;
        }
        
        nav a:hover {
            color: var(--accent);
        }
        
        nav a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--accent);
            transition: width 0.3s ease;
        }
        
        nav a:hover::after {
            width: 100%;
        }
        
        .header-actions {
            display: flex;
            align-items: center;
            gap: 1rem;
        }
        
        .search-box {
            display: flex;
            align-items: center;
            background: rgba(255,255,255,0.2);
            border-radius: 25px;
            padding: 5px 15px;
        }
        
        .search-box input {
            background: transparent;
            border: none;
            color: white;
            padding: 5px;
            outline: none;
            width: 200px;
        }
        
        .search-box input::placeholder {
            color: rgba(255,255,255,0.7);
        }
        
        .search-box button {
            background: transparent;
            border: none;
            color: white;
            cursor: pointer;
        }
        
        .cart-icon {
            position: relative;
            cursor: pointer;
        }
        
        .cart-count {
            position: absolute;
            top: -8px;
            right: -8px;
            background: var(--accent);
            color: var(--primary);
            font-size: 0.7rem;
            width: 18px;
            height: 18px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
        }
        
        /* Hero Section */
        .hero {
            height: 80vh;
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://placehold.co/1920x1080/8B4513/FFFFFF?text=Middle+East+Fashion') no-repeat center center/cover;
            display: flex;
            align-items: center;
            color: white;
            text-align: center;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            padding: 2rem;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            font-family: 'Playfair Display', serif;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }
        
        .btn {
            display: inline-block;
            background: var(--accent);
            color: var(--primary);
            padding: 12px 30px;
            border: none;
            border-radius: 30px;
            font-weight: 600;
            text-decoration: none;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 1rem;
        }
        
        .btn:hover {
            background: white;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }
        
        .btn-outline {
            background: transparent;
            border: 2px solid var(--accent);
            color: var(--accent);
            margin-left: 1rem;
        }
        
        .btn-outline:hover {
            background: var(--accent);
            color: var(--primary);
        }
        
        /* Categories Section */
        .categories {
            padding: 5rem 0;
            background-color: white;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            font-family: 'Playfair Display', serif;
            color: var(--primary);
            position: relative;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background: var(--accent);
        }
        
        .categories-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }
        
        .category-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            text-align: center;
        }
        
        .category-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.2);
        }
        
        .category-img {
            height: 200px;
            overflow: hidden;
        }
        
        .category-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .category-card:hover .category-img img {
            transform: scale(1.1);
        }
        
        .category-info {
            padding: 1.5rem;
        }
        
        .category-info h3 {
            color: var(--primary);
            margin-bottom: 0.5rem;
            font-family: 'Playfair Display', serif;
        }
        
        .category-info p {
            color: #666;
            margin-bottom: 1rem;
        }
        
        /* Products Section */
        .products {
            padding: 5rem 0;
            background-color: var(--light);
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }
        
        .product-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }
        
        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.15);
        }
        
        .product-img {
            height: 300px;
            overflow: hidden;
            position: relative;
        }
        
        .product-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .product-card:hover .product-img img {
            transform: scale(1.1);
        }
        
        .product-badge {
            position: absolute;
            top: 15px;
            right: 15px;
            background: var(--accent);
            color: var(--primary);
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
        }
        
        .product-info {
            padding: 1.5rem;
        }
        
        .product-category {
            color: var(--secondary);
            font-size: 0.9rem;
            margin-bottom: 0.5rem;
        }
        
        .product-title {
            color: var(--primary);
            margin-bottom: 0.5rem;
            font-family: 'Playfair Display', serif;
            font-size: 1.2rem;
        }
        
        .product-price {
            font-weight: 700;
            color: var(--primary);
            font-size: 1.3rem;
            margin-bottom: 1rem;
        }
        
        .product-rating {
            display: flex;
            align-items: center;
            margin-bottom: 1rem;
            color: var(--accent);
        }
        
        .product-rating span {
            margin-right: 5px;
        }
        
        .product-actions {
            display: flex;
            gap: 1rem;
        }
        
        .btn-add-cart {
            flex: 1;
            background: var(--primary);
            color: white;
            padding: 10px;
            border-radius: 8px;
            text-align: center;
            font-weight: 500;
            transition: all 0.3s ease;
        }
        
        .btn-add-cart:hover {
            background: var(--secondary);
        }
        
        .btn-wishlist {
            width: 40px;
            height: 40px;
            border: 1px solid var(--primary);
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
            transition: all 0.3s ease;
        }
        
        .btn-wishlist:hover {
            background: var(--primary);
            color: white;
        }
        
        /* Features Section */
        .features {
            padding: 5rem 0;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            text-align: center;
        }
        
        .feature-item {
            padding: 2rem;
            background: rgba(255,255,255,0.1);
            border-radius: 15px;
            backdrop-filter: blur(10px);
        }
        
        .feature-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
            color: var(--accent);
        }
        
        .feature-item h3 {
            margin-bottom: 1rem;
            font-family: 'Playfair Display', serif;
        }
        
        /* Newsletter */
        .newsletter {
            padding: 5rem 0;
            background-color: white;
            text-align: center;
        }
        
        .newsletter-container {
            max-width: 600px;
            margin: 0 auto;
        }
        
        .newsletter p {
            margin-bottom: 2rem;
            color: #666;
        }
        
        .newsletter-form {
            display: flex;
            gap: 10px;
        }
        
        .newsletter-form input {
            flex: 1;
            padding: 15px;
            border: 2px solid #ddd;
            border-radius: 30px;
            font-size: 1rem;
            outline: none;
        }
        
        .newsletter-form input:focus {
            border-color: var(--primary);
        }
        
        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 5rem 0 2rem;
        }
        
        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }
        
        .footer-column h3 {
            font-size: 1.3rem;
            margin-bottom: 1.5rem;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-column h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 2px;
            background: var(--accent);
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            color: #ddd;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .footer-column ul li a:hover {
            color: var(--accent);
            padding-left: 5px;
        }
        
        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
            color: white;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background: var(--accent);
            color: var(--primary);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: #aaa;
            font-size: 0.9rem;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                gap: 1rem;
            }
            
            nav ul {
                gap: 1rem;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .search-box {
                order: 3;
                width: 100%;
                max-width: 300px;
            }
            
            .search-box input {
                width: 100%;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .newsletter-form {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container header-container">
            <div class="logo">
                <span class="logo-icon">👑</span>
                <span>Дубайский и Аббая</span>
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Главная</a></li>
                    <li><a href="#categories">Категории</a></li>
                    <li><a href="#products">Товары</a></li>
                    <li><a href="#about">О нас</a></li>
                    <li><a href="#contact">Контакты</a></li>
                </ul>
            </nav>
            <div class="header-actions">
                <div class="search-box">
                    <input type="text" placeholder="Поиск...">
                    <button>🔍</button>
                </div>
                <div class="cart-icon">
                    <span>🛒</span>
                    <div class="cart-count">3</div>
                </div>
            </div>
        </div>
    </header>

    <section class="hero" id="home">
        <div class="hero-content">
            <h1>Роскошная мода из Дубая</h1>
            <p>Исследуйте нашу эксклюзивную коллекцию традиционной и современной одежды из Дубая и Аббая. Качество, стиль и комфорт в каждом изделии.</p>
            <div>
                <a href="#products" class="btn">Посмотреть коллекцию</a>
                <a href="#categories" class="btn btn-outline">Категории</a>
            </div>
        </div>
    </section>

    <section class="categories" id="categories">
        <div class="container">
            <h2 class="section-title">Категории</h2>
            <div class="categories-grid">
                <div class="category-card">
                    <div class="category-img">
                        <img src="https://placehold.co/400x300/D2691E/FFFFFF?text=Abayas" alt="Аббая">
                    </div>
                    <div class="category-info">
                        <h3>Аббая</h3>
                        <p>Элегантные традиционные аббая для любого случая</p>
                        <a href="#" class="btn">Смотреть</a>
                    </div>
                </div>
                <div class="category-card">
                    <div class="category-img">
                        <img src="https://placehold.co/400x300/8B4513/FFFFFF?text=Kanduras" alt="Кандура">
                    </div>
                    <div class="category-info">
                        <h3>Кандура</h3>
                        <p>Традиционная мужская одежда Дубая</p>
                        <a href="#" class="btn">Смотреть</a>
                    </div>
                </div>
                <div class="category-card">
                    <div class="category-img">
                        <img src="https://placehold.co/400x300/FFD700/000000?text=Accessories" alt="Аксессуары">
                    </div>
                    <div class="category-info">
                        <h3>Аксессуары</h3>
                        <p>Шарфы, головные уборы и украшения</p>
                        <a href="#" class="btn">Смотреть</a>
                    </div>
                </div>
                <div class="category-card">
                    <div class="category-img">
                        <img src="https://placehold.co/400x300/2F4F4F/FFFFFF?text=Evening" alt="Вечерние">
                    </div>
                    <div class="category-info">
                        <h3>Вечерние наряды</h3>
                        <p>Роскошные наряды для особых случаев</p>
                        <a href="#" class="btn">Смотреть</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="products" id="products">
        <div class="container">
            <h2 class="section-title">Популярные товары</h2>
            <div class="products-grid">
                <div class="product-card">
                    <div class="product-img">
                        <img src="https://placehold.co/400x500/F5F5DC/8B4513?text=Premium+Abaya" alt="Премиум аббая">
                        <div class="product-badge">Новинка</div>
                    </div>
                    <div class="product-info">
                        <div class="product-category">Аббая</div>
                        <h3 class="product-title">Премиум аббая с вышивкой</h3>
                        <div class="product-price">25 000 ₽</div>
                        <div class="product-rating">
                            <span>⭐</span>
                            <span>⭐</span>
                            <span>⭐</span>
                            <span>⭐</span>
                            <span>⭐</span>
                            <span>(48)</span>
                        </div>
                        <div class="product-actions">
                            <button class="btn-add-cart">В корзину</button>
                            <button class="btn-wishlist">❤️</button>
                        </div>
                    </div>
                </div>
                <div class="product-card">
                    <div class="product-img">
                        <img src="https://placehold.co/400x500/8B4513/FFFFFF?text=Classic+Kandura" alt="Классическая кандура">
                        <div class="product-badge">Хит</div>
                    </div>
                    <div class="product-info">
                        <div class="product-category">Кандура</div>
                        <h3 class="product-title">Классическая кандура</h3>
                        <div class="product-price">18 500 ₽</div>
                        <div class="product-rating">
                            <span>⭐</span>
                            <span>⭐</span>
                            <span>⭐</span>
                            <span>⭐</span>
                            <span>⭐</span>
                            <span>(32)</span>
                        </div>
                        <div class="product-actions">
                            <button class="btn-add-cart">В корзину</button>
                            <button class="btn-wishlist">❤️</button>
                        </div>
                    </div>
                </div>
                <div class="product-card">
                    <div class="product-img">
                        <img src="https://placehold.co/400x500/FFD700/000000?text=Evening+Abaya" alt="Вечерняя аббая">
                    </div>
                    <div class="product-info">
                        <div class="product-category">Вечерние</div>
                        <h3 class="product-title">Вечерняя аббая с пайетками</h3>
                        <div class="product-price">32 000 ₽</div>
                        <div class="product-rating">
                            <span>⭐</span>
                            <span>⭐</span>
                            <span>⭐</span>
                            <span>⭐</span>
                            <span>⭐</span>
                            <span>(24)</span>
                        </div>
                        <div class="product-actions">
                            <button class="btn-add-cart">В корзину</button>
                            <button class="btn-wishlist">❤️</button>
                        </div>
                    </div>
                </div>
                <div class="product-card">
                    <div class="product-img">
                        <img src="https://placehold.co/400x500/2F4F4F/FFFFFF?text=Silk+Abaya" alt="Шелковая аббая">
                        <div class="product-badge">Скидка</div>
                    </div>
                    <div class="product-info">
                        <div class="product-category">Аббая</div>
                        <h3 class="product-title">Шелковая аббая</h3>
                        <div class="product-price">22 000 ₽ <span style="text-decoration: line-through; color: #999; font-size: 0.9rem;">28 000 ₽</span></div>
                        <div class="product-rating">
                            <span>⭐</span>
                            <span>⭐</span>
                            <span>⭐</span>
                            <span>⭐</span>
                            <span>⭐</span>
                            <span>(41)</span>
                        </div>
                        <div class="product-actions">
                            <button class="btn-add-cart">В корзину</button>
                            <button class="btn-wishlist">❤️</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="features">
        <div class="container">
            <h2 class="section-title" style="color: white;">Почему выбирают нас</h2>
            <div class="features-grid">
                <div class="feature-item">
                    <div class="feature-icon">✈️</div>
                    <h3>Быстрая доставка</h3>
                    <p>Доставка по всему миру всего за 3-7 дней</p>
                </div>
                <div class="feature-item">
                    <div class="feature-icon">💎</div>
                    <h3>Премиум качество</h3>
                    <p>Только высококачественные материалы и пошив</p>
                </div>
                <div class="feature-item">
                    <div class="feature-icon">🔄</div>
                    <h3>Легкий возврат</h3>
                    <p>Бесплатный возврат в течение 30 дней</p>
                </div>
                <div class="feature-item">
                    <div class="feature-icon">👑</div>
                    <h3>Эксклюзивные дизайны</h3>
                    <p>Уникальные модели, которых нет в других магазинах</p>
                </div>
            </div>
        </div>
    </section>

    <section class="newsletter">
        <div class="container">
            <div class="newsletter-container">
                <h2 class="section-title">Подпишитесь на новости</h2>
                <p>Получайте уведомления о новых поступлениях, скидках и эксклюзивных предложениях</p>
                <form class="newsletter-form">
                    <input type="email" placeholder="Введите ваш email">
                    <button type="submit" class="btn">Подписаться</button>
                </form>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="footer-grid">
                <div class="footer-column">
                    <h3>Дубайский и Аббая</h3>
                    <p style="color: #ddd; margin-bottom: 1.5rem;">Лучшая традиционная и современная одежда из Дубая. Качество, стиль и комфорт в каждом изделии.</p>
                    <div class="social-links">
                        <a href="#">📱</a>
                        <a href="#">📘</a>
                        <a href="#">📸</a>
                        <a href="#">🐦</a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Информация</h3>
                    <ul>
                        <li><a href="#">О нас</a></li>
                        <li><a href="#">Наши магазины</a></li>
                        <li><a href="#">Карьера</a></li>
                        <li><a href="#">Новости</a></li>
                        <li><a href="#">Пресса</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Покупка</h3>
                    <ul>
                        <li><a href="#">Как заказать</a></li>
                        <li><a href="#">Оплата</a></li>
                        <li><a href="#">Доставка</a></li>
                        <li><a href="#">Возврат</a></li>
                        <li><a href="#">Гарантия</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Контакты</h3>
                    <ul>
                        <li>📞 +7 (495) 123-45-67</li>
                        <li>✉️ info@dubai-abbaya.ru</li>
                        <li>📍 Москва, ул. Тверская, 1</li>
                        <li>🕒 Пн-Сб: 10:00-20:00</li>
                        <li>🌍 Москва, Россия</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                &copy; 2024 Дубайский и Аббая. Все права защищены.
            </div>
        </div>
    </footer>

    <script>
        // Простая анимация для карточек
        document.addEventListener('DOMContentLoaded', function() {
            const productCards = document.querySelectorAll('.product-card');
            const categoryCards = document.querySelectorAll('.category-card');
            
            // Анимация появления
            const observerOptions = {
                threshold: 0.1
            };
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = '1';
                        entry.target.style.transform = 'translateY(0)';
                    }
                });
            }, observerOptions);
            
            [...productCards, ...categoryCards].forEach(card => {
                card.style.opacity = '0';
                card.style.transform = 'translateY(20px)';
                card.style.transition = 'all 0.5s ease';
                observer.observe(card);
            });
            
            // Обработчики кнопок
            const cartButtons = document.querySelectorAll('.btn-add-cart');
            cartButtons.forEach(button => {
                button.addEventListener('click', function() {
                    const cartCount = document.querySelector('.cart-count');
                    let count = parseInt(cartCount.textContent);
                    cartCount.textContent = count + 1;
                    
                    // Визуальный эффект добавления в корзину
                    this.textContent = 'Добавлено!';
                    setTimeout(() => {
                        this.textContent = 'В корзину';
                    }, 1500);
                });
            });
            
            const wishlistButtons = document.querySelectorAll('.btn-wishlist');
            wishlistButtons.forEach(button => {
                button.addEventListener('click', function() {
                    this.style.color = this.style.color === 'white' ? 'var(--primary)' : 'white';
                    this.style.background = this.style.background.includes('var(--primary)') ? 'rgba(255,255,255,0.1)' : 'var(--primary)';
                });
            });
        });
    </script>
</body>
</html># Dubai-Abaya
