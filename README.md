<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Likith J | SEO Growth Specialist</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #FF6500;
            --secondary: #1E3E62;
            --dark: #0B192C;
            --black: #000000;
            --text: #0B192C;
            --light: #FFFFFF;
        }
        
        * {
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            margin: 0;
            padding: 0;
            color: var(--text);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        /* Smooth scrolling */
        html {
            scroll-behavior: smooth;
        }
        
        /* Header animations */
        header {
            background: linear-gradient(135deg, var(--secondary) 0%, var(--dark) 100%);
            color: white;
            padding: 4rem 2rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        header::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            animation: shimmer 3s infinite;
        }
        
        @keyframes shimmer {
            0% { left: -100%; }
            100% { left: 100%; }
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            position: relative;
            z-index: 2;
            animation: fadeInUp 1s ease-out;
        }
        
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
        
        h1, h2, h3, h4 {
            color: var(--dark);
            margin-top: 0;
        }
        
        h1 {
            font-size: 2.8rem;
            margin-bottom: 0.5rem;
            color: white;
            animation: slideInLeft 1s ease-out 0.3s both;
        }
        
        @keyframes slideInLeft {
            from {
                opacity: 0;
                transform: translateX(-50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }
        
        .tagline {
            font-size: 1.4rem;
            font-weight: 500;
            margin-bottom: 1.5rem;
            color: rgba(255,255,255,0.9);
            animation: slideInRight 1s ease-out 0.6s both;
        }
        
        @keyframes slideInRight {
            from {
                opacity: 0;
                transform: translateX(50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }
        
        .hero-content p:last-child {
            animation: fadeIn 1s ease-out 0.9s both;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }
        
        section {
            padding: 4rem 0;
            opacity: 0;
            animation: fadeInUp 0.8s ease-out forwards;
        }
        
        section:nth-child(even) {
            animation-delay: 0.2s;
        }
        
        section:nth-child(odd) {
            animation-delay: 0.1s;
        }
        
        .section-title {
            color: var(--secondary);
            font-size: 2rem;
            margin-bottom: 2rem;
            text-align: center;
            position: relative;
            animation: slideInDown 0.8s ease-out;
        }
        
        @keyframes slideInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .section-title:after {
            content: "";
            display: block;
            width: 0;
            height: 4px;
            background: var(--primary);
            margin: 0.5rem auto 0;
            animation: expandWidth 1s ease-out 0.5s forwards;
        }
        
        @keyframes expandWidth {
            to {
                width: 80px;
            }
        }
        
        /* Value Proposition Section */
        .value-props {
            background-color: #f9f9f9;
        }
        
        .props-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .prop-card {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            border-top: 4px solid var(--primary);
            transform: translateY(20px);
            opacity: 0;
            animation: slideInUp 0.8s ease-out forwards;
            transition: all 0.3s ease;
        }
        
        .prop-card:nth-child(1) { animation-delay: 0.2s; }
        .prop-card:nth-child(2) { animation-delay: 0.4s; }
        .prop-card:nth-child(3) { animation-delay: 0.6s; }
        
        .prop-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.15);
        }
        
        @keyframes slideInUp {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        /* Results Section */
        .results-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
            margin: 2rem 0;
        }
        
        .result-card {
            background-color: var(--primary);
            color: white;
            padding: 1.5rem;
            border-radius: 8px;
            text-align: center;
            transform: scale(0.8);
            opacity: 0;
            animation: popIn 0.6s ease-out forwards;
            transition: transform 0.3s ease;
        }
        
        .result-card:nth-child(1) { animation-delay: 0.1s; }
        .result-card:nth-child(2) { animation-delay: 0.2s; }
        .result-card:nth-child(3) { animation-delay: 0.3s; }
        .result-card:nth-child(4) { animation-delay: 0.4s; }
        
        .result-card:hover {
            transform: scale(1.05);
        }
        
        @keyframes popIn {
            to {
                opacity: 1;
                transform: scale(1);
            }
        }
        
        .result-number {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            animation: countUp 1s ease-out;
        }
        
        @keyframes countUp {
            from {
                opacity: 0;
                transform: translateY(10px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        /* Experience Timeline */
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .timeline:before {
            content: '';
            position: absolute;
            width: 4px;
            background-color: var(--primary);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -2px;
            transform: scaleY(0);
            transform-origin: top;
            animation: growLine 1.5s ease-out 0.5s forwards;
        }
        
        @keyframes growLine {
            to {
                transform: scaleY(1);
            }
        }
        
        .timeline-item {
            padding: 10px 40px;
            position: relative;
            width: 50%;
            box-sizing: border-box;
            opacity: 0;
            animation: slideInTimeline 0.8s ease-out forwards;
        }
        
        .timeline-item:nth-child(1) { animation-delay: 0.8s; }
        .timeline-item:nth-child(2) { animation-delay: 1.0s; }
        .timeline-item:nth-child(3) { animation-delay: 1.2s; }
        .timeline-item:nth-child(4) { animation-delay: 1.4s; }
        
        .timeline-item:nth-child(odd) {
            left: 0;
            animation-name: slideInTimelineLeft;
        }
        
        .timeline-item:nth-child(even) {
            left: 50%;
            animation-name: slideInTimelineRight;
        }
        
        @keyframes slideInTimelineLeft {
            from {
                opacity: 0;
                transform: translateX(-50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }
        
        @keyframes slideInTimelineRight {
            from {
                opacity: 0;
                transform: translateX(50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }
        
        .timeline-content {
            padding: 20px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            position: relative;
            transition: all 0.3s ease;
        }
        
        .timeline-content:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.15);
        }
        
        .timeline-content:after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            right: -10px;
            background-color: white;
            top: 30px;
            border-radius: 50%;
            z-index: 1;
            border: 4px solid var(--primary);
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }
        
        .timeline-item:nth-child(even) .timeline-content:after {
            left: -10px;
        }
        
        .company {
            font-weight: 700;
            color: var(--secondary);
        }
        
        .date {
            color: #666;
            font-size: 0.9rem;
        }
        
        /* Skills Section */
        .skills-container {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-bottom: 2rem;
        }
        
        .skills-box {
            flex: 1;
            min-width: 300px;
            background-color: white;
            padding: 1.5rem;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            opacity: 0;
            transform: translateY(30px);
            animation: fadeInUp 0.8s ease-out forwards;
            transition: all 0.3s ease;
        }
        
        .skills-box:nth-child(1) { animation-delay: 0.2s; }
        .skills-box:nth-child(2) { animation-delay: 0.4s; }
        
        .skills-box:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.15);
        }
        
        .skills-box ul li {
            opacity: 0;
            animation: fadeInLeft 0.5s ease-out forwards;
        }
        
        .skills-box ul li:nth-child(1) { animation-delay: 0.5s; }
        .skills-box ul li:nth-child(2) { animation-delay: 0.6s; }
        .skills-box ul li:nth-child(3) { animation-delay: 0.7s; }
        .skills-box ul li:nth-child(4) { animation-delay: 0.8s; }
        .skills-box ul li:nth-child(5) { animation-delay: 0.9s; }
        
        @keyframes fadeInLeft {
            from {
                opacity: 0;
                transform: translateX(-20px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }
        
        /* Case Studies */
        .case-studies {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .case-study {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            opacity: 0;
            transform: translateY(30px);
            animation: slideInUp 0.8s ease-out forwards;
        }
        
        .case-study:nth-child(1) { animation-delay: 0.2s; }
        .case-study:nth-child(2) { animation-delay: 0.4s; }
        .case-study:nth-child(3) { animation-delay: 0.6s; }
        
        .case-study:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 15px 35px rgba(0,0,0,0.2);
        }
        
        .case-study-img {
            height: 200px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 2rem;
            font-weight: 700;
            position: relative;
            overflow: hidden;
        }
        
        .case-study-img::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: left 0.5s ease;
        }
        
        .case-study:hover .case-study-img::before {
            left: 100%;
        }
        
        .case-study-content {
            padding: 1.5rem;
        }
        
        /* Tools */
        .tools-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .tool-item {
            background-color: var(--primary);
            color: white;
            padding: 0.8rem;
            text-align: center;
            border-radius: 4px;
            font-weight: 500;
            opacity: 0;
            transform: scale(0.8);
            animation: toolAppear 0.5s ease-out forwards;
            transition: all 0.3s ease;
        }
        
        .tool-item:nth-child(1) { animation-delay: 0.1s; }
        .tool-item:nth-child(2) { animation-delay: 0.2s; }
        .tool-item:nth-child(3) { animation-delay: 0.3s; }
        .tool-item:nth-child(4) { animation-delay: 0.4s; }
        .tool-item:nth-child(5) { animation-delay: 0.5s; }
        .tool-item:nth-child(6) { animation-delay: 0.6s; }
        .tool-item:nth-child(7) { animation-delay: 0.7s; }
        .tool-item:nth-child(8) { animation-delay: 0.8s; }
        
        .tool-item:hover {
            transform: scale(1.05);
            background-color: #e05c00;
        }
        
        @keyframes toolAppear {
            to {
                opacity: 1;
                transform: scale(1);
            }
        }
        
        /* Contact */
        .contact-section {
            background-color: var(--secondary);
            color: white;
            text-align: center;
            padding: 4rem 2rem;
            position: relative;
            overflow: hidden;
        }
        
        .contact-section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: radial-gradient(circle at 30% 80%, rgba(255, 101, 0, 0.1) 0%, transparent 50%);
            animation: floating 6s ease-in-out infinite;
        }
        
        @keyframes floating {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }
        
        .contact-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }
        
        .contact-link {
            background-color: var(--primary);
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 4px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            opacity: 0;
            transform: translateY(20px);
            animation: slideInUp 0.6s ease-out forwards;
            position: relative;
            overflow: hidden;
        }
        
        .contact-link:nth-child(1) { animation-delay: 0.2s; }
        .contact-link:nth-child(2) { animation-delay: 0.4s; }
        .contact-link:nth-child(3) { animation-delay: 0.6s; }
        .contact-link:nth-child(4) { animation-delay: 0.8s; }
        
        .contact-link:hover {
            background-color: #e05c00;
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(255, 101, 0, 0.3);
        }
        
        .contact-link::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: left 0.5s ease;
        }
        
        .contact-link:hover::before {
            left: 100%;
        }
        
        footer {
            background-color: var(--dark);
            color: white;
            text-align: center;
            padding: 2rem;
            animation: fadeIn 1s ease-out;
        }
        
        /* Scroll animations */
        .scroll-reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease-out;
        }
        
        .scroll-reveal.revealed {
            opacity: 1;
            transform: translateY(0);
        }
        
        /* Mobile responsiveness */
        @media (max-width: 768px) {
            .timeline:before {
                left: 31px;
            }
            
            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 25px;
            }
            
            .timeline-item:nth-child(even) {
                left: 0;
            }
            
            .timeline-content:after {
                left: 21px;
            }
            
            .timeline-item:nth-child(even) .timeline-content:after {
                left: 21px;
            }
            
            h1 {
                font-size: 2.2rem;
            }
            
            .tagline {
                font-size: 1.2rem;
            }
            
            .contact-links {
                flex-direction: column;
                align-items: center;
            }
            
            .contact-link {
                width: 200px;
            }
        }
        
        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 10px;
        }
        
        ::-webkit-scrollbar-track {
            background: #f1f1f1;
        }
        
        ::-webkit-scrollbar-thumb {
            background: var(--primary);
            border-radius: 5px;
        }
        
        ::-webkit-scrollbar-thumb:hover {
            background: #e05c00;
        }
    </style>
