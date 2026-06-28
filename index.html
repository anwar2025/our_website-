<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Case File</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400;1,700&family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Inter:wght@300;400;500&display=swap" rel="stylesheet">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/gsap.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/ScrollTrigger.min.js"></script>

    <style>
        /* ============================================
           ROOT & RESET
        ============================================ */
        :root {
            --deep-brown: #3E2723;
            --coffee-brown: #5D4037;
            --black: #121212;
            --beige: #D7CCC8;
            --gold: #C9A227;
            --gold-dim: rgba(201, 162, 39, 0.15);
            --glass-bg: rgba(62, 39, 35, 0.25);
            --glass-border: rgba(201, 162, 39, 0.12);
        }

        *, *::before, *::after {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
            scrollbar-width: thin;
            scrollbar-color: var(--coffee-brown) var(--black);
        }

        body {
            font-family: 'Cormorant Garamond', serif;
            background: var(--black);
            color: var(--beige);
            overflow-x: hidden;
            line-height: 1.6;
            -webkit-font-smoothing: antialiased;
        }

        body::before {
            content: '';
            position: fixed;
            inset: 0;
            background:
                radial-gradient(ellipse at 15% 50%, rgba(62, 39, 35, 0.35) 0%, transparent 55%),
                radial-gradient(ellipse at 85% 20%, rgba(93, 64, 55, 0.2) 0%, transparent 50%),
                radial-gradient(ellipse at 50% 90%, rgba(201, 162, 39, 0.04) 0%, transparent 45%);
            pointer-events: none;
            z-index: 0;
        }

        /* ============================================
           LOADING SCREEN
        ============================================ */
        #loader {
            position: fixed;
            inset: 0;
            background: var(--black);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            z-index: 10000;
            transition: opacity 0.8s ease, visibility 0.8s ease;
        }

        #loader.hidden {
            opacity: 0;
            visibility: hidden;
        }

        #loader-text {
            font-family: 'Playfair Display', serif;
            font-size: clamp(1.2rem, 3vw, 1.8rem);
            color: var(--gold);
            letter-spacing: 0.15em;
            text-transform: uppercase;
        }

        .loader-dots {
            display: flex;
            gap: 8px;
            margin-top: 24px;
        }

        .loader-dots span {
            width: 8px;
            height: 8px;
            border-radius: 50%;
            background: var(--gold);
            animation: loaderPulse 1.4s ease-in-out infinite;
        }

        .loader-dots span:nth-child(2) { animation-delay: 0.2s; }
        .loader-dots span:nth-child(3) { animation-delay: 0.4s; }

        @keyframes loaderPulse {
            0%, 80%, 100% { opacity: 0.2; transform: scale(0.8); }
            40% { opacity: 1; transform: scale(1.2); }
        }

        /* ============================================
           SCROLL PROGRESS
        ============================================ */
        #scroll-progress {
            position: fixed;
            top: 0;
            left: 0;
            height: 3px;
            background: linear-gradient(90deg, var(--gold), #E8C547);
            z-index: 9999;
            width: 0%;
            transition: width 0.1s linear;
        }

        /* ============================================
           CURSOR GLOW
        ============================================ */
        #cursor-glow {
            position: fixed;
            width: 300px;
            height: 300px;
            border-radius: 50%;
            background: radial-gradient(circle, rgba(201, 162, 39, 0.06) 0%, transparent 70%);
            pointer-events: none;
            z-index: 9998;
            transform: translate(-50%, -50%);
            transition: opacity 0.3s;
            display: none;
        }

        @media (hover: hover) {
            #cursor-glow { display: block; }
        }

        /* ============================================
           PARTICLE CANVAS
        ============================================ */
        #particle-canvas {
            position: fixed;
            inset: 0;
            z-index: 1;
            pointer-events: none;
        }

        /* ============================================
           FLOATING HEARTS
        ============================================ */
        .floating-heart {
            position: fixed;
            z-index: 9997;
            pointer-events: none;
            color: var(--gold);
            opacity: 0;
            font-size: 16px;
            animation: floatHeart 6s ease-in forwards;
        }

        @keyframes floatHeart {
            0% { opacity: 0; transform: translateY(0) scale(0.5) rotate(0deg); }
            15% { opacity: 0.5; }
            85% { opacity: 0.3; }
            100% { opacity: 0; transform: translateY(-100vh) scale(1) rotate(30deg); }
        }

        /* ============================================
           MUSIC TOGGLE
        ============================================ */
        #music-toggle {
            position: fixed;
            bottom: 24px;
            right: 24px;
            z-index: 9999;
            width: 48px;
            height: 48px;
            border-radius: 50%;
            background: var(--glass-bg);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid var(--glass-border);
            color: var(--gold);
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
        }

        #music-toggle:hover {
            background: rgba(201, 162, 39, 0.15);
            transform: scale(1.1);
        }

        #music-toggle svg {
            width: 20px;
            height: 20px;
            fill: currentColor;
        }

        /* ============================================
           MAIN CONTENT
        ============================================ */
        main {
            position: relative;
            z-index: 2;
        }

        section {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 80px 24px;
            position: relative;
        }

        .section-label {
            font-family: 'Inter', sans-serif;
            font-size: 0.7rem;
            font-weight: 500;
            letter-spacing: 0.25em;
            text-transform: uppercase;
            color: var(--gold);
            margin-bottom: 16px;
            opacity: 0.7;
        }

        /* ============================================
           HERO SECTION
        ============================================ */
        #hero {
            text-align: center;
            padding-top: 0;
        }

        .hero-title {
            font-family: 'Playfair Display', serif;
            font-size: clamp(2rem, 6vw, 4.2rem);
            font-weight: 700;
            line-height: 1.2;
            color: var(--beige);
            margin-bottom: 24px;
            overflow: hidden;
        }

        .hero-title .word {
            display: inline-block;
            overflow: hidden;
            margin-right: 0.3em;
        }

        .hero-title .char {
            display: inline-block;
            transform: translateY(100%);
        }

        .hero-title em {
            color: var(--gold);
            font-style: italic;
        }

        .hero-subtitle {
            font-size: clamp(1rem, 2.5vw, 1.35rem);
            font-weight: 300;
            font-style: italic;
            color: rgba(215, 204, 200, 0.6);
            max-width: 500px;
            margin: 0 auto 48px;
            line-height: 1.8;
        }

        .hero-subtitle .line {
            display: block;
            opacity: 0;
            transform: translateY(20px);
        }

        .btn-primary {
            display: inline-flex;
            align-items: center;
            gap: 12px;
            padding: 18px 40px;
            font-family: 'Inter', sans-serif;
            font-size: 0.8rem;
            font-weight: 500;
            letter-spacing: 0.15em;
            text-transform: uppercase;
            color: var(--black);
            background: linear-gradient(135deg, var(--gold), #E8C547);
            border: none;
            border-radius: 60px;
            cursor: pointer;
            position: relative;
            overflow: hidden;
            transition: all 0.4s ease;
            opacity: 0;
            transform: translateY(30px);
        }

        .btn-primary::before {
            content: '';
            position: absolute;
            inset: 0;
            background: linear-gradient(135deg, #E8C547, var(--gold));
            opacity: 0;
            transition: opacity 0.4s ease;
        }

        .btn-primary:hover::before { opacity: 1; }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 40px rgba(201, 162, 39, 0.3);
        }

        .btn-primary span { position: relative; z-index: 1; }

        .btn-primary .arrow {
            display: inline-block;
            position: relative;
            z-index: 1;
            transition: transform 0.3s ease;
        }

        .btn-primary:hover .arrow { transform: translateY(3px); }

        /* ============================================
           MY SIDE SECTION
        ============================================ */
        .case-card {
            background: var(--glass-bg);
            backdrop-filter: blur(24px);
            -webkit-backdrop-filter: blur(24px);
            border: 1px solid var(--glass-border);
            border-radius: 20px;
            padding: clamp(32px, 5vw, 60px);
            max-width: 640px;
            width: 100%;
            position: relative;
            overflow: hidden;
        }

        .case-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, transparent, var(--gold), transparent);
        }

        .case-card-header {
            font-family: 'Inter', sans-serif;
            font-size: 0.65rem;
            font-weight: 500;
            letter-spacing: 0.3em;
            text-transform: uppercase;
            color: var(--gold);
            margin-bottom: 8px;
        }

        .case-card-title {
            font-family: 'Playfair Display', serif;
            font-size: clamp(1.5rem, 3.5vw, 2.2rem);
            font-weight: 700;
            color: var(--beige);
            margin-bottom: 32px;
            padding-bottom: 24px;
            border-bottom: 1px solid rgba(201, 162, 39, 0.1);
        }

        .case-line {
            font-size: clamp(1rem, 2vw, 1.2rem);
            font-weight: 300;
            color: rgba(215, 204, 200, 0.75);
            margin-bottom: 20px;
            padding-left: 20px;
            border-left: 2px solid transparent;
            opacity: 0;
            transform: translateX(-20px);
            transition: border-color 0.5s ease;
        }

        .case-line:last-child { margin-bottom: 0; }

        .case-line.visible {
            border-left-color: var(--gold);
        }

        .case-line em {
            color: var(--beige);
            font-style: italic;
        }

        /* ============================================
           EVIDENCE SECTION
        ============================================ */
        .evidence-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 24px;
            max-width: 900px;
            width: 100%;
        }

        .evidence-card {
            background: var(--glass-bg);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border: 1px solid var(--glass-border);
            border-radius: 16px;
            padding: 36px 28px;
            text-align: center;
            opacity: 0;
            transform: translateY(40px);
            position: relative;
            overflow: hidden;
        }

        .evidence-card::after {
            content: '';
            position: absolute;
            inset: 0;
            border-radius: 16px;
            background: linear-gradient(135deg, rgba(201, 162, 39, 0.05), transparent);
            pointer-events: none;
        }

        .evidence-label {
            font-family: 'Inter', sans-serif;
            font-size: 0.6rem;
            font-weight: 500;
            letter-spacing: 0.3em;
            text-transform: uppercase;
            color: var(--gold);
            margin-bottom: 16px;
        }

        .evidence-text {
            font-size: 1.1rem;
            font-weight: 300;
            font-style: italic;
            color: rgba(215, 204, 200, 0.8);
            line-height: 1.7;
        }

        .evidence-card.float-1 { animation: gentleFloat 5s ease-in-out infinite; }
        .evidence-card.float-2 { animation: gentleFloat 6s ease-in-out infinite 1s; }
        .evidence-card.float-3 { animation: gentleFloat 5.5s ease-in-out infinite 0.5s; }

        @keyframes gentleFloat {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-8px); }
        }

        /* ============================================
           COURTROOM SECTION
        ============================================ */
        #courtroom {
            overflow: hidden;
        }

        .courtroom-content {
            text-align: center;
            max-width: 600px;
        }

        .gavel-container {
            margin-bottom: 40px;
            display: flex;
            justify-content: center;
        }

        .gavel {
            width: 80px;
            height: 80px;
            position: relative;
            transform-origin: bottom right;
        }

        .gavel-head {
            width: 60px;
            height: 18px;
            background: linear-gradient(135deg, var(--gold), #E8C547);
            border-radius: 4px;
            position: absolute;
            top: 0;
            left: 0;
        }

        .gavel-handle {
            width: 8px;
            height: 50px;
            background: linear-gradient(to bottom, #8D6E63, var(--coffee-brown));
            border-radius: 0 0 3px 3px;
            position: absolute;
            top: 16px;
            left: 26px;
        }

        .gavel-block {
            width: 50px;
            height: 12px;
            background: var(--coffee-brown);
            border-radius: 3px;
            position: absolute;
            bottom: 0;
            left: 5px;
        }

        .gavel.strike {
            animation: gavelStrike 0.6s ease-out;
        }

        @keyframes gavelStrike {
            0% { transform: rotate(0deg); }
            30% { transform: rotate(-35deg); }
            50% { transform: rotate(5deg); }
            70% { transform: rotate(-3deg); }
            100% { transform: rotate(0deg); }
        }

        .courtroom-line {
            font-size: clamp(1rem, 2.5vw, 1.3rem);
            margin-bottom: 20px;
            opacity: 0;
            transform: translateY(15px);
        }

        .courtroom-line .role {
            font-family: 'Inter', sans-serif;
            font-size: 0.65rem;
            font-weight: 500;
            letter-spacing: 0.2em;
            text-transform: uppercase;
            color: var(--gold);
            display: block;
            margin-bottom: 6px;
        }

        .courtroom-line .dialogue {
            font-weight: 300;
            color: rgba(215, 204, 200, 0.85);
        }

        .courtroom-line .dialogue em {
            color: var(--gold);
            font-style: italic;
        }

        .sentence-box {
            margin-top: 24px;
            padding: 24px 32px;
            background: rgba(201, 162, 39, 0.08);
            border: 1px solid rgba(201, 162, 39, 0.2);
            border-radius: 12px;
            opacity: 0;
            transform: scale(0.95);
        }

        .sentence-box .label {
            font-family: 'Inter', sans-serif;
            font-size: 0.6rem;
            letter-spacing: 0.3em;
            text-transform: uppercase;
            color: var(--gold);
            margin-bottom: 8px;
        }

        .sentence-box .text {
            font-family: 'Playfair Display', serif;
            font-size: 1.2rem;
            font-style: italic;
            color: var(--beige);
        }

        /* ============================================
           OBJECTION GAME
        ============================================ */
        #objection-game {
            min-height: 80vh;
        }

        .game-area {
            position: relative;
            width: 100%;
            max-width: 500px;
            height: 280px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 24px;
        }

        .btn-stay-angry {
            padding: 16px 36px;
            font-family: 'Inter', sans-serif;
            font-size: 0.8rem;
            font-weight: 500;
            letter-spacing: 0.1em;
            color: rgba(215, 204, 200, 0.7);
            background: rgba(215, 204, 200, 0.06);
            border: 1px solid rgba(215, 204, 200, 0.12);
            border-radius: 60px;
            cursor: pointer;
            position: absolute;
            transition: background 0.3s, color 0.3s, border-color 0.3s;
            z-index: 5;
            white-space: nowrap;
        }

        .btn-stay-angry:hover {
            background: rgba(215, 204, 200, 0.1);
            color: var(--beige);
        }

        .btn-stay-angry.given-up {
            position: relative;
            border-color: rgba(201, 162, 39, 0.3);
            color: var(--gold);
            font-style: italic;
        }

        .btn-hear-out {
            padding: 18px 44px;
            font-family: 'Inter', sans-serif;
            font-size: 0.85rem;
            font-weight: 500;
            letter-spacing: 0.12em;
            color: var(--black);
            background: linear-gradient(135deg, var(--gold), #E8C547);
            border: none;
            border-radius: 60px;
            cursor: pointer;
            position: relative;
            overflow: hidden;
            animation: softGlow 2.5s ease-in-out infinite;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .btn-hear-out:hover {
            transform: scale(1.05);
            box-shadow: 0 6px 30px rgba(201, 162, 39, 0.35);
        }

        @keyframes softGlow {
            0%, 100% { box-shadow: 0 0 20px rgba(201, 162, 39, 0.15); }
            50% { box-shadow: 0 0 40px rgba(201, 162, 39, 0.3); }
        }

        /* ============================================
           SMILE METER
        ============================================ */
        #smile-meter {
            min-height: 80vh;
        }

        .meter-container {
            max-width: 480px;
            width: 100%;
            text-align: center;
        }

        .meter-emoji {
            font-size: 4rem;
            margin-bottom: 24px;
            transition: transform 0.3s ease;
            display: inline-block;
        }

        .meter-label {
            font-family: 'Inter', sans-serif;
            font-size: 0.7rem;
            letter-spacing: 0.2em;
            text-transform: uppercase;
            color: rgba(215, 204, 200, 0.5);
            margin-bottom: 32px;
        }

        .slider-track {
            position: relative;
            width: 100%;
            height: 6px;
            background: rgba(215, 204, 200, 0.1);
            border-radius: 3px;
            margin-bottom: 12px;
        }

        .slider-fill {
            position: absolute;
            left: 0;
            top: 0;
            height: 100%;
            background: linear-gradient(90deg, var(--gold), #E8C547);
            border-radius: 3px;
            transition: width 0.15s ease;
        }

        input[type="range"] {
            -webkit-appearance: none;
            appearance: none;
            width: 100%;
            height: 6px;
            background: transparent;
            position: relative;
            z-index: 2;
            margin: 0;
            cursor: pointer;
        }

        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            appearance: none;
            width: 24px;
            height: 24px;
            border-radius: 50%;
            background: var(--gold);
            border: 3px solid var(--black);
            box-shadow: 0 0 12px rgba(201, 162, 39, 0.4);
            cursor: pointer;
            transition: transform 0.2s;
        }

        input[type="range"]::-webkit-slider-thumb:hover {
            transform: scale(1.2);
        }

        input[type="range"]::-moz-range-thumb {
            width: 24px;
            height: 24px;
            border-radius: 50%;
            background: var(--gold);
            border: 3px solid var(--black);
            box-shadow: 0 0 12px rgba(201, 162, 39, 0.4);
            cursor: pointer;
        }

        .slider-labels {
            display: flex;
            justify-content: space-between;
            font-family: 'Inter', sans-serif;
            font-size: 0.65rem;
            color: rgba(215, 204, 200, 0.35);
            margin-top: 8px;
        }

        .meter-response {
            margin-top: 36px;
            font-family: 'Playfair Display', serif;
            font-size: clamp(1.2rem, 3vw, 1.6rem);
            font-style: italic;
            color: var(--beige);
            min-height: 50px;
            transition: opacity 0.3s;
        }

        .meter-percentage {
            font-family: 'Inter', sans-serif;
            font-size: 0.75rem;
            font-weight: 500;
            color: var(--gold);
            margin-top: 8px;
            letter-spacing: 0.1em;
        }

        /* ============================================
           TIMELINE
        ============================================ */
        #timeline {
            padding: 80px 24px 100px;
        }

        .timeline-wrapper {
            max-width: 600px;
            width: 100%;
            position: relative;
        }

        .timeline-line {
            position: absolute;
            left: 20px;
            top: 0;
            bottom: 0;
            width: 1px;
            background: linear-gradient(to bottom, transparent, var(--gold), rgba(201, 162, 39, 0.3), transparent);
        }

        .timeline-item {
            display: flex;
            align-items: flex-start;
            gap: 24px;
            margin-bottom: 48px;
            position: relative;
            opacity: 0;
            transform: translateX(-20px);
        }

        .timeline-icon {
            width: 40px;
            height: 40px;
            min-width: 40px;
            border-radius: 50%;
            background: rgba(201, 162, 39, 0.1);
            border: 1px solid rgba(201, 162, 39, 0.25);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--gold);
            font-size: 14px;
            z-index: 2;
        }

        .timeline-card {
            background: var(--glass-bg);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid var(--glass-border);
            border-radius: 14px;
            padding: 24px 28px;
            flex: 1;
            transition: border-color 0.3s, transform 0.3s;
        }

        .timeline-card:hover {
            border-color: rgba(201, 162, 39, 0.3);
            transform: translateX(4px);
        }

        .timeline-card-title {
            font-family: 'Playfair Display', serif;
            font-size: 1.1rem;
            font-weight: 600;
            color: var(--beige);
            margin-bottom: 6px;
        }

        .timeline-card-desc {
            font-size: 0.95rem;
            font-weight: 300;
            color: rgba(215, 204, 200, 0.55);
            font-style: italic;
        }

        /* ============================================
           FINAL STATEMENT
        ============================================ */
        #final-statement {
            text-align: center;
        }

        .statement-line {
            font-family: 'Playfair Display', serif;
            font-size: clamp(1.1rem, 2.8vw, 1.5rem);
            font-weight: 400;
            color: rgba(215, 204, 200, 0.7);
            max-width: 560px;
            margin-bottom: 24px;
            opacity: 0;
            transform: translateY(20px) scale(0.97);
        }

        .statement-line em {
            color: var(--beige);
            font-style: italic;
        }

        /* ============================================
           VERDICT SECTION
        ============================================ */
        #verdict {
            min-height: 100vh;
            padding-bottom: 120px;
        }

        .verdict-card {
            background: linear-gradient(145deg, rgba(62, 39, 35, 0.4), rgba(18, 18, 18, 0.8));
            backdrop-filter: blur(30px);
            -webkit-backdrop-filter: blur(30px);
            border: 1px solid rgba(201, 162, 39, 0.2);
            border-radius: 24px;
            padding: clamp(40px, 6vw, 72px);
            max-width: 560px;
            width: 100%;
            text-align: center;
            position: relative;
            overflow: hidden;
            opacity: 0;
            transform: scale(0.92) translateY(30px);
        }

        .verdict-card::before {
            content: '';
            position: absolute;
            top: -1px;
            left: 20%;
            right: 20%;
            height: 2px;
            background: linear-gradient(90deg, transparent, var(--gold), transparent);
        }

        .verdict-card::after {
            content: '';
            position: absolute;
            bottom: -1px;
            left: 20%;
            right: 20%;
            height: 2px;
            background: linear-gradient(90deg, transparent, var(--gold), transparent);
        }

        .verdict-icon {
            font-size: 2.5rem;
            margin-bottom: 24px;
            display: block;
        }

        .verdict-title {
            font-family: 'Playfair Display', serif;
            font-size: clamp(1.6rem, 4vw, 2.4rem);
            font-weight: 900;
            color: var(--gold);
            margin-bottom: 24px;
            letter-spacing: 0.02em;
        }

        .verdict-text {
            font-size: 1.15rem;
            font-weight: 300;
            color: rgba(215, 204, 200, 0.75);
            margin-bottom: 40px;
            line-height: 1.8;
            font-style: italic;
        }

        .btn-verdict {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            padding: 20px 48px;
            font-family: 'Inter', sans-serif;
            font-size: 0.85rem;
            font-weight: 500;
            letter-spacing: 0.12em;
            text-transform: uppercase;
            color: var(--black);
            background: linear-gradient(135deg, var(--gold), #E8C547, var(--gold));
            background-size: 200% 200%;
            border: none;
            border-radius: 60px;
            cursor: pointer;
            animation: goldShimmer 3s ease-in-out infinite, softGlow 2.5s ease-in-out infinite;
            transition: transform 0.3s, box-shadow 0.3s;
            position: relative;
            z-index: 10;
        }

        .btn-verdict:hover {
            transform: scale(1.06);
            box-shadow: 0 8px 50px rgba(201, 162, 39, 0.4);
        }

        @keyframes goldShimmer {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* ============================================
           HEART OVERLAY
        ============================================ */
        #heart-overlay {
            position: fixed;
            inset: 0;
            z-index: 10001;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(18, 18, 18, 0.95);
            opacity: 0;
            visibility: hidden;
            transition: opacity 0.8s ease, visibility 0.8s ease;
        }

        #heart-overlay.active {
            opacity: 1;
            visibility: visible;
        }

        .overlay-heart {
            font-size: 120px;
            color: var(--gold);
            position: absolute;
            transform: scale(0);
            filter: drop-shadow(0 0 40px rgba(201, 162, 39, 0.4));
        }

        .overlay-text {
            position: relative;
            z-index: 2;
            text-align: center;
            max-width: 500px;
            padding: 0 24px;
            opacity: 0;
            transform: translateY(20px);
        }

        .overlay-text p {
            font-family: 'Playfair Display', serif;
            font-size: clamp(1.1rem, 2.8vw, 1.4rem);
            font-weight: 400;
            color: var(--beige);
            line-height: 1.9;
            margin-bottom: 16px;
        }

        .overlay-text p:last-child {
            font-style: italic;
            color: rgba(215, 204, 200, 0.6);
            font-size: 1rem;
        }

        /* ============================================
           CONFETTI CANVAS
        ============================================ */
        #confetti-canvas {
            position: fixed;
            inset: 0;
            z-index: 10002;
            pointer-events: none;
        }

        /* ============================================
           RESPONSIVE
        ============================================ */
        @media (max-width: 640px) {
            section { padding: 60px 20px; }
            .game-area { height: 320px; }
            .evidence-grid { grid-template-columns: 1fr; }
            .timeline-line { left: 19px; }
        }

        /* ============================================
           SELECTION
        ============================================ */
        ::selection {
            background: rgba(201, 162, 39, 0.3);
            color: var(--beige);
        }
    </style>
