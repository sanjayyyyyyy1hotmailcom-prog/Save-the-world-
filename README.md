<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Wake Up, World! — Modern Communism for Humanity</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a2a6c, #b21f1f, #1a2a6c);
            color: #fff;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            overflow-x: hidden;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            text-align: center;
        }
        
        h1 {
            font-size: 3.5rem;
            text-shadow: 0 0 15px rgba(255, 255, 255, 0.7);
            margin-bottom: 30px;
            letter-spacing: 1px;
            animation: glow 2s infinite alternate;
        }
        
        .subtitle {
            font-size: 1.8rem;
            margin-bottom: 40px;
            font-weight: 300;
            text-shadow: 0 0 10px rgba(255, 255, 255, 0.5);
        }
        
        .flipbook-container {
            perspective: 2000px;
            margin: 0 auto 40px;
            width: 900px;
            height: 600px;
            position: relative;
        }
        
        .flipbook {
            width: 100%;
            height: 100%;
            position: relative;
            transform-style: preserve-3d;
            transform: translateZ(-450px);
        }
        
        .page {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 25px rgba(0, 0, 0, 0.7);
            background: linear-gradient(45deg, #2c3e50, #1a1a2e);
            padding: 30px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            backface-visibility: hidden;
            transition: transform 0.8s ease;
        }
        
        .page-content {
            max-width: 80%;
            z-index: 2;
        }
        
        .page-title {
            font-size: 2.5rem;
            margin-bottom: 20px;
            text-shadow: 0 0 10px rgba(255, 255, 255, 0.5);
        }
        
        .page-text {
            font-size: 1.5rem;
            margin-bottom: 30px;
            line-height: 1.6;
        }
        
        .visual {
            width: 100%;
            height: 200px;
            margin: 20px 0;
            border-radius: 10px;
            position: relative;
            overflow: hidden;
        }
        
        .navigation {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }
        
        .nav-btn {
            background: linear-gradient(45deg, #e74c3c, #c0392b);
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 1.2rem;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }
        
        .nav-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.4);
            background: linear-gradient(45deg, #c0392b, #e74c3c);
        }
        
        .nav-btn:disabled {
            opacity: 0.5;
            cursor: not-allowed;
            transform: none;
        }
        
        .page-counter {
            font-size: 1.3rem;
            margin-top: 15px;
            background: rgba(0, 0, 0, 0.3);
            padding: 8px 20px;
            border-radius: 30px;
            display: inline-block;
        }
        
        /* Animation classes */
        .animate-in {
            animation: fadeIn 0.8s ease-out forwards;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        @keyframes glow {
            from { text-shadow: 0 0 10px rgba(255, 255, 255, 0.7); }
            to { text-shadow: 0 0 20px rgba(255, 255, 255, 0.9), 0 0 30px rgba(255, 255, 255, 0.8); }
        }
        
        /* Visual animations */
        .sun-rise {
            background: linear-gradient(to bottom, #1a237e, #5d4037);
            position: relative;
        }
        
        .sun {
            position: absolute;
            width: 80px;
            height: 80px;
            background: radial-gradient(circle, #ffeb3b, #ff9800);
            border-radius: 50%;
            bottom: 10px;
            left: 50%;
            transform: translateX(-50%);
            box-shadow: 0 0 40px #ff9800;
            animation: rise 15s infinite alternate;
        }
        
        @keyframes rise {
            0% { bottom: 10px; box-shadow: 0 0 20px #ff9800; }
            100% { bottom: 150px; box-shadow: 0 0 60px #ffeb3b; }
        }
        
        .split-world {
            display: flex;
            height: 100%;
        }
        
        .luxury {
            flex: 1;
            background: linear-gradient(45deg, #3498db, #2c3e50);
            position: relative;
            overflow: hidden;
        }
        
        .slums {
            flex: 1;
            background: linear-gradient(45deg, #e74c3c, #c0392b);
            position: relative;
            overflow: hidden;
        }
        
        .building {
            position: absolute;
            bottom: 0;
            width: 30px;
            background: linear-gradient(to top, #3498db, #2c3e50);
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
        }
        
        .worker {
            position: absolute;
            bottom: 0;
            width: 15px;
            height: 25px;
            background: #ecf0f1;
            border-radius: 3px;
        }
        
        .headline {
            position: absolute;
            width: 100%;
            height: 30px;
            background: rgba(0, 0, 0, 0.7);
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.9rem;
            animation: scroll 20s linear infinite;
        }
        
        @keyframes scroll {
            0% { transform: translateY(200px); }
            100% { transform: translateY(-30px); }
        }
        
        .eye-animation {
            position: relative;
            width: 100px;
            height: 100px;
            margin: 0 auto;
        }
        
        .eye {
            position: absolute;
            width: 100px;
            height: 60px;
            background: #5d4037;
            border-radius: 50%;
            overflow: hidden;
            top: 20px;
        }
        
        .eyelid {
            position: absolute;
            width: 100px;
            height: 60px;
            background: #3e2723;
            border-radius: 50%;
            top: -30px;
            animation: blink 4s infinite;
        }
        
        .pupil {
            position: absolute;
            width: 30px;
            height: 30px;
            background: #000;
            border-radius: 50%;
            top: 15px;
            left: 35px;
        }
        
        @keyframes blink {
            0%, 45%, 55%, 100% { top: -30px; }
            50% { top: 0; }
        }
        
        .heart-symbol {
            width: 120px;
            height: 120px;
            background: #e74c3c;
            position: relative;
            transform: rotate(45deg);
            margin: 40px auto;
            animation: beat 1.5s infinite;
        }
        
        .heart-symbol:before,
        .heart-symbol:after {
            content: '';
            width: 120px;
            height: 120px;
            background: #e74c3c;
            border-radius: 50%;
            position: absolute;
        }
        
        .heart-symbol:before {
            top: -60px;
            left: 0;
        }
        
        .heart-symbol:after {
            top: 0;
            left: -60px;
        }
        
        @keyframes beat {
            0% { transform: rotate(45deg) scale(1); }
            50% { transform: rotate(45deg) scale(1.1); }
            100% { transform: rotate(45deg) scale(1); }
        }
        
        .hands-up {
            position: relative;
            height: 100%;
            width: 100%;
        }
        
        .hand {
            position: absolute;
            width: 40px;
            height: 80px;
            background: #ffccbc;
            border-radius: 20px;
            bottom: 0;
            animation: raise 3s forwards;
        }
        
        @keyframes raise {
            0% { bottom: 0; }
            100% { bottom: 150px; }
        }
        
        .protest-crowd {
            position: relative;
            height: 100%;
        }
        
        .person {
            position: absolute;
            width: 20px;
            height: 40px;
            background: #78909c;
            bottom: 0;
            border-radius: 5px;
        }
        
        .banner {
            position: absolute;
            width: 40px;
            height: 10px;
            background: #e74c3c;
            bottom: 45px;
            animation: wave 3s infinite;
        }
        
        @keyframes wave {
            0%, 100% { transform: rotate(0); }
            50% { transform: rotate(5deg); }
        }
        
        .dove {
            position: absolute;
            color: white;
            font-size: 24px;
            animation: fly 10s linear infinite;
        }
        
        @keyframes fly {
            0% { transform: translateX(-100px) translateY(100px); }
            100% { transform: translateX(900px) translateY(0); }
        }
        
        .kite {
            position: absolute;
            width: 30px;
            height: 50px;
            background: linear-gradient(45deg, #ff0000, #ffff00, #00ff00, #0000ff, #ff00ff);
            clip-path: polygon(50% 0%, 0% 100%, 100% 100%);
            animation: float 8s infinite ease-in-out;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-30px); }
        }
        
        .unity-wave {
            position: relative;
            height: 100%;
        }
        
        .wave-person {
            position: absolute;
            width: 20px;
            height: 40px;
            background: #78909c;
            bottom: 0;
            border-radius: 5px;
            animation: wave-rise 2s forwards;
        }
        
        @keyframes wave-rise {
            0% { bottom: 0; }
            100% { bottom: 100px; }
        }
        
        /* Responsive design */
        @media (max-width: 1000px) {
            .flipbook-container {
                width: 95%;
                height: 500px;
            }
            
            h1 {
                font-size: 2.8rem;
            }
            
            .page-title {
                font-size: 2rem;
            }
            
            .page-text {
                font-size: 1.3rem;
            }
        }
        
        @media (max-width: 768px) {
            .flipbook-container {
                height: 400px;
            }
            
            h1 {
                font-size: 2.2rem;
            }
            
            .subtitle {
                font-size: 1.4rem;
            }
            
            .page-title {
                font-size: 1.6rem;
            }
            
            .page-text {
                font-size: 1.1rem;
            }
            
            .visual {
                height: 150px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Wake Up, World!</h1>
        <div class="subtitle">Modern Communism for Humanity</div>
        
        <div class="flipbook-container">
            <div class="flipbook" id="flipbook">
                <!-- Page 1 -->
                <div class="page" id="page1" style="transform: rotateY(0deg) translateZ(1px); z-index: 20;">
                    <div class="page-content animate-in">
                        <h2 class="page-title">The Broken World</h2>
                        <p class="page-text">"The world is broken... but not by accident. It was built this way."</p>
                        <div class="visual sun-rise">
                            <div class="sun"></div>
                        </div>
                    </div>
                </div>
                
                <!-- Page 2 -->
                <div class="page" id="page2" style="transform: rotateY(0deg) translateZ(1px); z-index: 19;">
                    <div class="page-content">
                        <h2 class="page-title">Exposing the System</h2>
                        <p class="page-text">"Corporate greed has failed us all. It chews up workers. It fattens billionaires. It leaves families behind."</p>
                        <div class="visual split-world">
                            <div class="luxury" id="luxury-side"></div>
                            <div class="slums" id="slums-side"></div>
                        </div>
                    </div>
                </div>
                
                <!-- Page 3 -->
                <div class="page" id="page3" style="transform: rotateY(0deg) translateZ(1px); z-index: 18;">
                    <div class="page-content">
                        <h2 class="page-title">Who Built It?</h2>
                        <p class="page-text">"We built the world… yet we’re denied the dignity to live in it."</p>
                        <div class="visual" style="background: linear-gradient(45deg, #455a64, #37474f);">
                            <div class="headline">Workers Demand Fair Wages</div>
                            <div class="headline" style="top: 50px;">Healthcare Crisis Deepens</div>
                            <div class="headline" style="top: 100px;">Families Struggle to Make Ends Meet</div>
                        </div>
                    </div>
                </div>
                
                <!-- Page 4 -->
                <div class="page" id="page4" style="transform: rotateY(0deg) translateZ(1px); z-index: 17;">
                    <div class="page-content">
                        <h2 class="page-title">Awakening</h2>
                        <p class="page-text">"It's time to wake up."</p>
                        <div class="visual" style="background: linear-gradient(45deg, #0d47a1, #1976d2);">
                            <div class="eye-animation">
                                <div class="eye">
                                    <div class="eyelid"></div>
                                    <div class="pupil"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Page 5 -->
                <div class="page" id="page5" style="transform: rotateY(0deg) translateZ(1px); z-index: 16;">
                    <div class="page-content">
                        <h2 class="page-title">A Vision for Change</h2>
                        <p class="page-text">"This is not about the past. This is about our future."</p>
                        <div class="visual hands-up">
                            <div class="hand" style="left: 20%;"></div>
                            <div class="hand" style="left: 40%; background: #d7ccc8;"></div>
                            <div class="hand" style="left: 60%; background: #bcaaa4;"></div>
                            <div class="hand" style="left: 80%; background: #a1887f;"></div>
                        </div>
                    </div>
                </div>
                
                <!-- Page 6 -->
                <div class="page" id="page6" style="transform: rotateY(0deg) translateZ(1px); z-index: 15;">
                    <div class="page-content">
                        <h2 class="page-title">Introducing Modern Communism</h2>
                        <p class="page-text">"Modern Communism is a revolution of the heart—a system that puts people first."</p>
                        <div class="visual">
                            <div class="heart-symbol"></div>
                        </div>
                    </div>
                </div>
                
                <!-- Page 7 -->
                <div class="page" id="page7" style="transform: rotateY(0deg) translateZ(1px); z-index: 14;">
                    <div class="page-content">
                        <h2 class="page-title">Justice</h2>
                        <p class="page-text">"A world where healthcare is a right, not a luxury."</p>
                        <div class="visual" style="background: linear-gradient(45deg, #388e3c, #66bb6a); display: flex; justify-content: center; align-items: center;">
                            <i class="fas fa-heartbeat" style="font-size: 80px; color: white;"></i>
                        </div>
                    </div>
                </div>
                
                <!-- Page 8 -->
                <div class="page" id="page8" style="transform: rotateY(0deg) translateZ(1px); z-index: 13;">
                    <div class="page-content">
                        <h2 class="page-title">Equality</h2>
                        <p class="page-text">"Education is free, excellent, and universal."</p>
                        <div class="visual" style="background: linear-gradient(45deg, #ffa000, #ffca28); display: flex; justify-content: center; align-items: center;">
                            <i class="fas fa-graduation-cap" style="font-size: 80px; color: white;"></i>
                        </div>
                    </div>
                </div>
                
                <!-- Page 9 -->
                <div class="page" id="page9" style="transform: rotateY(0deg) translateZ(1px); z-index: 12;">
                    <div class="page-content">
                        <h2 class="page-title">Dignity of Work</h2>
                        <p class="page-text">"Every job is secure and respected."</p>
                        <div class="visual" style="background: linear-gradient(45deg, #7b1fa2, #ab47bc); display: flex; justify-content: center; align-items: center; gap: 20px;">
                            <i class="fas fa-hammer" style="font-size: 60px;"></i>
                            <i class="fas fa-paint-brush" style="font-size: 60px;"></i>
                            <i class="fas fa-laptop-code" style="font-size: 60px;"></i>
                        </div>
                    </div>
                </div>
                
                <!-- Page 10 -->
                <div class="page" id="page10" style="transform: rotateY(0deg) translateZ(1px); z-index: 11;">
                    <div class="page-content">
                        <h2 class="page-title">No Family Left Behind</h2>
                        <p class="page-text">"No family is left to struggle."</p>
                        <div class="visual" style="background: linear-gradient(45deg, #0288d1, #4fc3f7); display: flex; justify-content: center; align-items: center;">
                            <i class="fas fa-home" style="font-size: 80px;"></i>
                        </div>
                    </div>
                </div>
                
                <!-- Page 11 -->
                <div class="page" id="page11" style="transform: rotateY(0deg) translateZ(1px); z-index: 10;">
                    <div class="page-content">
                        <h2 class="page-title">Values</h2>
                        <p class="page-text">“This is Modern Communism: Democratic. Compassionate. Built for the real world.”</p>
                        <div class="visual" style="display: flex; justify-content: center; align-items: center; gap: 30px;">
                            <i class="fas fa-balance-scale" style="font-size: 60px; color: #4CAF50;"></i>
                            <i class="fas fa-equals" style="font-size: 60px; color: #FFC107;"></i>
                            <i class="fas fa-heart" style="font-size: 60px; color: #F44336;"></i>
                        </div>
                    </div>
                </div>
                
                <!-- Page 12 -->
                <div class="page" id="page12" style="transform: rotateY(0deg) translateZ(1px); z-index: 9;">
                    <div class="page-content">
                        <h2 class="page-title">Uprising</h2>
                        <p class="page-text">"The time for polite reform is over."</p>
                        <div class="visual protest-crowd" id="protest-crowd"></div>
                    </div>
                </div>
                
                <!-- Page 13 -->
                <div class="page" id="page13" style="transform: rotateY(0deg) translateZ(1px); z-index: 8;">
                    <div class="page-content">
                        <h2 class="page-title">Breaking the Illusion</h2>
                        <p class="page-text">"The system isn’t broken — it’s rigged."</p>
                        <div class="visual" style="background: linear-gradient(45deg, #5d4037, #8d6e63); display: flex; justify-content: center; align-items: center;">
                            <i class="fas fa-cut" style="font-size: 80px; color: #e74c3c;"></i>
                        </div>
                    </div>
                </div>
                
                <!-- Page 14 -->
                <div class="page" id="page14" style="transform: rotateY(0deg) translateZ(1px); z-index: 7;">
                    <div class="page-content">
                        <h2 class="page-title">Empowerment</h2>
                        <p class="page-text">"It’s time to rewrite the rules."</p>
                        <div class="visual" style="background: linear-gradient(45deg, #00838f, #4fb3bf); display: flex; justify-content: center; align-items: center;">
                            <i class="fas fa-pencil-alt" style="font-size: 80px;"></i>
                        </div>
                    </div>
                </div>
                
                <!-- Page 15 -->
                <div class="page" id="page15" style="transform: rotateY(0deg) translateZ(1px); z-index: 6;">
                    <div class="page-content">
                        <h2 class="page-title">The Movement Grows</h2>
                        <p class="page-text">"Raise your voice. Join the peaceful revolution."</p>
                        <div class="visual" style="background: linear-gradient(45deg, #6a1b9a, #9c27b0); display: flex; justify-content: center; align-items: center; gap: 30px;">
                            <i class="fas fa-bullhorn" style="font-size: 60px;"></i>
                            <i class="fas fa-hashtag" style="font-size: 60px;"></i>
                            <i class="fas fa-share-alt" style="font-size: 60px;"></i>
                        </div>
                    </div>
                </div>
                
                <!-- Page 16 -->
                <div class="page" id="page16" style="transform: rotateY(0deg) translateZ(1px); z-index: 5;">
                    <div class="page-content">
                        <h2 class="page-title">The Peaceful Revolution</h2>
                        <p class="page-text">"Power to the Workers. Dignity for All."</p>
                        <div class="visual protest-crowd" id="global-crowd"></div>
                    </div>
                </div>
                
                <!-- Page 17 -->
                <div class="page" id="page17" style="transform: rotateY(0deg) translateZ(1px); z-index: 4;">
                    <div class="page-content">
                        <h2 class="page-title">Hopeful Future</h2>
                        <p class="page-text">"For a future where everyone rises."</p>
                        <div class="visual" style="background: linear-gradient(45deg, #2e7d32, #66bb6a); position: relative;">
                            <div class="kite" style="left: 20%; top: 30%;"></div>
                            <div class="kite" style="left: 50%; top: 20%; animation-delay: 0.5s;"></div>
                            <div class="kite" style="left: 70%; top: 40%; animation-delay: 1s;"></div>
                        </div>
                    </div>
                </div>
                
                <!-- Page 18 -->
                <div class="page" id="page18" style="transform: rotateY(0deg) translateZ(1px); z-index: 3;">
                    <div class="page-content">
                        <h2 class="page-title">Together, We Rise</h2>
                        <p class="page-text">"We are many. They are few. But only together, can we rise."</p>
                        <div class="visual unity-wave" id="unity-wave"></div>
                    </div>
                </div>
                
                <!-- Page 19 -->
                <div class="page" id="page19" style="transform: rotateY(0deg) translateZ(1px); z-index: 2;">
                    <div class="page-content">
                        <h2 class="page-title">The Dream</h2>
                        <p class="page-text">"For justice. For humanity. For a brighter world."</p>
                        <div class="visual" style="background: linear-gradient(45deg, #ff8f00, #ffb300); display: flex; justify-content: center; align-items: center;">
                            <i class="fas fa-sun" style="font-size: 100px; color: white;"></i>
                        </div>
                    </div>
                </div>
                
                <!-- Page 20 -->
                <div class="page" id="page20" style="transform: rotateY(0deg) translateZ(1px); z-index: 1;">
                    <div class="page-content">
                        <h2 class="page-title">Call to Action</h2>
                        <p class="page-text">"Join the movement. Share the message. Stand for humanity."</p>
                        <div class="visual" style="background: linear-gradient(45deg, #d32f2f, #f44336); display: flex; justify-content: center; align-items: center; flex-direction: column; gap: 20px;">
                            <div style="font-size: 1.8rem; font-weight: bold;">#ModernCommunismNow</div>
                            <div style="font-size: 1.8rem; font-weight: bold;">#PeopleOverProfit</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="navigation">
            <button class="nav-btn" id="prevBtn" disabled>
                <i class="fas fa-arrow-left"></i> Previous
            </button>
            <button class="nav-btn" id="nextBtn">
                Next <i class="fas fa-arrow-right"></i>
            </button>
        </div>
        
        <div class="page-counter">
            Page <span id="currentPage">1</span> of 20
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const flipbook = document.getElementById('flipbook');
            const prevBtn = document.getElementById('prevBtn');
            const nextBtn = document.getElementById('nextBtn');
            const currentPageEl = document.getElementById('currentPage');
            let currentPage = 1;
            const totalPages = 20;
            
            // Create visual elements for pages
            createBuildings();
            createWorkers();
            createProtestCrowd();
            createGlobalCrowd();
            createUnityWave();
            
            // Navigation
            nextBtn.addEventListener('click', goToNextPage);
            prevBtn.addEventListener('click', goToPrevPage);
            
            function goToNextPage() {
                if (currentPage < totalPages) {
                    // Hide current page
                    document.getElementById(`page${currentPage}`).classList.remove('animate-in');
                    
                    currentPage++;
                    updateNavigation();
                    
                    // Show new page with animation
                    setTimeout(() => {
                        document.getElementById(`page${currentPage}`).classList.add('animate-in');
                    }, 100);
                }
            }
            
            function goToPrevPage() {
                if (currentPage > 1) {
                    document.getElementById(`page${currentPage}`).classList.remove('animate-in');
                    
                    currentPage--;
                    updateNavigation();
                    
                    setTimeout(() => {
                        document.getElementById(`page${currentPage}`).classList.add('animate-in');
                    }, 100);
                }
            }
            
            function updateNavigation() {
                currentPageEl.textContent = currentPage;
                prevBtn.disabled = currentPage === 1;
                nextBtn.disabled = currentPage === totalPages;
            }
            
            // Create visual elements
            function createBuildings() {
                const luxurySide = document.getElementById('luxury-side');
                const slumsSide = document.getElementById('slums-side');
                
                // Create luxury buildings
                for (let i = 0; i < 8; i++) {
                    const building = document.createElement('div');
                    building.classList.add('building');
                    building.style.left = `${i * 40 + 20}px`;
                    building.style.height = `${Math.random() * 150 + 80}px`;
                    luxurySide.appendChild(building);
                }
                
                // Create slum buildings
                for (let i = 0; i < 12; i++) {
                    const building = document.createElement('div');
                    building.classList.add('building');
                    building.style.left = `${i * 30 + 10}px`;
                    building.style.height = `${Math.random() * 80 + 40}px`;
                    building.style.background = 'linear-gradient(to top, #e74c3c, #c0392b)';
                    slumsSide.appendChild(building);
                }
            }
            
            function createWorkers() {
                const slumsSide = document.getElementById('slums-side');
                
                // Create workers
                for (let i = 0; i < 6; i++) {
                    const worker = document.createElement('div');
                    worker.classList.add('worker');
                    worker.style.left = `${Math.random() * 300}px`;
                    slumsSide.appendChild(worker);
                }
            }
            
            function createProtestCrowd() {
                const crowd = document.getElementById('protest-crowd');
                
                // Create people
                for (let i = 0; i < 20; i++) {
                    const person = document.createElement('div');
                    person.classList.add('person');
                    person.style.left = `${i * 40 + 20}px`;
                    crowd.appendChild(person);
                    
                    // Add banners to some people
                    if (i % 4 === 0) {
                        const banner = document.createElement('div');
                        banner.classList.add('banner');
                        banner.style.left = `${i * 40 + 10}px`;
                        crowd.appendChild(banner);
                    }
                }
                
                // Add doves
                for (let i = 0; i < 5; i++) {
                    const dove = document.createElement('div');
                    dove.classList.add('dove');
                    dove.innerHTML = '🕊️';
                    dove.style.top = `${Math.random() * 100}px`;
                    dove.style.animationDelay = `${i * 2}s`;
                    crowd.appendChild(dove);
                }
            }
            
            function createGlobalCrowd() {
                const crowd = document.getElementById('global-crowd');
                
                // Create people with different colors
                for (let i = 0; i < 25; i++) {
                    const person = document.createElement('div');
                    person.classList.add('person');
                    person.style.left = `${i * 35 + 10}px`;
                    
                    // Different skin tones
                    const skinTones = ['#78909c', '#5d4037', '#ffccbc', '#d7ccc8', '#bcaaa4'];
                    person.style.background = skinTones[i % skinTones.length];
                    
                    crowd.appendChild(person);
                    
                    // Add banners to some people
                    if (i % 3 === 0) {
                        const banner = document.createElement('div');
                        banner.classList.add('banner');
                        banner.style.left = `${i * 35}px`;
                        banner.style.background = i % 2 === 0 ? '#e74c3c' : '#1a237e';
                        crowd.appendChild(banner);
                    }
                }
            }
            
            function createUnityWave() {
                const wave = document.getElementById('unity-wave');
                
                // Create people with different colors in a wave pattern
                const skinTones = ['#78909c', '#5d4037', '#ffccbc', '#d7ccc8', '#bcaaa4'];
                
                for (let i = 0; i < 20; i++) {
                    const person = document.createElement('div');
                    person.classList.add('wave-person');
                    person.style.left = `${i * 40 + 20}px`;
                    person.style.background = skinTones[i % skinTones.length];
                    person.style.animationDelay = `${i * 0.1}s`;
                    wave.appendChild(person);
                }
            }
            
            // Initialize animations for the first page
            document.getElementById('page1').classList.add('animate-in');
        });
    </script>
</body>
</html>