</head>
<body>
    <header>
        <div class="hero-content">
            <h1>Likith J</h1>
            <p class="tagline">SEO Growth Specialist | Technical SEO Expert | Organic Traffic Architect</p>
            <p>5+ years driving measurable results through data-driven SEO strategies across IT, EdTech, and FoodTech sectors. Proven ability to increase keyword rankings, organic traffic, and revenue through technical audits, content optimization, and strategic link-building.</p>
        </div>
    </header>
    
    <section class="value-props">
        <div class="container">
            <h2 class="section-title">How I Drive Growth</h2>
            <div class="props-grid">
                <div class="prop-card">
                    <h3>Technical SEO Mastery</h3>
                    <p>I identify and resolve complex technical issues that hinder search performance, from crawl errors to Core Web Vitals optimization, ensuring your site meets Google's highest standards.</p>
                </div>
                <div class="prop-card">
                    <h3>Content That Converts</h3>
                    <p>Beyond keyword stuffing, I craft content strategies aligned with user intent and business goals, building topical authority that drives sustainable organic growth.</p>
                </div>
                <div class="prop-card">
                    <h3>Data-Driven Decisions</h3>
                    <p>Using advanced analytics and competitive intelligence, I focus on high-impact opportunities that deliver measurable ROI, not vanity metrics.</p>
                </div>
            </div>
        </div>
    </section>
    
    <section id="results">
        <div class="container">
            <h2 class="section-title">By The Numbers</h2>
            <div class="results-grid">
                <div class="result-card">
                    <div class="result-number">2500+</div>
                    <div>Keywords Ranked</div>
                </div>
                <div class="result-card">
                    <div class="result-number">150%</div>
                    <div>Traffic Increase</div>
                </div>
                <div class="result-card">
                    <div class="result-number">₹20L+</div>
                    <div>Revenue Generated</div>
                </div>
                <div class="result-card">
                    <div class="result-number">5X</div>
                    <div>Traffic Growth</div>
                </div>
            </div>
        </div>
    </section>
    
    <section id="experience">
        <div class="container">
            <h2 class="section-title">Professional Journey</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-content">
                        <span class="company">Ace Creative Learning</span>
                        <span class="date">2025 - Present</span>
                        <h3>SEO Manager</h3>
                        <ul>
                            <li>Led SEO for 3 E-learning verticals, contributing to ₹20+ lakhs in organic revenue within 2 months</li>
                            <li>Launched optimized course landing pages aligned with user intent and high-volume keywords</li>
                            <li>Managed Technical SEO, Core Web Vitals, Schema Markup, and Programmatic SEO</li>
                        </ul>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <span class="company">Eridium Digital Marketing</span>
                        <span class="date">2024</span>
                        <h3>Senior SEO Analyst</h3>
                        <ul>
                            <li>Led multiple SEO projects simultaneously across IT, electronics, and retail sectors</li>
                            <li>Oversaw client communication, audits, technical strategy, and performance tracking</li>
                            <li>Key clients: Ascendion, Harman, Trigent, and Algonomy</li>
                        </ul>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <span class="company">Hogr Food Networks (Curefoods)</span>
                        <span class="date">2022-2024</span>
                        <h3>SEO Specialist</h3>
                        <ul>
                            <li>5,000+ keyword rankings and 5X increase in organic traffic for EatFit, CakeZone, MasalaBox</li>
                            <li>Implemented city-specific GMB listings and built high-authority backlinks</li>
                            <li>Developed content clusters and pillar pages following E-E-A-T guidelines</li>
                        </ul>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <span class="company">Learnyst</span>
                        <span class="date">2020 - 2022</span>
                        <h3>Digital Marketing Associate</h3>
                        <ul>
                            <li>Managed SEO/SEM campaigns and optimized company blogs</li>
                            <li>Produced explainer videos and creatives for demand generation</li>
                            <li>Implemented schema markup and improved website performance</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <section id="case-studies">
        <div class="container">
            <h2 class="section-title">Brand Success Stories</h2>
            <div class="case-studies">
                <div class="case-study">
                    <div class="case-study-img" style="background-color: #1E3E62;">CakeZone</div>
                    <div class="case-study-content">
                        <h3>43% Organic Traffic Growth</h3>
                        <ul>
                            <li>800+ first-page keyword rankings</li>
                            <li>Developed category-specific landing pages (birthday cakes, photo cakes, etc.)</li>
                            <li>Localized pages for "near me" searches in Bangalore, Chennai, Delhi</li>
                            <li>Implemented Google Merchant Center for product visibility</li>
                        </ul>
                    </div>
                </div>
                
                <div class="case-study">
                    <div class="case-study-img" style="background-color: #FF6500;">EatFit</div>
                    <div class="case-study-content">
                        <h3>35% Traffic Increase in 4 Months</h3>
                        <ul>
                            <li>500+ first-page keyword rankings</li>
                            <li>Competitive analysis and comprehensive technical audit</li>
                            <li>Meal plan and location-specific landing pages</li>
                            <li>Content strategy establishing dietary authority</li>
                        </ul>
                    </div>
                </div>
                
                <div class="case-study">
                    <div class="case-study-img" style="background-color: #0B192C;">Trigent</div>
                    <div class="case-study-content">
                        <h3>Technical SEO Transformation</h3>
                        <ul>
                            <li>250+ new keyword rankings</li>
                            <li>Service page audits and content enhancements</li>
                            <li>Strategic backlink campaigns (PR, guest posts, events)</li>
                            <li>Core Web Vitals optimization</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <section id="skills">
        <div class="container">
            <h2 class="section-title">SEO Toolkit</h2>
            <div class="skills-container">
                <div class="skills-box">
                    <h3>Technical Expertise</h3>
                    <ul>
                        <li>Technical SEO audits</li>
                        <li>Core Web Vitals optimization</li>
                        <li>International SEO (hreflang)</li>
                        <li>Structured data & schema markup</li>
                        <li>Website architecture</li>
                    </ul>
                </div>
                <div class="skills-box">
                    <h3>Growth Strategies</h3>
                    <ul>
                        <li>Keyword research & clustering</li>
                        <li>Content strategy & optimization</li>
                        <li>Backlink strategy & outreach</li>
                        <li>Local SEO & GMB optimization</li>
                        <li>Data-driven decision making</li>
                    </ul>
                </div>
            </div>
            
            <h3 style="margin-top: 2rem;">Tools I Master</h3>
            <div class="tools-grid">
                <div class="tool-item">Ahrefs</div>
                <div class="tool-item">SEMrush</div>
                <div class="tool-item">Google Analytics 4</div>
                <div class="tool-item">Search Console</div>
                <div class="tool-item">Screaming Frog</div>
                <div class="tool-item">Google Looker</div>
                <div class="tool-item">n8n Automation</div>
                <div class="tool-item">LLM Prompt Engineering</div>
            </div>
        </div>
    </section>
    
    <section class="contact-section">
        <div class="container">
            <h2 style="color: white;">Ready to Transform Your Organic Growth?</h2>
            <p>I'm currently available for consulting and leadership opportunities.</p>
            <div class="contact-links">
                <a href="mailto:liikkeshav1024@gmail.com" class="contact-link">Email Me</a>
                <a href="tel:+919632271484" class="contact-link">Call +91 96322 71484</a>
                <a href="https://linkedin.com/in/likithjay" class="contact-link">LinkedIn</a>
                <a href="https://traffyki.in" class="contact-link">Read My Blog</a>
            </div>
        </div>
    </section>
    
    <footer>
        <p>&copy; 2025 Likith J | SEO Growth Specialist</p>
        <p>E-city, Bengaluru, Karnataka</p>
    </footer>

    <script>
        // Intersection Observer for scroll animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Observe all sections
        document.querySelectorAll('section').forEach(section => {
            observer.observe(section);
        });

        // Add floating animation to result numbers
        document.querySelectorAll('.result-number').forEach((element, index) => {
            element.style.animationDelay = `${index * 0.2}s`;
        });

        // Add staggered animation to timeline items
        document.querySelectorAll('.timeline-item').forEach((item, index) => {
            item.style.animationDelay = `${0.8 + index * 0.2}s`;
        });

        // Add parallax effect to header
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const header = document.querySelector('header');
            header.style.transform = `translateY(${scrolled * 0.5}px)`;
        });

        // Add smooth scroll for internal links
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
    </script>
</body>
</html>
