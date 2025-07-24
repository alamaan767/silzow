# silzow
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Silzow - Leading Innovation in Technology and Design</title>
    <meta name="description" content="Leading innovation in technology and design. We create solutions that transform businesses and empower growth.">
    <meta name="author" content="Silzow">
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <style>
        /* CSS Variables - Design System */
        :root {
            --background: 0 0% 100%;
            --foreground: 222.2 84% 4.9%;
            --card: 0 0% 100%;
            --card-foreground: 222.2 84% 4.9%;
            --primary: 222.2 47.4% 11.2%;
            --primary-foreground: 210 40% 98%;
            --secondary: 210 40% 96.1%;
            --secondary-foreground: 222.2 47.4% 11.2%;
            --muted: 210 40% 96.1%;
            --muted-foreground: 215.4 16.3% 46.9%;
            --accent: 210 40% 96.1%;
            --accent-foreground: 222.2 47.4% 11.2%;
            --border: 214.3 31.8% 91.4%;
            --input: 214.3 31.8% 91.4%;
            --ring: 222.2 84% 4.9%;
            --radius: 0.5rem;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            line-height: 1.6;
            color: hsl(var(--foreground));
            background-color: hsl(var(--background));
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1rem;
        }

        /* Header Styles */
        .header {
            position: sticky;
            top: 0;
            z-index: 50;
            width: 100%;
            border-bottom: 1px solid hsl(var(--border));
            background: hsl(var(--background) / 0.95);
            backdrop-filter: blur(8px);
        }

        .nav-container {
            display: flex;
            height: 4rem;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: hsl(var(--primary));
            text-decoration: none;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 0.25rem;
        }

        .nav-link {
            display: inline-flex;
            height: 2.5rem;
            align-items: center;
            justify-content: center;
            padding: 0 1rem;
            font-size: 0.875rem;
            font-weight: 500;
            color: hsl(var(--foreground));
            text-decoration: none;
            border-radius: var(--radius);
            transition: all 0.2s;
        }

        .nav-link:hover {
            background-color: hsl(var(--accent));
            color: hsl(var(--accent-foreground));
        }

        /* Button Styles */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
            white-space: nowrap;
            border-radius: var(--radius);
            font-size: 0.875rem;
            font-weight: 500;
            text-decoration: none;
            transition: all 0.2s;
            cursor: pointer;
            border: none;
            outline: none;
        }

        .btn:focus-visible {
            outline: 2px solid hsl(var(--ring));
            outline-offset: 2px;
        }

        .btn-primary {
            background-color: hsl(var(--primary));
            color: hsl(var(--primary-foreground));
            padding: 0.5rem 1rem;
            height: 2.5rem;
        }

        .btn-primary:hover {
            background-color: hsl(var(--primary) / 0.9);
        }

        .btn-outline {
            border: 1px solid hsl(var(--input));
            background-color: hsl(var(--background));
            color: hsl(var(--foreground));
            padding: 0.5rem 1rem;
            height: 2.5rem;
        }

        .btn-outline:hover {
            background-color: hsl(var(--accent));
            color: hsl(var(--accent-foreground));
        }

        .btn-lg {
            height: 2.75rem;
            padding: 0 2rem;
            font-size: 1.125rem;
        }

        .btn-sm {
            height: 2.25rem;
            padding: 0 0.75rem;
            border-radius: calc(var(--radius) - 2px);
        }

        /* Hero Section */
        .hero {
            position: relative;
            padding: 5rem 1rem;
            text-align: center;
        }

        .hero h1 {
            font-size: 3.75rem;
            font-weight: 700;
            margin-bottom: 1.5rem;
            color: hsl(var(--primary));
            line-height: 1.1;
        }

        .hero p {
            font-size: 1.25rem;
            color: hsl(var(--muted-foreground));
            margin-bottom: 2rem;
            max-width: 42rem;
            margin-left: auto;
            margin-right: auto;
        }

        .hero-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        /* Features Section */
        .features {
            padding: 4rem 1rem;
            background-color: hsl(var(--muted) / 0.3);
        }

        .features h2 {
            font-size: 2.5rem;
            font-weight: 700;
            text-align: center;
            margin-bottom: 3rem;
            color: hsl(var(--primary));
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        /* Card Styles */
        .card {
            background-color: hsl(var(--card));
            color: hsl(var(--card-foreground));
            border: 1px solid hsl(var(--border));
            border-radius: calc(var(--radius) + 2px);
            box-shadow: 0 1px 3px 0 rgb(0 0 0 / 0.1), 0 1px 2px -1px rgb(0 0 0 / 0.1);
            text-align: center;
        }

        .card-header {
            padding: 1.5rem 1.5rem 0;
        }

        .card-title {
            font-size: 1.5rem;
            font-weight: 600;
            line-height: 1;
            margin-bottom: 0.5rem;
        }

        .card-description {
            color: hsl(var(--muted-foreground));
            font-size: 0.875rem;
        }

        .card-content {
            padding: 1.5rem;
        }

        .card-content p {
            color: hsl(var(--muted-foreground));
        }

        /* Footer */
        .footer {
            padding: 2rem 1rem;
            border-top: 1px solid hsl(var(--border));
            text-align: center;
        }

        .footer p {
            color: hsl(var(--muted-foreground));
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
                font-size: 1rem;
            }

            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }

            .features h2 {
                font-size: 2rem;
            }

            .features-grid {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 640px) {
            .hero {
                padding: 3rem 1rem;
            }

            .features {
                padding: 3rem 1rem;
            }

            .hero h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <div class="container">
            <div class="nav-container">
                <a href="#" class="logo">Silzow</a>
                
                <nav>
                    <ul class="nav-menu">
                        <li><a href="#" class="nav-link">Home</a></li>
                        <li><a href="#" class="nav-link">Source</a></li>
                        <li><a href="#" class="nav-link">About Us</a></li>
                    </ul>
                </nav>

                <a href="#contact" class="btn btn-outline btn-sm">Contact</a>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h1>Welcome to Silzow</h1>
            <p>Leading innovation in technology and design. We create solutions that transform businesses and empower growth.</p>
            <div class="hero-buttons">
                <a href="#" class="btn btn-primary btn-lg">Get Started</a>
                <a href="#" class="btn btn-outline btn-lg">Learn More</a>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features">
        <div class="container">
            <h2>Our Services</h2>
            <div class="features-grid">
                <div class="card">
                    <div class="card-header">
                        <h3 class="card-title">Innovation</h3>
                        <p class="card-description">Cutting-edge solutions tailored to your needs</p>
                    </div>
                    <div class="card-content">
                        <p>We bring fresh perspectives and innovative approaches to solve complex challenges.</p>
                    </div>
                </div>

                <div class="card">
                    <div class="card-header">
                        <h3 class="card-title">Quality</h3>
                        <p class="card-description">Excellence in every project we deliver</p>
                    </div>
                    <div class="card-content">
                        <p>Our commitment to quality ensures that every solution meets the highest standards.</p>
                    </div>
                </div>

                <div class="card">
                    <div class="card-header">
                        <h3 class="card-title">Support</h3>
                        <p class="card-description">Dedicated support throughout your journey</p>
                    </div>
                    <div class="card-content">
                        <p>Our team is always ready to assist and ensure your success with our solutions.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <p>&copy; 2024 Silzow. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
