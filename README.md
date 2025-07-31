* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
  background-color: #f9f7f4;
  color: #333;
  line-height: 1.6;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}

header {
  background: linear-gradient(135deg, #8B4513, #D2691E);
  color: white;
  padding: 20px 0;
  text-align: center;
  border-radius: 10px;
  margin-bottom: 30px;
}

header h1 {
  font-size: 2.5rem;
}

nav {
  background-color: #fff;
  padding: 15px 0;
  text-align: center;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  margin-bottom: 30px;
  border-radius: 8px;
}

nav a {
  margin: 0 15px;
  text-decoration: none;
  color: #8B4513;
  font-weight: bold;
  font-size: 1.1rem;
  transition: color 0.3s;
}

nav a:hover {
  color: #D2691E;
}

.section-title {
  text-align: center;
  font-size: 2rem;
  margin: 40px 0 20px;
  color: #8B4513;
}

/* Каталог товаров */
.products {
  display: flex;
  flex-wrap: wrap;
  gap: 25px;
  justify-content: center;
}

.product {
  background: white;
  border-radius: 12px;
  overflow: hidden;
  width: 280px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
  transition: transform 0.3s ease;
}

.product:hover {
  transform: translateY(-5px);
}

.product img, .product video {
  width: 100%;
  height: 280px;
  object-fit: cover;
}

.product .info {
  padding: 15px;
  text-align: center;
}

.product .info h3 {
  font-size: 1.3rem;
  color: #555;
  margin-bottom: 8px;
}

.product .info .price {
  font-weight: bold;
  color: #8B4513;
  font-size: 1.2rem;
  margin: 5px 0;
}

.product .info p {
  color: #777;
  font-size: 0.95rem;
}

/* Форма заказа */
.form-container {
  max-width: 600px;
  margin: 40px auto;
  padding: 30px;
  background: white;
  border-radius: 12px;
  box-shadow: 0 4px 15px rgba(0,0,0,0.1);
}

.form-container h2 {
  text-align: center;
  color: #8B4513;
  margin-bottom: 20px;
}

.form-container label {
  display: block;
  margin: 12px 0 6px;
  font-weight: bold;
  color: #555;
}

.form-container input,
.form-container textarea,
.form-container select {
  width: 100%;
  padding: 10px;
  margin-bottom: 15px;
  border: 1px solid #ddd;
  border-radius: 6px;
  font-size: 1rem;
}

.form-container button {
  background-color: #8B4513;
  color: white;
  border: none;
  padding: 14px 25px;
  font-size: 1.1rem;
  border-radius: 8px;
  cursor: pointer;
  width: 100%;
  font-weight: bold;
}

.form-container button:hover {
  background-color: #A0522D;
}

/* Контакты */
.contact-buttons {
  display: flex;
  justify-content: center;
  gap: 20px;
  margin: 30px 0;
  flex-wrap: wrap;
}

.btn {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  padding: 14px 25px;
  font-size: 1.1rem;
  font-weight: bold;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  text-decoration: none;
}

.btn-whatsapp {
  background-color: #25D366;
  color: white;
}

.btn-whatsapp:hover {
  background-color: #128C7E;
}

.btn-telegram {
  background-color: #0088cc;
  color: white;
}

.btn-telegram:hover {
  background-color: #006699;
}

footer {
  text-align: center;
  padding: 30px;
  margin-top: 50px;
  background-color: #fff;
  border-radius: 10px;
  color: #777;
  font-size: 0.9rem;
  box-shadow: 0 2px 8px rgba(0,0,0,0.05);
}

footer a {
  color: #8B4513;
  text-decoration: none;
}

/* Адаптивность */
@media (max-width: 768px) {
  header h1 {
    font-size: 2rem;
  }
  nav a {
    margin: 0 10px;
    font-size: 1rem;
  }
  .product {
    width: 100%;
  }
}