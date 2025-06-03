<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EYECAB International University | The Future of Higher Education</title>
    <meta name="description" content="World-class education with innovative programs at EYECAB International University">
    <meta property="og:title" content="EYECAB International University">
    <meta property="og:image" content="https://example.com/uni-social-preview.jpg">
    
    <!-- Preload Optimizations -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link rel="preload" href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Raleway:wght@300;400;600&display=swap" as="style">
    <link rel="preload" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" as="style">
    <link rel="preload" href="https://maps.googleapis.com/maps/api/js?key=YOUR_KEY&callback=initMap" as="script">
    <link rel="preload" href="https://cdn.jsdelivr.net/npm/panolens@0.11.0/build/panolens.min.js" as="script">
    
    <!-- Fonts and Icons -->
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Raleway:wght@300;400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    
    <style>
        :root {
            --primary: #0A2463;
            --secondary: #3E92CC;
            --accent: #FFD700;
            --light: #FFF9F0;
            --dark: #1A1A1A;
            --success: #28a745;
            --info: #17a2b8;
            --font-heading: 'Playfair Display', serif;
            --font-body: 'Raleway', sans-serif;
            --accent-rgb: 255, 215, 0;
            --primary-rgb: 10, 36, 99;
            --background: var(--light);
            --text-color: var(--dark);
            --card-bg: white;
            --header-bg: rgba(10, 36, 99, 0.95);
        }
        
        /* Dark Mode Variables */
        .dark-theme {
            --bg-dark: #121212;
            --text-dark: #f0f0f0;
            --card-dark: #1e1e1e;
            
            --background: var(--bg-dark);
            --text-color: var(--text-dark);
            --card-bg: var(--card-dark);
            --header-bg: rgba(30, 30, 30, 0.9);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: var(--font-body);
            line-height: 1.8;
            color: var(--text-color);
            background-color: var(--background);
            overflow-x: hidden;
            transition: background-color 0.3s ease, color 0.3s ease;
        }
        
        .container {
            width: 90%;
            max-width: 1400px;
            margin: 0 auto;
        }
        
        /* Header Styles */
        header {
            background-color: var(--header-bg);
            color: white;
            padding: 1.5rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            transition: all 0.3s ease;
            box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
            backdrop-filter: blur(8px);
        }
        
        header.scrolled {
            padding: 1rem 0;
            background-color: rgba(var(--primary-rgb), 0.98);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            text-decoration: none;
        }
        
        .logo-icon {
            font-size: 2.5rem;
            color: var(--accent);
            margin-right: 15px;
        }
        
        .logo-text {
            font-family: var(--font-heading);
        }
        
        .logo-text h1 {
            font-size: 1.8rem;
            font-weight: 700;
            line-height: 1.2;
            color: white;
        }
        
        .logo-text p {
            font-size: 0.7rem;
            letter-spacing: 2px;
            text-transform: uppercase;
            opacity: 0.8;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 2rem;
            position: relative;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 600;
            font-size: 1rem;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            padding: 0.5rem 0;
            position: relative;
        }
        
        nav ul li a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--accent);
            transition: width 0.3s ease;
        }
        
        nav ul li a:hover::after {
            width: 100%;
        }
        
        nav ul li a.active {
            color: var(--accent);
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Theme Toggle */
        .theme-toggle {
            position: relative;
            width: 60px;
            height: 30px;
            border-radius: 30px;
            background: var(--card-bg);
            border: none;
            cursor: pointer;
            display: flex;
            align-items: center;
            padding: 0 5px;
            margin-left: 15px;
        }
        
        .theme-toggle i {
            font-size: 14px;
            padding: 0 5px;
            color: var(--text-color);
        }
        
        .toggle-ball {
            position: absolute;
            left: 5px;
            width: 22px;
            height: 22px;
            background: var(--accent);
            border-radius: 50%;
            transition: transform 0.3s ease;
        }
        
        .dark-theme .toggle-ball {
            transform: translateX(30px);
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            min-height: 800px;
            background: linear-gradient(rgba(10, 36, 99, 0.7), rgba(10, 36, 99, 0.7)), 
                        url('https://images.unsplash.com/photo-1522202176988-66273c2fd55f?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: white;
            display: flex;
            align-items: center;
            text-align: center;
            padding-top: 80px;
        }
        
        .hero-content {
            max-width: 900px;
            margin: 0 auto;
            padding: 0 2rem;
        }
        
        .hero h1 {
            font-family: var(--font-heading);
            font-size: 4rem;
            margin-bottom: 1.5rem;
            line-height: 1.2;
            text-shadow: 2px 2px 8px rgba(0,0,0,0.3);
            animation: fadeInUp 1s ease;
        }
        
        .hero p {
            font-size: 1.5rem;
            margin-bottom: 2.5rem;
            opacity: 0.9;
            animation: fadeInUp 1s ease 0.2s forwards;
            opacity: 0;
        }
        
        .hero-btns {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            animation: fadeInUp 1s ease 0.4s forwards;
            opacity: 0;
        }
        
        .btn {
            display: inline-block;
            padding: 1rem 2.5rem;
            border-radius: 50px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
            letter-spacing: 1px;
        }
        
        .btn-primary {
            background-color: var(--accent);
            color: var(--primary);
            box-shadow: 0 4px 15px rgba(255, 215, 0, 0.3);
        }
        
        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(255, 215, 0, 0.4);
        }
        
        .btn-outline {
            border: 2px solid white;
            color: white;
        }
        
        .btn-outline:hover {
            background-color: white;
            color: var(--primary);
            transform: translateY(-3px);
        }
        
        .btn-accent {
            background-color: var(--accent);
            color: var(--primary);
            font-weight: 600;
        }
        
        .btn-accent:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(255, 215, 0, 0.3);
        }
        
        /* About Section */
        .section {
            padding: 8rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 5rem;
        }
        
        .section-title h2 {
            font-family: var(--font-heading);
            font-size: 3rem;
            color: var(--primary);
            position: relative;
            display: inline-block;
            margin-bottom: 1.5rem;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background-color: var(--accent);
        }
        
        .section-title p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto;
            color: var(--text-color);
            opacity: 0.8;
        }
        
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }
        
        .about-text h3 {
            font-family: var(--font-heading);
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }
        
        .about-text p {
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
            line-height: 1.8;
        }
        
        .about-features {
            margin-top: 2rem;
        }
        
        .feature-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 1.5rem;
        }
        
        .feature-icon {
            font-size: 1.5rem;
            color: var(--accent);
            margin-right: 1rem;
            margin-top: 0.3rem;
        }
        
        .feature-text h4 {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
            color: var(--primary);
        }
        
        .about-image {
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 30px 60px rgba(10, 36, 99, 0.2);
            transform: rotate(-2deg);
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
            transition: transform 0.5s ease;
        }
        
        .about-image:hover img {
            transform: scale(1.05);
        }
        
        .about-image::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(10, 36, 99, 0.2), rgba(62, 146, 204, 0.2));
            z-index: 1;
        }
        
        /* Schools Section with Program Filter */
        .schools {
            background-color: var(--card-bg);
        }
        
        .program-filter {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-bottom: 3rem;
            flex-wrap: wrap;
        }
        
        .filter-btn {
            padding: 0.8rem 1.8rem;
            border-radius: 50px;
            background: transparent;
            border: 2px solid var(--accent);
            color: var(--text-color);
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .filter-btn.active {
            background: var(--accent);
            color: var(--primary);
        }
        
        .filter-btn:hover:not(.active) {
            background: rgba(var(--accent-rgb), 0.1);
        }
        
        .schools-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .school-card {
            background-color: var(--card-bg);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
            border: 1px solid rgba(var(--primary-rgb), 0.1);
        }
        
        .school-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.1);
        }
        
        .school-card-img {
            height: 200px;
            overflow: hidden;
        }
        
        .school-card-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .school-card:hover .school-card-img img {
            transform: scale(1.1);
        }
        
        .school-card-content {
            padding: 2rem;
        }
        
        .program-badge {
            display: inline-block;
            padding: 3px 10px;
            background: var(--accent);
            color: var(--primary);
            border-radius: 4px;
            font-size: 0.7rem;
            font-weight: 600;
            margin-bottom: 10px;
        }
        
        .school-card-content h3 {
            font-family: var(--font-heading);
            font-size: 1.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }
        
        .school-card-content p {
            margin-bottom: 1.5rem;
            color: var(--text-color);
            opacity: 0.8;
        }
        
        .school-card-link {
            display: inline-flex;
            align-items: center;
            color: var(--secondary);
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .school-card-link i {
            margin-left: 0.5rem;
            transition: transform 0.3s ease;
        }
        
        .school-card-link:hover {
            color: var(--primary);
        }
        
        .school-card-link:hover i {
            transform: translateX(5px);
        }
        
        /* Stats Section */
        .stats {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 6rem 0;
            text-align: center;
        }
        
        .stats-container {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 2rem;
        }
        
        .stat-item {
            padding: 2rem;
        }
        
        .stat-number {
            font-family: var(--font-heading);
            font-size: 3.5rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            color: var(--accent);
        }
        
        .stat-label {
            font-size: 1.2rem;
            letter-spacing: 1px;
            opacity: 0.9;
        }
        
        /* Testimonials */
        .testimonials {
            position: relative;
            padding: 8rem 0;
            background-color: var(--background);
        }
        
        .testimonial-slider {
            max-width: 1000px;
            margin: 0 auto;
            position: relative;
        }
        
        .testimonial-card {
            background-color: var(--card-bg);
            border-radius: 10px;
            padding: 3rem;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            text-align: center;
            margin: 0 1rem;
        }
        
        .testimonial-quote {
            font-size: 1.2rem;
            font-style: italic;
            color: var(--text-color);
            margin-bottom: 2rem;
            line-height: 1.8;
            position: relative;
        }
        
        .testimonial-quote::before,
        .testimonial-quote::after {
            content: '"';
            font-size: 3rem;
            color: var(--accent);
            opacity: 0.3;
            position: absolute;
        }
        
        .testimonial-quote::before {
            top: -20px;
            left: -15px;
        }
        
        .testimonial-quote::after {
            bottom: -40px;
            right: -15px;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .testimonial-author-img {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            overflow: hidden;
            margin-right: 1rem;
        }
        
        .testimonial-author-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .testimonial-author-info h4 {
            font-family: var(--font-heading);
            color: var(--primary);
            margin-bottom: 0.3rem;
        }
        
        .testimonial-author-info p {
            color: var(--text-color);
            opacity: 0.7;
            font-size: 0.9rem;
        }
        
        /* Virtual Tour Section */
        .virtual-tour {
            background-color: var(--card-bg);
        }
        
        .tour-container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .panorama-view {
            width: 100%;
            height: 500px;
            border-radius: 10px;
            overflow: hidden;
            margin-bottom: 20px;
            background-color: #eee;
        }
        
        .tour-hotspots {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
        }
        
        .hotspot {
            background: var(--card-bg);
            border: 2px solid var(--accent);
            padding: 10px 20px;
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.3s ease;
            color: var(--text-color);
            font-weight: 600;
        }
        
        .hotspot.active {
            background: var(--accent);
            color: var(--primary);
        }
        
        /* Tuition Calculator */
        .calculator {
            background-color: var(--background);
        }
        
        .calculator-card {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            background: var(--card-bg);
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            max-width: 1000px;
            margin: 0 auto;
        }
        
        .calculator-form {
            display: grid;
            gap: 20px;
        }
        
        .form-group {
            display: flex;
            flex-direction: column;
        }
        
        .form-group label {
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--primary);
        }
        
        .form-group select {
            padding: 12px 15px;
            border-radius: 8px;
            border: 1px solid rgba(var(--primary-rgb), 0.2);
            background-color: var(--card-bg);
            <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EYECAB International University | The Future of Higher Education</title>
    <meta name="description" content="World-class education with innovative programs at EYECAB International University">
    <meta property="og:title" content="EYECAB International University">
    <meta property="og:image" content="https://example.com/uni-social-preview.jpg">
    
    <!-- Preload Optimizations -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link rel="preload" href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Raleway:wght@300;400;600&display=swap" as="style">
    <link rel="preload" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" as="style">
    <link rel="preload" href="https://maps.googleapis.com/maps/api/js?key=YOUR_KEY&callback=initMap" as="script">
    <link rel="preload" href="https://cdn.jsdelivr.net/npm/panolens@0.11.0/build/panolens.min.js" as="script">
    
    <!-- Fonts and Icons -->
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Raleway:wght@300;400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    
    <style>
        :root {
            --primary: #0A2463;
            --secondary: #3E92CC;
            --accent: #FFD700;
            --light: #FFF9F0;
            --dark: #1A1A1A;
            --success: #28a745;
            --info: #17a2b8;
            --font-heading: 'Playfair Display', serif;
            --font-body: 'Raleway', sans-serif;
            --accent-rgb: 255, 215, 0;
            --primary-rgb: 10, 36, 99;
            --background: var(--light);
            --text-color: var(--dark);
            --card-bg: white;
            --header-bg: rgba(10, 36, 99, 0.95);
        }
        
        /* Dark Mode Variables */
        .dark-theme {
            --bg-dark: #121212;
            --text-dark: #f0f0f0;
            --card-dark: #1e1e1e;
            
            --background: var(--bg-dark);
            --text-color: var(--text-dark);
            --card-bg: var(--card-dark);
            --header-bg: rgba(30, 30, 30, 0.9);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: var(--font-body);
            line-height: 1.8;
            color: var(--text-color);
            background-color: var(--background);
            overflow-x: hidden;
            transition: background-color 0.3s ease, color 0.3s ease;
        }
        
        .container {
            width: 90%;
            max-width: 1400px;
            margin: 0 auto;
        }
        
        /* Header Styles */
        header {
            background-color: var(--header-bg);
            color: white;
            padding: 1.5rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            transition: all 0.3s ease;
            box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
            backdrop-filter: blur(8px);
        }
        
        header.scrolled {
            padding: 1rem 0;
            background-color: rgba(var(--primary-rgb), 0.98);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            text-decoration: none;
        }
        
        .logo-icon {
            font-size: 2.5rem;
            color: var(--accent);
            margin-right: 15px;
        }
        
        .logo-text {
            font-family: var(--font-heading);
        }
        
        .logo-text h1 {
            font-size: 1.8rem;
            font-weight: 700;
            line-height: 1.2;
            color: white;
        }
        
        .logo-text p {
            font-size: 0.7rem;
            letter-spacing: 2px;
            text-transform: uppercase;
            opacity: 0.8;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 2rem;
            position: relative;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 600;
            font-size: 1rem;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            padding: 0.5rem 0;
            position: relative;
        }
        
        nav ul li a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--accent);
            transition: width 0.3s ease;
        }
        
        nav ul li a:hover::after {
            width: 100%;
        }
        
        nav ul li a.active {
            color: var(--accent);
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Theme Toggle */
        .theme-toggle {
            position: relative;
            width: 60px;
            height: 30px;
            border-radius: 30px;
            background: var(--card-bg);
            border: none;
            cursor: pointer;
            display: flex;
            align-items: center;
            padding: 0 5px;
            margin-left: 15px;
        }
        
        .theme-toggle i {
            font-size: 14px;
            padding: 0 5px;
            color: var(--text-color);
        }
        
        .toggle-ball {
            position: absolute;
            left: 5px;
            width: 22px;
            height: 22px;
            background: var(--accent);
            border-radius: 50%;
            transition: transform 0.3s ease;
        }
        
        .dark-theme .toggle-ball {
            transform: translateX(30px);
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            min-height: 800px;
            background: linear-gradient(rgba(10, 36, 99, 0.7), rgba(10, 36, 99, 0.7)), 
                        url('https://images.unsplash.com/photo-1522202176988-66273c2fd55f?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: white;
            display: flex;
            align-items: center;
            text-align: center;
            padding-top: 80px;
        }
        
        .hero-content {
            max-width: 900px;
            margin: 0 auto;
            padding: 0 2rem;
        }
        
        .hero h1 {
            font-family: var(--font-heading);
            font-size: 4rem;
            margin-bottom: 1.5rem;
            line-height: 1.2;
            text-shadow: 2px 2px 8px rgba(0,0,0,0.3);
            animation: fadeInUp 1s ease;
        }
        
        .hero p {
            font-size: 1.5rem;
            margin-bottom: 2.5rem;
            opacity: 0.9;
            animation: fadeInUp 1s ease 0.2s forwards;
            opacity: 0;
        }
        
        .hero-btns {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            animation: fadeInUp 1s ease 0.4s forwards;
            opacity: 0;
        }
        
        .btn {
            display: inline-block;
            padding: 1rem 2.5rem;
            border-radius: 50px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
            letter-spacing: 1px;
        }
        
        .btn-primary {
            background-color: var(--accent);
            color: var(--primary);
            box-shadow: 0 4px 15px rgba(255, 215, 0, 0.3);
        }
        
        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(255, 215, 0, 0.4);
        }
        
        .btn-outline {
            border: 2px solid white;
            color: white;
        }
        
        .btn-outline:hover {
            background-color: white;
            color: var(--primary);
            transform: translateY(-3px);
        }
        
        .btn-accent {
            background-color: var(--accent);
            color: var(--primary);
            font-weight: 600;
        }
        
        .btn-accent:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(255, 215, 0, 0.3);
        }
        
        /* About Section */
        .section {
            padding: 8rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 5rem;
        }
        
        .section-title h2 {
            font-family: var(--font-heading);
            font-size: 3rem;
            color: var(--primary);
            position: relative;
            display: inline-block;
            margin-bottom: 1.5rem;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background-color: var(--accent);
        }
        
        .section-title p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto;
            color: var(--text-color);
            opacity: 0.8;
        }
        
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }
        
        .about-text h3 {
            font-family: var(--font-heading);
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }
        
        .about-text p {
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
            line-height: 1.8;
        }
        
        .about-features {
            margin-top: 2rem;
        }
        
        .feature-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 1.5rem;
        }
        
        .feature-icon {
            font-size: 1.5rem;
            color: var(--accent);
            margin-right: 1rem;
            margin-top: 0.3rem;
        }
        
        .feature-text h4 {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
            color: var(--primary);
        }
        
        .about-image {
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 30px 60px rgba(10, 36, 99, 0.2);
            transform: rotate(-2deg);
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
            transition: transform 0.5s ease;
        }
        
        .about-image:hover img {
            transform: scale(1.05);
        }
        
        .about-image::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(10, 36, 99, 0.2), rgba(62, 146, 204, 0.2));
            z-index: 1;
        }
        
        /* Schools Section with Program Filter */
        .schools {
            background-color: var(--card-bg);
        }
        
        .program-filter {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-bottom: 3rem;
            flex-wrap: wrap;
        }
        
        .filter-btn {
            padding: 0.8rem 1.8rem;
            border-radius: 50px;
            background: transparent;
            border: 2px solid var(--accent);
            color: var(--text-color);
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .filter-btn.active {
            background: var(--accent);
            color: var(--primary);
        }
        
        .filter-btn:hover:not(.active) {
            background: rgba(var(--accent-rgb), 0.1);
        }
        
        .schools-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .school-card {
            background-color: var(--card-bg);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
            border: 1px solid rgba(var(--primary-rgb), 0.1);
        }
        
        .school-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.1);
        }
        
        .school-card-img {
            height: 200px;
            overflow: hidden;
        }
        
        .school-card-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .school-card:hover .school-card-img img {
            transform: scale(1.1);
        }
        
        .school-card-content {
            padding: 2rem;
        }
        
        .program-badge {
            display: inline-block;
            padding: 3px 10px;
            background: var(--accent);
            color: var(--primary);
            border-radius: 4px;
            font-size: 0.7rem;
            font-weight: 600;
            margin-bottom: 10px;
        }
        
        .school-card-content h3 {
            font-family: var(--font-heading);
            font-size: 1.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }
        
        .school-card-content p {
            margin-bottom: 1.5rem;
            color: var(--text-color);
            opacity: 0.8;
        }
        
        .school-card-link {
            display: inline-flex;
            align-items: center;
            color: var(--secondary);
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .school-card-link i {
            margin-left: 0.5rem;
            transition: transform 0.3s ease;
        }
        
        .school-card-link:hover {
            color: var(--primary);
        }
        
        .school-card-link:hover i {
            transform: translateX(5px);
        }
        
        /* Stats Section */
        .stats {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 6rem 0;
            text-align: center;
        }
        
        .stats-container {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 2rem;
        }
        
        .stat-item {
            padding: 2rem;
        }
        
        .stat-number {
            font-family: var(--font-heading);
            font-size: 3.5rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            color: var(--accent);
        }
        
        .stat-label {
            font-size: 1.2rem;
            letter-spacing: 1px;
            opacity: 0.9;
        }
        
        /* Testimonials */
        .testimonials {
            position: relative;
            padding: 8rem 0;
            background-color: var(--background);
        }
        
        .testimonial-slider {
            max-width: 1000px;
            margin: 0 auto;
            position: relative;
        }
        
        .testimonial-card {
            background-color: var(--card-bg);
            border-radius: 10px;
            padding: 3rem;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            text-align: center;
            margin: 0 1rem;
        }
        
        .testimonial-quote {
            font-size: 1.2rem;
            font-style: italic;
            color: var(--text-color);
            margin-bottom: 2rem;
            line-height: 1.8;
            position: relative;
        }
        
        .testimonial-quote::before,
        .testimonial-quote::after {
            content: '"';
            font-size: 3rem;
            color: var(--accent);
            opacity: 0.3;
            position: absolute;
        }
        
        .testimonial-quote::before {
            top: -20px;
            left: -15px;
        }
        
        .testimonial-quote::after {
            bottom: -40px;
            right: -15px;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .testimonial-author-img {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            overflow: hidden;
            margin-right: 1rem;
        }
        
        .testimonial-author-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .testimonial-author-info h4 {
            font-family: var(--font-heading);
            color: var(--primary);
            margin-bottom: 0.3rem;
        }
        
        .testimonial-author-info p {
            color: var(--text-color);
            opacity: 0.7;
            font-size: 0.9rem;
        }
        
        /* Virtual Tour Section */
        .virtual-tour {
            background-color: var(--card-bg);
        }
        
        .tour-container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .panorama-view {
            width: 100%;
            height: 500px;
            border-radius: 10px;
            overflow: hidden;
            margin-bottom: 20px;
            background-color: #eee;
        }
        
        .tour-hotspots {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
        }
        
        .hotspot {
            background: var(--card-bg);
            border: 2px solid var(--accent);
            padding: 10px 20px;
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.3s ease;
            color: var(--text-color);
            font-weight: 600;
        }
        
        .hotspot.active {
            background: var(--accent);
            color: var(--primary);
        }
        
        /* Tuition Calculator */
        .calculator {
            background-color: var(--background);
        }
        
        .calculator-card {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            background: var(--card-bg);
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            max-width: 1000px;
            margin: 0 auto;
        }
        
        .calculator-form {
            display: grid;
            gap: 20px;
        }
        
        .form-group {
            display: flex;
            flex-direction: column;
        }
        
        .form-group label {
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--primary);
        }
        
        .form-group select {
            padding: 12px 15px;
            border-radius: 8px;
            border: 1px solid rgba(var(--primary-rgb), 0.2);
            background-color: var(--card-bg);
            
