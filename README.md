<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Transport Touristique Fès - Découvrez le Maroc</title>
    <style>
        /* Reset and Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f8f9fa;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* Header Styles */
        header {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1543832923-44667a44c804?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 100px 0;
            text-align: center;
        }
        
        .logo {
            font-size: 36px;
            font-weight: bold;
            margin-bottom: 20px;
            color: #f8c300;
        }
        
        .tagline {
            font-size: 20px;
            margin-bottom: 30px;
        }
        
        /* Navigation */
        nav {
            background-color: #2c3e50;
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
        }
        
        nav li {
            margin: 0 20px;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav a:hover {
            color: #f8c300;
        }
        
        /* Section Styles */
        section {
            padding: 60px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 40px;
            color: #2c3e50;
            font-size: 32px;
            position: relative;
        }
        
        .section-title:after {
            content: '';
            display: block;
            width: 80px;
            height: 3px;
            background: #f8c300;
            margin: 10px auto;
        }
        
        /* About Section */
        .about-content {
            display: flex;
            align-items: center;
            gap: 40px;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-image {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        /* Services Section */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .service-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
        }
        
        .service-image {
            height: 200px;
            overflow: hidden;
        }
        
        .service-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .service-card:hover .service-image img {
            transform: scale(1.1);
        }
        
        .service-info {
            padding: 20px;
        }
        
        .service-title {
            font-size: 20px;
            margin-bottom: 10px;
            color: #2c3e50;
        }
        
        /* Gallery Section */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 15px;
        }
        
        .gallery-item {
            border-radius: 10px;
            overflow: hidden;
            height: 250px;
            position: relative;
        }
        
        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .gallery-item:hover img {
            transform: scale(1.1);
        }
        
        .gallery-caption {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: rgba(0, 0, 0, 0.7);
            color: white;
            padding: 10px;
            text-align: center;
            transform: translateY(100%);
            transition: transform 0.3s;
        }
        
        .gallery-item:hover .gallery-caption {
            transform: translateY(0);
        }
        
        /* Contact Section */
        .contact-container {
            display: flex;
            gap: 40px;
        }
        
        .contact-info {
            flex: 1;
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .contact-details {
            margin-top: 20px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .contact-icon {
            width: 50px;
            height: 50px;
            background: #f8c300;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            color: white;
            font-size: 20px;
        }
        
        .contact-form {
            flex: 1;
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: 500;
        }
        
        .form-control {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
        }
        
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        .btn {
            background: #f8c300;
            color: white;
            border: none;
            padding: 12px 30px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            font-weight: 500;
            transition: background 0.3s;
        }
        
        .btn:hover {
            background: #e6b400;
        }
        
        /* Footer */
        footer {
            background: #2c3e50;
            color: white;
            padding: 40px 0;
            text-align: center;
        }
        
        .footer-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .footer-logo {
            font-size: 24px;
            font-weight: bold;
            color: #f8c300;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
        }
        
        .social-link {
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-decoration: none;
            transition: background 0.3s;
        }
        
        .social-link:hover {
            background: #f8c300;
        }
        
        .copyright {
            margin-top: 20px;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .about-content, .contact-container {
                flex-direction: column;
            }
            
            nav ul {
                flex-direction: column;
                align-items: center;
            }
            
            nav li {
                margin: 10px 0;
            }
            
            .footer-content {
                flex-direction: column;
                gap: 20px;
            }
            
            header {
                padding: 60px 0;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="logo">Transport Touristique Fès</div>
            <p class="tagline">Découvrez la beauté du Maroc avec notre service de transport de qualité</p>
            <a href="#contact" class="btn">Contactez-nous</a>
        </div>
    </header>

    <!-- Navigation -->
    <nav>
        <div class="container">
            <ul>
                <li><a href="#accueil">Accueil</a></li>
                <li><a href="#about">À propos</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#gallery">Galerie</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- About Section -->
    <section id="about">
        <div class="container">
            <h2 class="section-title">À propos de nous</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>Nous sommes une entreprise de transport touristique basée à Fès, au Maroc, spécialisée dans les voyages confortables et sécurisés vers les destinations les plus prisées du pays.</p>
                    <p>Avec des années d'expérience, nous offrons un service personnalisé pour répondre à tous vos besoins de voyage, que vous soyez un touriste individuel, un couple ou un groupe.</p>
                    <p>Notre flotte de véhicules modernes et nos chauffeurs professionnels vous garantissent une expérience de voyage exceptionnelle à travers le Maroc.</p>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1552733407-5d5c46c3bb3b?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Fès, Maroc">
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services">
        <div class="container">
            <h2 class="section-title">Nos Services</h2>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-image">
                        <img src="https://images.unsplash.com/photo-1597079550029-5d5c46c3bb3b?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Transferts aéroport">
                    </div>
                    <div class="service-info">
                        <h3 class="service-title">Transferts Aéroport</h3>
                        <p>Service de transfert depuis et vers l'Aéroport Fès-Saïss. Accueil personnalisé et ponctuel.</p>
                    </div>
                </div>
                <div class="service-card">
                    <div class="service-image">
                        <img src="https://images.unsplash.com/photo-1570077188670-e3a8d69ac5ff?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Excursions touristiques">
                    </div>
                    <div class="service-info">
                        <h3 class="service-title">Excursions Touristiques</h3>
                        <p>Découvrez les joyaux du Maroc avec nos excursions guidées vers les sites les plus emblématiques.</p>
                    </div>
                </div>
                <div class="service-card">
                    <div class="service-image">
                        <img src="https://images.unsplash.com/photo-1544620347-c4fd4a3d5957?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Transport de groupe">
                    </div>
                    <div class="service-info">
                        <h3 class="service-title">Transport de Groupe</h3>
                        <p>Véhicules spacieux et confortables pour les groupes, familles et voyages d'affaires.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section id="gallery">
        <div class="container">
            <h2 class="section-title">Destinations Populaires</h2>
            <div class="gallery-grid">
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1597079550029-5d5c46c3bb3b?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Aéroport Fès-Saïss">
                    <div class="gallery-caption">Aéroport Fès-Saïss</div>
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1552733407-5d5c46c3bb3b?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Ancienne Médina de Fès">
                    <div class="gallery-caption">Ancienne Médina de Fès</div>
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1570077188670-e3a8d69ac5ff?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Tanger">
                    <div class="gallery-caption">Tanger</div>
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1578632749014-ca77efd052eb?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Chefchaouen">
                    <div class="gallery-caption">Chefchaouen</div>
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1518548419970-58e3b4079ab2?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Marrakech">
                    <div class="gallery-caption">Marrakech</div>
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1593693397697-4c8b4e6b6c0b?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Sefrou">
                    <div class="gallery-caption">Sefrou</div>
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1578632749014-ca77efd052eb?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Ouarzazate">
                    <div class="gallery-caption">Ouarzazate</div>
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1570077188670-e3a8d69ac5ff?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Essaouira">
                    <div class="gallery-caption">Essaouira</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <h2 class="section-title">Contactez-nous</h2>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Nos Coordonnées</h3>
                    <div class="contact-details">
                        <div class="contact-item">
                            <div class="contact-icon">📞</div>
                            <div>
                                <h4>Téléphone</h4>
                                <p>0602411130</p>
                            </div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">✉️</div>
                            <div>
                                <h4>Email</h4>
                                <p>tahahmidouch@gmail.com</p>
                            </div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">📍</div>
                            <div>
                                <h4>Adresse</h4>
                                <p>Fès, Maroc</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="contact-form">
                    <h3>Envoyez-nous un message</h3>
                    <form>
                        <div class="form-group">
                            <label for="name">Nom complet</label>
                            <input type="text" id="name" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="phone">Téléphone</label>
                            <input type="tel" id="phone" class="form-control">
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" class="form-control" required></textarea>
                        </div>
                        <button type="submit" class="btn">Envoyer le message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-logo">Transport Touristique Fès</div>
                <div class="social-links">
                    <a href="#" class="social-link">f</a>
                    <a href="#" class="social-link">in</a>
                    <a href="#" class="social-link">ig</a>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Transport Touristique Fès. Tous droits réservés.</p>
            </div>
        </div>
    </footer>

    <script>
        // Simple form submission handler
        document.querySelector('form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Merci pour votre message! Nous vous contacterons bientôt.');
            this.reset();
        });
        
        // Smooth scrolling for navigation links
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                document.querySelector(targetId).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
