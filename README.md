<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CYJ Construcciones - Servicios Profesionales en Construcción</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #ffffff;
        }

        /* Header */
        .header {
            background: linear-gradient(135deg, #ff6600, #ff8533);
            color: white;
            padding: 1rem 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 20px;
        }

        .logo {
            display: flex;
            align-items: center;
            font-size: 1.5rem;
            font-weight: bold;
        }

        .logo-icon img{
            width: 50px;
            height: 50px;
            background: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            color: #ff6600;
            font-weight: bold;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-menu a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: opacity 0.3s;
        }

        .nav-menu a:hover {
            opacity: 0.8;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 600"><rect width="1200" height="600" fill="%23f5f5f5"/><path d="M100 200h200v200h-200z" fill="%23ff6600" opacity="0.1"/><path d="M400 150h300v250h-300z" fill="%23333" opacity="0.1"/><path d="M800 180h250v180h-250z" fill="%23ff6600" opacity="0.1"/></svg>');
            background-size: cover;
            background-position: center;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            margin-top: 80px;
        }

        .hero-content {
            max-width: 800px;
            padding: 0 20px;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            font-weight: bold;
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .cta-button {
            background: #ff6600;
            color: white;
            padding: 15px 40px;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1.1rem;
            transition: all 0.3s;
            display: inline-block;
        }

        .cta-button:hover {
            background: #e55a00;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(255,102,0,0.3);
        }

        /* Main Content */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            color: #333;
        }

        .section-title p {
            font-size: 1.2rem;
            color: #666;
            max-width: 600px;
            margin: 0 auto;
        }

        /* Services Grid */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }

        .service-card {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
            border-left: 4px solid #ff6600;
        }

        .service-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
        }

        .service-card h3 {
            color: #ff6600;
            margin-bottom: 15px;
            font-size: 1.3rem;
        }

        .service-card ul {
            list-style: none;
            color: #666;
        }

        .service-card li {
            padding: 5px 0;
            position: relative;
            padding-left: 20px;
        }

        .service-card li:before {
            content: "▶";
            color: #ff6600;
            position: absolute;
            left: 0;
            font-size: 0.8rem;
        }

        /* Product Technical Sheet */
        .product-section {
            background: #f8f9fa;
        }

        .product-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
            margin-top: 50px;
        }

        .product-specs {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
        }

        .spec-table {
            width: 100%;
            border-collapse: collapse;
            margin-bottom: 30px;
        }

        .spec-table th,
        .spec-table td {
            padding: 12px;
            text-align: left;
            border-bottom: 1px solid #eee;
        }

        .spec-table th {
            background: #ff6600;
            color: white;
            font-weight: bold;
        }

        .benefits-list {
            list-style: none;
        }

        .benefits-list li {
            padding: 8px 0;
            position: relative;
            padding-left: 25px;
            color: #666;
        }

        .benefits-list li:before {
            content: "✓";
            color: #ff6600;
            font-weight: bold;
            position: absolute;
            left: 0;
        }

        .product-diagram {
            text-align: center;
        }

        .diagram-box {
            background: white;
            border: 2px solid #ff6600;
            border-radius: 10px;
            padding: 30px;
            margin: 20px 0;
            display: inline-block;
        }

        /* Contact Section */
        .contact-section {
            background: #333;
            color: white;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            margin-top: 50px;
        }

        .contact-info {
            background: rgba(255,102,0,0.1);
            padding: 30px;
            border-radius: 10px;
            border: 1px solid #ff6600;
        }

        .contact-info h3 {
            color: #ff6600;
            margin-bottom: 20px;
            font-size: 1.3rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
            padding: 10px 0;
        }

        .contact-icon {
            width: 40px;
            height: 40px;
            background: #ff6600;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            color: white;
            font-weight: bold;
        }

        /* Footer */
        .footer {
            background: #222;
            color: white;
            text-align: center;
            padding: 30px 0;
        }

        .footer-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .social-links {
            display: flex;
            gap: 15px;
        }

        .social-links a {
            width: 40px;
            height: 40px;
            background: #ff6600;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-decoration: none;
            transition: background 0.3s;
        }

        .social-links a:hover {
            background: #e55a00;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-menu {
                display: none;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .hero p {
                font-size: 1.1rem;
            }

            .product-grid {
                grid-template-columns: 1fr;
                gap: 30px;
            }

            .contact-grid {
                grid-template-columns: 1fr;
            }

            .footer-content {
                flex-direction: column;
                gap: 20px;
            }

            .section-title h2 {
                font-size: 2rem;
            }
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .fade-in {
            animation: fadeInUp 0.6s ease-out;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <div class="nav-container">
            <div class="logo">
                <div class="logo-icon"><img src="172887726165653384.jpg" alt=""></div>
                <span>CYJ CONSTRUCCIONES</span>
            </div>
            <nav>
                <ul class="nav-menu">
                    <li><a href="#inicio">Inicio</a></li>
                    <li><a href="#servicios">Servicios</a></li>
                    <li><a href="#productos">Productos</a></li>
                    <li><a href="#contacto">Contacto</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="inicio">
        <div class="hero-content fade-in">
            <h1>CYJ CONSTRUCCIONES</h1>
            <p>Remodelación y Renovación - Servicios Profesionales en Construcción</p>
            <a href="#contacto" class="cta-button">Solicitar Cotización</a>
        </div>
    </section>

    <!-- Services Section -->
    <section class="section" id="servicios">
        <div class="container">
            <div class="section-title">
                <h2>Nuestros Servicios</h2>
                <p>Ofrecemos servicios integrales de construcción con la más alta calidad y profesionalismo</p>
            </div>
            
            <div class="services-grid">
                <div class="service-card">
                    <h3>Construcción General</h3>
                    <ul>
                        <li>Construcción General</li>
                        <li>Topografía y Planos</li>
                        <li>Diseño Arquitectónico</li>
                        <li>Acabados, Pisos, Pared</li>
                        <li>Pintura y Gasfitería en General</li>
                    </ul>
                </div>

                <div class="service-card">
                    <h3>Servicios Especializados</h3>
                    <ul>
                        <li>Electricidad General</li>
                        <li>Aire Acondicionado</li>
                        <li>Cámaras de Vigilancia</li>
                        <li>Alquiler Maquinarias Pesada</li>
                        <li>Alcantarillado, Pistas y Veredas</li>
                    </ul>
                </div>

                <div class="service-card">
                    <h3>Estructuras y Materiales</h3>
                    <ul>
                        <li>Cercos Prefabricados de Concreto</li>
                        <li>Fabricación de Moldes y Mesa Vibradora</li>
                        <li>Estructura Metálica Maderas y Melamina</li>
                        <li>Compra y Venta de Terrenos</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Product Section -->
    <section class="section product-section" id="productos">
        <div class="container">
            <div class="section-title">
                <h2>Ficha Técnica de Productos</h2>
                <p>Especificaciones técnicas de nuestros productos especializados</p>
            </div>

            <div class="product-grid">
                <div class="product-specs">
                    <h3 style="color: #ff6600; margin-bottom: 20px;">Especificaciones Técnicas</h3>
                    
                    <table class="spec-table">
                        <thead>
                            <tr>
                                <th>PRODUCTO</th>
                                <th>MODELO</th>
                                <th>MEDIDA</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>Centrales Esquineros</td>
                                <td>CENTRALES ESQUINEROS</td>
                                <td>0.14M X 0.14M X 3.20M DE ALTO</td>
                            </tr>
                            <tr>
                                <td>Ladrillos</td>
                                <td>LAJA PIEDRECILLAS LISO</td>
                                <td>0.42M X 2.00M X 0.036M DE ESPESOR</td>
                            </tr>
                        </tbody>
                    </table>

                    <h4 style="color: #ff6600; margin: 20px 0 10px 0;">Beneficios</h4>
                    <ul class="benefits-list">
                        <li><strong>Rápida instalación:</strong> Montaje sencillo en obra</li>
                        <li><strong>Alta durabilidad:</strong> Materiales resistentes a la corrosión</li>
                        <li><strong>Mantenimiento mínimo:</strong> No requiere tratamientos adicionales</li>
                    </ul>

                    <h4 style="color: #ff6600; margin: 20px 0 10px 0;">Ventajas</h4>
                    <ul class="benefits-list">
                        <li><strong>Ahorro de tiempo:</strong> Se ensambla en menos de 2 horas por módulo</li>
                        <li><strong>Costos optimizados:</strong> Mejor relación costo-beneficio frente a muros tradicionales</li>
                        <li><strong>Seguridad estructural:</strong> Cumple norma PER-CIRS-2020 para carga sísmica</li>
                    </ul>
                </div>

                <div class="product-diagram">
                    <h3 style="color: #ff6600; margin-bottom: 20px;">Diagrama del Producto</h3>
                    <div class="diagram-box">
                        <div style="font-size: 1.1rem; margin-bottom: 15px; font-weight: bold;">Dimensiones del Módulo</div>
                        <div style="border: 2px solid #ff6600; padding: 20px; margin: 10px; position: relative;">
                            <div style="position: absolute; top: -15px; left: 50%; transform: translateX(-50%); background: white; padding: 0 10px; color: #ff6600; font-weight: bold;">3 mt</div>
                            <div style="position: absolute; right: -25px; top: 50%; transform: translateY(-50%); background: white; padding: 5px; color: #ff6600; font-weight: bold; writing-mode: vertical-rl;">2.52 mt</div>
                            <div style="position: absolute; bottom: -40px; left: 50%; transform: translateX(-50%); background: white; padding: 0 10px; color: #ff6600; font-weight: bold;">2 mt</div>
                            <div style="position: absolute; left: -30px; bottom: -10px; background: white; padding: 5px; color: #ff6600; font-weight: bold;">70 cm</div>
                            <div style="height: 150px; background: linear-gradient(45deg, #f0f0f0 25%, transparent 25%), linear-gradient(-45deg, #f0f0f0 25%, transparent 25%), linear-gradient(45deg, transparent 75%, #f0f0f0 75%), linear-gradient(-45deg, transparent 75%, #f0f0f0 75%); background-size: 20px 20px; background-position: 0 0, 0 10px, 10px -10px, -10px 0px; border: 1px solid #ccc;"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="section contact-section" id="contacto">
        <div class="container">
            <div class="section-title">
                <h2>Contáctanos</h2>
                <p>Estamos listos para hacer realidad tu proyecto de construcción</p>
            </div>

            <div class="contact-grid">
                <div class="contact-info">
                    <h3>Información de Contacto</h3>
                    <div class="contact-item">
                        <div class="contact-icon">📱</div>
                        <div>
                            <strong>Teléfonos:</strong><br>
                            930 643 975 / 912 976 870<br>
                            973 886 850 - 912 976 870
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">✉️</div>
                        <div>
                            <strong>Email:</strong><br>
                            cyjconstrucciones393@gmail.com
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">📍</div>
                        <div>
                            <strong>Dirección:</strong><br>
                            Av. Mariscal Benavides N° 1431<br>
                            Cercado Chincha Alta
                        </div>
                    </div>
                </div>

                <div class="contact-info">
                    <h3>Información del Propietario</h3>
                    <div class="contact-item">
                        <div class="contact-icon">👤</div>
                        <div>
                            <strong>Propietario:</strong><br>
                            Carlos J. Castilla CH
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">🆔</div>
                        <div>
                            <strong>RUC:</strong><br>
                            10453766123
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">🏢</div>
                        <div>
                            <strong>Oficina:</strong><br>
                            Panamericana Sur km 199 #1184 oficina
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">✅</div>
                        <div>
                            <strong>Certificación:</strong><br>
                            Registro Nacional de Proveedores del Estado
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="footer-content">
            <div>
                <p>&copy; 2025 CYJ Construcciones. Todos los derechos reservados.</p>
            </div>
            <div class="social-links">
                <a href="#" title="Facebook">f</a>
                <a href="#" title="TikTok">T</a>
                <a href="#" title="Instagram">📷</a>
            </div>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
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

        // Add fade-in animation to elements when they come into view
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('fade-in');
                }
            });
        }, observerOptions);

        // Observe service cards and other elements
        document.querySelectorAll('.service-card, .product-specs, .contact-info').forEach(el => {
            observer.observe(el);
        });
    </script>
</body>
</html>
