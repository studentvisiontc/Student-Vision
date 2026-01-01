<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" type="image/png" href="https://studentvisiontc.github.io/SVTC-Images/SV%20Circle%20logo.png">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Roboto+Slab:wght@400;700;800;900&family=Inter:wght@400;500;600;700;800&family=Bebas+Neue&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <title>Student Vision - Dashboard Overview</title>
    <style>
        :root {
            --primary-blue: #00008B;
            --accent-yellow: #ffeb3b;
            --accent-orange: #ffa500;
            --bg-gray: #f4f7f9;
            --text-dark: #1e293b;
            --border-color: #e2e8f0;
            --white: #ffffff;
            --success-green: #16a34a;
            --live-gradient: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);
        }

        * { font-family: 'Inter', sans-serif; box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
        h1, h2, h3, .main-title { font-family: 'Roboto Slab', serif; }
        html, body { margin: 0; padding: 0; width: 100%; min-height: 100vh; overflow-x: hidden; }
        body { background-color: var(--bg-gray); color: var(--text-dark); display: flex; flex-direction: column; }

        header { 
            background: var(--primary-blue); 
            padding: 8px clamp(10px, 3vw, 25px); 
            display: flex; 
            justify-content: space-between; 
            align-items: center; 
            color: white; 
            width: 100%; 
            position: relative; 
            overflow: hidden; 
            min-height: 55px; 
            z-index: 100;
        }
        .header-scroll-bg { 
            position: absolute; 
            top: 0; left: 0; 
            width: 400%; height: 100%; 
            background: linear-gradient(to right, transparent 0%, rgba(255, 255, 255, 0.2) 5%, rgba(255, 255, 255, 0.6) 10%, rgba(255, 255, 255, 0.1) 15%, transparent 20%); 
            z-index: 1; 
            animation: scrollGlow 25s linear infinite; 
            opacity: 0.9; 
        }
        @keyframes scrollGlow { 0% { transform: translateX(-100%); } 100% { transform: translateX(25%); } }
        
        header .header-left, header .header-right, .header-corner, .header-corner-right { z-index: 10; }
        header .header-left { display: flex; align-items: center; gap: 10px; }
        header .logo { height: 34px; width: 34px; border-radius: 50%; border: 1.5px solid #ffffff; background: white; flex-shrink: 0; }
        header .main-title { font-size: clamp(11px, 2.8vw, 16px); font-weight: 900; line-height: 1.1; }
        header .sub-title { font-size: clamp(7.5px, 1.8vw, 10px); font-weight: 600; color: var(--accent-yellow); margin-top: 1px; }
        
        header .header-right { display: flex; gap: clamp(6px, 1.8vw, 12px); align-items: center; }
        .menu-item a { display: flex; flex-direction: column; align-items: center; text-decoration: none; color: white; transition: transform 0.2s; }
        header .icon { font-size: clamp(14px, 2.8vw, 18px); color: var(--accent-orange); }
        .icon-label { font-size: 6px; margin-top: 1px; font-weight: 800; text-transform: uppercase; letter-spacing: 0.2px; }
        
        .header-corner { position: absolute; top: 0; left: 0; height: 35px; opacity: 0.8; pointer-events: none; z-index: 15; }
        .header-corner-right { position: absolute; top: 0; right: 0; height: 35px; opacity: 0.8; transform: scaleX(-1); pointer-events: none; z-index: 15; }

        .vision-banner {
            width: 100%;
            height: 220px;
            background: linear-gradient(rgba(0, 0, 139, 0.5), rgba(0, 0, 139, 0.5)), url('https://studentvisiontc.github.io/SVTC-Images/BG%20TOP.jpeg');
            background-size: cover;
            background-position: center 20%;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: white;
            border-top: 4px solid var(--accent-orange);
            border-bottom: 4px solid var(--accent-orange);
        }
        .vision-content h2 {
            font-size: clamp(1.5rem, 4vw, 2.5rem);
            text-transform: uppercase;
            letter-spacing: 2px;
            margin: 0;
            text-shadow: 2px 2px 10px rgba(0,0,0,0.5);
        }
        .vision-content p {
            font-size: clamp(0.8rem, 2vw, 1.1rem);
            color: var(--accent-yellow);
            font-weight: 600;
            margin-top: 5px;
        }

        .why-learn-section {
            padding: 50px 8%;
            background: white;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            border-bottom: 1px solid var(--border-color);
        }
        .why-learn-box {
            padding: 30px;
            border-radius: 20px;
            background: #f8fafc;
            border-top: 5px solid var(--primary-blue);
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
        }
        .why-learn-box.alt { border-top-color: var(--accent-orange); }
        .why-learn-box h3 {
            color: var(--primary-blue);
            font-size: 22px;
            margin-bottom: 15px;
            text-transform: uppercase;
            display: flex;
            align-items: center;
            gap: 12px;
        }
        .why-learn-box h3 i { color: var(--accent-orange); }
        .why-learn-box p {
            font-size: 14px;
            line-height: 1.8;
            color: #475569;
            font-weight: 500;
            text-align: justify;
        }

        .class-offer-section {
            padding: 30px 0;
            background: white;
            text-align: center;
            border-bottom: 1px solid var(--border-color);
        }
        .class-offer-title {
            font-size: 18px;
            font-weight: 800;
            color: var(--primary-blue);
            text-transform: uppercase;
            margin-bottom: 20px;
            letter-spacing: 0.5px;
        }
        .class-scroller {
            width: 100%;
            overflow: hidden;
            white-space: nowrap;
            padding: 10px 0;
        }
        .class-track {
            display: flex;
            gap: 25px;
            width: max-content;
            animation: slowScroll 40s linear infinite;
        }
        .class-circle {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, var(--primary-blue), #1e40af);
            color: white;
            border-radius: 50%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            font-weight: 800;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(0,0,139,0.2);
            transition: transform 0.3s, border-color 0.3s;
            border: 3px solid transparent;
            flex-shrink: 0;
        }
        .class-circle span { font-size: 14px; display: block; }
        .class-circle small { font-size: 8px; text-transform: uppercase; opacity: 0.9; }
        .class-circle:hover {
            transform: scale(1.1);
            border-color: var(--accent-orange);
            background: var(--accent-orange);
            color: var(--primary-blue);
        }
        @keyframes slowScroll {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }

        .entrance-exams-section {
            padding: 60px 5%;
            background: #ffffff;
            border-bottom: 1px solid var(--border-color);
        }
        .entrance-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
            max-width: 1200px;
            margin: 0 auto;
        }
        .entrance-card {
            background: var(--bg-gray);
            border-radius: 15px;
            padding: 25px;
            border-left: 6px solid var(--primary-blue);
            transition: transform 0.3s;
        }
        .entrance-card:hover { transform: translateY(-5px); }
        .entrance-card h3 { 
            color: var(--primary-blue); 
            font-size: 18px; 
            margin-bottom: 15px; 
            display: flex; 
            align-items: center; 
            gap: 10px; 
        }
        .entrance-card h3 i { color: var(--accent-orange); }
        .exam-list { list-style: none; padding: 0; margin: 0; }
        .exam-list li { 
            font-size: 13px; 
            padding: 8px 0; 
            border-bottom: 1px solid rgba(0,0,0,0.05); 
            display: flex; 
            justify-content: space-between; 
            font-weight: 600; 
        }
        .exam-list li span { color: var(--primary-blue); }
        .syllabus-box {
            background: var(--primary-blue);
            color: white;
            border-radius: 15px;
            padding: 25px;
        }
        .syllabus-box h3 { color: var(--accent-yellow); font-size: 18px; margin-bottom: 15px; }
        .subject-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
        .subject-item { 
            background: rgba(255,255,255,0.1); 
            padding: 8px 12px; 
            border-radius: 6px; 
            font-size: 12px; 
            font-weight: 700; 
            display: flex; 
            align-items: center; 
            gap: 8px; 
        }
        .syllabus-points { margin-top: 15px; font-size: 11px; line-height: 1.6; color: rgba(255,255,255,0.8); }

        .performance-section {
            padding: 50px 5%;
            background: linear-gradient(135deg, #ffffff 0%, #f1f5f9 100%);
            border-bottom: 1px solid var(--border-color);
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            align-items: center;
        }
        .tc-score-display {
            background: white;
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.05);
            text-align: center;
            border-top: 5px solid var(--accent-orange);
        }
        .tc-score-circle {
            width: 150px;
            height: 150px;
            margin: 0 auto 20px;
            border-radius: 50%;
            border: 10px solid var(--bg-gray);
            border-top-color: var(--accent-orange);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            animation: rotateScore 2s ease-out forwards;
        }
        .tc-score-circle h3 { font-size: 42px; margin: 0; color: var(--primary-blue); font-weight: 900; }
        .tc-score-circle span { font-size: 10px; font-weight: 800; text-transform: uppercase; color: var(--accent-orange); }
        
        .performance-info h2 { font-size: 28px; color: var(--primary-blue); margin-bottom: 15px; text-transform: uppercase; }
        .performance-info p { font-size: 14px; line-height: 1.6; color: #475569; margin-bottom: 20px; }
        .skill-tags { display: flex; flex-wrap: wrap; gap: 10px; }
        .skill-tag { background: var(--primary-blue); color: white; padding: 6px 15px; border-radius: 40px; font-size: 11px; font-weight: 700; text-transform: uppercase; border: 1px solid var(--accent-yellow); }
        
        .cert-preview {
            background: white;
            padding: 20px;
            border-radius: 15px;
            border: 2px dashed var(--accent-orange);
            display: flex;
            align-items: center;
            gap: 20px;
            margin-top: 20px;
        }
        .cert-icon { font-size: 40px; color: var(--accent-orange); }
        .cert-details h4 { margin: 0; font-size: 14px; color: var(--primary-blue); }
        .cert-details p { margin: 5px 0 0; font-size: 11px; }

        .stats-section {
            padding: 40px 5%;
            background: linear-gradient(to right, #00008B, #000044);
            color: white;
            text-align: center;
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            gap: 20px;
            border-bottom: 4px solid var(--accent-orange);
        }
        .stat-item { flex: 1; min-width: 150px; padding: 20px; border: 1px solid rgba(255,255,255,0.1); border-radius: 15px; background: rgba(255,255,255,0.05); }
        .stat-item h4 { font-size: 32px; color: var(--accent-yellow); margin: 0; font-weight: 900; }
        .stat-item p { font-size: 12px; text-transform: uppercase; font-weight: 700; margin-top: 5px; opacity: 0.8; }

        .action-buttons-section {
            padding: 60px 5%;
            background: #ffffff;
            border-bottom: 1px solid var(--border-color);
            text-align: center;
        }
        .action-grid {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            max-width: 1200px;
            margin: 0 auto;
        }
        .action-btn {
            flex: 1;
            min-width: 300px;
            padding: 25px 20px;
            border-radius: 20px;
            text-decoration: none;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 10px;
            font-weight: 800;
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            position: relative;
            overflow: hidden;
            border: 2px solid transparent;
        }
        .action-btn i { font-size: 35px; margin-bottom: 5px; }
        .action-btn span { font-size: 20px; text-transform: uppercase; letter-spacing: 1px; }
        .action-btn small { font-size: 10px; opacity: 0.8; font-weight: 600; }

        .register-btn { 
            background: linear-gradient(135deg, #ff9800, #f57c00); 
            color: white; 
            box-shadow: 0 10px 20px rgba(245, 124, 0, 0.3);
        }
        .login-btn { 
            background: linear-gradient(135deg, #00008B, #0000cd); 
            color: white;
            box-shadow: 0 10px 20px rgba(0, 0, 139, 0.3);
        }
        .pricing-btn { 
            background: linear-gradient(135deg, #2e7d32, #1b5e20); 
            color: white;
            box-shadow: 0 10px 20px rgba(46, 125, 50, 0.3);
        }

        .action-btn:hover {
            transform: translateY(-12px) scale(1.02);
            box-shadow: 0 20px 35px rgba(0,0,0,0.2);
            border-color: var(--accent-yellow);
        }

        .school-demo-section {
            padding: 80px 5%;
            background: #f8fafc;
            border-bottom: 1px solid var(--border-color);
        }
        .school-column-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            max-width: 1300px;
            margin: 40px auto 0;
        }
        .school-row-card {
            background: white;
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            border-left: 5px solid var(--primary-blue);
            display: flex;
            flex-direction: column;
            gap: 10px;
            transition: 0.3s;
            position: relative;
        }
        .school-row-card:hover { transform: scale(1.03); box-shadow: 0 10px 25px rgba(0,0,0,0.1); }
        .school-row-card.private { border-left-color: var(--accent-orange); }
        .school-row-card.public { border-left-color: var(--success-green); }
        
        .school-badge { 
            align-self: flex-start; 
            font-size: 9px; 
            padding: 3px 10px; 
            border-radius: 4px; 
            font-weight: 800; 
            text-transform: uppercase; 
        }
        .badge-govt { background: #dcfce7; color: #166534; }
        .badge-priv { background: #fff7ed; color: #9a3412; }
        
        .school-info h4 { margin: 5px 0; font-size: 15px; color: var(--primary-blue); font-weight: 900; }
        .school-loc { font-size: 11px; color: #64748b; font-weight: 700; display: flex; align-items: center; gap: 5px; }
        .school-status { 
            margin-top: 10px; 
            font-size: 10px; 
            font-weight: 800; 
            color: var(--success-green); 
            display: flex; 
            align-items: center; 
            gap: 6px; 
            background: #f0fdf4; 
            padding: 5px 10px; 
            border-radius: 6px; 
        }

        /* UPDATED SOCIAL MEDIA SECTION STYLES */
        .social-promo-section {
            padding: 50px 5%;
            background: #ffffff;
            border-bottom: 1px solid var(--border-color);
            text-align: center;
        }
        .social-promo-grid {
            display: flex;
            justify-content: center;
            gap: clamp(10px, 2vw, 25px);
            flex-wrap: wrap;
            max-width: 1200px;
            margin: 30px auto 0;
        }
        .social-promo-card {
            flex: 1;
            min-width: clamp(100px, 25vw, 280px);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: clamp(8px, 1.5vw, 20px);
            padding: clamp(15px, 2vw, 25px);
            border-radius: 12px;
            text-decoration: none;
            transition: 0.3s;
            color: white;
            position: relative;
            overflow: hidden;
        }
        .social-promo-card.youtube { background: linear-gradient(135deg, #FF0000, #b20000); }
        .social-promo-card.facebook { background: linear-gradient(135deg, #1877F2, #0e52a5); }
        .social-promo-card.insta { background: linear-gradient(45deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%); }
        
        .social-promo-card:hover { transform: translateY(-8px); filter: brightness(1.1); box-shadow: 0 10px 20px rgba(0,0,0,0.15); }
        .social-promo-card i { font-size: clamp(24px, 4vw, 40px); }
        .social-promo-card div { text-align: left; }
        .social-promo-card h3 { margin: 0; font-size: clamp(14px, 2.2vw, 20px); text-transform: uppercase; font-weight: 900; }
        .social-promo-card p { margin: 2px 0 0; font-size: clamp(8px, 1.1vw, 11px); font-weight: 700; opacity: 0.9; display: block; }

        .fame-box { padding: 25px 5%; background: white; width: 100%; border-bottom: 1px solid var(--border-color); position: relative; overflow: hidden; }
        .fame-track { display: flex; gap: 15px; width: max-content; animation: liveScroll 85s linear infinite; padding: 10px 0; }
        
        .topper-unit { 
            background: white; 
            border: 2px solid #bae6fd; 
            width: 290px; 
            min-height: 330px; 
            flex-shrink: 0; 
            display: flex; 
            flex-direction: column; 
            align-items: center; 
            justify-content: center; 
            text-align: center; 
            position: relative; 
            overflow: hidden; 
            border-radius: 15px;
            background-image: linear-gradient(135deg, #fff 0%, #fff 40%, rgba(255, 215, 0, 0.1) 50%, #fff 60%, #fff 100%);
            background-size: 200% 200%;
            animation: goldScrollBG 5s infinite linear;
        }
        @keyframes goldScrollBG { 0% { background-position: -100% -100%; } 100% { background-position: 100% 100%; } }

        .rank-badge { position: absolute; top: 10px; left: 10px; background: linear-gradient(135deg, var(--primary-blue), #3b82f6); color: white; padding: 4px 10px; border-radius: 6px; font-size: 9px; font-weight: 900; z-index: 10; text-transform: uppercase; box-shadow: 0 2px 5px rgba(0,0,0,0.1); }
        .topper-photo { width: 75px; height: 75px; border-radius: 50%; border: 3px solid var(--accent-orange); object-fit: cover; margin-bottom: 12px; z-index: 5; position: relative; }
        .topper-score { font-size: 13px; font-weight: 900; color: var(--success-green); background: #f0fdf4; padding: 6px 15px; border-radius: 40px; margin-top: 8px; border: 1px solid var(--success-green); width: 80%; z-index: 5; position: relative; }
        .congrats-txt { font-size: 18px; font-weight: 900; font-family: 'Bebas Neue', cursive; letter-spacing: 1.5px; margin-bottom: 8px; background: linear-gradient(135deg, #d00000 0%, #ffa500 50%, #d00000 100%); -webkit-background-clip: text; -webkit-text-fill-color: transparent; animation: congratsShine 3s linear infinite, congratsPulse 1.5s ease-in-out infinite alternate; z-index: 5; position: relative; }

        .card-firework-container { position: absolute; top: 0; left: 0; width: 100%; height: 100%; pointer-events: none; z-index: 1; }
        .mini-rocket { position: absolute; bottom: -20px; width: 2px; height: 10px; background: var(--accent-orange); opacity: 0; animation: rocketFlight 3s infinite; }
        .mini-burst { position: absolute; width: 2px; height: 2px; border-radius: 50%; opacity: 0; animation: burstPop 3s infinite; }
        
        @keyframes rocketFlight { 0% { transform: translateY(0); opacity: 0; } 10% { opacity: 1; } 50% { transform: translateY(-150px); opacity: 1; } 51% { opacity: 0; } 100% { opacity: 0; } }
        @keyframes burstPop { 0%, 50% { opacity: 0; transform: scale(0); } 55% { opacity: 1; transform: scale(1.5); box-shadow: 0 0 10px var(--accent-yellow), 0 0 20px var(--accent-orange); } 70% { opacity: 0; transform: scale(3); } 100% { opacity: 0; } }
        @keyframes liveScroll { 0% { transform: translateX(0); } 100% { transform: translateX(-50%); } }
        @keyframes congratsShine { 0% { background-position: 0% 50%; } 100% { background-position: 100% 50%; } }
        @keyframes congratsPulse { from { transform: scale(1); } to { transform: scale(1.05); } }

        main { width: 100%; overflow: hidden; min-height: 200px; }

        footer { background: var(--primary-blue); color: white; padding: 15px 20px; border-top: 3px solid var(--accent-orange); margin-top: auto; width: 100%; }
        .footer-content { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px; max-width: 1450px; margin: 0 auto; text-align: left; }
        .footer-column { display: flex; flex-direction: column; }
        .footer-column h4 { color: var(--accent-yellow); border-bottom: 1px solid var(--accent-yellow); display: inline-block; margin-bottom: 12px; font-weight: 900; font-size: 12px; text-transform: uppercase; align-self: flex-start; }
        .footer-column p, .footer-column a { font-size: 10.5px; color: rgba(255,255,255,0.9); text-decoration: none; display: flex; align-items: center; gap: 8px; margin-bottom: 6px; line-height: 1.4; font-weight: 600; }
        .social-icons { display: flex; gap: 10px; margin: 5px 0; }
        .social-icons a { font-size: 18px; color: white; }

        @media (max-width: 850px) {
            header { flex-direction: column; height: auto; padding: 8px 10px; text-align: center; gap: 5px; }
            header .header-left { flex-direction: column; align-items: center; width: 100%; gap: 3px; }
            header .header-right { border-top: 1px solid rgba(255, 255, 255, 0.1); width: 100%; justify-content: center; padding-top: 5px; flex-wrap: wrap; }
            .footer-content { grid-template-columns: 1fr; text-align: center; }
            .footer-column { align-items: center; }
            .footer-column h4 { align-self: center; }
            .vision-banner { height: 180px; }
            .action-btn { min-width: 100%; }
            .why-learn-section { grid-template-columns: 1fr; padding: 30px 5%; gap: 20px; }
            .social-promo-card p { display: none; }
        }
    </style>
</head>
<body>

<header>
    <div class="header-scroll-bg"></div>
    <img src="https://studentvisiontc.github.io/SVTC-Images/hh%20logo.png" class="header-corner">
    <img src="https://studentvisiontc.github.io/SVTC-Images/hh%20logo.png" class="header-corner-right">
    <div class="header-left">
        <img src="https://studentvisiontc.github.io/SVTC-Images/SV%20Circle%20logo.png" alt="SV Logo" class="logo">
        <div>
            <div class="main-title">Student Vision Talent Competition</div>
            <div class="sub-title">“See Your Success”</div>
        </div>
    </div>
    <div class="header-right">
        <div class="menu-item"><a href="#"><i class="fa-solid fa-house icon"></i><span class="icon-label">Home</span></a></div>
        <div class="menu-item"><a href="#"><i class="fa-solid fa-user-plus icon"></i><span class="icon-label">Register</span></a></div>
        <div class="menu-item"><a href="#"><i class="fa-solid fa-right-to-bracket icon"></i><span class="icon-label">Login</span></a></div>
        <div class="menu-item"><a href="#"><i class="fa-solid fa-user-tie icon"></i><span class="icon-label">Admin</span></a></div>
        <div class="menu-item"><a href="#"><i class="fa-solid fa-tags icon"></i><span class="icon-label">Pricing</span></a></div>
    </div>
</header>

<main>
    <div class="vision-banner">
        <div class="vision-content">
            <h2>Our Vision Student Success</h2>
            <p>Empowering minds with knowledge and books</p>
        </div>
    </div>

    <section class="why-learn-section">
        <div class="why-learn-box">
            <h3><i class="fa-solid fa-lightbulb"></i> Why Students Should Learn?</h3>
            <p>Learning is the ultimate key to unlocking a world of endless possibilities. In an ever-evolving era, knowledge empowers young minds to think critically, solve complex problems, and build a solid foundation for their future careers. It’s about more than just grades; it’s about nurturing curiosity and developing the wisdom to navigate the challenges of tomorrow with confidence.</p>
        </div>
        <div class="why-learn-box alt">
            <h3><i class="fa-solid fa-star"></i> Why Learn From Us?</h3>
            <p>At Student Vision, we go beyond traditional textbooks to provide a holistic competitive environment. We prepare students for All India level entrance exams with a unique focus on skill mapping and our proprietary TC Score. By combining academic rigor with real-world talent tracking, we ensure that every student recognizes their true potential and achieves measurable success in their educational journey.</p>
        </div>
    </section>

    <section class="class-offer-section">
        <div class="class-offer-title">We offer to improve the knowledge of these people</div>
        <div class="class-scroller">
            <div class="class-track" id="classTrack">
                <script>
                    const classes = ["10th", "9th", "8th", "7th", "6th", "5th", "4th", "3rd"];
                    const track = document.getElementById('classTrack');
                    function createClassBtn(c) {
                        return `<div class="class-circle"><span>${c}</span><small>Class</small></div>`;
                    }
                    let content = classes.map(createClassBtn).join('');
                    track.innerHTML = content + content + content;
                </script>
            </div>
        </div>
    </section>

    <section class="entrance-exams-section">
        <div style="text-align:center; margin-bottom:40px;">
            <h2 style="color:var(--primary-blue); font-size:28px; text-transform:uppercase;">All India Entrance Exams (Class 3-10)</h2>
            <p style="color:#64748b; font-weight:600;">Comprehensive coverage for competitive excellence</p>
        </div>
        
        <div class="entrance-grid">
            <div class="entrance-card">
                <h3><i class="fa-solid fa-school"></i> National Entrance Exams</h3>
                <ul class="exam-list">
                    <li>Sainik School Entrance (AISSEE) <span>Class 6 & 9</span></li>
                    <li>Jawahar Navodaya Vidyalaya (JNVST) <span>Class 6 & 9</span></li>
                    <li>Rashtriya Military School (RMS) <span>Class 6 & 9</span></li>
                    <li>RIMC Dehradun Entrance <span>Class 8</span></li>
                    <li>Olympiads (IMO, NSO, IEO) <span>Class 3-10</span></li>
                    <li>NTSE & NMMS Exams <span>Class 8-10</span></li>
                </ul>
            </div>

            <div class="syllabus-box">
                <h3><i class="fa-solid fa-book-open"></i> Subjects & Syllabus Covered</h3>
                <div class="subject-grid">
                    <div class="subject-item"><i class="fa-solid fa-calculator"></i> Mathematics</div>
                    <div class="subject-item"><i class="fa-solid fa-atom"></i> Science (P, C, B)</div>
                    <div class="subject-item"><i class="fa-solid fa-brain"></i> Mental Ability</div>
                    <div class="subject-item"><i class="fa-solid fa-language"></i> English Grammar</div>
                    <div class="subject-item"><i class="fa-solid fa-earth-americas"></i> Social Studies</div>
                    <div class="subject-item"><i class="fa-solid fa-lightbulb"></i> Gen. Knowledge</div>
                </div>
                <div class="syllabus-points">
                    • Foundation & Concept building for all subjects.<br>
                    • Intensive training for logical and verbal reasoning.<br>
                    • Advanced problem-solving techniques for competitive speed.<br>
                    • Detailed mock tests based on latest All India exam patterns.
                </div>
            </div>
        </div>
    </section>

    <section class="performance-section">
        <div class="tc-score-display">
            <div class="tc-score-circle">
                <span style="font-size: 12px; margin-bottom: 5px;">Your Index</span>
                <h3>850</h3>
                <span>TC Score</span>
            </div>
            <div style="font-weight: 800; color: var(--primary-blue); font-size: 18px; margin-top: 15px;">Vision Intelligence Report</div>
            <p style="font-size: 11px; margin-top: 10px;">Proprietary AI-driven talent mapping for every student.</p>
        </div>

        <div class="performance-info">
            <h2>Maintain Talent Records & Skills</h2>
            <p>We provide a comprehensive <b>TC Score</b> to maintain detailed student talent records. Our platform doesn't just track marks; it evaluates skill proficiency across various domains to prove student performance excellence.</p>
            
            <div class="skill-tags">
                <div class="skill-tag">Logical Reasoning</div>
                <div class="skill-tag">Analytical Thinking</div>
                <div class="skill-tag">Time Management</div>
                <div class="skill-tag">Subject Mastery</div>
                <div class="skill-tag">Accuracy</div>
            </div>

            <div class="cert-preview">
                <div class="cert-icon"><i class="fa-solid fa-certificate"></i></div>
                <div class="cert-details">
                    <h4>Student Performance Certificate</h4>
                    <p>Earn a verified digital certificate validating all your academic and creative skills.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="stats-section">
        <div class="stat-item">
            <h4>150+</h4>
            <p>Today Joined</p>
        </div>
        <div class="stat-item">
            <h4>4.2k+</h4>
            <p>This Month Joined</p>
        </div>
        <div class="stat-item">
            <h4>50k+</h4>
            <p>Total Joined Persons</p>
        </div>
    </section>

    <section class="action-buttons-section">
        <div class="action-grid">
            <a href="#" class="action-btn register-btn">
                <i class="fa-solid fa-user-plus"></i>
                <span>Register Now</span>
                <small>Create your student profile</small>
            </a>
            <a href="#" class="action-btn login-btn">
                <i class="fa-solid fa-unlock-keyhole"></i>
                <span>Student Login</span>
                <small>Access your dashboard</small>
            </a>
            <a href="#" class="action-btn pricing-btn">
                <i class="fa-solid fa-gem"></i>
                <span>View Pricing</span>
                <small>Explore premium plans</small>
            </a>
        </div>
    </section>

    <div class="fame-box">
        <div style="border-left: 5px solid var(--accent-orange); padding-left: 15px; margin-bottom: 10px;">
            <span style="font-size:16px; font-weight:900; color:var(--primary-blue); text-transform:uppercase; letter-spacing:1px;">SVTC State Level Toppers</span>
        </div>
        <div style="width: 100%; overflow: hidden;">
            <div class="fame-track">
                <script>
                    const logoFallback = "https://studentvisiontc.github.io/SVTC-Images/SV%20Circle%20logo.png";
                    const topStars = [
                        { name: "Rohan Sharma", class: "3rd Class", school: "Holy Cross High School", city: "Hyderabad", uid: "SVTC_03_001", score: "99/100", photo: "" },
                        { name: "Ananya Reddy", class: "4th Class", school: "Little Angels EM School", city: "Visakhapatnam", uid: "SVTC_04_023", score: "98/100", photo: "" },
                        { name: "P. Karthik", class: "5th Class", school: "Sri Chaitanya School", city: "Vijayawada", uid: "SVTC_05_102", score: "97/100", photo: "" },
                        { name: "Sneha Latha", class: "6th Class", school: "Narayana Olympiad", city: "Guntur", uid: "SVTC_06_056", score: "96/100", photo: "" },
                        { name: "Vikas Kumar", class: "7th Class", school: "Government High School", city: "Tirupati", uid: "SVTC_07_089", score: "95/100", photo: "" }
                    ];

                    function renderStar(p) {
                        return `
                        <div class="topper-unit">
                            <div class="rank-badge">1st Rank</div>
                            <div class="card-firework-container">
                                <div class="mini-rocket" style="left: 20%; animation-delay: 0s;"></div>
                                <div class="mini-burst" style="left: 20%; top: 30%; animation-delay: 1.5s;"></div>
                                <div class="mini-rocket" style="left: 50%; animation-delay: 1.5s;"></div>
                                <div class="mini-burst" style="left: 50%; top: 20%; animation-delay: 3s;"></div>
                                <div class="mini-rocket" style="left: 80%; animation-delay: 0.5s;"></div>
                                <div class="mini-burst" style="left: 80%; top: 40%; animation-delay: 2s;"></div>
                            </div>
                            
                            <div class="congrats-txt">CONGRATULATIONS!</div>
                            <img src="${p.photo || logoFallback}" class="topper-photo" onerror="this.src='${logoFallback}'">
                            
                            <div style="font-size: 16px; font-weight: 900; color: var(--primary-blue); margin-bottom: 4px; z-index: 5;">${p.name}</div>
                            <div style="font-family: 'Inter'; font-size: 9px; font-weight: 800; color: var(--accent-orange); margin-bottom: 6px; z-index: 5; text-transform: uppercase;">${p.uid}</div>
                            <div style="font-size: 12px; font-weight: 800; color: #475569; margin-bottom: 4px; z-index: 5;">${p.class}</div>
                            <div style="font-size: 10px; font-weight: 700; color: #64748b; margin-bottom: 2px; z-index: 5;">${p.school}</div>
                            <div style="font-size: 9px; font-weight: 800; color: #94a3b8; text-transform: uppercase; margin-bottom: 8px; z-index: 5;">${p.city}</div>
                            
                            <div class="topper-score">Score: ${p.score}</div>
                        </div>`;
                    }
                    let fameHtml = topStars.map(p => renderStar(p)).join('');
                    document.write(fameHtml + fameHtml);
                </script>
            </div>
        </div>
    </div>

    <section class="school-demo-section">
        <div style="border-left: 5px solid var(--accent-orange); padding-left: 15px; text-align: left; max-width: 1300px; margin: 0 auto 30px;">
            <h2 style="color:var(--primary-blue); font-size:26px; text-transform:uppercase; margin:0;">School Demo Program & Success Partners</h2>
            <p style="color:#64748b; font-weight:700; font-size:14px; margin-top:5px;">Successfully completed demo sessions across various districts</p>
        </div>
        
        <div class="school-column-grid">
            <div class="school-row-card public">
                <span class="school-badge badge-govt">Public High School</span>
                <div class="school-info">
                    <h4>Z.P.H.S (High School)</h4>
                    <div class="school-loc"><i class="fa-solid fa-location-dot"></i> Nandyala District</div>
                </div>
                <div class="school-status"><i class="fa-solid fa-circle-check"></i> Completed Demo 2 Supporter</div>
            </div>

            <div class="school-row-card private">
                <span class="school-badge badge-priv">Private School</span>
                <div class="school-info">
                    <h4>Keshava Reddy EM School</h4>
                    <div class="school-loc"><i class="fa-solid fa-location-dot"></i> Kurnool District</div>
                </div>
                <div class="school-status"><i class="fa-solid fa-circle-check"></i> Completed Demo 2 Supporter</div>
            </div>

            <div class="school-row-card private">
                <span class="school-badge badge-priv">Private High School</span>
                <div class="school-info">
                    <h4>Narayana Olympiad Academy</h4>
                    <div class="school-loc"><i class="fa-solid fa-location-dot"></i> Kadapa District</div>
                </div>
                <div class="school-status"><i class="fa-solid fa-circle-check"></i> Completed Demo 2 Supporter</div>
            </div>

            <div class="school-row-card public">
                <span class="school-badge badge-govt">Govt High School</span>
                <div class="school-info">
                    <h4>G.H.S (Boys & Girls)</h4>
                    <div class="school-loc"><i class="fa-solid fa-location-dot"></i> Anantapur & Chittoor</div>
                </div>
                <div class="school-status"><i class="fa-solid fa-circle-check"></i> Completed Demo 2 Supporter</div>
            </div>

            <div class="school-row-card private">
                <span class="school-badge badge-priv">Private School</span>
                <div class="school-info">
                    <h4>Sri Chaitanya Techno School</h4>
                    <div class="school-loc"><i class="fa-solid fa-location-dot"></i> Guntur District</div>
                </div>
                <div class="school-status"><i class="fa-solid fa-circle-check"></i> Completed Demo 2 Supporter</div>
            </div>

            <div class="school-row-card public">
                <span class="school-badge badge-govt">Public High School</span>
                <div class="school-info">
                    <h4>Z.P.H.S High School</h4>
                    <div class="school-loc"><i class="fa-solid fa-location-dot"></i> Krishna District</div>
                </div>
                <div class="school-status"><i class="fa-solid fa-circle-check"></i> Completed Demo 2 Supporter</div>
            </div>

            <div class="school-row-card public">
                <span class="school-badge badge-govt">Public School</span>
                <div class="school-info">
                    <h4>Municipal High School</h4>
                    <div class="school-loc"><i class="fa-solid fa-location-dot"></i> Vizag & Vizianagaram</div>
                </div>
                <div class="school-status"><i class="fa-solid fa-circle-check"></i> Completed Demo 2 Supporter</div>
            </div>

            <div class="school-row-card private">
                <span class="school-badge badge-priv">Private High School</span>
                <div class="school-info">
                    <h4>Vikas English Medium School</h4>
                    <div class="school-loc"><i class="fa-solid fa-location-dot"></i> Nellore District</div>
                </div>
                <div class="school-status"><i class="fa-solid fa-circle-check"></i> Completed Demo 2 Supporter</div>
            </div>
        </div>
        
        <button class="pricing-btn" style="margin-top: 50px; padding: 18px 45px; border-radius: 50px; border:none; cursor:pointer; font-weight:900; text-transform:uppercase; box-shadow:0 8px 20px rgba(0,0,0,0.2); transition: 0.3s;">Book Your School Demo Now</button>
    </section>

    <!-- UPDATED SOCIAL MEDIA SECTION -->
    <section class="social-promo-section">
        <div style="border-left: 5px solid var(--accent-orange); padding-left: 15px; text-align: left; max-width: 1200px; margin: 0 auto 30px;">
            <h2 style="color:var(--primary-blue); font-size:24px; text-transform:uppercase; margin:0;">Follow Our Social Media</h2>
            <p style="color:#64748b; font-weight:700; font-size:13px; margin-top:5px;">Stay connected for educational updates & regular class alerts</p>
        </div>
        
        <div class="social-promo-grid">
            <a href="#" class="social-promo-card youtube">
                <i class="fab fa-youtube"></i>
                <div>
                    <h3>YouTube</h3>
                    <p>Free Classes</p>
                </div>
            </a>
            <a href="#" class="social-promo-card facebook">
                <i class="fab fa-facebook"></i>
                <div>
                    <h3>Facebook</h3>
                    <p>Community</p>
                </div>
            </a>
            <a href="#" class="social-promo-card insta">
                <i class="fab fa-instagram"></i>
                <div>
                    <h3>Instagram</h3>
                    <p>Updates</p>
                </div>
            </a>
        </div>
    </section>
</main>

<footer>
    <div class="footer-content">
        <div class="footer-column">
            <h4><i class="fa-solid fa-headset"></i> Support</h4>
            <p><i class="fa-solid fa-phone"></i> +91 8985170500</p>
            <p><i class="fa-solid fa-envelope"></i> contact.studentvision@gmail.com</p>
        </div>
        <div class="footer-column">
            <h4><i class="fa-solid fa-link"></i> Quick Links</h4>
            <a href="#"><i class="fa-solid fa-circle-info"></i> About Us</a>
            <a href="#"><i class="fa-solid fa-shield-halved"></i> Privacy Policy</a>
        </div>
        <div class="footer-column">
            <h4><i class="fa-solid fa-share-nodes"></i> Follow Us</h4>
            <div class="social-icons">
                <a href="#"><i class="fab fa-whatsapp"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="fab fa-youtube"></i></a>
                <a href="#"><i class="fab fa-facebook"></i></a>
            </div>
            <p style="opacity: 0.7; font-size: 10px;">&copy; 2025 Student Vision TC. All rights reserved.</p>
        </div>
    </div>
</footer>

</body>
</html>
