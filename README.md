<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Ер-Ана – современная стоматологическая клиника в Шымкенте. Имплантация, брекеты, кариес, хирургия. Работаем 24/7. Принимаем ОСМС.">
    <meta property="og:title" content="Ер-Ана | Стоматология & Медицина Шымкент">
    <meta property="og:description" content="Профессиональная стоматология и медицинные услуги в Шымкенте. 10+ лет опыта. Врачи высокого уровня.">
    <meta property="og:image" content="">
    <meta property="og:url" content="">
    <link rel="canonical" href="">
    
    <title>Ер-Ана | Стоматология & Медицина Шымкент</title>
    
    <!-- Google Fonts: Nunito -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Nunito:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --navy: #0D2B55;
            --blue: #1A5CB8;
            --mint: #2DAB80;
            --gold: #E8A020;
            --light: #EBF3FF;
            --gray: #6B7A8D;
            --border: #D8E4F0;
            --bg: #F8FAFB;
            --white: #FFFFFF;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Nunito', sans-serif;
            color: #1E293B;
            background-color: var(--bg);
            line-height: 1.6;
            overflow-x: hidden;
        }

        h1, h2, h3, h4, h5, h6 {
            color: var(--navy);
            font-weight: 700;
        }

        a {
            text-decoration: none;
            transition: all 0.3s ease;
        }

        button {
            font-family: 'Nunito', sans-serif;
            border: none;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* ===== Animations ===== */
        @keyframes reveal {
            from {
                opacity: 0;
                transform: translateY(40px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes slideInLeft {
            from {
                opacity: 0;
                transform: translateX(-30px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        @keyframes pulse-glow {
            0%, 100% {
                box-shadow: 0 0 0 0 rgba(37, 211, 102, 0.7);
            }
            50% {
                box-shadow: 0 0 0 10px rgba(37, 211, 102, 0);
            }
        }

        @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateY(-20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @media (prefers-reduced-motion: reduce) {
            *,
            *::before,
            *::after {
                animation-duration: 0.01ms !important;
                animation-iteration-count: 1 !important;
                transition-duration: 0.01ms !important;
                scroll-behavior: auto !important;
            }
        }

        /* ===== Header & Navigation ===== */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.98);
            backdrop-filter: blur(10px);
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 80px;
        }

        .logo {
            font-size: 1.4rem;
            font-weight: 800;
            color: var(--navy);
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .logo i {
            color: var(--mint);
            font-size: 1.6rem;
        }

        .nav-links {
            display: flex;
            gap: 40px;
            list-style: none;
        }

        .nav-links a {
            color: var(--navy);
            font-weight: 600;
            font-size: 0.95rem;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -3px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--blue);
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after,
        .nav-links a.active::after {
            width: 100%;
        }

        .header-right {
            display: flex;
            align-items: center;
            gap: 20px;
        }

        .phone-header {
            font-weight: 700;
            color: var(--navy);
            font-size: 0.95rem;
        }

        .btn-header {
            background: var(--blue);
            color: var(--white);
            padding: 12px 24px;
            border-radius: 12px;
            font-weight: 600;
            font-size: 0.9rem;
            box-shadow: 0 4px 12px rgba(26, 92, 184, 0.25);
        }

        .btn-header:hover {
            background: #153a8a;
            transform: translateY(-2px);
            box-shadow: 0 6px 16px rgba(26, 92, 184, 0.35);
        }

        .hamburger {
            display: none;
            flex-direction: column;
            cursor: pointer;
            gap: 5px;
            background: none;
            padding: 5px;
        }

        .hamburger span {
            width: 25px;
            height: 3px;
            background: var(--navy);
            border-radius: 2px;
            transition: all 0.3s ease;
        }

        .hamburger.active span:nth-child(1) {
            transform: rotate(45deg) translate(10px, 10px);
        }

        .hamburger.active span:nth-child(2) {
            opacity: 0;
        }

        .hamburger.active span:nth-child(3) {
            transform: rotate(-45deg) translate(8px, -8px);
        }

        .mobile-menu {
            display: none;
            position: fixed;
            right: -100%;
            top: 0;
            width: 70%;
            height: 100vh;
            background: var(--white);
            flex-direction: column;
            padding: 100px 30px 30px;
            gap: 20px;
            z-index: 999;
            transition: right 0.3s ease;
            box-shadow: -2px 0 10px rgba(0, 0, 0, 0.1);
        }

        .mobile-menu.active {
            right: 0;
        }

        .mobile-menu a {
            color: var(--navy);
            font-weight: 600;
            font-size: 1rem;
            padding: 12px 0;
            border-bottom: 1px solid var(--border);
        }

        @media (max-width: 768px) {
            .nav-links,
            .phone-header {
                display: none;
            }

            .hamburger {
                display: flex;
            }

            .mobile-menu {
                display: flex;
            }

            .header-content {
                justify-content: space-between;
                padding: 0 20px;
            }
        }

        /* ===== Hero Section ===== */
        .hero {
            margin-top: 80px;
            min-height: 100vh;
            display: flex;
            align-items: center;
            background: linear-gradient(135deg, var(--white) 0%, var(--light) 100%);
            padding: 40px 20px;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 10%;
            right: -10%;
            width: 500px;
            height: 500px;
            background: linear-gradient(135deg, var(--light) 0%, var(--blue) 100%);
            border-radius: 50%;
            opacity: 0.1;
            z-index: 0;
        }

        .hero-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
            position: relative;
            z-index: 1;
        }

        .hero-left h2 {
            display: inline-block;
            background: linear-gradient(135deg, var(--mint) 0%, var(--blue) 100%);
            color: var(--white);
            padding: 8px 16px;
            border-radius: 30px;
            font-size: 0.9rem;
            font-weight: 600;
            margin-bottom: 20px;
            animation: slideInLeft 0.6s ease;
        }

        .hero-left h1 {
            font-size: 3.5rem;
            line-height: 1.2;
            margin-bottom: 20px;
            color: var(--navy);
            animation: slideInLeft 0.8s ease 0.1s both;
        }

        .hero-left p {
            font-size: 1.1rem;
            color: var(--gray);
            margin-bottom: 30px;
            max-width: 450px;
            animation: slideInLeft 1s ease 0.2s both;
        }

        .hero-facts {
            display: grid;
            gap: 15px;
            margin-bottom: 30px;
            animation: slideInLeft 1.2s ease 0.3s both;
        }

        .fact-item {
            display: flex;
            align-items: center;
            gap: 12px;
            font-weight: 600;
            color: var(--navy);
            font-size: 0.95rem;
        }

        .fact-item i {
            color: var(--mint);
            font-size: 1.2rem;
        }

        .hero-buttons {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
            animation: slideInLeft 1.4s ease 0.4s both;
        }

        .btn-primary {
            background: var(--blue);
            color: var(--white);
            padding: 14px 32px;
            border-radius: 12px;
            font-weight: 700;
            font-size: 0.95rem;
            box-shadow: 0 4px 15px rgba(26, 92, 184, 0.3);
        }

        .btn-primary:hover {
            background: #153a8a;
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(26, 92, 184, 0.4);
        }

        .btn-secondary {
            background: var(--white);
            color: var(--blue);
            padding: 14px 32px;
            border: 2px solid var(--blue);
            border-radius: 12px;
            font-weight: 700;
            font-size: 0.95rem;
        }

        .btn-secondary:hover {
            background: var(--light);
            transform: translateY(-3px);
        }

        .hero-right {
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
            animation: slideInLeft 0.8s ease 0.2s both;
            animation-direction: reverse;
        }

        .doctor-placeholder {
            width: 280px;
            height: 380px;
            background: linear-gradient(135deg, var(--blue) 0%, var(--mint) 100%);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 4rem;
            box-shadow: 0 20px 60px rgba(26, 92, 184, 0.2);
            position: relative;
            z-index: 2;
        }

        .floating-card {
            position: absolute;
            background: var(--white);
            border-radius: 12px;
            padding: 16px 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            display: flex;
            align-items: center;
            gap: 12px;
            font-weight: 600;
            color: var(--navy);
            font-size: 0.9rem;
        }

        .floating-card.card-1 {
            top: -20px;
            right: -40px;
            animation: slideDown 0.6s ease 0.5s both;
        }

        .floating-card.card-2 {
            bottom: 40px;
            right: -50px;
            animation: slideDown 0.6s ease 0.7s both;
        }

        .floating-card i {
            color: var(--mint);
            font-size: 1.4rem;
        }

        @media (max-width: 768px) {
            .hero {
                min-height: auto;
                padding: 40px 20px 60px;
            }

            .hero-content {
                grid-template-columns: 1fr;
                gap: 40px;
            }

            .hero-left h1 {
                font-size: 2.2rem;
            }

            .hero-left p {
                font-size: 1rem;
            }

            .hero-buttons {
                flex-direction: column;
            }

            .btn-primary,
            .btn-secondary {
                width: 100%;
                text-align: center;
            }

            .hero-right {
                justify-content: center;
            }

            .floating-card {
                display: none;
            }
        }

        /* ===== Stats Bar ===== */
        .stats-bar {
            background: var(--navy);
            padding: 60px 20px;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
        }

        .stat-item {
            text-align: center;
            color: var(--white);
        }

        .stat-number {
            font-size: 2.8rem;
            font-weight: 800;
            color: var(--mint);
            margin-bottom: 10px;
        }

        .stat-label {
            font-size: 1rem;
            color: rgba(255, 255, 255, 0.8);
            font-weight: 500;
        }

        /* ===== Services Section ===== */
        .services {
            padding: 100px 20px;
            background: var(--white);
        }

        .section-header {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-header h2 {
            font-size: 2.8rem;
            margin-bottom: 15px;
        }

        .section-header p {
            font-size: 1.1rem;
            color: var(--gray);
            max-width: 600px;
            margin: 0 auto;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }

        .service-card {
            background: var(--white);
            border: 1px solid var(--border);
            border-radius: 16px;
            padding: 30px;
            text-align: center;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            opacity: 0;
            animation: reveal 0.6s ease forwards;
        }

        .service-card:hover {
            transform: translateY(-8px);
            border-color: var(--blue);
            box-shadow: 0 15px 40px rgba(26, 92, 184, 0.15);
        }

        .service-card.stagger-1 { animation-delay: 0.1s; }
        .service-card.stagger-2 { animation-delay: 0.2s; }
        .service-card.stagger-3 { animation-delay: 0.3s; }
        .service-card.stagger-4 { animation-delay: 0.4s; }
        .service-card.stagger-5 { animation-delay: 0.5s; }
        .service-card.stagger-6 { animation-delay: 0.6s; }
        .service-card.stagger-7 { animation-delay: 0.7s; }
        .service-card.stagger-8 { animation-delay: 0.8s; }

        .service-icon {
            width: 70px;
            height: 70px;
            background: linear-gradient(135deg, var(--light) 0%, var(--light) 100%);
            border-radius: 14px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            color: var(--blue);
            margin: 0 auto 20px;
        }

        .service-card h3 {
            font-size: 1.2rem;
            margin-bottom: 10px;
        }

        .service-card p {
            color: var(--gray);
            font-size: 0.95rem;
            line-height: 1.6;
        }

        .service-badge {
            display: inline-block;
            background: var(--gold);
            color: var(--white);
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 0.75rem;
            font-weight: 700;
            margin-top: 15px;
            text-transform: uppercase;
        }

        /* ===== Medical Center Section ===== */
        .medical-center {
            padding: 100px 20px;
            background: var(--light);
        }

        .medical-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .medical-left h2 {
            font-size: 2.5rem;
            margin-bottom: 30px;
        }

        .medical-checklist {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin-bottom: 30px;
        }

        .check-item {
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 0.95rem;
            color: var(--navy);
            font-weight: 600;
        }

        .check-item i {
            color: var(--mint);
            font-size: 1.3rem;
            flex-shrink: 0;
        }

        .medical-button {
            background: var(--mint);
            color: var(--white);
            padding: 14px 30px;
            border-radius: 12px;
            font-weight: 700;
            font-size: 0.95rem;
            display: inline-block;
            box-shadow: 0 4px 15px rgba(45, 171, 128, 0.3);
        }

        .medical-button:hover {
            background: #249665;
            transform: translateY(-3px);
        }

        .medical-right {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }

        .medical-mini-card {
            background: var(--white);
            padding: 20px;
            border-radius: 12px;
            text-align: center;
            border: 1px solid var(--border);
            transition: all 0.3s ease;
            opacity: 0;
            animation: reveal 0.6s ease forwards;
        }

        .medical-mini-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.08);
        }

        .medical-mini-card.stagger-1 { animation-delay: 0.1s; }
        .medical-mini-card.stagger-2 { animation-delay: 0.2s; }
        .medical-mini-card.stagger-3 { animation-delay: 0.3s; }
        .medical-mini-card.stagger-4 { animation-delay: 0.4s; }
        .medical-mini-card.stagger-5 { animation-delay: 0.5s; }
        .medical-mini-card.stagger-6 { animation-delay: 0.6s; }

        .medical-mini-card i {
            font-size: 2rem;
            color: var(--blue);
            margin-bottom: 10px;
        }

        .medical-mini-card h4 {
            font-size: 0.9rem;
            color: var(--navy);
        }

        @media (max-width: 768px) {
            .medical-content {
                grid-template-columns: 1fr;
            }

            .medical-right {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        /* ===== Why Us Section ===== */
        .why-us {
            padding: 100px 20px;
            background: var(--white);
        }

        .why-us .section-header {
            margin-bottom: 60px;
        }

        .why-us-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
        }

        .why-item {
            text-align: center;
            opacity: 0;
            animation: reveal 0.6s ease forwards;
        }

        .why-item.stagger-1 { animation-delay: 0.1s; }
        .why-item.stagger-2 { animation-delay: 0.2s; }
        .why-item.stagger-3 { animation-delay: 0.3s; }
        .why-item.stagger-4 { animation-delay: 0.4s; }

        .why-icon {
            width: 100px;
            height: 100px;
            background: linear-gradient(135deg, var(--blue) 0%, var(--mint) 100%);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            color: var(--white);
            margin: 0 auto 20px;
        }

        .why-item h3 {
            font-size: 1.5rem;
            margin-bottom: 10px;
        }

        .why-item p {
            color: var(--gray);
        }

        /* ===== Doctors Slider ===== */
        .doctors {
            padding: 100px 20px;
            background: var(--light);
        }

        .doctors .section-header {
            margin-bottom: 60px;
        }

        .doctors-slider {
            position: relative;
            overflow: hidden;
        }

        .doctors-track {
            display: grid;
            grid-template-columns: repeat(6, 1fr);
            gap: 20px;
            scroll-snap-type: x mandatory;
            overflow-x: auto;
            scroll-behavior: smooth;
            padding-bottom: 10px;
            scroll-padding: 20px;
        }

        .doctors-track::-webkit-scrollbar {
            height: 6px;
        }

        .doctors-track::-webkit-scrollbar-track {
            background: var(--border);
            border-radius: 10px;
        }

        .doctors-track::-webkit-scrollbar-thumb {
            background: var(--blue);
            border-radius: 10px;
        }

        .doctor-card {
            background: var(--white);
            border-radius: 16px;
            overflow: hidden;
            scroll-snap-align: start;
            min-width: 280px;
            transition: all 0.3s ease;
            opacity: 0;
            animation: reveal 0.6s ease forwards;
        }

        .doctor-card.stagger-1 { animation-delay: 0.1s; }
        .doctor-card.stagger-2 { animation-delay: 0.2s; }
        .doctor-card.stagger-3 { animation-delay: 0.3s; }
        .doctor-card.stagger-4 { animation-delay: 0.4s; }
        .doctor-card.stagger-5 { animation-delay: 0.5s; }
        .doctor-card.stagger-6 { animation-delay: 0.6s; }

        .doctor-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.1);
        }

        .doctor-image {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, var(--blue) 0%, var(--mint) 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 3rem;
        }

        .doctor-info {
            padding: 20px;
            text-align: center;
        }

        .doctor-specialty {
            display: inline-block;
            background: var(--light);
            color: var(--blue);
            padding: 4px 10px;
            border-radius: 8px;
            font-size: 0.75rem;
            font-weight: 600;
            margin-bottom: 10px;
            text-transform: uppercase;
        }

        .doctor-name {
            font-size: 1.1rem;
            margin-bottom: 8px;
        }

        .doctor-rating {
            display: flex;
            justify-content: center;
            gap: 4px;
            margin-bottom: 12px;
            font-size: 0.9rem;
        }

        .doctor-rating i {
            color: var(--gold);
        }

        .doctor-button {
            width: 100%;
            background: var(--blue);
            color: var(--white);
            padding: 10px;
            border-radius: 8px;
            font-weight: 600;
            font-size: 0.9rem;
        }

        .doctor-button:hover {
            background: #153a8a;
        }

        .slider-nav {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 30px;
        }

        .slider-btn {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: var(--blue);
            color: var(--white);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1rem;
            cursor: pointer;
        }

        .slider-btn:hover {
            background: #153a8a;
        }

        @media (max-width: 1024px) {
            .doctors-track {
                grid-template-columns: repeat(4, 1fr);
            }
        }

        @media (max-width: 768px) {
            .doctors-track {
                grid-template-columns: repeat(2, 1fr);
                gap: 15px;
            }

            .doctor-card {
                min-width: auto;
            }

            .slider-nav {
                display: none;
            }
        }

        /* ===== Reviews Section ===== */
        .reviews {
            padding: 100px 20px;
            background: var(--white);
        }

        .reviews-header {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
            margin-bottom: 60px;
        }

        .rating-block h2 {
            font-size: 3rem;
            margin-bottom: 10px;
        }

        .rating-stars {
            display: flex;
            gap: 5px;
            margin-bottom: 15px;
        }

        .rating-stars i {
            color: var(--gold);
            font-size: 1.5rem;
        }

        .rating-count {
            color: var(--gray);
            font-size: 0.95rem;
        }

        .reviews-slider {
            position: relative;
            overflow: hidden;
        }

        .reviews-track {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            scroll-snap-type: x mandatory;
            overflow-x: auto;
            scroll-behavior: smooth;
            padding-bottom: 10px;
        }

        .review-card {
            background: var(--light);
            border-radius: 16px;
            padding: 30px;
            scroll-snap-align: start;
            min-width: 350px;
            position: relative;
        }

        .review-quote {
            font-size: 3rem;
            color: var(--blue);
            opacity: 0.2;
            position: absolute;
            top: 10px;
            left: 15px;
        }

        .review-text {
            color: var(--navy);
            margin-bottom: 15px;
            font-style: italic;
            font-size: 0.95rem;
            position: relative;
            z-index: 1;
        }

        .review-author {
            font-weight: 600;
            color: var(--navy);
        }

        .review-role {
            font-size: 0.85rem;
            color: var(--gray);
        }

        @media (max-width: 1024px) {
            .reviews-track {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 768px) {
            .reviews-header {
                grid-template-columns: 1fr;
            }

            .reviews-track {
                grid-template-columns: 1fr;
            }

            .review-card {
                min-width: auto;
            }
        }

        /* ===== Appointment Section ===== */
        .appointment {
            background: linear-gradient(135deg, var(--navy) 0%, var(--blue) 100%);
            padding: 80px 20px;
            color: var(--white);
        }

        .appointment-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .appointment-left h2 {
            font-size: 2.5rem;
            color: var(--white);
            margin-bottom: 20px;
        }

        .appointment-left p {
            font-size: 1.05rem;
            color: rgba(255, 255, 255, 0.9);
            margin-bottom: 30px;
            line-height: 1.8;
        }

        .appointment-form {
            background: var(--white);
            border-radius: 16px;
            padding: 40px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .form-group {
            display: flex;
            flex-direction: column;
        }

        .form-group label {
            color: var(--navy);
            font-weight: 600;
            margin-bottom: 8px;
            font-size: 0.9rem;
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            padding: 12px 16px;
            border: 1px solid var(--border);
            border-radius: 8px;
            font-family: 'Nunito', sans-serif;
            font-size: 0.95rem;
            color: var(--navy);
            transition: all 0.3s ease;
        }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--blue);
            box-shadow: 0 0 0 3px rgba(26, 92, 184, 0.1);
        }

        .form-group textarea {
            resize: vertical;
            min-height: 100px;
        }

        .form-submit {
            background: var(--mint);
            color: var(--white);
            padding: 14px;
            border-radius: 8px;
            font-weight: 700;
            font-size: 0.95rem;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(45, 171, 128, 0.3);
        }

        .form-submit:hover {
            background: #249665;
            transform: translateY(-2px);
        }

        .form-message {
            padding: 12px;
            border-radius: 8px;
            text-align: center;
            font-weight: 600;
            display: none;
        }

        .form-message.success {
            background: var(--mint);
            color: var(--white);
            display: block;
        }

        @media (max-width: 768px) {
            .appointment-content {
                grid-template-columns: 1fr;
            }

            .appointment-form {
                padding: 30px;
            }
        }

        /* ===== Contacts Section ===== */
        .contacts {
            padding: 100px 20px;
            background: var(--light);
        }

        .contacts .section-header {
            margin-bottom: 60px;
        }

        .contacts-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
        }

        .branches {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .branch-card {
            background: var(--white);
            border-radius: 16px;
            padding: 30px;
            border-left: 4px solid var(--blue);
            opacity: 0;
            animation: reveal 0.6s ease forwards;
        }

        .branch-card.stagger-1 { animation-delay: 0.1s; }
        .branch-card.stagger-2 { animation-delay: 0.2s; }

        .branch-card h3 {
            margin-bottom: 15px;
            font-size: 1.2rem;
        }

        .branch-item {
            display: flex;
            align-items: flex-start;
            gap: 12px;
            margin-bottom: 15px;
            font-size: 0.95rem;
        }

        .branch-item i {
            color: var(--mint);
            font-size: 1.2rem;
            flex-shrink: 0;
            margin-top: 3px;
        }

        .branch-whatsapp {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: #25D366;
            color: var(--white);
            padding: 10px 16px;
            border-radius: 8px;
            font-weight: 600;
            font-size: 0.9rem;
            margin-top: 15px;
        }

        .branch-whatsapp:hover {
            background: #1ea952;
            transform: translateY(-2px);
        }

        .map-container {
            border-radius: 16px;
            overflow: hidden;
            height: 400px;
        }

        .map-container iframe {
            width: 100%;
            height: 100%;
            border: none;
        }

        @media (max-width: 768px) {
            .contacts-content {
                grid-template-columns: 1fr;
            }

            .map-container {
                height: 300px;
            }
        }

        /* ===== Footer ===== */
        footer {
            background: var(--navy);
            color: var(--white);
            padding: 60px 20px 30px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-section h4 {
            color: var(--white);
            margin-bottom: 15px;
            font-size: 1.1rem;
        }

        .footer-section ul {
            list-style: none;
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .footer-section a {
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.95rem;
        }

        .footer-section a:hover {
            color: var(--mint);
        }

        .footer-logo {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 1.3rem;
            font-weight: 800;
            margin-bottom: 15px;
        }

        .footer-logo i {
            color: var(--mint);
        }

        .footer-social {
            display: flex;
            gap: 12px;
            margin-top: 15px;
        }

        .social-icon {
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 1.1rem;
        }

        .social-icon:hover {
            background: var(--mint);
        }

        .footer-bottom {
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            padding-top: 30px;
            text-align: center;
            color: rgba(255, 255, 255, 0.6);
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            footer {
                padding: 40px 20px 20px;
            }

            .footer-grid {
                gap: 30px;
            }
        }

        /* ===== Floating WhatsApp Button ===== */
        .whatsapp-float {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 60px;
            height: 60px;
            background: #25D366;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 1.8rem;
            z-index: 998;
            cursor: pointer;
            box-shadow: 0 4px 20px rgba(37, 211, 102, 0.4);
            animation: pulse-glow 2s infinite;
            transition: all 0.3s ease;
        }

        .whatsapp-float:hover {
            transform: scale(1.1);
            animation: none;
            box-shadow: 0 6px 30px rgba(37, 211, 102, 0.6);
        }

        .whatsapp-tooltip {
            position: absolute;
            right: 80px;
            background: var(--navy);
            color: var(--white);
            padding: 8px 12px;
            border-radius: 6px;
            font-size: 0.85rem;
            white-space: nowrap;
            opacity: 0;
            pointer-events: none;
            transition: opacity 0.3s ease;
        }

        .whatsapp-float:hover .whatsapp-tooltip {
            opacity: 1;
        }

        /* ===== Scroll to Top Button ===== */
        .scroll-to-top {
            position: fixed;
            bottom: 100px;
            right: 30px;
            width: 50px;
            height: 50px;
            background: var(--blue);
            border-radius: 50%;
            display: none;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 1.4rem;
            z-index: 997;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(26, 92, 184, 0.3);
            transition: all 0.3s ease;
        }

        .scroll-to-top.show {
            display: flex;
        }

        .scroll-to-top:hover {
            background: #153a8a;
            transform: translateY(-3px);
        }

        @media (max-width: 768px) {
            .whatsapp-float {
                bottom: 20px;
                right: 20px;
                width: 55px;
                height: 55px;
            }

            .scroll-to-top {
                bottom: 90px;
                right: 20px;
                width: 45px;
                height: 45px;
            }

            .whatsapp-tooltip {
                display: none;
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
                    <i class="fas fa-tooth"></i>
                    <span>Ер-Ана</span>
                </div>

                <ul class="nav-links">
                    <li><a href="#services">Услуги</a></li>
                    <li><a href="#medical">Медицина</a></li>
                    <li><a href="#doctors">Врачи</a></li>
                    <li><a href="#reviews">Отзывы</a></li>
                    <li><a href="#contacts">Контакты</a></li>
                </ul>

                <div class="header-right">
                    <a href="tel:+77053563838" class="phone-header">+7 705 356-38-38</a>
                    <button class="btn-header" onclick="document.querySelector('#appointment').scrollIntoView({behavior: 'smooth'})">Запись</button>
                </div>

                <button class="hamburger" id="hamburger">
                    <span></span>
                    <span></span>
                    <span></span>
                </button>
            </div>
        </div>

        <!-- Mobile Menu -->
        <div class="mobile-menu" id="mobileMenu">
            <a href="#services">Услуги</a>
            <a href="#medical">Медицина</a>
            <a href="#doctors">Врачи</a>
            <a href="#reviews">Отзывы</a>
            <a href="#contacts">Контакты</a>
            <a href="tel:+77053563838" style="color: var(--mint);">+7 705 356-38-38</a>
            <a href="https://wa.me/77029863043" target="_blank" style="color: #25D366;">WhatsApp</a>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container hero-content">
            <div class="hero-left">
                <h2>Открыто круглосуточно</h2>
                <h1>Ваша улыбка — наша забота</h1>
                <p>Современная стоматология и комплексная медицина в Шымкенте. Профессиональные врачи, новейшее оборудование, заботливое отношение.</p>

                <div class="hero-facts">
                    <div class="fact-item">
                        <i class="fas fa-check-circle"></i>
                        <span>Имплантаты Osstem & Dentylux премиум класса</span>
                    </div>
                    <div class="fact-item">
                        <i class="fas fa-check-circle"></i>
                        <span>Все врачи имеют международные сертификаты</span>
                    </div>
                    <div class="fact-item">
                        <i class="fas fa-check-circle"></i>
                        <span>Приём ОСМС и частные услуги</span>
                    </div>
                </div>

                <div class="hero-buttons">
                    <button class="btn-primary" onclick="document.querySelector('#appointment').scrollIntoView({behavior: 'smooth'})">Записаться на прием</button>
                    <a href="https://wa.me/77029863043" target="_blank" class="btn-secondary">Написать в WhatsApp</a>
                </div>
            </div>

            <div class="hero-right">
                <div class="doctor-placeholder">
                    <i class="fas fa-user-doctor"></i>
                </div>
                <div class="floating-card card-1">
                    <i class="fas fa-star"></i>
                    <span>Рейтинг 4.7</span>
                </div>
                <div class="floating-card card-2">
                    <i class="fas fa-award"></i>
                    <span>10+ лет опыта</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Stats Bar -->
    <section class="stats-bar">
        <div class="container">
            <div class="stats-grid">
                <div class="stat-item">
                    <div class="stat-number" data-countup="5000">0</div>
                    <div class="stat-label">Пациентов</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number" data-countup="2">0</div>
                    <div class="stat-label">Филиала в Шымкенте</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number" data-countup="10">0</div>
                    <div class="stat-label">Лет опыта</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number" data-countup="100">0</div>
                    <div class="stat-label">% приём ОСМС</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="services">
        <div class="container">
            <div class="section-header">
                <h2>Услуги стоматологии</h2>
                <p>Полный спектр стоматологических услуг с использованием современного оборудования и материалов премиум класса</p>
            </div>

            <div class="services-grid">
                <div class="service-card stagger-1">
                    <div class="service-icon"><i class="fas fa-tooth"></i></div>
                    <h3>Лечение кариеса</h3>
                    <p>Безболезненное лечение с использованием современных методик и материалов</p>
                </div>

                <div class="service-card stagger-2">
                    <div class="service-icon"><i class="fas fa-crown"></i></div>
                    <h3>Коронки и мосты</h3>
                    <p>Восстановление зубов керамическими коронками высшего качества</p>
                </div>

                <div class="service-card stagger-3">
                    <div class="service-icon"><i class="fas fa-bone"></i></div>
                    <h3>Имплантация</h3>
                    <p>Установка имплантатов Osstem & Dentylux с пожизненной гарантией</p>
                    <div class="service-badge">ТОП услуга</div>
                </div>

                <div class="service-card stagger-4">
                    <div class="service-icon"><i class="fas fa-align-center"></i></div>
                    <h3>Брекеты и Invisalign</h3>
                    <p>Исправление прикуса современными методами и невидимыми элайнерами</p>
                </div>

                <div class="service-card stagger-5">
                    <div class="service-icon"><i class="fas fa-flask"></i></div>
                    <h3>Хирургия полости рта</h3>
                    <p>Удаление зубов и хирургические операции с минимальной травматичностью</p>
                </div>

                <div class="service-card stagger-6">
                    <div class="service-icon"><i class="fas fa-child"></i></div>
                    <h3>Детская стоматология</h3>
                    <p>Специальный подход к детям со специализированным оборудованием</p>
                </div>

                <div class="service-card stagger-7">
                    <div class="service-icon"><i class="fas fa-moon"></i></div>
                    <h3>Лечение во сне</h3>
                    <p>Седация и общий наркоз для безболезненного лечения</p>
                </div>

                <div class="service-card stagger-8">
                    <div class="service-icon"><i class="fas fa-scanner"></i></div>
                    <h3>КТ 3D сканирование</h3>
                    <p>Диагностика высочайшей точности для планирования лечения</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Medical Center Section -->
    <section id="medical" class="medical-center">
        <div class="container">
            <div class="medical-content">
                <div class="medical-left">
                    <h2>Медицинский центр</h2>
                    <div class="medical-checklist">
                        <div class="check-item">
                            <i class="fas fa-check-circle"></i>
                            <span>Полная диагностика состояния здоровья</span>
                        </div>
                        <div class="check-item">
                            <i class="fas fa-check-circle"></i>
                            <span>Консультация специалистов 24/7</span>
                        </div>
                        <div class="check-item">
                            <i class="fas fa-check-circle"></i>
                            <span>Комплексные медицинные пакеты</span>
                        </div>
                        <div class="check-item">
                            <i class="fas fa-check-circle"></i>
                            <span>Выезд врача на дом и в офис</span>
                        </div>
                        <div class="check-item">
                            <i class="fas fa-check-circle"></i>
                            <span>Приём ОСМС и частные услуги</span>
                        </div>
                    </div>
                    <button class="medical-button" onclick="document.querySelector('#appointment').scrollIntoView({behavior: 'smooth'})">Запросить консультацию</button>
                </div>

                <div class="medical-right">
                    <div class="medical-mini-card stagger-1">
                        <i class="fas fa-ultrasound"></i>
                        <h4>УЗ диагностика</h4>
                    </div>
                    <div class="medical-mini-card stagger-2">
                        <i class="fas fa-heart"></i>
                        <h4>Кардиология</h4>
                    </div>
                    <div class="medical-mini-card stagger-3">
                        <i class="fas fa-baby"></i>
                        <h4>Педиатрия</h4>
                    </div>
                    <div class="medical-mini-card stagger-4">
                        <i class="fas fa-brain"></i>
                        <h4>Неврология</h4>
                    </div>
                    <div class="medical-mini-card stagger-5">
                        <i class="fas fa-leaf"></i>
                        <h4>Детокс программы</h4>
                    </div>
                    <div class="medical-mini-card stagger-6">
                        <i class="fas fa-house"></i>
                        <h4>Выезд врача</h4>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Why Us Section -->
    <section class="why-us">
        <div class="container">
            <div class="section-header">
                <h2>Почему выбирают нас</h2>
                <p>Уникальное сочетание качества, профессионализма и внимания к пациентам</p>
            </div>

            <div class="why-us-grid">
                <div class="why-item stagger-1">
                    <div class="why-icon">
                        <i class="fas fa-graduation-cap"></i>
                    </div>
                    <h3>10+ лет опыта</h3>
                    <p>Доверие тысяч пациентов и богатый опыт специалистов</p>
                </div>

                <div class="why-item stagger-2">
                    <div class="why-icon">
                        <i class="fas fa-star"></i>
                    </div>
                    <h3>Лучшие врачи</h3>
                    <p>Команда профессионалов с международными сертификатами</p>
                </div>

                <div class="why-item stagger-3">
                    <div class="why-icon">
                        <i class="fas fa-tag"></i>
                    </div>
                    <h3>Цены ОСМС</h3>
                    <p>Доступные цены с покрытием гос. страховкой ОСМС</p>
                </div>

                <div class="why-item stagger-4">
                    <div class="why-icon">
                        <i class="fas fa-clock"></i>
                    </div>
                    <h3>24/7 режим</h3>
                    <p>Открыты круглосуточно для экстренных ситуаций</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Doctors Section -->
    <section id="doctors" class="doctors">
        <div class="container">
            <div class="section-header">
                <h2>Наши врачи</h2>
                <p>Команда высокопрофессиональных специалистов с международной квалификацией</p>
            </div>

            <div class="doctors-slider">
                <div class="doctors-track">
                    <div class="doctor-card stagger-1">
                        <div class="doctor-image">
                            <i class="fas fa-user-doctor"></i>
                        </div>
                        <div class="doctor-info">
                            <div class="doctor-specialty">Стоматолог</div>
                            <h3 class="doctor-name">Алтай Сулейменов</h3>
                            <div class="doctor-rating">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <span style="font-size: 0.8rem; color: var(--gray);">5.0</span>
                            </div>
                            <button class="doctor-button">Записаться</button>
                        </div>
                    </div>

                    <div class="doctor-card stagger-2">
                        <div class="doctor-image">
                            <i class="fas fa-user-doctor"></i>
                        </div>
                        <div class="doctor-info">
                            <div class="doctor-specialty">Хирург</div>
                            <h3 class="doctor-name">Рустем Батыров</h3>
                            <div class="doctor-rating">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <span style="font-size: 0.8rem; color: var(--gray);">4.9</span>
                            </div>
                            <button class="doctor-button">Записаться</button>
                        </div>
                    </div>

                    <div class="doctor-card stagger-3">
                        <div class="doctor-image">
                            <i class="fas fa-user-nurse"></i>
                        </div>
                        <div class="doctor-info">
                            <div class="doctor-specialty">Ортодонт</div>
                            <h3 class="doctor-name">Айнур Абикулова</h3>
                            <div class="doctor-rating">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <span style="font-size: 0.8rem; color: var(--gray);">5.0</span>
                            </div>
                            <button class="doctor-button">Записаться</button>
                        </div>
                    </div>

                    <div class="doctor-card stagger-4">
                        <div class="doctor-image">
                            <i class="fas fa-user-doctor"></i>
                        </div>
                        <div class="doctor-info">
                            <div class="doctor-specialty">Детский врач</div>
                            <h3 class="doctor-name">Дарина Касымова</h3>
                            <div class="doctor-rating">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <span style="font-size: 0.8rem; color: var(--gray);">4.8</span>
                            </div>
                            <button class="doctor-button">Записаться</button>
                        </div>
                    </div>

                    <div class="doctor-card stagger-5">
                        <div class="doctor-image">
                            <i class="fas fa-user-nurse"></i>
                        </div>
                        <div class="doctor-info">
                            <div class="doctor-specialty">Гигиенист</div>
                            <h3 class="doctor-name">Марат Жуманов</h3>
                            <div class="doctor-rating">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <span style="font-size: 0.8rem; color: var(--gray);">4.9</span>
                            </div>
                            <button class="doctor-button">Записаться</button>
                        </div>
                    </div>

                    <div class="doctor-card stagger-6">
                        <div class="doctor-image">
                            <i class="fas fa-user-doctor"></i>
                        </div>
                        <div class="doctor-info">
                            <div class="doctor-specialty">Кардиолог</div>
                            <h3 class="doctor-name">Илья Петухов</h3>
                            <div class="doctor-rating">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <span style="font-size: 0.8rem; color: var(--gray);">4.7</span>
                            </div>
                            <button class="doctor-button">Записаться</button>
                        </div>
                    </div>
                </div>
            </div>

            <div class="slider-nav">
                <button class="slider-btn" id="doctorsPrev" onclick="scrollDoctors('left')">
                    <i class="fas fa-chevron-left"></i>
                </button>
                <button class="slider-btn" id="doctorsNext" onclick="scrollDoctors('right')">
                    <i class="fas fa-chevron-right"></i>
                </button>
            </div>
        </div>
    </section>

    <!-- Reviews Section -->
    <section id="reviews" class="reviews">
        <div class="container">
            <div class="reviews-header">
                <div class="rating-block">
                    <h2>4.7</h2>
                    <div class="rating-stars">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star-half-alt"></i>
                    </div>
                    <p class="rating-count">На основе 43 отзывов из 2GIS</p>
                </div>

                <div class="reviews-slider">
                    <div class="reviews-track">
                        <div class="review-card">
                            <div class="review-quote">"</div>
                            <p class="review-text">Отличная клиника! Врачи очень внимательные и профессиональные. Лечение прошло без боли. Рекомендую всем знакомым и друзьям!</p>
                            <p class="review-author">Айнара Бейсенова</p>
                            <p class="review-role">Пациент</p>
                        </div>

                        <div class="review-card">
                            <div class="review-quote">"</div>
                            <p class="review-text">Спасибо за круглосуточное обслуживание! Попал с острой болью ночью, врач помог немедленно. Очень благодарен клинике Ер-Ана.</p>
                            <p class="review-author">Кайрат Мусин</p>
                            <p class="review-role">Пациент</p>
                        </div>

                        <div class="review-card">
                            <div class="review-quote">"</div>
                            <p class="review-text">Делал имплантацию. Весь процесс был безболезненным. Врач подробно объяснил каждый этап. Результат превосходит ожидания. Спасибо команде Ер-Ана!</p>
                            <p class="review-author">Гульжан Умарова</p>
                            <p class="review-role">Пациент</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Appointment Section -->
    <section id="appointment" class="appointment">
        <div class="container">
            <div class="appointment-content">
                <div class="appointment-left">
                    <h2>Запишитесь на приём</h2>
                    <p>Заполните форму, и наши менеджеры свяжутся с вами в течение 15 минут для подтверждения время приёма. Мы открыты 24/7.</p>
                </div>

                <form class="appointment-form" id="appointmentForm">
                    <div class="form-group">
                        <label for="name">Ваше имя</label>
                        <input type="text" id="name" name="name" placeholder="Введите ваше имя" required>
                    </div>

                    <div class="form-group">
                        <label for="service">Выбор услуги</label>
                        <select id="service" name="service" required>
                            <option value="">Выберите услугу</option>
                            <option value="Лечение кариеса">Лечение кариеса</option>
                            <option value="Коронки и мосты">Коронки и мосты</option>
                            <option value="Имплантация">Имплантация</option>
                            <option value="Брекеты">Брекеты и Invisalign</option>
                            <option value="Хирургия">Хирургия полости рта</option>
                            <option value="Детская">Детская стоматология</option>
                            <option value="Седация">Лечение во сне</option>
                            <option value="КТ">КТ 3D сканирование</option>
                        </select>
                    </div>

                    <div class="form-group">
                        <label for="message">Дополнительная информация</label>
                        <textarea id="message" name="message" placeholder="Расскажите о ваших жалобах или вопросах..."></textarea>
                    </div>

                    <button type="submit" class="form-submit">Отправить заявку</button>
                    <div class="form-message" id="formMessage"></div>
                </form>
            </div>
        </div>
    </section>

    <!-- Contacts Section -->
    <section id="contacts" class="contacts">
        <div class="container">
            <div class="section-header">
                <h2>Контакты и адреса</h2>
                <p>Посетите один из наших филиалов или свяжитесь с нами по телефону</p>
            </div>

            <div class="contacts-content">
                <div class="branches">
                    <div class="branch-card stagger-1">
                        <h3>Главное отделение</h3>
                        <div class="branch-item">
                            <i class="fas fa-map-marker-alt"></i>
                            <a href="https://www.google.com/maps/search/?api=1&query=%D1%83%D0%BB.+%D0%90%D0%BA%D0%BF%D0%B0%D0%BD+%D0%B1%D0%B0%D1%82%D1%8B%D1%80%D0%B0+108,+%D0%A8%D1%8B%D0%BC%D0%BA%D0%B5%D0%BD%D1%82" target="_blank" style="color: var(--navy); font-weight: 600; text-decoration: underline;">ул. Акпан батыра 108, Шымкент</a>
                        </div>
                        <div class="branch-item">
                            <i class="fas fa-phone"></i>
                            <a href="tel:+77053563838" style="color: var(--navy); font-weight: 600;">+7 705 356-38-38</a>
                        </div>
                        <div class="branch-item">
                            <i class="fas fa-clock"></i>
                            <span>24 часа в сутки, 7 дней в неделю</span>
                        </div>
                        <a href="https://wa.me/77029863043" target="_blank" class="branch-whatsapp">
                            <i class="fab fa-whatsapp"></i>
                            Написать в WhatsApp
                        </a>
                    </div>

                    <div class="branch-card stagger-2">
                        <h3>Филиал на проспекте Республики</h3>
                        <div class="branch-item">
                            <i class="fas fa-map-marker-alt"></i>
                            <a href="https://2gis.kz/shymkent/search/пр.%20Республики%2042" target="_blank" style="color: var(--navy); font-weight: 600; text-decoration: underline;">пр. Республики 42, Шымкент</a>
                        </div>
                        <div class="branch-item">
                            <i class="fas fa-phone"></i>
                            <a href="tel:+77053563838" style="color: var(--navy); font-weight: 600;">+7 705 356-38-38</a>
                        </div>
                        <div class="branch-item">
                            <i class="fas fa-clock"></i>
                            <span>9:00 - 22:00 (ежедневно)</span>
                        </div>
                        <a href="https://wa.me/77029863043" target="_blank" class="branch-whatsapp">
                            <i class="fab fa-whatsapp"></i>
                            Написать в WhatsApp
                        </a>
                    </div>
                </div>

                <div class="map-container">
                    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d620.1434170616742!2d69.6185104610227!3d42.32299343758882!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38a91e8032bcc58d%3A0xc79e8bab0ab26b66!2z0YPQu9C40YbQsCDQkNC60L_QsNC9INCR0LDRgtGL0YDQsCAxMDgsINCo0YvQvNC60LXQvdGC!5e0!3m2!1sru!2skz!4v1781378370668!5m2!1sru!2skz" width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-grid">
                <div class="footer-section">
                    <div class="footer-logo">
                        <i class="fas fa-tooth"></i>
                        <span>Ер-Ана</span>
                    </div>
                    <p style="color: rgba(255, 255, 255, 0.7); margin-bottom: 15px;">Современная стоматология и медицина в Шымкенте с опытом более 10 лет.</p>
                    <div class="footer-social">
                        <a href="https://wa.me/77029863043" target="_blank" class="social-icon">
                            <i class="fab fa-whatsapp"></i>
                        </a>
                        <a href="#" class="social-icon">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                        <a href="#" class="social-icon">
                            <i class="fab fa-instagram"></i>
                        </a>
                    </div>
                </div>

                <div class="footer-section">
                    <h4>Услуги</h4>
                    <ul>
                        <li><a href="#services">Стоматология</a></li>
                        <li><a href="#medical">Медицина</a></li>
                        <li><a href="#doctors">Врачи</a></li>
                        <li><a href="#appointment">Запись на приём</a></li>
                    </ul>
                </div>

                <div class="footer-section">
                    <h4>Компания</h4>
                    <ul>
                        <li><a href="#reviews">Отзывы</a></li>
                        <li><a href="#why-us">Почему мы</a></li>
                        <li><a href="#contacts">Контакты</a></li>
                        <li><a href="#">Политика конфиденциальности</a></li>
                    </ul>
                </div>

                <div class="footer-section">
                    <h4>Контакты</h4>
                    <ul>
                        <li><a href="tel:+77053563838">+7 705 356-38-38</a></li>
                        <li><a href="https://wa.me/77029863043" target="_blank">WhatsApp</a></li>
                        <li><a href="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d620.1434170616742!2d69.6185104610227!3d42.32299343758882!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38a91e8032bcc58d%3A0xc79e8bab0ab26b66!2z0YPQu9C40YbQsCDQkNC60L_QsNC9INCR0LDRgtGL0YDQsCAxMDgsINCo0YvQvNC60LXQvdGC!5e0!3m2!1sru!2skz!4v1781378370668!5m2!1sru!2skz" target="_blank" style="color: rgba(255, 255, 255, 0.8);">ул. Акпан батыра 108</a></li>
                        <li><span style="color: rgba(255, 255, 255, 0.7);">Шымкент, Казахстан</span></li>
                    </ul>
                </div>
            </div>

            <div class="footer-bottom">
                <p>&copy; 2024 Ер-Ана. Все права защищены. | Стоматология & Медицина Шымкент</p>
            </div>
        </div>
    </footer>

    <!-- WhatsApp Float Button -->
    <a href="https://wa.me/77029863043" target="_blank" class="whatsapp-float">
        <i class="fab fa-whatsapp"></i>
        <div class="whatsapp-tooltip">Написать нам</div>
    </a>

    <!-- Scroll to Top Button -->
    <button class="scroll-to-top" id="scrollToTop" onclick="scrollToTop()">
        <i class="fas fa-arrow-up"></i>
    </button>

    <!-- JSON-LD Schema -->
    <script type="application/ld+json">
    {
        "@context": "https://schema.org",
        "@type": "MedicalClinic",
        "name": "Ер-Ана",
        "url": "",
        "telephone": "+77053563838",
        "address": {
            "@type": "PostalAddress",
            "streetAddress": "ул. Акпан батыра 108",
            "addressLocality": "Шымкент",
            "addressCountry": "KZ"
        },
        "contactPoint": {
            "@type": "ContactPoint",
            "contactType": "Customer Service",
            "telephone": "+77053563838"
        },
        "areaServed": "KZ",
        "serviceType": ["Dentistry", "Medical Services"],
        "description": "Современная стоматология и комплексная медицина в Шымкенте"
    }
    </script>

    <script>
        // ===== Hamburger Menu =====
        const hamburger = document.getElementById('hamburger');
        const mobileMenu = document.getElementById('mobileMenu');

        hamburger.addEventListener('click', () => {
            hamburger.classList.toggle('active');
            mobileMenu.classList.toggle('active');
            document.body.style.overflow = mobileMenu.classList.contains('active') ? 'hidden' : 'auto';
        });

        document.querySelectorAll('.mobile-menu a').forEach(link => {
            link.addEventListener('click', () => {
                hamburger.classList.remove('active');
                mobileMenu.classList.remove('active');
                document.body.style.overflow = 'auto';
            });
        });

        // ===== Scroll to Top =====
        const scrollToTopBtn = document.getElementById('scrollToTop');

        window.addEventListener('scroll', () => {
            if (window.scrollY > 400) {
                scrollToTopBtn.classList.add('show');
            } else {
                scrollToTopBtn.classList.remove('show');
            }
        });

        function scrollToTop() {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // ===== Smooth Scroll Active Link =====
        const navLinks = document.querySelectorAll('.nav-links a');

        window.addEventListener('scroll', () => {
            let current = '';
            
            document.querySelectorAll('section').forEach(section => {
                const sectionTop = section.offsetTop;
                if (pageYOffset >= sectionTop - 200) {
                    current = section.getAttribute('id');
                }
            });

            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href').slice(1) === current) {
                    link.classList.add('active');
                }
            });
        });

        // ===== CountUp Animation =====
        const countUpElements = document.querySelectorAll('[data-countup]');

        const observerCountUp = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting && !entry.target.classList.contains('counted')) {
                    const target = parseInt(entry.target.dataset.countup);
                    let current = 0;
                    const increment = target / 50;

                    const counter = setInterval(() => {
                        current += increment;
                        if (current >= target) {
                            entry.target.textContent = target;
                            clearInterval(counter);
                        } else {
                            entry.target.textContent = Math.floor(current);
                        }
                    }, 30);

                    entry.target.classList.add('counted');
                }
            });
        }, { threshold: 0.5 });

        countUpElements.forEach(el => observerCountUp.observe(el));

        // ===== Reveal Animation =====
        const revealElements = document.querySelectorAll('[class*="stagger-"], .floating-card, [class*="reveal"]');

        const observerReveal = new IntersectionObserver((entries) => {
            entries.forEach((entry, index) => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.animation = `reveal 0.6s ease forwards`;
                }
            });
        }, { threshold: 0.1 });

        document.querySelectorAll('.service-card, .medical-mini-card, .why-item, .doctor-card, .branch-card').forEach(el => {
            observerReveal.observe(el);
        });

        // ===== Slider Navigation =====
        function scrollDoctors(direction) {
            const track = document.querySelector('.doctors-track');
            const scrollAmount = 320;

            if (direction === 'left') {
                track.scrollBy({ left: -scrollAmount, behavior: 'smooth' });
            } else {
                track.scrollBy({ left: scrollAmount, behavior: 'smooth' });
            }
        }

        // ===== Form Submission =====
        document.getElementById('appointmentForm')?.addEventListener('submit', (e) => {
            e.preventDefault();

            const formMessage = document.getElementById('formMessage');
            const form = document.getElementById('appointmentForm');

            // Get form data
            const name = document.getElementById('name').value;
            const service = document.getElementById('service').value;
            const message = document.getElementById('message').value;

            // Create WhatsApp message
            const whatsappMessage = `Здравствуйте!\n\nЯ хочу записаться на приём.\n\nИмя: ${name}\nУслуга: ${service}\nСообщение: ${message || 'Нет'}`;

            // Show success message
            formMessage.textContent = '✓ Спасибо! Перенаправляем в WhatsApp...';
            formMessage.classList.add('success');

            // Redirect to WhatsApp after 1 second
            setTimeout(() => {
                const encodedMessage = encodeURIComponent(whatsappMessage);
                window.open(`https://wa.me/77029863043?text=${encodedMessage}`, '_blank');

                // Reset form
                form.reset();
                formMessage.classList.remove('success');
                formMessage.textContent = '';
            }, 1000);
        });

        // ===== Initialize Services Grid =====
        document.addEventListener('DOMContentLoaded', () => {
            const serviceCards = document.querySelectorAll('.service-card');
            serviceCards.forEach((card, index) => {
                card.classList.add(`stagger-${index + 1}`);
            });
        });
    </script>

</body>
</html>
