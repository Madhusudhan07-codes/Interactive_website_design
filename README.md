<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cognifyz - Where Data Meets Intelligence</title>
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css">
    <style>
        :root {
            --primary: #3a86ff;
            --secondary: #8338ec;
            --dark: #212529;
            --light: #f8f9fa;
            --success: #06d6a0;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--light);
            color: var(--dark);
            transition: background-color 0.5s ease;
        }
        
        .hero {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 5rem 0;
            text-align: center;
            margin-bottom: 3rem;
            border-radius: 0 0 20px 20px;
        }
        
        .features {
            padding: 4rem 0;
        }
        
        .feature-card {
            background: white;
            border-radius: 10px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            margin-bottom: 2rem;
            transition: transform 0.3s ease;
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
        }
        
        .feature-icon {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }
        
        .btn-cognifyz {
            background: var(--primary);
            color: white;
            padding: 0.8rem 2rem;
            border-radius: 50px;
            font-weight: 600;
            border: none;
            transition: all 0.3s ease;
        }
        
        .btn-cognifyz:hover {
            background: var(--secondary);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        
        #apiDataContainer {
            margin-top: 2rem;
        }
        
        .post-card {
            background: white;
            padding: 1.5rem;
            border-radius: 10px;
            margin-bottom: 1rem;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
        }
        
        footer {
            background: var(--dark);
            color: white;
            padding: 3rem 0;
            margin-top: 3rem;
        }
        
        .form-container {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        @media (max-width: 768px) {
            .hero {
                padding: 3rem 0;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container">
            <a class="navbar-brand" href="#">Cognifyz</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link active" href="#">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#features">Features</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#contact">Contact</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h1 class="display-4 mb-4">Where Data Meets Intelligence</h1>
            <p class="lead mb-4">Transform your business with our cutting-edge AI solutions</p>
            <button id="colorChanger" class="btn btn-cognifyz">Try Dynamic Mode</button>
        </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="features">
        <div class="container">
            <div class="row">
                <div class="col-md-4">
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-brain"></i>
                        </div>
                        <h3>AI-Powered Insights</h3>
                        <p>Leverage advanced machine learning algorithms to uncover hidden patterns in your data.</p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-chart-line"></i>
                        </div>
                        <h3>Real-Time Analytics</h3>
                        <p>Get actionable insights with our real-time data processing capabilities.</p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-shield-alt"></i>
                        </div>
                        <h3>Secure & Scalable</h3>
                        <p>Enterprise-grade security with seamless scalability to handle your growing data needs.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- API Demo Section -->
    <section class="api-demo py-5 bg-light">
        <div class="container">
            <h2 class="text-center mb-4">API Integration Demo</h2>
            <button id="fetchData" class="btn btn-cognifyz d-block mx-auto">Load Sample Posts</button>
            <div id="apiDataContainer" class="row"></div>
        </div>
    </section>

    <!-- Contact Form Section -->
    <section id="contact" class="contact py-5">
        <div class="container">
            <h2 class="text-center mb-5">Get In Touch</h2>
            <div class="row justify-content-center">
                <div class="col-md-8">
                    <div class="form-container">
                        <form id="contactForm" novalidate>
                            <div class="mb-3">
                                <label for="name" class="form-label">Name</label>
                                <input type="text" class="form-control" id="name" required>
                                <div class="invalid-feedback">
                                    Please provide your name.
                                </div>
                            </div>
                            <div class="mb-3">
                                <label for="email" class="form-label">Email</label>
                                <input type="email" class="form-control" id="email" required>
                                <div class="invalid-feedback">
                                    Please provide a valid email.
                                </div>
                            </div>
                            <div class="mb-3">
                                <label for="message" class="form-label">Message</label>
                                <textarea class="form-control" id="message" rows="3" required></textarea>
                                <div class="invalid-feedback">
                                    Please enter your message.
                                </div>
                            </div>
                            <button type="submit" class="btn btn-cognifyz">Submit</button>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container text-center">
            <p>&copy; 2023 Cognifyz. All rights reserved.</p>
            <div class="social-links mt-3">
                <a href="#" class="text-light mx-2"><i class="fab fa-facebook-f"></i></a>
                <a href="#" class="text-light mx-2"><i class="fab fa-twitter"></i></a>
                <a href="#" class="text-light mx-2"><i class="fab fa-linkedin-in"></i></a>
                <a href="#" class="text-light mx-2"><i class="fab fa-github"></i></a>
            </div>
        </div>
    </footer>

    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
    
    <!-- Custom JavaScript -->
    <script>
        // Task 4: Interactive Button
        document.getElementById('colorChanger').addEventListener('click', function() {
            document.body.classList.toggle('dark-mode');
            document.body.style.backgroundColor = document.body.classList.contains('dark-mode') ? '#212529' : '#f8f9fa';
            document.body.style.color = document.body.classList.contains('dark-mode') ? '#ffffff' : '#212529';
            
            // Change button text based on current mode
            this.textContent = document.body.classList.contains('dark-mode') 
                ? 'Light Mode' 
                : 'Dark Mode';
        });
        
        // Task 5: API Integration
        document.getElementById('fetchData').addEventListener('click', function() {
            const container = document.getElementById('apiDataContainer');
            container.innerHTML = '<div class="text-center"><div class="spinner-border text-primary" role="status"></div></div>';
            
            fetch('https://jsonplaceholder.typicode.com/posts?_limit=3')
                .then(response => response.json())
                .then(data => {
                    container.innerHTML = '';
                    data.forEach(post => {
                        const postElement = document.createElement('div');
                        postElement.className = 'col-md-4 mb-4';
                        postElement.innerHTML = `
                            <div class="post-card">
                                <h4>${post.title}</h4>
                                <p>${post.body.substring(0, 100)}...</p>
                            </div>
                        `;
                        container.appendChild(postElement);
                    });
                })
                .catch(error => {
                    container.innerHTML = `<div class="alert alert-danger">Error loading data: ${error.message}</div>`;
                });
        });
        
        // Task 6: Form Validation
        document.getElementById('contactForm').addEventListener('submit', function(event) {
            event.preventDefault();
            event.stopPropagation();
            
            const form = event.target;
            if (form.checkValidity()) {
                // Form is valid - you would normally send this data to a server
                alert('Thank you for your message! We will get back to you soon.');
                form.reset();
                form.classList.remove('was-validated');
            } else {
                form.classList.add('was-validated');
            }
        }, false);
    </script>
</body>
</html>
