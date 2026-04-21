<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <title>太空射擊：學號挑戰</title>
    <style>
        body { text-align: center; background: #0b0d17; color: #00d4ff; font-family: 'Segoe UI', sans-serif; margin: 0; overflow: hidden; }
        #ui { position: absolute; top: 10px; width: 100%; pointer-events: none; z-index: 10; }
        canvas { background: radial-gradient(circle, #1b2735 0%, #090a0f 100%); display: block; margin: 0 auto; }
        .logo { margin-top: 10px; border-radius: 10px; border: 2px solid #00d4ff; box-shadow: 0 0 15px #00d4ff; }
    </style>
</head>
<body>
    <div id="ui">
        <!-- 這裡已更新為你的檔案名稱 shotgame.webp -->
        <img src="shotgame.webp" alt="Logo" class="logo" width="100">
        <h1>太空射擊挑戰</h1>
        <p>分數: <span id="score">0</span></p>
    </div>
    <canvas id="gameCanvas"></canvas>

    <script>
        const canvas = document.getElementById('gameCanvas');
        const ctx = canvas.getContext('2d');
        canvas.width = 600; canvas.height = 750;

        let score = 0;
        let player = { x: 280, y: 650, size: 40, speed: 6 };
        let bullets = [];
        let enemies = [];
        let keys = {};

        // 載入你的 Logo 作為玩家戰機圖示
        const playerImg = new Image();
        playerImg.src = 'shotgame.webp';

        window.addEventListener('keydown', e => keys[e.code] = true);
        window.addEventListener('keyup', e => keys[e.code] = false);

        function spawnEnemy() {
            enemies.push({ x: Math.random() * (canvas.width - 30), y: -30, size: 30, speed: 2 + Math.random() * 2 });
        }
        setInterval(spawnEnemy, 1000);

        function update() {
            if (keys['ArrowLeft'] && player.x > 0) player.x -= player.speed;
            if (keys['ArrowRight'] && player.x < canvas.width - player.size) player.x += player.speed;
            if (keys['Space']) {
                if (bullets.length === 0 || bullets[bullets.length - 1].y < player.y - 30) {
                    bullets.push({ x: player.x + player.size / 2 - 2, y: player.y, w: 4, h: 12 });
                }
            }

            bullets.forEach((b, bi) => {
                b.y -= 8;
                if (b.y < 0) bullets.splice(bi, 1);
            });

            enemies.forEach((en, ei) => {
                en.y += en.speed;
                if (en.x < player.x + player.size && en.x + en.size > player.x && en.y < player.y + player.size && en.y + en.size > player.y) {
                    alert("遊戲結束！最終得分: " + score);
                    document.location.reload();
                }
                bullets.forEach((b, bi) => {
                    if (b.x < en.x + en.size && b.x + b.w > en.x && b.y < en.y + en.size && b.y + b.h > en.y) {
                        enemies.splice(ei, 1);
                        bullets.splice(bi, 1);
                        score += 10;
                        document.getElementById('score').innerText = score;
                    }
                });
                if (en.y > canvas.height) enemies.splice(ei, 1);
            });
        }

        function draw() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 繪製玩家戰機 (使用你的 Logo)
            ctx.drawImage(playerImg, player.x, player.y, player.size, player.size);
            
            // 繪製子彈
            ctx.fillStyle = '#fff700';
            bullets.forEach(b => ctx.fillRect(b.x, b.y, b.w, b.h));
            
            // 繪製敵人
            ctx.fillStyle = '#ff4d4d';
            enemies.forEach(en => ctx.fillRect(en.x, en.y, en.size, en.size));
        }

        function loop() { update(); draw(); requestAnimationFrame(loop); }
        loop();
    </script>
</body>
</html>
