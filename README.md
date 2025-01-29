<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>\\ELAGoffe - Кофейня с душой</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }

        body {
            background-color: #f5e6d3;
        }

        .header {
            background-color: #6f4e37;
            padding: 20px;
            color: white;
            text-align: center;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        .nav {
            margin-top: 15px;
        }

        .nav a {
            color: white;
            text-decoration: none;
            margin: 0 15px;
            font-size: 1.1em;
        }

        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), 
                        url('https://images.unsplash.com/photo-1497935586351-b67a49e012bf?ixlib=rb-1.2.1&auto=format&fit=crop&w=1351&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-align: center;
            margin-top: 60px;
        }

        .hero-content h1 {
            font-size: 3.5em;
            margin-bottom: 20px;
        }

        .menu-section {
            padding: 50px 20px;
            text-align: center;
        }

        .menu-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            padding: 30px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .menu-item {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 3px 15px rgba(0,0,0,0.2);
        }

        .menu-item img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 5px;
        }

        .about-section {
            background-color: #fff;
            padding: 50px 20px;
            text-align: center;
        }

        .contact-section {
            padding: 50px 20px;
            background-color: #6f4e37;
            color: white;
        }

        .contact-form {
            max-width: 600px;
            margin: 0 auto;
        }

        input, textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 5px;
        }

        button {
            background-color: #b08a69;
            color: white;
            padding: 12px 30px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1.1em;
        }

        @media (max-width: 768px) {
            .nav {
                display: none;
            }
            .hero-content h1 {
                font-size: 2.5em;
            }
        }
    </style>
</head>
<body>
    <header class="header">
        <h1>Кофеини</h1>
        <nav class="nav">
            <a href="#home">Главная</a>
            <a href="#menu">Меню</a>
            <a href="#about">О нас</a>
            <a href="#contact">Контакты</a>
        </nav>
    </header>

    <section class="hero" id="home">
        <div class="hero-content">
            <h1>Добро пожаловать в Кофеини</h1>
            <p>Наслаждайтесь искусством настоящего кофе</p>
            <button>Посмотреть меню</button>
        </div>
    </section>

    <section class="menu-section" id="menu">
        <h2>Наше меню</h2>
        <div class="menu-grid">
            <div class="menu-item">
                <img src="https://images.unsplash.com/photo-1509042239860-f550ce710b93" alt="Эспрессо">
                <h3>Эспрессо</h3>
                <p>Классический крепкий кофе</p>
                <p>150 ₽</p>
            </div>
            <div class="menu-item">
                <img src="https://images.unsplash.com/photo-1572449043416-55f4685c9f27" alt="Капучино">
                <h3>Капучино</h3>
                <p>Идеальный баланс эспрессо и молока</p>
                <p>180 ₽</p>
            </div>
            <!-- Добавьте больше позиций меню -->
        </div>
    </section>

    <section class="about-section" id="about">
        <h2>О нашей кофейне</h2>
        <p>Мы используем только отборные зерна арабики и готовим кофе с любовью</p>
        <!-- Добавьте больше информации -->
    </section>

    <section class="contact-section" id="contact">
        <h2>Свяжитесь с нами</h2>
        <div class="contact-form">
            <form>
                <input type="text" placeholder="Ваше имя">
                <input type="email" placeholder="Ваш email">
                <textarea placeholder="Сообщение" rows="5"></textarea>
                <button type="submit">Отправить</button>
            </form>
        </div>
        <p>Телефон: +7 (999) 123-45-67</p>
        <p>Адрес: ул. Кофейная, 15</p>
    </section>

    <script>
        // Плавная прокрутка для навигации
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Кофеини - Кофейня с душой</title>
    <style>
        /* ... предыдущие стили ... */

        /* Галерея */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 15px;
            padding: 30px;
        }

        /* Корзина */
        .cart-sidebar {
            position: fixed;
            right: -350px;
            top: 0;
            width: 350px;
            height: 100%;
            background: white;
            box-shadow: -2px 0 15px rgba(0,0,0,0.1);
            padding: 20px;
            transition: 0.3s;
        }

        /* Отзывы */
        .reviews-slider {
            display: flex;
            overflow-x: auto;
            scroll-snap-type: x mandatory;
            padding: 20px 0;
        }

        .review-card {
            flex: 0 0 300px;
            margin: 0 15px;
            padding: 20px;
            background: white;
            border-radius: 10px;
            scroll-snap-align: start;
        }

        /* Карта */
        #map {
            height: 400px;
            width: 100%;
            margin-top: 30px;
        }

        /* Расписание */
        .schedule {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
            max-width: 500px;
            margin: 20px auto;
        }

        /* Бронирование */
        .booking-form {
            max-width: 600px;
            margin: 0 auto;
            background: white;
            padding: 30px;
            border-radius: 10px;
        }
    </style>
    <script src="https://api-maps.yandex.ru/2.1/?apikey=ваш_ключ&lang=ru_RU"></script>