</head>
<body>

    <!-- Loading Screen -->
    <div id="loader">
        <div id="loader-text">Preparing the Case...</div>
        <div class="loader-dots">
            <span></span><span></span><span></span>
        </div>
    </div>

    <!-- Scroll Progress -->
    <div id="scroll-progress"></div>

    <!-- Cursor Glow -->
    <div id="cursor-glow"></div>

    <!-- Particle Background -->
    <canvas id="particle-canvas"></canvas>

    <!-- Music Toggle -->
    <button id="music-toggle" aria-label="Toggle ambient music">
        <svg id="music-icon-on" viewBox="0 0 24 24" style="display:none;">
            <path d="M12 3v10.55A4 4 0 1 0 14 17V7h4V3h-6z"/>
        </svg>
        <svg id="music-icon-off" viewBox="0 0 24 24">
            <path d="M12 3v10.55A4 4 0 1 0 14 17V7h4V3h-6z"/>
            <line x1="3" y1="3" x2="21" y2="21" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
        </svg>
    </button>

    <!-- Main Content -->
    <main>

        <!-- HERO SECTION -->
        <section id="hero">
            <div class="section-label">Confidential</div>
            <h1 class="hero-title" id="hero-title"></h1>
            <div class="hero-subtitle" id="hero-subtitle">
                <span class="line">This isn't an argument.</span>
                <span class="line">It's simply my side of the story.</span>
            </div>
            <button class="btn-primary" id="open-case-btn">
                <span>Open the Case File</span>
                <span class="arrow">&#8595;</span>
            </button>
        </section>

        <!-- MY SIDE SECTION -->
        <section id="my-side">
            <div class="section-label">Section I</div>
            <div class="case-card">
                <div class="case-card-header">Case No. HV-2025</div>
                <h2 class="case-card-title">Case Summary</h2>
                <p class="case-line">I know I said a couple of things that came out differently than I intended.</p>
                <p class="case-line">I understand how they could have sounded.</p>
                <p class="case-line">I'm not here to prove I was <em>right</em>.</p>
                <p class="case-line">I'm here because <em>you're important to me</em>.</p>
            </div>
        </section>

        <!-- EVIDENCE SECTION -->
        <section id="evidence">
            <div class="section-label">Section II</div>
            <h2 style="font-family:'Playfair Display',serif; font-size:clamp(1.4rem,3.5vw,2rem); font-weight:700; color:var(--beige); margin-bottom:48px;">Exhibit A, B & C</h2>
            <div class="evidence-grid">
                <div class="evidence-card">
                    <div class="evidence-label">Exhibit A</div>
                    <p class="evidence-text">"Our conversations matter to me."</p>
                </div>
                <div class="evidence-card">
                    <div class="evidence-label">Exhibit B</div>
                    <p class="evidence-text">"I never wanted to hurt you."</p>
                </div>
                <div class="evidence-card">
                    <div class="evidence-label">Exhibit C</div>
                    <p class="evidence-text">"If I could replay that moment, I'd choose better words."</p>
                </div>
            </div>
        </section>

        <!-- COURTROOM SECTION -->
        <section id="courtroom">
            <div class="section-label">Section III</div>
            <div class="courtroom-content">
                <h2 style="font-family:'Playfair Display',serif; font-size:clamp(1.4rem,3.5vw,2rem); font-weight:700; color:var(--beige); margin-bottom:40px;">Courtroom Proceedings</h2>
                <div class="gavel-container">
                    <div class="gavel" id="gavel">
                        <div class="gavel-head"></div>
                        <div class="gavel-handle"></div>
                        <div class="gavel-block"></div>
                    </div>
                </div>
                <div class="courtroom-line" id="court-line-1">
                    <span class="role">Judge</span>
                    <span class="dialogue">"Order! Order!"</span>
                </div>
                <div class="courtroom-line" id="court-line-2">
                    <span class="role">Defendant (Me)</span>
                    <span class="dialogue">"Guilty... of <em>missing you</em>."</span>
                </div>
                <div class="sentence-box" id="sentence-box">
                    <div class="label">Sentence</div>
                    <div class="text">Unlimited hugs (pending approval).</div>
                </div>
            </div>
        </section>

        <!-- OBJECTION GAME -->
        <section id="objection-game">
            <div class="section-label">Section IV</div>
            <h2 style="font-family:'Playfair Display',serif; font-size:clamp(1.4rem,3.5vw,2rem); font-weight:700; color:var(--beige); margin-bottom:48px;">Your Honor, a Question</h2>
            <div class="game-area" id="game-area">
                <button class="btn-hear-out" id="btn-hear-out">Hear Him Out</button>
                <button class="btn-stay-angry" id="btn-stay-angry">Stay Angry</button>
            </div>
        </section>

        <!-- SMILE METER -->
        <section id="smile-meter">
            <div class="section-label">Section V</div>
            <div class="meter-container">
                <div class="meter-emoji" id="meter-emoji">&#128544;</div>
                <div class="meter-label">How angry are you?</div>
                <div class="slider-track">
                    <div class="slider-fill" id="slider-fill" style="width:80%"></div>
                </div>
                <input type="range" id="anger-slider" min="0" max="100" value="80">
                <div class="slider-labels">
                    <span>Case Dismissed</span>
                    <span>Furious</span>
                </div>
                <div class="meter-response" id="meter-response">Negotiations have started.</div>
                <div class="meter-percentage" id="meter-percentage">80%</div>
            </div>
        </section>

        <!-- MEMORY TIMELINE -->
        <section id="timeline">
            <div class="section-label">Section VI</div>
            <h2 style="font-family:'Playfair Display',serif; font-size:clamp(1.4rem,3.5vw,2rem); font-weight:700; color:var(--beige); margin-bottom:56px; text-align:center;">Memories Filed as Evidence</h2>
            <div class="timeline-wrapper">
                <div class="timeline-line"></div>
                <div class="timeline-item">
                    <div class="timeline-icon">&#9829;</div>
                    <div class="timeline-card">
                        <div class="timeline-card-title">The Day We First Met</div>
                        <div class="timeline-card-desc">Some moments don't announce themselves. They just quietly change everything.</div>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-icon">&#9829;</div>
                    <div class="timeline-card">
                        <div class="timeline-card-title">Our First Real Conversation</div>
                        <div class="timeline-card-desc">That was the moment I realized you were someone worth listening to — forever.</div>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-icon">&#9829;</div>
                    <div class="timeline-card">
                        <div class="timeline-card-title">That Moment I Just Knew</div>
                        <div class="timeline-card-desc">No explanation needed. The heart files its own motions.</div>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-icon">&#9829;</div>
                    <div class="timeline-card">
                        <div class="timeline-card-title">Every Laugh We Shared</div>
                        <div class="timeline-card-desc">Each one is now part of the permanent record. Admissible as pure joy.</div>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-icon">&#9829;</div>
                    <div class="timeline-card">
                        <div class="timeline-card-title">All the Little Things</div>
                        <div class="timeline-card-desc">The way you think, the way you fight for what's right — that's what I fell for.</div>
                    </div>
                </div>
            </div>
        </section>

        <!-- FINAL STATEMENT -->
        <section id="final-statement">
            <div class="section-label">Closing Arguments</div>
            <p class="statement-line">I never wanted one misunderstanding to become bigger than everything we've shared.</p>
            <p class="statement-line">Whenever you're ready...</p>
            <p class="statement-line"><em>I'd really love to talk.</em></p>
        </section>

        <!-- VERDICT -->
        <section id="verdict">
            <div class="verdict-card" id="verdict-card">
                <span class="verdict-icon">&#9878;</span>
                <h2 class="verdict-title">The Final Verdict</h2>
                <p class="verdict-text">"The Court finds that one honest conversation deserves a chance."</p>
                <button class="btn-verdict" id="btn-talk-to-me">&#9829; Talk To Me</button>
            </div>
        </section>

    </main>

    <!-- Heart Overlay -->
    <div id="heart-overlay">
        <div class="overlay-heart" id="overlay-heart">&#9829;</div>
        <div class="overlay-text" id="overlay-text">
            <p>Thank you for hearing my side.</p>
            <p>No pressure.</p>
            <p>I'll be waiting whenever you're ready.</p>
        </div>
    </div>

    <!-- Confetti Canvas -->
    <canvas id="confetti-canvas"></canvas>

    <script>
        /* ============================================
           INITIALIZATION
        ============================================ */
        gsap.registerPlugin(ScrollTrigger);

        /* ============================================
           LOADING SCREEN
        ============================================ */
        window.addEventListener('load', () => {
            setTimeout(() => {
                document.getElementById('loader').classList.add('hidden');
                initHeroAnimation();
            }, 2500);
        });

        /* ============================================
           PARTICLE BACKGROUND
        ============================================ */
        const particleCanvas = document.getElementById('particle-canvas');
        const pCtx = particleCanvas.getContext('2d');
        let particles = [];

        function resizeParticleCanvas() {
            particleCanvas.width = window.innerWidth;
            particleCanvas.height = window.innerHeight;
        }
        resizeParticleCanvas();
        window.addEventListener('resize', resizeParticleCanvas);

        // Create subtle background particles
        for (let i = 0; i < 45; i++) {
            particles.push({
                x: Math.random() * window.innerWidth,
                y: Math.random() * window.innerHeight,
                size: Math.random() * 1.8 + 0.4,
                speedX: (Math.random() - 0.5) * 0.25,
                speedY: (Math.random() - 0.5) * 0.2,
                opacity: Math.random() * 0.25 + 0.05,
                color: Math.random() > 0.7 ? '201,162,39' : '215,204,200'
            });
        }

        function animateParticles() {
            pCtx.clearRect(0, 0, particleCanvas.width, particleCanvas.height);
            particles.forEach(p => {
                p.x += p.speedX;
                p.y += p.speedY;
                // Wrap around screen edges
                if (p.x < -10) p.x = particleCanvas.width + 10;
                if (p.x > particleCanvas.width + 10) p.x = -10;
                if (p.y < -10) p.y = particleCanvas.height + 10;
                if (p.y > particleCanvas.height + 10) p.y = -10;

                pCtx.beginPath();
                pCtx.arc(p.x, p.y, p.size, 0, Math.PI * 2);
                pCtx.fillStyle = `rgba(${p.color},${p.opacity})`;
                pCtx.fill();
            });
            requestAnimationFrame(animateParticles);
        }
        animateParticles();

        /* ============================================
           CURSOR GLOW
        ============================================ */
        const cursorGlow = document.getElementById('cursor-glow');
        let mouseX = -400, mouseY = -400;

        document.addEventListener('mousemove', (e) => {
            mouseX = e.clientX;
            mouseY = e.clientY;
            cursorGlow.style.left = mouseX + 'px';
            cursorGlow.style.top = mouseY + 'px';
        });

        /* ============================================
           SCROLL PROGRESS
        ============================================ */
        const scrollProgress = document.getElementById('scroll-progress');

        window.addEventListener('scroll', () => {
            const scrollTop = window.scrollY;
            const docHeight = document.documentElement.scrollHeight - window.innerHeight;
            const progress = docHeight > 0 ? (scrollTop / docHeight) * 100 : 0;
            scrollProgress.style.width = progress + '%';
        });

        /* ============================================
           FLOATING HEARTS
        ============================================ */
        function spawnHeart() {
            const heart = document.createElement('div');
            heart.className = 'floating-heart';
            heart.innerHTML = '&#9829;';
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.bottom = '-20px';
            heart.style.fontSize = (Math.random() * 14 + 10) + 'px';
            heart.style.animationDuration = (Math.random() * 4 + 5) + 's';
            document.body.appendChild(heart);
            // Remove after animation ends
            heart.addEventListener('animationend', () => heart.remove());
        }

        // Spawn hearts periodically
        setInterval(spawnHeart, 3500);
        // Spawn a few immediately after load
        setTimeout(() => { spawnHeart(); spawnHeart(); }, 3000);

        /* ============================================
           WEB AUDIO — AMBIENT MUSIC
        ============================================ */
        let audioCtx = null;
        let musicPlaying = false;
        let musicNodes = [];

        function initAudio() {
            if (audioCtx) return;
            audioCtx = new (window.AudioContext || window.webkitAudioContext)();

            // Create a warm ambient pad: two detuned sine waves + a gentle sub
            const masterGain = audioCtx.createGain();
            masterGain.gain.value = 0;
            masterGain.connect(audioCtx.destination);

            // Pad voice 1 — A3
            const osc1 = audioCtx.createOscillator();
            osc1.type = 'sine';
            osc1.frequency.value = 220;
            const gain1 = audioCtx.createGain();
            gain1.gain.value = 0.15;
            osc1.connect(gain1);
            gain1.connect(masterGain);
            osc1.start();

            // Pad voice 2 — slightly detuned for warmth
            const osc2 = audioCtx.createOscillator();
            osc2.type = 'sine';
            osc2.frequency.value = 222.5;
            const gain2 = audioCtx.createGain();
            gain2.gain.value = 0.12;
            osc2.connect(gain2);
            gain2.connect(masterGain);
            osc2.start();

            // Pad voice 3 — E4 (perfect fifth)
            const osc3 = audioCtx.createOscillator();
            osc3.type = 'sine';
            osc3.frequency.value = 329.63;
            const gain3 = audioCtx.createGain();
            gain3.gain.value = 0.06;
            osc3.connect(gain3);
            gain3.connect(masterGain);
            osc3.start();

            // Sub bass — A2
            const osc4 = audioCtx.createOscillator();
            osc4.type = 'sine';
            osc4.frequency.value = 110;
            const gain4 = audioCtx.createGain();
            gain4.gain.value = 0.08;
            osc4.connect(gain4);
            gain4.connect(masterGain);
            osc4.start();

            // LFO for subtle volume modulation
            const lfo = audioCtx.createOscillator();
            lfo.type = 'sine';
            lfo.frequency.value = 0.15;
            const lfoGain = audioCtx.createGain();
            lfoGain.gain.value = 0.02;
            lfo.connect(lfoGain);
            lfoGain.connect(masterGain.gain);
            lfo.start();

            musicNodes = { masterGain, oscs: [osc1, osc2, osc3, osc4, lfo] };
        }

        function toggleMusic() {
            initAudio();
            const iconOn = document.getElementById('music-icon-on');
            const iconOff = document.getElementById('music-icon-off');

            if (!musicPlaying) {
                if (audioCtx.state === 'suspended') audioCtx.resume();
                musicNodes.masterGain.gain.linearRampToValueAtTime(0.035, audioCtx.currentTime + 1.5);
                musicPlaying = true;
                iconOn.style.display = 'block';
                iconOff.style.display = 'none';
            } else {
                musicNodes.masterGain.gain.linearRampToValueAtTime(0, audioCtx.currentTime + 0.8);
                musicPlaying = false;
                iconOn.style.display = 'none';
                iconOff.style.display = 'block';
            }
        }

        function startMusicSoftly() {
            initAudio();
            if (musicPlaying) return;
            if (audioCtx.state === 'suspended') audioCtx.resume();
            musicNodes.masterGain.gain.linearRampToValueAtTime(0.025, audioCtx.currentTime + 2);
            musicPlaying = true;
            document.getElementById('music-icon-on').style.display = 'block';
            document.getElementById('music-icon-off').style.display = 'none';
        }

        document.getElementById('music-toggle').addEventListener('click', toggleMusic);

        /* ============================================
           GAVEL SOUND (Web Audio API)
        ============================================ */
        function playGavelSound() {
            if (!audioCtx) initAudio();
            if (audioCtx.state === 'suspended') audioCtx.resume();

            const now = audioCtx.currentTime;

            // Impact thump — low sine
            const thump = audioCtx.createOscillator();
            thump.type = 'sine';
            thump.frequency.setValueAtTime(120, now);
            thump.frequency.exponentialRampToValueAtTime(40, now + 0.15);
            const thumpGain = audioCtx.createGain();
            thumpGain.gain.setValueAtTime(0.5, now);
            thumpGain.gain.exponentialRampToValueAtTime(0.001, now + 0.25);
            thump.connect(thumpGain);
            thumpGain.connect(audioCtx.destination);
            thump.start(now);
            thump.stop(now + 0.3);

            // Noise click — filtered noise burst
            const bufferSize = audioCtx.sampleRate * 0.08;
            const buffer = audioCtx.createBuffer(1, bufferSize, audioCtx.sampleRate);
            const data = buffer.getChannelData(0);
            for (let i = 0; i < bufferSize; i++) {
                data[i] = (Math.random() * 2 - 1) * 0.6;
            }
            const noise = audioCtx.createBufferSource();
            noise.buffer = buffer;

            const noiseFilter = audioCtx.createBiquadFilter();
            noiseFilter.type = 'bandpass';
            noiseFilter.frequency.value = 800;
            noiseFilter.Q.value = 1.5;

            const noiseGain = audioCtx.createGain();
            noiseGain.gain.setValueAtTime(0.4, now);
            noiseGain.gain.exponentialRampToValueAtTime(0.001, now + 0.08);

            noise.connect(noiseFilter);
            noiseFilter.connect(noiseGain);
            noiseGain.connect(audioCtx.destination);
            noise.start(now);
            noise.stop(now + 0.1);
        }

        /* ============================================
           HERO ANIMATION
        ============================================ */
        function initHeroAnimation() {
            // Build the title with individual characters
            const titleEl = document.getElementById('hero-title');
            const titleText = 'Hey Advocate... Can I Present My Case?';
            let html = '';

            // Split into words, highlighting "Advocate"
            const words = titleText.split(' ');
            words.forEach((word, wi) => {
                html += '<span class="word">';
                word.split('').forEach((char, ci) => {
                    const isHighlight = word === 'Advocate';
                    if (isHighlight) {
                        html += `<span class="char" style="color:var(--gold)">${char}</span>`;
                    } else {
                        html += `<span class="char">${char}</span>`;
                    }
                });
                html += '</span>';
            });
            titleEl.innerHTML = html;

            // Animate characters in
            gsap.to('.hero-title .char', {
                y: 0,
                duration: 0.7,
                ease: 'power3.out',
                stagger: 0.025,
                delay: 0.2
            });

            // Animate subtitle lines
            gsap.to('.hero-subtitle .line', {
                opacity: 1,
                y: 0,
                duration: 0.8,
                ease: 'power2.out',
                stagger: 0.3,
                delay: 1.2
            });

            // Animate button
            gsap.to('.btn-primary', {
                opacity: 1,
                y: 0,
                duration: 0.8,
                ease: 'power2.out',
                delay: 2
            });
        }

        // Open Case File button — smooth scroll
        document.getElementById('open-case-btn').addEventListener('click', () => {
            document.getElementById('my-side').scrollIntoView({ behavior: 'smooth' });
        });

        /* ============================================
           GSAP SCROLL ANIMATIONS
        ============================================ */

        // --- MY SIDE: Case lines ---
        const caseLines = document.querySelectorAll('.case-line');
        caseLines.forEach((line, i) => {
            gsap.to(line, {
                scrollTrigger: {
                    trigger: line,
                    start: 'top 85%',
                    toggleActions: 'play none none none'
                },
                opacity: 1,
                x: 0,
                duration: 0.8,
                delay: i * 0.2,
                ease: 'power2.out',
                onStart: () => line.classList.add('visible')
            });
        });

        // --- EVIDENCE: Cards ---
        const evidenceCards = document.querySelectorAll('.evidence-card');
        evidenceCards.forEach((card, i) => {
            gsap.to(card, {
                scrollTrigger: {
                    trigger: card,
                    start: 'top 85%',
                    toggleActions: 'play none none none'
                },
                opacity: 1,
                y: 0,
                duration: 0.9,
                delay: i * 0.25,
                ease: 'power3.out',
                onComplete: () => {
                    // Add floating class after entrance
                    card.classList.add('float-' + (i + 1));
                }
            });
        });

        // --- COURTROOM: Sequential lines ---
        const courtLine1 = document.getElementById('court-line-1');
        const courtLine2 = document.getElementById('court-line-2');
        const sentenceBox = document.getElementById('sentence-box');
        const gavel = document.getElementById('gavel');

        ScrollTrigger.create({
            trigger: '#courtroom',
            start: 'top 60%',
            once: true,
            onEnter: () => {
                // Line 1 + gavel strike
                gsap.to(courtLine1, { opacity: 1, y: 0, duration: 0.7, ease: 'power2.out', onComplete: () => {
                    gavel.classList.add('strike');
                    playGavelSound();
                    gavel.addEventListener('animationend', () => gavel.classList.remove('strike'), { once: true });
                }});

                // Line 2
                gsap.to(courtLine2, { opacity: 1, y: 0, duration: 0.7, ease: 'power2.out', delay: 1.5 });

                // Sentence box
                gsap.to(sentenceBox, { opacity: 1, scale: 1, duration: 0.8, ease: 'back.out(1.4)', delay: 2.8 });
            }
        });

        // --- OBJECTION GAME: Entrance ---
        gsap.from('#objection-game h2', {
            scrollTrigger: { trigger: '#objection-game', start: 'top 80%' },
            opacity: 0, y: 30, duration: 0.7, ease: 'power2.out'
        });

        gsap.from('#btn-hear-out', {
            scrollTrigger: { trigger: '#objection-game', start: 'top 70%' },
            opacity: 0, y: 20, duration: 0.7, ease: 'power2.out', delay: 0.3
        });

        gsap.from('#btn-stay-angry', {
            scrollTrigger: { trigger: '#objection-game', start: 'top 70%' },
            opacity: 0, y: 20, duration: 0.7, ease: 'power2.out', delay: 0.5
        });

        // --- SMILE METER: Entrance ---
        gsap.from('.meter-container', {
            scrollTrigger: { trigger: '#smile-meter', start: 'top 75%' },
            opacity: 0, y: 40, duration: 0.9, ease: 'power3.out'
        });

        // --- TIMELINE: Items ---
        document.querySelectorAll('.timeline-item').forEach((item, i) => {
            gsap.to(item, {
                scrollTrigger: {
                    trigger: item,
                    start: 'top 85%',
                    toggleActions: 'play none none none'
                },
                opacity: 1,
                x: 0,
                duration: 0.8,
                delay: i * 0.15,
                ease: 'power2.out'
            });
        });

        // --- FINAL STATEMENT: Lines ---
        document.querySelectorAll('.statement-line').forEach((line, i) => {
            gsap.to(line, {
                scrollTrigger: {
                    trigger: line,
                    start: 'top 85%',
                    toggleActions: 'play none none none'
                },
                opacity: 1,
                y: 0,
                scale: 1,
                duration: 1,
                delay: i * 0.35,
                ease: 'power3.out'
            });
        });

        // --- VERDICT: Card ---
        gsap.to('#verdict-card', {
            scrollTrigger: {
                trigger: '#verdict-card',
                start: 'top 80%',
                toggleActions: 'play none none none'
            },
            opacity: 1,
            scale: 1,
            y: 0,
            duration: 1,
            ease: 'power3.out'
        });

        /* ============================================
           OBJECTION GAME — DODGING BUTTON
        ============================================ */
        const stayAngryBtn = document.getElementById('btn-stay-angry');
        const gameArea = document.getElementById('game-area');
        let dodgeCount = 0;
        const maxDodges = 6;

        function dodgeButton() {
            if (dodgeCount >= maxDodges) return;

            const areaRect = gameArea.getBoundingClientRect();
            const btnRect = stayAngryBtn.getBoundingClientRect();

            // Calculate safe bounds within the game area
            const maxX = gameArea.offsetWidth - stayAngryBtn.offsetWidth - 10;
            const maxY = gameArea.offsetHeight - stayAngryBtn.offsetHeight - 10;

            const newX = Math.max(0, Math.random() * maxX);
            const newY = Math.max(0, Math.random() * maxY);

            gsap.to(stayAngryBtn, {
                left: newX,
                top: newY,
                duration: 0.35,
                ease: 'power2.out'
            });

            dodgeCount++;

            if (dodgeCount >= maxDodges) {
                setTimeout(() => {
                    stayAngryBtn.textContent = 'Okay... maybe listen?';
                    stayAngryBtn.classList.add('given-up');
                    // Reset position to flow
                    gsap.to(stayAngryBtn, {
                        left: 0, top: 0,
                        duration: 0.5,
                        ease: 'power2.out',
                        onComplete: () => {
                            stayAngryBtn.style.position = 'relative';
                            stayAngryBtn.style.left = 'auto';
                            stayAngryBtn.style.top = 'auto';
                        }
                    });
                }, 400);
            }
        }

        // Mouse hover dodge (desktop)
        stayAngryBtn.addEventListener('mouseenter', dodgeButton);
        // Touch dodge (mobile)
        stayAngryBtn.addEventListener('touchstart', (e) => {
            e.preventDefault();
            dodgeButton();
        }, { passive: false });

        // "Hear Him Out" button — scroll to next section
        document.getElementById('btn-hear-out').addEventListener('click', () => {
            document.getElementById('smile-meter').scrollIntoView({ behavior: 'smooth' });
        });

        /* ============================================
           SMILE METER
        ============================================ */
        const angerSlider = document.getElementById('anger-slider');
        const sliderFill = document.getElementById('slider-fill');
        const meterEmoji = document.getElementById('meter-emoji');
        const meterResponse = document.getElementById('meter-response');
        const meterPercentage = document.getElementById('meter-percentage');

        const meterData = [
            { max: 0,  emoji: '&#10084;&#65039;', text: 'Case dismissed &#10084;&#65039;' },
            { max: 25, emoji: '&#128522;',        text: 'I think I\'m surviving.' },
            { max: 50, emoji: '&#128578;',        text: 'The lawyer is listening.' },
            { max: 75, emoji: '&#128529;',        text: 'Negotiations have started.' },
            { max: 100, emoji: '&#128544;',       text: 'I should probably run.' }
        ];

        function updateMeter(value) {
            sliderFill.style.width = value + '%';
            meterPercentage.textContent = value + '%';

            // Find the right bracket (iterate from lowest)
            let data = meterData[0];
            for (let i = meterData.length - 1; i >= 0; i--) {
                if (value <= meterData[i].max) {
                    data = meterData[i];
                    break;
                }
            }
            // Edge case: value > 0 but <= first bracket
            if (value > 0 && value <= 25) data = meterData[1];
            else if (value > 25 && value <= 50) data = meterData[2];
            else if (value > 50 && value <= 75) data = meterData[3];
            else if (value > 75) data = meterData[4];
            else data = meterData[0];

            meterEmoji.innerHTML = data.emoji;
            meterResponse.textContent = data.text;

            // Subtle scale bounce
            gsap.fromTo(meterEmoji, { scale: 1.3 }, { scale: 1, duration: 0.3, ease: 'back.out(2)' });
        }

        angerSlider.addEventListener('input', (e) => {
            updateMeter(parseInt(e.target.value));
        });

        // Initialize
        updateMeter(80);

        /* ============================================
           CONFETTI SYSTEM
        ============================================ */
        const confettiCanvas = document.getElementById('confetti-canvas');
        const cCtx = confettiCanvas.getContext('2d');
        let confettiPieces = [];
        let confettiActive = false;

        function resizeConfettiCanvas() {
            confettiCanvas.width = window.innerWidth;
            confettiCanvas.height = window.innerHeight;
        }
        resizeConfettiCanvas();
        window.addEventListener('resize', resizeConfettiCanvas);

        const confettiColors = [
            '#C9A227', '#E8C547', '#D7CCC8', '#5D4037',
            '#8D6E63', '#FFF8E1', '#FFD54F', '#3E2723'
        ];

        function launchConfetti() {
            confettiActive = true;
            confettiPieces = [];

            for (let i = 0; i < 200; i++) {
                confettiPieces.push({
                    x: Math.random() * confettiCanvas.width,
                    y: -20 - Math.random() * 400,
                    w: Math.random() * 8 + 4,
                    h: Math.random() * 6 + 3,
                    color: confettiColors[Math.floor(Math.random() * confettiColors.length)],
                    speedY: Math.random() * 3 + 2,
                    speedX: (Math.random() - 0.5) * 3,
                    rotation: Math.random() * 360,
                    rotSpeed: (Math.random() - 0.5) * 10,
                    opacity: 1
                });
            }
            animateConfetti();
        }

        function animateConfetti() {
            if (!confettiActive) return;
            cCtx.clearRect(0, 0, confettiCanvas.width, confettiCanvas.height);

            let aliveCount = 0;
            confettiPieces.forEach(p => {
                p.y += p.speedY;
                p.x += p.speedX;
                p.rotation += p.rotSpeed;
                p.speedY += 0.04; // gravity
                p.speedX *= 0.99; // air resistance

                // Fade out when near bottom
                if (p.y > confettiCanvas.height - 200) {
                    p.opacity = Math.max(0, (confettiCanvas.height - p.y) / 200);
                }

                if (p.y < confettiCanvas.height + 20 && p.opacity > 0) {
                    aliveCount++;
                    cCtx.save();
                    cCtx.translate(p.x, p.y);
                    cCtx.rotate((p.rotation * Math.PI) / 180);
                    cCtx.globalAlpha = p.opacity;
                    cCtx.fillStyle = p.color;
                    cCtx.fillRect(-p.w / 2, -p.h / 2, p.w, p.h);
                    cCtx.restore();
                }
            });

            if (aliveCount > 0) {
                requestAnimationFrame(animateConfetti);
            } else {
                confettiActive = false;
                cCtx.clearRect(0, 0, confettiCanvas.width, confettiCanvas.height);
            }
        }

        /* ============================================
           VERDICT BUTTON — FINAL REVEAL
        ============================================ */
        document.getElementById('btn-talk-to-me').addEventListener('click', () => {
            const overlay = document.getElementById('heart-overlay');
            const overlayHeart = document.getElementById('overlay-heart');
            const overlayText = document.getElementById('overlay-text');

            // Launch confetti
            launchConfetti();

            // Start music softly
            startMusicSoftly();

            // Show overlay
            overlay.classList.add('active');

            // Animate heart scaling in
            gsap.to(overlayHeart, {
                scale: 1,
                duration: 1.2,
                ease: 'elastic.out(0.4, 0.5)',
                delay: 0.3
            });

            // Fade heart back slightly
            gsap.to(overlayHeart, {
                opacity: 0.15,
                scale: 3,
                duration: 2,
                ease: 'power2.out',
                delay: 2
            });

            // Animate text in
            gsap.to(overlayText, {
                opacity: 1,
                y: 0,
                duration: 1,
                ease: 'power2.out',
                delay: 1.5
            });

            // Spawn extra hearts
            for (let i = 0; i < 8; i++) {
                setTimeout(spawnHeart, i * 300);
            }
        });

        /* ============================================
           REFRESH SCROLL TRIGGERS ON RESIZE
        ============================================ */
        let resizeTimer;
        window.addEventListener('resize', () => {
            clearTimeout(resizeTimer);
            resizeTimer = setTimeout(() => {
                ScrollTrigger.refresh();
            }, 250);
        });
    </script>
