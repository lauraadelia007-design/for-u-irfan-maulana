<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Untuk Kamu Sayang... ❤️</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f093fb 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow-x: hidden;
            position: relative;
            padding: 20px;
        }

        /* Animated Background */
        .bg-particle {
            position: fixed;
            pointer-events: none;
            animation: float-particle 8s infinite ease-in-out;
        }

        @keyframes float-particle {
            0%, 100% {
                transform: translateY(0) translateX(0) rotate(0deg);
                opacity: 0.3;
            }
            50% {
                transform: translateY(-50px) translateX(20px) rotate(180deg);
                opacity: 0.8;
            }
        }

        .container {
            background: rgba(255, 255, 255, 0.98);
            border-radius: 30px;
            padding: 50px 40px;
            max-width: 700px;
            width: 100%;
            box-shadow: 0 30px 80px rgba(0, 0, 0, 0.3);
            animation: fadeInScale 1s ease-out;
            position: relative;
            z-index: 10;
        }

        @keyframes fadeInScale {
            from {
                opacity: 0;
                transform: scale(0.8) translateY(50px);
            }
            to {
                opacity: 1;
                transform: scale(1) translateY(0);
            }
        }

        .page {
            display: none;
            animation: slideIn 0.6s ease-out;
        }

        .page.active {
            display: block;
        }

        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateX(50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        .emoji-header {
            font-size: 100px;
            text-align: center;
            margin-bottom: 20px;
            animation: bounce 2s infinite;
        }

        @keyframes bounce {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-20px);
            }
        }

        h1 {
            color: #e91e63;
            font-size: 2.5em;
            text-align: center;
            margin-bottom: 30px;
            text-shadow: 0 2px 10px rgba(233, 30, 99, 0.3);
        }

        .message-card {
            background: linear-gradient(135deg, #fff5f8 0%, #ffe6f0 100%);
            padding: 30px;
            border-radius: 20px;
            margin: 25px 0;
            border-left: 5px solid #e91e63;
            box-shadow: 0 5px 20px rgba(233, 30, 99, 0.15);
        }

        .message-text {
            font-size: 1.2em;
            line-height: 1.9;
            color: #333;
            text-align: center;
        }

        .highlight {
            color: #e91e63;
            font-weight: bold;
            font-size: 1.15em;
        }

        .rules-box {
            background: #fff9e6;
            border: 3px solid #ffcc00;
            border-radius: 20px;
            padding: 25px;
            margin: 30px 0;
        }

        .rules-title {
            font-size: 1.5em;
            color: #ff6b00;
            font-weight: bold;
            text-align: center;
            margin-bottom: 20px;
        }

        .rule-item {
            background: white;
            padding: 15px 20px;
            margin: 15px 0;
            border-radius: 15px;
            font-size: 1.1em;
            color: #444;
            display: flex;
            align-items: center;
            gap: 15px;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.1);
        }

        .rule-icon {
            font-size: 1.8em;
            min-width: 40px;
        }

        .date-box {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 30px;
            border-radius: 20px;
            text-align: center;
            margin: 30px 0;
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.4);
        }

        .date-big {
            font-size: 2.2em;
            font-weight: bold;
            margin: 15px 0;
        }

        .countdown {
            font-size: 1.3em;
            margin-top: 15px;
            background: rgba(255, 255, 255, 0.2);
            padding: 15px;
            border-radius: 10px;
        }

        .btn {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            color: white;
            border: none;
            padding: 18px 50px;
            font-size: 1.3em;
            font-weight: bold;
            border-radius: 50px;
            cursor: pointer;
            display: block;
            margin: 30px auto;
            box-shadow: 0 8px 25px rgba(245, 87, 108, 0.4);
            transition: all 0.3s;
        }

        .btn:hover {
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 12px 35px rgba(245, 87, 108, 0.5);
        }

        .btn:active {
            transform: translateY(0) scale(1);
        }

        .promise-card {
            background: linear-gradient(135deg, #e8f5e9 0%, #c8e6c9 100%);
            padding: 25px;
            border-radius: 20px;
            margin: 25px 0;
            border-left: 5px solid #4CAF50;
            text-align: center;
        }

        .promise-text {
            font-size: 1.3em;
            color: #2e7d32;
            font-weight: bold;
            line-height: 1.8;
        }

        /* Celebration Effects */
        .heart-float {
            position: fixed;
            font-size: 40px;
            animation: floatUp 4s ease-out forwards;
            pointer-events: none;
            z-index: 1000;
        }

        @keyframes floatUp {
            0% {
                opacity: 1;
                transform: translateY(0) scale(0) rotate(0deg);
            }
            50% {
                opacity: 1;
                transform: translateY(-200px) scale(1.5) rotate(180deg);
            }
            100% {
                opacity: 0;
                transform: translateY(-400px) scale(0.5) rotate(360deg);
            }
        }

        .sparkle {
            position: fixed;
            width: 8px;
            height: 8px;
            background: white;
            border-radius: 50%;
            animation: sparkleAnim 2s ease-out forwards;
            pointer-events: none;
            box-shadow: 0 0 10px white;
        }

        @keyframes sparkleAnim {
            0% {
                opacity: 1;
                transform: scale(0);
            }
            50% {
                opacity: 1;
                transform: scale(2);
            }
            100% {
                opacity: 0;
                transform: scale(0);
            }
        }

        .final-message {
            text-align: center;
            font-size: 1.4em;
            color: #e91e63;
            margin: 30px 0;
            font-weight: bold;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0%, 100% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.05);
            }
        }

        @media (max-width: 600px) {
            .container {
                padding: 30px 20px;
            }
            h1 {
                font-size: 1.8em;
            }
            .message-text {
                font-size: 1.05em;
            }
            .rule-item {
                font-size: 1em;
            }
            .date-big {
                font-size: 1.7em;
            }
        }
    </style>