</head>
<body>
    <!-- ... предыдущая разметка ... -->

    <!-- Галерея -->
    <section class="gallery-section">
        <h2>Наша галерея</h2>
        <div class="gallery-grid">
            <img src="gallery1.jpg" alt="Интерьер">
            <img src="gallery2.jpg" alt="Процесс приготовления">
            <!-- Добавьте больше изображений -->
        </div>
    </section>

    <!-- Корзина -->
    <div class="cart-sidebar" id="cart">
        <h3>Ваш заказ</h3>
        <div id="cart-items"></div>
        <p>Итого: <span id="total">0</span> ₽</p>
        <button onclick="checkout()">Оформить заказ</button>
    </div>

    <!-- Отзывы -->
    <section class="reviews-section">
        <h2>Отзывы</h2>
        <div class="reviews-slider">
            <div class="review-card">
                <h4>Анна Петрова</h4>
                <p>Лучший кофе в городе! Обслуживание на высоте.</p>
                <div class="rating">★★★★★</div>
            </div>
            <!-- Добавьте больше отзывов -->
        </div>
    </section>

    <!-- Карта -->
    <section class="map-section">
        <h2>Мы находимся</h2>
        <div id="map"></div>
    </section>

    <!-- Расписание -->
    <section class="schedule-section">
        <h2>Часы работы</h2>
        <div class="schedule">
            <div>Пн-Пт: 8:00 - 22:00</div>
            <div>Сб-Вс: 9:00 - 23:00</div>
        </div>
    </section>

    <!-- Бронирование -->
    <section class="booking-section">
        <h2>Бронирование столика</h2>
        <form class="booking-form" onsubmit="return bookTable(event)">
            <input type="date" id="booking-date" required>
            <input type="time" id="booking-time" required>
            <input type="number" min="1" max="8" placeholder="Количество гостей" required>
            <input type="text" placeholder="Ваше имя" required>
            <input type="tel" placeholder="Телефон" required>
            <button type="submit">Забронировать</button>
        </form>
    </section>

    <script>
        // Корзина
        let cart = [];
        
        function addToCart(item, price) {
            cart.push({item, price});
            updateCart();
            document.getElementById('cart').style.right = '0';
        }

        function updateCart() {
            const itemsDiv = document.getElementById('cart-items');
            itemsDiv.innerHTML = cart.map(item => 
                `<div>${item.item} - ${item.price} ₽</div>`
            ).join('');
            document.getElementById('total').textContent = 
                cart.reduce((sum, item) => sum + item.price, 0);
        }

        // Яндекс Карта
        ymaps.ready(initMap);
        function initMap() {
            const map = new ymaps.Map('map', {
                center: [55.76, 37.64],
                zoom: 15
            });
            map.geoObjects.add(new ymaps.Placemark([55.76, 37.64], {
                balloonContent: 'Наша кофейня'
            }));
        }

        // Бронирование
        function bookTable(e) {
            e.preventDefault();
            const formData = new FormData(e.target);
            // Здесь должна быть отправка данных на сервер
            alert('Столик успешно забронирован!');
            e.target.reset();
            return false;
        }

        // Закрытие корзины при клике вне области
        document.addEventListener('click', (e) => {
            if (!e.target.closest('#cart') && !e.target.closest('.add-to-cart')) {
                document.getElementById('cart').style.right = '-350px';
            }
        });
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Кофеини - Полная версия</title>
    <link rel="stylesheet" href="https://unpkg.com/scrollreveal@4.0.7/dist/scrollreveal.min.css">
    <style>
        /* ... предыдущие стили ... */

        /* Анимации */
        .reveal {
            opacity: 0;
            transform: translateY(20px);
            transition: 1s all ease;
        }
        
        /* Фильтры меню */
        .menu-filters {
            display: flex;
            gap: 10px;
            justify-content: center;
            margin: 20px 0;
        }
        
        .filter-btn {
            padding: 10px 20px;
            border: 1px solid #6f4e37;
            border-radius: 20px;
            cursor: pointer;
        }
        
        .filter-btn.active {
            background: #6f4e37;
            color: white;
        }

        /* Личный кабинет */
        .auth-section {
            max-width: 400px;
            margin: 50px auto;
            padding: 20px;
            background: white;
            border-radius: 10px;
        }

        /* Система лояльности */
        .loyalty-card {
            background: linear-gradient(45deg, #6f4e37, #b08a69);
            color: white;
            padding: 20px;
            border-radius: 15px;
            margin: 20px;
        }
    </style>
</head>
<body>
    <!-- ... предыдущая разметка ... -->

    <!-- Фильтры меню -->
    <div class="menu-filters">
        <button class="filter-btn active" data-filter="all">Все</button>
        <button class="filter-btn" data-filter="coffee">Кофе</button>
        <button class="filter-btn" data-filter="tea">Чай</button>
        <button class="filter-btn" data-filter="dessert">Десерты</button>
    </div>

    <!-- Личный кабинет -->
    <section class="auth-section" id="auth">
        <div id="auth-forms">
            <h2>Вход / Регистрация</h2>
            <form id="login-form">
                <input type="email" placeholder="Email" required>
                <input type="password" placeholder="Пароль" required>
                <button type="submit">Войти</button>
            </form>
            <button onclick="showRegistration()">Создать аккаунт</button>
        </div>

        <div id="user-profile" style="display: none;">
            <h2>Добро пожаловать, <span id="username"></span>!</h2>
            <div class="loyalty-card">
                <h3>Ваша карта лояльности</h3>
                <p>Баллы: <span id="loyalty-points">0</span></p>
                <p>Статус: <span id="loyalty-status">Новичок</span></p>
            </div>
            <button onclick="logout()">Выйти</button>
        </div>
    </section>

    <!-- Модальное окно оплаты -->
    <div id="payment-modal" class="modal">
        <div class="modal-content">
            <span class="close">&times;</span>
            <h2>Оплата заказа</h2>
            <div id="payment-form">
                <input type="text" placeholder="Номер карты" required>
                <input type="text" placeholder="Срок действия" required>
                <input type="text" placeholder="CVV" required>
                <button onclick="processPayment()">Оплатить</button>
            </div>
        </div>
    </div>

    <script src="https://unpkg.com/scrollreveal@4.0.7/dist/scrollreveal.min.js"></script>
    <script>
        // Анимации при скролле
        ScrollReveal().reveal('.reveal', {
            delay: 300,
            distance: '50px',
            origin: 'bottom',
            reset: true
        });

        // Фильтры меню
        document.querySelectorAll('.filter-btn').forEach(btn => {
            btn.addEventListener('click', function() {
                document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
                this.classList.add('active');
                
                const filter = this.dataset.filter;
                document.querySelectorAll('.menu-item').forEach(item => {
                    item.style.display = item.classList.contains(filter) || filter === 'all' 
                        ? 'block' 
                        : 'none';
                });
            });
        });

        // Система лояльности (пример)
        let user = {
            points: 0,
            orders: []
        };

        function updateLoyalty(points) {
            user.points += points;
            document.getElementById('loyalty-points').textContent = user.points;
            // Обновление статуса
            const status = user.points >= 100 ? 'Gold' : user.points >= 50 ? 'Silver' : 'Новичок';
            document.getElementById('loyalty-status').textContent = status;
        }

        // Личный кабинет
        function showRegistration() {
            document.getElementById('login-form').innerHTML = `
                <input type="text" placeholder="Имя" required>
                <input type="email" placeholder="Email" required>
                <input type="password" placeholder="Пароль" required>
                <button type="submit">Зарегистрироваться</button>
            `;
        }

        function logout() {
            document.getElementById('auth-forms').style.display = 'block';
            document.getElementById('user-profile').style.display = 'none';
        }

        // Онлайн-оплата (имитация)
        function checkout() {
            document.getElementById('payment-modal').style.display = 'block';
        }

        function processPayment() {
            alert('Оплата прошла успешно!');
            document.getElementById('payment-modal').style.display = 'none';
            cart = [];
            updateCart();
            updateLoyalty(cart.reduce((sum, item) => sum + item.price, 0) * 0.1);
        }

        // Push-уведомления (требует HTTPS и сервис воркера)
        if ('serviceWorker' in navigator && 'PushManager' in window) {
            navigator.serviceWorker.register('sw.js')
                .then(() => Notification.requestPermission());
        }
    </script>
</body>
</html>
self.addEventListener('push', event => {
    const data = event.data.json();
    self.registration.showNotification(data.title, {
        body: data.body,
        icon: '/icon.png'
    });
});