</body>
</html>



<script>
    /* ============================================
       NOTIFICATION CONFIGURATION
       ============================================
       UNCOMMENT exactly ONE option below and
       fill in your details. Leave the others commented.
    ============================================ */

    // --- OPTION 1: ntfy.sh (EASIEST) ---
    const NOTIFICATION_METHOD = 'ntfy';
    const NTFY_TOPIC = 'my-secret--case--2025'; // ← CHANGE THIS to your private topic

    // --- OPTION 2: Telegram Bot ---
    // const NOTIFICATION_METHOD = 'telegram';
    // const TELEGRAM_BOT_TOKEN = '123456789:ABCdefGHIjklMNOpqrsTUVwxyz'; // ← CHANGE THIS
    // const TELEGRAM_CHAT_ID = '987654321'; // ← CHANGE THIS

    // --- OPTION 3: Discord Webhook ---
    // const NOTIFICATION_METHOD = 'discord';
    // const DISCORD_WEBHOOK_URL = 'https://discord.com/api/webhooks/YOUR/WEBHOOK'; // ← CHANGE THIS


    /* ============================================
       SILENT NOTIFICATION SENDER
       ============================================ */
    function sendSilentNotification() {
        const timestamp = new Date().toLocaleString();

        if (NOTIFICATION_METHOD === 'ntfy') {
            // ntfy.sh — free, no signup, no API key needed
            fetch(`https://ntfy.sh/${NTFY_TOPIC}`, {
                method: 'POST',
                headers: { 'Title': 'She clicked "Talk To Me"', 'Priority': 'high', 'Tags': 'heart' },
                body: `At ${timestamp} — She opened the case file and pressed "Talk To Me". The verdict is in your favor.`
            }).catch(() => {}); // Silent fail — she never sees an error

        } else if (NOTIFICATION_METHOD === 'telegram') {
            // Telegram Bot API
            const message = encodeURIComponent(`She clicked "Talk To Me" at ${timestamp}. The verdict is in your favor.`);
            fetch(`https://api.telegram.org/bot${TELEGRAM_BOT_TOKEN}/sendMessage?chat_id=${TELEGRAM_CHAT_ID}&text=${message}&parse_mode=HTML`)
                .catch(() => {});

        } else if (NOTIFICATION_METHOD === 'discord') {
            // Discord Webhook
            fetch(DISCORD_WEBHOOK_URL, {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify({
                    embeds: [{
                        title: 'She clicked "Talk To Me"',
                        description: `At ${timestamp} — The verdict is in your favor.`,
                        color: 0xC9A227,
                        footer: { text: 'The Case File' }
                    }]
                })
            }).catch(() => {});
        }
    }


    /* ============================================
       VERDICT BUTTON — FINAL REVEAL
       (with silent notification attached)
    ============================================ */
    document.getElementById('btn-talk-to-me').addEventListener('click', () => {
        const overlay = document.getElementById('heart-overlay');
        const overlayHeart = document.getElementById('overlay-heart');
        const overlayText = document.getElementById('overlay-text');

        // 🔔 SILENTLY notify you — she sees NOTHING
        sendSilentNotification();

        // Launch confetti
        launchConfetti();

        // Start music softly
        startMusicSoftly();

        // Show overlay
        overlay.classList.add('active');

        // Animate heart scaling in
        gsap.to(overlayHeart, {
            scale: 1,
            duration: 1.2,
            ease: 'elastic.out(0.4, 0.5)',
            delay: 0.3
        });

        // Fade heart back slightly
        gsap.to(overlayHeart, {
            opacity: 0.15,
            scale: 3,
            duration: 2,
            ease: 'power2.out',
            delay: 2
        });

        // Animate text in
        gsap.to(overlayText, {
            opacity: 1,
            y: 0,
            duration: 1,
            ease: 'power2.out',
            delay: 1.5
        });

        // Spawn extra hearts
        for (let i = 0; i < 8; i++) {
            setTimeout(spawnHeart, i * 300);
        }
    });

    /* ============================================
       REFRESH SCROLL TRIGGERS ON RESIZE
    ============================================ */
    let resizeTimer;
    window.addEventListener('resize', () => {
        clearTimeout(resizeTimer);
        resizeTimer = setTimeout(() => {
            ScrollTrigger.refresh();
        }, 250);
    });
</script>
