<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Khaleej Telecom - Leading Telecom Solutions</title>
    
    <link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 512 512'%3E%3Cdefs%3E%3ClinearGradient id='g' x1='0%25' y1='0%25' x2='100%25' y2='100%25'%3E%3Cstop offset='0%25' style='stop-color:%23ff9500'/%3E%3Cstop offset='100%25' style='stop-color:%23ff6b00'/%3E%3C/linearGradient%3E%3C/defs%3E%3Ccircle cx='256' cy='256' r='240' fill='url(%23g)' stroke='%23fff' stroke-width='20'/%3E%3Ccircle cx='256' cy='256' r='180' fill='none' stroke='%23fff' stroke-width='15'/%3E%3Cellipse cx='256' cy='256' rx='180' ry='80' fill='none' stroke='%23fff' stroke-width='12'/%3E%3Cellipse cx='256' cy='256' rx='80' ry='180' fill='none' stroke='%23fff' stroke-width='12'/%3E%3Cline x1='76' y1='256' x2='436' y2='256' stroke='%23fff' stroke-width='12'/%3E%3Cline x1='256' y1='76' x2='256' y2='436' stroke='%23fff' stroke-width='12'/%3E%3Cpath d='M 150 150 Q 256 256 362 150' stroke='%23fff' stroke-width='12' fill='none'/%3E%3Cpath d='M 150 362 Q 256 256 362 362' stroke='%23fff' stroke-width='12' fill='none'/%3E%3C/svg%3E" type="image/svg+xml">
    <meta name="theme-color" content="#ff9500">
    <meta name="description" content="Khaleej Telecom - Leading telecommunications and technology solutions provider across the Gulf region. Connecting businesses and communities through innovation.">

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: #000;
            overflow-x: hidden;
        }

        .main-container {
            position: relative;
            width: 100%;
            height: 100vh;
            overflow: hidden;
        }

        .bg-slider {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 1;
        }

        .bg-slide {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-size: cover;
            background-position: center center;
            opacity: 0;
            transition: opacity 1.5s ease-in-out;
        }

        .bg-slide.active {
            opacity: 1;
        }

        .overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(ellipse at center, rgba(0,10,40,0.2) 0%, rgba(0,5,20,0.7) 100%);
            z-index: 2;
        }

        .content {
            position: relative;
            z-index: 10;
            width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding-top: 10vh;
        }

        .logo-section {
            text-align: center;
            animation: fadeInDown 1s ease-out;
            width: 95%;
            max-width: 1200px;
        }

        @keyframes fadeInDown {
            from { opacity: 0; transform: translateY(-30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .logo {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
            margin-bottom: 15px;
            flex-wrap: nowrap;
        }

        .globe-icon {
            width: 60px;
            height: 60px;
            position: relative;
            flex-shrink: 0;
            filter: drop-shadow(0 0 10px rgba(255,149,0,0.3));
        }

        .globe-svg {
            width: 100%;
            height: 100%;
        }

        .brand-text {
            font-size: 3.5rem;
            font-weight: 600;
            letter-spacing: -1px;
            display: flex;
            align-items: baseline;
            text-shadow: 0 4px 15px rgba(0,0,0,0.5);
            white-space: nowrap;
            line-height: 1;
        }

        .brand-white { color: #ffffff; }
        .brand-orange { color: #ff9500; }

        .company-tagline {
            color: rgba(255,255,255,0.95);
            font-size: 1.5rem;
            font-weight: 400;
            letter-spacing: 2px;
            text-shadow: 0 2px 8px rgba(0,0,0,0.8);
            animation: fadeIn 1.5s ease-out 0.5s both;
            white-space: nowrap;
            margin-top: 10px;
            text-transform: uppercase;
        }

        .company-subtitle {
            color: #ff9500;
            font-size: 1.1rem;
            font-weight: 300;
            letter-spacing: 3px;
            margin-top: 8px;
            text-shadow: 0 2px 4px rgba(0,0,0,0.8);
            animation: fadeIn 2s ease-out 0.8s both;
        }

        .tower-wrapper {
            position: absolute;
            bottom: 18%;
            left: 3%;
            width: 180px;
            height: 350px;
            z-index: 5;
            filter: drop-shadow(0 0 20px rgba(59,130,246,0.4));
        }

        .tower {
            width: 100%;
            height: 100%;
        }

        .signal-container {
            position: absolute;
            top: 8%;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 80px;
        }

        .signal {
            position: absolute;
            border: 3px solid #ff9500;
            border-radius: 50%;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            opacity: 0;
            animation: signalPulse 2s infinite;
        }

        .signal:nth-child(1) { width: 30px; height: 30px; animation-delay: 0s; }
        .signal:nth-child(2) { width: 50px; height: 50px; animation-delay: 0.4s; }
        .signal:nth-child(3) { width: 70px; height: 70px; animation-delay: 0.8s; }

        @keyframes signalPulse {
            0% { transform: translate(-50%, -50%) scale(0.5); opacity: 1; }
            100% { transform: translate(-50%, -50%) scale(1.5); opacity: 0; }
        }

        .fibers-wrapper {
            position: absolute;
            bottom: 10%;
            right: 0;
            width: 400px;
            height: 300px;
            z-index: 5;
            overflow: hidden;
        }

        .fiber-cable {
            position: absolute;
            bottom: 0;
            right: 0;
            transform-origin: bottom right;
            border-radius: 3px;
            box-shadow: 0 0 20px currentColor, 0 0 40px currentColor;
        }

        .fiber-1 {
            width: 350px; height: 6px;
            background: linear-gradient(135deg, transparent 0%, #2563eb 30%, #60a5fa 100%);
            transform: rotate(-35deg) translateX(50px);
            color: #3b82f6;
            animation: fiberGlow 2s ease-in-out infinite;
        }

        .fiber-2 {
            width: 320px; height: 5px;
            background: linear-gradient(135deg, transparent 0%, #ea580c 30%, #ff9500 100%);
            transform: rotate(-28deg) translateX(80px) translateY(-30px);
            color: #ff9500;
            animation: fiberGlow 2s ease-in-out infinite 0.3s;
        }

        .fiber-3 {
            width: 380px; height: 6px;
            background: linear-gradient(135deg, transparent 0%, #1d4ed8 30%, #3b82f6 100%);
            transform: rotate(-40deg) translateX(20px) translateY(40px);
            color: #3b82f6;
            animation: fiberGlow 2s ease-in-out infinite 0.6s;
        }

        @keyframes fiberGlow {
            0%, 100% { opacity: 0.8; box-shadow: 0 0 20px currentColor; }
            50% { opacity: 1; box-shadow: 0 0 40px currentColor, 0 0 80px currentColor; }
        }

        .light-dots {
            position: absolute;
            right: 5%;
            bottom: 25%;
            width: 200px;
            height: 180px;
        }

        .dot {
            position: absolute;
            border-radius: 50%;
            background: white;
            box-shadow: 0 0 20px 8px currentColor;
            animation: dotPulse 1.5s ease-in-out infinite;
        }

        .dot:nth-child(1) { width: 8px; height: 8px; top: 20%; left: 80%; background: #60a5fa; color: #2563eb; }
        .dot:nth-child(2) { width: 6px; height: 6px; top: 40%; left: 70%; background: #ff9500; color: #ea580c; animation-delay: 0.2s; }
        .dot:nth-child(3) { width: 7px; height: 7px; top: 60%; left: 85%; background: #3b82f6; color: #1d4ed8; animation-delay: 0.4s; }

        @keyframes dotPulse {
            0%, 100% { transform: scale(1); opacity: 0.9; }
            50% { transform: scale(1.4); opacity: 1; }
        }

        .bottom-banner {
            position: absolute;
            bottom: 5%;
            left: 50%;
            transform: translateX(-50%);
            width: 90%;
            max-width: 1000px;
            background: rgba(10, 30, 90, 0.9);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.15);
            border-radius: 4px;
            padding: 25px 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 20px 50px rgba(0,0,0,0.5);
            z-index: 20;
            flex-wrap: wrap;
            gap: 15px;
        }

        .investment-text {
            color: white;
            font-size: 2rem;
            font-weight: 700;
            letter-spacing: 1px;
            text-transform: uppercase;
            margin: 0;
        }

        .acquire-section {
            display: flex;
            align-items: center;
            gap: 10px;
            cursor: pointer;
            transition: all 0.3s;
            padding: 10px 20px;
            border-radius: 30px;
            background: rgba(255,149,0,0.1);
            border: 2px solid transparent;
        }

        .acquire-section:hover {
            background: rgba(255,149,0,0.2);
            border-color: rgba(255,149,0,0.5);
            transform: translateX(5px);
        }

        .acquire-text {
            color: #ff9500;
            font-size: 1.5rem;
            font-weight: 800;
            letter-spacing: 1px;
            text-transform: uppercase;
            white-space: nowrap;
        }

        .arrow-icon {
            color: #ff9500;
            font-size: 1.5rem;
        }

        .bg-controls {
            position: absolute;
            bottom: 22%;
            right: 5%;
            z-index: 15;
            display: flex;
            gap: 8px;
            background: rgba(0,0,0,0.5);
            padding: 10px;
            border-radius: 20px;
            backdrop-filter: blur(5px);
        }

        .bg-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: rgba(255,255,255,0.3);
            cursor: pointer;
            transition: all 0.3s;
            border: 2px solid transparent;
        }

        .bg-dot.active {
            background: #ff9500;
            border-color: white;
            transform: scale(1.3);
        }

        .whatsapp-float {
            position: fixed;
            bottom: 30px;
            left: 30px;
            z-index: 1000;
            background: #25D366;
            color: white;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 30px;
            box-shadow: 0 4px 20px rgba(37, 211, 102, 0.4);
            cursor: pointer;
            transition: all 0.3s;
            text-decoration: none;
            animation: pulse-whatsapp 2s infinite;
        }

        .whatsapp-float:hover {
            transform: scale(1.1);
            box-shadow: 0 6px 30px rgba(37, 211, 102, 0.6);
        }

        @keyframes pulse-whatsapp {
            0% { box-shadow: 0 0 0 0 rgba(37, 211, 102, 0.7); }
            70% { box-shadow: 0 0 0 20px rgba(37, 211, 102, 0); }
            100% { box-shadow: 0 0 0 0 rgba(37, 211, 102, 0); }
        }

        .whatsapp-tooltip {
            position: absolute;
            bottom: 70px;
            left: 50%;
            transform: translateX(-50%);
            background: white;
            color: #333;
            padding: 8px 12px;
            border-radius: 8px;
            font-size: 12px;
            white-space: nowrap;
            opacity: 0;
            transition: opacity 0.3s;
            pointer-events: none;
            box-shadow: 0 2px 10px rgba(0,0,0,0.2);
        }

        .whatsapp-float:hover .whatsapp-tooltip {
            opacity: 1;
        }

        .cities-section {
            position: relative;
            width: 100%;
            background: linear-gradient(to bottom, #000 0%, #0a0e27 50%, #000 100%);
            padding: 80px 20px;
            z-index: 30;
        }

        .cities-header {
            text-align: center;
            margin-bottom: 50px;
        }

        .cities-title {
            color: #ff9500;
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 10px;
            text-transform: uppercase;
            letter-spacing: 3px;
        }

        .cities-subtitle {
            color: rgba(255,255,255,0.7);
            font-size: 1.2rem;
            font-weight: 300;
        }

        .cities-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            max-width: 1400px;
            margin: 0 auto;
        }

        .city-card {
            position: relative;
            height: 400px;
            border-radius: 15px;
            overflow: hidden;
            cursor: pointer;
            transition: all 0.4s ease;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
            border: 2px solid transparent;
        }

        .city-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 20px 60px rgba(59,130,246,0.4);
            border-color: #3b82f6;
        }

        .city-image {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .city-card:hover .city-image {
            transform: scale(1.1);
        }

        .city-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to top, rgba(0,0,0,0.9) 0%, rgba(0,0,0,0.3) 50%, transparent 100%);
            display: flex;
            flex-direction: column;
            justify-content: flex-end;
            padding: 30px;
            transition: all 0.3s;
        }

        .city-card:hover .city-overlay {
            background: linear-gradient(to top, rgba(255,149,0,0.2) 0%, rgba(0,0,0,0.4) 100%);
        }

        .city-name {
            color: white;
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 5px;
            text-transform: uppercase;
            letter-spacing: 2px;
            transform: translateY(20px);
            opacity: 0;
            transition: all 0.3s ease 0.1s;
        }

        .city-country {
            color: #ff9500;
            font-size: 1rem;
            font-weight: 600;
            transform: translateY(20px);
            opacity: 0;
            transition: all 0.3s ease 0.2s;
        }

        .city-card:hover .city-name,
        .city-card:hover .city-country {
            transform: translateY(0);
            opacity: 1;
        }

        .city-icon {
            position: absolute;
            top: 20px;
            right: 20px;
            width: 50px;
            height: 50px;
            background: rgba(255,149,0,0.9);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            opacity: 0;
            transform: scale(0);
            transition: all 0.3s ease;
        }

        .city-card:hover .city-icon {
            opacity: 1;
            transform: scale(1);
        }

        @media (max-width: 768px) {
            .brand-text { 
                font-size: 1.6rem; 
                letter-spacing: -0.5px;
            }
            .globe-icon { 
                width: 35px; 
                height: 35px; 
            }
            .logo {
                gap: 8px;
            }
            .company-tagline {
                font-size: 1rem;
                letter-spacing: 1px;
            }
            .company-subtitle {
                font-size: 0.8rem;
                letter-spacing: 2px;
            }
            .tower-wrapper { width: 100px; height: 200px; left: 0; bottom: 25%; }
            .fibers-wrapper { width: 200px; height: 180px; }
            .fiber-1 { width: 180px; height: 4px; }
            .fiber-2 { width: 160px; height: 3px; }
            .fiber-3 { width: 190px; height: 4px; }
            .bottom-banner { 
                width: 95%;
                padding: 15px 20px;
                flex-direction: column;
                text-align: center;
                bottom: 2%;
            }
            .investment-text { font-size: 1.2rem; }
            .acquire-text { font-size: 1.1rem; }
            .content { padding-top: 8vh; }
            .bg-controls { bottom: 30%; right: 50%; transform: translateX(50%); }
            .cities-title { font-size: 2rem; }
            .cities-grid { grid-template-columns: 1fr; }
            .city-card { height: 300px; }
            .whatsapp-float {
                width: 50px;
                height: 50px;
                font-size: 24px;
                bottom: 20px;
                left: 20px;
            }
        }

        @media (max-width: 480px) {
            .brand-text { 
                font-size: 1.3rem; 
                letter-spacing: 0;
            }
            .globe-icon { 
                width: 30px; 
                height: 30px; 
            }
            .company-tagline {
                font-size: 0.85rem;
            }
            .investment-text { font-size: 1rem; }
            .acquire-text { font-size: 0.9rem; }
        }
    </style>
<base target="_blank">
</head>
<body>

    <div class="main-container">
        <div class="bg-slider" id="bgSlider">
            <!-- صورة دبي عالية الجودة -->
            <div class="bg-slide active" style="background-image: url('https://images.unsplash.com/photo-1461664054097-e319867377a0?q=80&w=2000&auto=format&fit=crop');"></div>
            <div class="bg-slide" style="background-image: url('https://images.unsplash.com/photo-1661630802951-9bf877543041?q=80&w=2000&auto=format&fit=crop');"></div>
            <div class="bg-slide" style="background-image: url('https://images.unsplash.com/photo-1663900108404-a05e8bf82cda?q=80&w=2000&auto=format&fit=crop');"></div>
            <div class="bg-slide" style="background-image: url('https://images.unsplash.com/photo-1759222973646-6f12426f1285?q=80&w=2000&auto=format&fit=crop');"></div>
            <div class="bg-slide" style="background-image: url('https://images.unsplash.com/photo-1547548731-e95343697eb4?q=80&w=2000&auto=format&fit=crop');"></div>
            <div class="bg-slide" style="background-image: url('https://images.unsplash.com/photo-1683194247996-43897678c94c?q=80&w=2000&auto=format&fit=crop');"></div>
        </div>
        <div class="overlay"></div>
        
        <div class="content">
            <div class="logo-section">
                <div class="logo">
                    <div class="globe-icon">
                        <svg class="globe-svg" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <circle cx="50" cy="50" r="45" stroke="white" stroke-width="3"/>
                            <path d="M 50 5 A 45 45 0 0 1 95 50" stroke="#ff9500" stroke-width="4" fill="none" stroke-linecap="round"/>
                            <ellipse cx="50" cy="50" rx="45" ry="20" stroke="white" stroke-width="2"/>
                            <ellipse cx="50" cy="50" rx="20" ry="45" stroke="white" stroke-width="2"/>
                            <line x1="5" y1="50" x2="95" y2="50" stroke="white" stroke-width="2"/>
                            <line x1="50" y1="5" x2="50" y2="95" stroke="white" stroke-width="2"/>
                        </svg>
                    </div>
                    <div class="brand-text">
                        <span class="brand-white">khaleej</span>
                        <span class="brand-orange">telecom</span>
                        <span class="brand-white">.com</span>
                    </div>
                </div>
                
                <div class="company-tagline">Leader in Digital Transformation</div>
                <div class="company-subtitle">Connecting the Gulf • Empowering Futures</div>
            </div>
        </div>

        <div class="tower-wrapper">
            <svg class="tower" viewBox="0 0 200 400" fill="none" xmlns="http://www.w3.org/2000/svg">
                <defs>
                    <linearGradient id="metalGrad" x1="0%" y1="0%" x2="100%" y2="0%">
                        <stop offset="0%" style="stop-color:#1e3a8a"/>
                        <stop offset="50%" style="stop-color:#3b82f6"/>
                        <stop offset="100%" style="stop-color:#1e3a8a"/>
                    </linearGradient>
                </defs>
                <path d="M100 10 L40 380 L160 380 Z" fill="url(#metalGrad)" stroke="#60a5fa" stroke-width="2"/>
                <line x1="48" y1="320" x2="152" y2="320" stroke="#93c5fd" stroke-width="4"/>
                <line x1="56" y1="260" x2="144" y2="260" stroke="#93c5fd" stroke-width="4"/>
                <line x1="64" y1="200" x2="136" y2="200" stroke="#93c5fd" stroke-width="4"/>
                <line x1="72" y1="140" x2="128" y2="140" stroke="#93c5fd" stroke-width="4"/>
                <line x1="80" y1="80" x2="120" y2="80" stroke="#93c5fd" stroke-width="3"/>
                <line x1="100" y1="10" x2="100" y2="0" stroke="#ff9500" stroke-width="4"/>
                <ellipse cx="145" cy="220" rx="35" ry="28" fill="#cbd5e1" stroke="#64748b" stroke-width="2"/>
                <ellipse cx="55" cy="290" rx="28" ry="22" fill="#cbd5e1" stroke="#64748b" stroke-width="2" transform="rotate(-25 55 290)"/>
                <circle cx="100" cy="10" r="10" fill="#ff9500" filter="drop-shadow(0 0 15px #ff9500)"/>
            </svg>
            <div class="signal-container">
                <div class="signal"></div>
                <div class="signal"></div>
                <div class="signal"></div>
            </div>
        </div>

        <div class="fibers-wrapper">
            <div class="fiber-cable fiber-1"></div>
            <div class="fiber-cable fiber-2"></div>
            <div class="fiber-cable fiber-3"></div>
            <div class="light-dots">
                <div class="dot"></div>
                <div class="dot"></div>
                <div class="dot"></div>
            </div>
        </div>

        <div class="bg-controls">
            <div class="bg-dot active" onclick="changeBg(0)"></div>
            <div class="bg-dot" onclick="changeBg(1)"></div>
            <div class="bg-dot" onclick="changeBg(2)"></div>
            <div class="bg-dot" onclick="changeBg(3)"></div>
            <div class="bg-dot" onclick="changeBg(4)"></div>
            <div class="bg-dot" onclick="changeBg(5)"></div>
        </div>

        <div class="bottom-banner">
            <h2 class="investment-text">INVESTMENT OPPORTUNITY</h2>
            <div class="acquire-section">
                <span class="acquire-text">ACQUIRE TODAY!</span>
                <span class="arrow-icon">▶</span>
            </div>
        </div>
    </div>

    <a href="https://wa.me/213665817023" class="whatsapp-float" target="_blank" title="Contact us on WhatsApp">
        <svg viewBox="0 0 24 24" width="35" height="35" fill="currentColor">
            <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"/>
        </svg>
        <span class="whatsapp-tooltip">Chat with us</span>
    </a>

    <section class="cities-section">
        <div class="cities-header">
            <h2 class="cities-title">Our Presence Across the Gulf</h2>
            <p class="cities-subtitle">Connecting major cities with cutting-edge telecom infrastructure</p>
        </div>

        <div class="cities-grid">
            <div class="city-card" onclick="changeBg(0)">
                <img src="https://images.unsplash.com/photo-1461664054097-e319867377a0?q=80&w=800&auto=format&fit=crop" alt="Dubai" class="city-image">
                <div class="city-overlay">
                    <h3 class="city-name">Dubai</h3>
                    <span class="city-country">UAE Headquarters</span>
                </div>
                <div class="city-icon">🇦🇪</div>
            </div>

            <div class="city-card" onclick="changeBg(1)">
                <img src="https://images.unsplash.com/photo-1661630802951-9bf877543041?q=80&w=800&auto=format&fit=crop" alt="Abu Dhabi" class="city-image">
                <div class="city-overlay">
                    <h3 class="city-name">Abu Dhabi</h3>
                    <span class="city-country">Operations Center</span>
                </div>
                <div class="city-icon">🇦🇪</div>
            </div>

            <div class="city-card" onclick="changeBg(2)">
                <img src="https://images.unsplash.com/photo-1663900108404-a05e8bf82cda?q=80&w=800&auto=format&fit=crop" alt="Riyadh" class="city-image">
                <div class="city-overlay">
                    <h3 class="city-name">Riyadh</h3>
                    <span class="city-country">KSA Operations</span>
                </div>
                <div class="city-icon">🇸🇦</div>
            </div>

            <div class="city-card" onclick="changeBg(3)">
                <img src="https://images.unsplash.com/photo-1759222973646-6f12426f1285?q=80&w=800&auto=format&fit=crop" alt="Kuwait" class="city-image">
                <div class="city-overlay">
                    <h3 class="city-name">Kuwait City</h3>
                    <span class="city-country">Network Hub</span>
                </div>
                <div class="city-icon">🇰🇼</div>
            </div>

            <div class="city-card" onclick="changeBg(4)">
                <img src="https://images.unsplash.com/photo-1547548731-e95343697eb4?q=80&w=800&auto=format&fit=crop" alt="Manama" class="city-image">
                <div class="city-overlay">
                    <h3 class="city-name">Manama</h3>
                    <span class="city-country">Gulf Gateway</span>
                </div>
                <div class="city-icon">🇧🇭</div>
            </div>

            <div class="city-card" onclick="changeBg(5)">
                <img src="https://images.unsplash.com/photo-1683194247996-43897678c94c?q=80&w=800&auto=format&fit=crop" alt="Doha" class="city-image">
                <div class="city-overlay">
                    <h3 class="city-name">Doha</h3>
                    <span class="city-country">Qatar Branch</span>
                </div>
                <div class="city-icon">🇶🇦</div>
            </div>
        </div>
    </section>

    <script>
        let currentSlide = 0;
        const slides = document.querySelectorAll('.bg-slide');
        const dots = document.querySelectorAll('.bg-dot');
        const totalSlides = slides.length;
        let slideInterval;

        function changeBg(index) {
            currentSlide = index;
            updateSlides();
            resetInterval();
        }

        function updateSlides() {
            slides.forEach((slide, i) => {
                slide.classList.remove('active');
                dots[i].classList.remove('active');
                if (i === currentSlide) {
                    slide.classList.add('active');
                    dots[i].classList.add('active');
                }
            });
        }

        function nextSlide() {
            currentSlide = (currentSlide + 1) % totalSlides;
            updateSlides();
        }

        function resetInterval() {
            clearInterval(slideInterval);
            slideInterval = setInterval(nextSlide, 4000);
        }

        resetInterval();
    </script>
</body>
</html>