</head>
<body>
    <!-- Background Particles -->
    <script>
        for (let i = 0; i < 20; i++) {
            const particle = document.createElement('div');
            particle.className = 'bg-particle';
            particle.textContent = ['❤️', '💕', '💖', '✨', '⭐'][Math.floor(Math.random() * 5)];
            particle.style.left = Math.random() * 100 + '%';
            particle.style.top = Math.random() * 100 + '%';
            particle.style.fontSize = (Math.random() * 25 + 20) + 'px';
            particle.style.animationDelay = Math.random() * 5 + 's';
            particle.style.animationDuration = (Math.random() * 4 + 6) + 's';
            document.body.appendChild(particle);
        }
    </script>

    <div class="container">
        <!-- Page 1: Opening -->
        <div class="page active" id="page1">
            <div class="emoji-header">💑</div>
            <h1>Hai Sayang... 💕</h1>
            <div class="message-card">
                <div class="message-text">
                    Aku mau bilang sesuatu yang penting banget...<br><br>
                    Ada beberapa hal yang pengen aku sampaikan ke kamu.<br><br>
                    <span class="highlight">Boleh minta waktu kamu sebentar? aku tau kok kamu lagi pusing,tapi bentar aja yaa 🥺</span>
                </div>
            </div>
            <button class="btn" onclick="nextPage(2)">Oke Sayang 💖</button>
        </div>

        <!-- Page 2: Promise from You -->
        <div class="page" id="page2">
            <div class="emoji-header">🥰</div>
            <h1>Aku Janji Ya... 💕</h1>
            <div class="promise-card">
                <div class="promise-text">
                    Aku janji sama kamu...<br><br>
                    ✨ Aku <span style="color: #e91e63;">SAYANG BANGET</span> sama kamu<br><br>
                    ✨ Aku <span style="color: #e91e63;">GAK AKAN BAPER</span> sama cowok lain<br><br>
                    ✨ Kamu <span style="color: #e91e63;">SATU-SATUNYA</span> yang ada di hati aku<br><br>
                    💖 <strong>AKU CUMA MAU KAMU AJA!</strong> 💖
                </div>
            </div>
            <div class="message-card">
                <div class="message-text">
                    Aku serius banget sayang...<br>
                    Hati aku cuma buat kamu doang! ❤️
                </div>
            </div>
            <button class="btn" onclick="nextPage(3)">Lanjut Sayang 💕</button>
        </div>

        <!-- Page 3: Rules -->
        <div class="page" id="page3">
            <div class="emoji-header">⚠️</div>
            <h1>Tapi Ada Syaratnya... 🙏</h1>
            <div class="message-card">
                <div class="message-text">
                    Aku udah janji sama kamu kan...<br>
                    Sekarang giliran kamu yang harus <span class="highlight">JANJI</span> sama aku! 💕
                </div>
            </div>
            <div class="rules-box">
                <div class="rules-title">🚫 JANGAN DILANGGAR YA! 🚫</div>
                <div class="rule-item">
                    <div class="rule-icon">🍺❌</div>
                    <div><strong>JANGAN MINUM MIRAS!</strong><br>Aku serius banget soal ini sayang!</div>
                </div>
                <div class="rule-item">
                    <div class="rule-icon">💔❌</div>
                    <div><strong>JANGAN MAIN BELAKANG!</strong><br>Jangan nyari kenyamanan sama cewe lain!</div>
                </div>
                <div class="rule-item">
                    <div class="rule-icon">👭❌</div>
                    <div><strong>JANGAN DEKET-DEKET SAMA CEWE LAIN!</strong><br>Aku cemburu tau! 😤</div>
                </div>
            </div>
            <div class="message-card">
                <div class="message-text">
                    Kalau kamu langgar...<br>
                    <span class="highlight" style="font-size: 1.3em;">AKU BAKAL SEDIH BANGET! 😢💔</span>
                </div>
            </div>
            <button class="btn" onclick="nextPage(4)">Aku Janji! 💖</button>
        </div>

        <!-- Page 4: Date -->
        <div class="page" id="page4">
            <div class="emoji-header">📅</div>
            <h1>Aku tau kok kamu masi banyak masalah, kamu yang kuat ya sayangku.
                Tunggu Aku Ya... 🥺</h1>
            <div class="date-box">
                <div style="font-size: 1.5em;">Aku Akan ke Balam</div>
                <div class="date-big">📅 25 Januari 2025 ✨</div>
                <div class="countdown" id="countdown">⏰ Menghitung hari...</div>
            </div>
            <div class="message-card">
                <div class="message-text">
                    Sampai tanggal 25, kamu harus:<br><br>
                    ✅ Inget janji kamu<br>
                    ✅ Jaga diri baik-baik<br>
                    ✅ Jangan langgar aturan yang aku kasih<br>
                    ✅ Tetep sayang sama aku<br><br>
                    <span class="highlight">Bisa kan sayang? 🥺❤️</span>
                </div>
            </div>
            <button class="btn" onclick="nextPage(5)">Iya Bisa! 💕</button>
        </div>

        <!-- Page 5: Final -->
        <div class="page" id="page5">
            <div class="emoji-header">😍</div>
            <h1>Makasih Sayang! 💖</h1>
            <div class="promise-card" style="background: linear-gradient(135deg, #fce4ec 0%, #f8bbd0 100%); border-left-color: #e91e63;">
                <div class="promise-text" style="color: #c2185b;">
                    INGAT YA! 💕<br><br>
                    ✨ Aku sayang banget sama kamu<br>
                    ✨ kamu harus kuat ya sayang, aku ada buat kamu kok<br>
                    ✨ Kamu harus jaga janji kamu juga!<br><br>
                    <span style="font-size: 1.3em;">📅 Sampai ketemu tanggal 25! 🎉</span>
                </div>
            </div>
            <div class="final-message">
                💖 I LOVE YOU SO MUCH! 💖<br>
                <span style="font-size: 2em;">👩‍❤️‍👨</span><br>
                Forever & Always! ✨
            </div>
        </div>
    </div>

    <script>
        let currentPage = 1;

        function nextPage(pageNum) {
            // Hide current page
            document.getElementById('page' + currentPage).classList.remove('active');
            
            // Show next page
            setTimeout(() => {
                document.getElementById('page' + pageNum).classList.add('active');
                currentPage = pageNum;
                
                // Add celebration effects
                createCelebration();
                
                // Update countdown if on page 4
                if (pageNum === 4) {
                    updateCountdown();
                    setInterval(updateCountdown, 60000);
                }
                
                // Final celebration on page 5
                if (pageNum === 5) {
                    finalCelebration();
                }
            }, 300);
        }

        function createCelebration() {
            for (let i = 0; i < 15; i++) {
                setTimeout(() => {
                    createHeart();
                    createSparkle();
                }, i * 100);
            }
        }

        function finalCelebration() {
            for (let i = 0; i < 30; i++) {
                setTimeout(() => {
                    createHeart();
                    createSparkle();
                }, i * 80);
            }
        }

        function createHeart() {
            const heart = document.createElement('div');
            heart.className = 'heart-float';
            heart.textContent = ['❤️', '💕', '💖', '💗', '💝', '💓'][Math.floor(Math.random() * 6)];
            heart.style.left = Math.random() * 100 + '%';
            heart.style.bottom = '0';
            document.body.appendChild(heart);
            
            setTimeout(() => heart.remove(), 4000);
        }

        function createSparkle() {
            const sparkle = document.createElement('div');
            sparkle.className = 'sparkle';
            sparkle.style.left = Math.random() * 100 + '%';
            sparkle.style.top = Math.random() * 100 + '%';
            const colors = ['#fff', '#ffd700', '#ff69b4', '#87ceeb'];
            sparkle.style.background = colors[Math.floor(Math.random() * colors.length)];
            document.body.appendChild(sparkle);
            
            setTimeout(() => sparkle.remove(), 2000);
        }

        function updateCountdown() {
            const now = new Date();
            const target = new Date('2025-01-25T00:00:00');
            const diff = target - now;

            if (diff > 0) {
                const days = Math.floor(diff / (1000 * 60 * 60 * 24));
                const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
                const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
                
                document.getElementById('countdown').textContent = 
                    `⏰ Tinggal ${days} hari, ${hours} jam, ${minutes} menit lagi!`;
            } else {
                document.getElementById('countdown').textContent = '🎉 HARI INI! 🎉';
            }
        }

        // Add continuous background particles
        setInterval(() => {
            const particle = document.createElement('div');
            particle.className = 'bg-particle';
            particle.textContent = ['❤️', '💕', '✨'][Math.floor(Math.random() * 3)];
            particle.style.left = Math.random() * 100 + '%';
            particle.style.top = '100%';
            particle.style.fontSize = (Math.random() * 20 + 15) + 'px';
            document.body.appendChild(particle);
            
            setTimeout(() => particle.remove(), 8000);
        }, 3000);
    </script>
</body>
</html>
