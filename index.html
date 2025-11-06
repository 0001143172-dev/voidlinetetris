<!doctype html>
<html lang="pt-BR">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Voidline Tetris Game</title>
  <script src="/_sdk/element_sdk.js"></script>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/tone/14.8.52/Tone.js"></script>
  <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'void-blue': '#00F0FF',
                        'void-dark': '#0A0A1F',
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    }
                }
            }
        }
    </script>
  <style>
        body {
            box-sizing: border-box;
            background-color: #000;
            margin: 0;
            padding: 0;
            height: 100%;
        }
        html {
            height: 100%;
        }
        #fundo {        /* cor  da  borda*/
            border: 2px solid #00F0FF;
            box-shadow: 0 0 20px rgba(0, 240, 255, 0.5);
            background-color: #1a1a2e;
            padding: 1rem;
            display: flex;
            gap: 1rem;
            font-family: 'Inter', sans-serif;
            border-radius: 8px;
        }
        #t {                            /*tamanho da fonte*/
            font-size: 2.5rem;
            color: #00F0FF;
            text-shadow: 0 0 10px #00F0FF;
            margin-bottom: 1rem;
            font-weight: 800;
            text-align: center;
        }
        .coluna1 h3, .coluna3 h3 {      /*cor da fonte*/
            color: #00F0FF;
            font-weight: 700;
            margin-top: 0.5rem;
            font-size: 1.25rem;
        }
        .coluna1 p, .caixa-texto {     /*cor de fundo*   e caixa de texto */
            background-color: #0A0A1F;
            border: 1px solid #00F0FF;
            color: #00FF99;
            padding: 0.5rem;
            margin-bottom: 1rem;
            font-family: monospace;
            min-height: 2.5rem;
            font-size: 1.5rem;
            text-align: right;c
            border-radius: 4px;
            overflow: hidden;
        }
        #in01 {      /*  cor de fundo */
            background-color: #0A0A1F;
            border: 1px solid #00F0FF;
            color: #00FF99;
            padding: 0.25rem;
            width: 100%;
            margin-bottom: 0.5rem;
            border-radius: 4px;
        }
        button {   /* cor  botão */
            background-color: #00F0FF;
            color: #1a1a2e;
            padding: 0.5rem 1rem;
            border: none;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.2s;
            border-radius: 4px;
        }
        button:hover {   /*cor de fundo */
            background-color: #00CCFF;
            box-shadow: 0 0 8px #00F0FF;
        }
        .main-canvas {
            border: 2px solid #00F0FF;
            background-color: #0A0A1F;
            box-shadow: 0 0 15px rgba(0, 240, 255, 0.7);
        }
        .next-canvas {
            border: 1px solid #00F0FF;
            background-color: #0A0A1F;
        }
        #loreDisplay {
            max-height: 200px;
            overflow-y: auto;
            font-size: 0.875rem;
            line-height: 1.4;
        }
    </style>     /*estilo   */
  <style>@view-transition { navigation: auto; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
 
 </head>
 <body class="flex flex-col items-center justify-center min-h-full"><!-- Tela do Menu -->
 <div class="coluna1 w-40 flex flex-col">
     <h3>NÍVEL</h3>
     <p id="levelDisplay" class="text-right">0</p>
     <h3>LINHAS</h3>
     <p id="linesDisplay" class="text-right">0</p>
     <h3 id="scoreLabel">PONTUAÇÃO</h3>
     <p id="scoreDisplay" class="score text-right">000000</p>
          <h3>RECORDE</h3>
     <p id="highScoreDisplay" class="caixa-texto text-right text-xl">000000</p>
          <input type="text" id="in01" placeholder="Comando (ex: 'restart')">
     ...
    </div>
  <div id="menuScreen" class="flex flex-col items-center justify-center min-h-full">       /*botão de menu*/
   <h1 id="menuTitle" class="text-6xl font-bold text-void-blue mb-4 text-center" style="text-shadow: 0 0 20px #00F0FF;">VOIDLINE TETRIS</h1>
   <div class="text-center mb-8">
    <p class="text-void-blue text-xl font-semibold" style="text-shadow: 0 0 10px #00F0FF;">Desenvolvido por</p>
    <p class="text-white text-2xl font-bold mt-2" style="text-shadow: 0 0 15px #00F0FF;">Luciana Logarezzi V s</p>
   </div>
   <div class="flex flex-col gap-4 items-center"><button id="startButton" onclick="startGame()" class="bg-void-blue text-void-dark px-8 py-4 text-xl font-bold rounded hover:bg-cyan-300 transition-all duration-200" style="box-shadow: 0 0 15px rgba(0, 240, 255, 0.5);">INICIAR JOGO</button> <button id="controlsButton" onclick="showControls()" class="bg-void-blue text-void-dark px-8 py-4 text-xl font-bold rounded hover:bg-cyan-300 transition-all duration-200" style="box-shadow: 0 0 15px rgba(0, 240, 255, 0.5);">CONTROLES</button> <button id="creditsButton" onclick="showCredits()" class="bg-void-blue text-void-dark px-8 py-4 text-xl font-bold rounded hover:bg-cyan-300 transition-all duration-200" style="box-shadow: 0 0 15px rgba(0, 240, 255, 0.5);">CRÉDITOS</button> <button id="menuMusicButton" onclick="toggleMusic()" class="bg-purple-600 text-white px-6 py-3 text-lg font-bold rounded hover:bg-purple-500 transition-all duration-200 mt-4">🎵 Música OFF</button>
   </div>
  </div><!-- Tela de Controles -->
  <div id="controlsScreen" class="hidden flex-col items-center justify-center min-h-full">
   <div class="bg-void-dark border-2 border-void-blue rounded-lg p-8 max-w-md" style="box-shadow: 0 0 20px rgba(0, 240, 255, 0.3);">
    <h2 class="text-3xl font-bold text-void-blue mb-6 text-center">CONTROLES</h2>
    <div class="text-void-blue space-y-3">
     <div class="flex justify-between"><span>Mover Esquerda:</span> <span class="text-white">← Seta Esquerda</span>
     </div>
     <div class="flex justify-between"><span>Mover Direita:</span> <span class="text-white">→ Seta Direita</span>
     </div>
     <div class="flex justify-between"><span>Girar Peça:</span> <span class="text-white">↑ Seta Cima</span>
     </div>
     <div class="flex justify-between"><span>Descer Rápido:</span> <span class="text-white">↓ Seta Baixo</span>
     </div>
     <div class="flex justify-between"><span>Queda Instantânea:</span> <span class="text-white">Espaço</span>
     </div>
     <div class="flex justify-between"><span>Pausar:</span> <span class="text-white">Botão PAUSAR</span>
     </div>
    </div><button id="controlsMusicButton" onclick="toggleMusic()" class="bg-purple-600 text-white px-6 py-3 font-bold rounded mt-4 w-full hover:bg-purple-500 transition-all duration-200">🎵 Música OFF</button> <button id="backFromControls" onclick="showMenu()" class="bg-void-blue text-void-dark px-6 py-3 font-bold rounded mt-2 w-full hover:bg-cyan-300 transition-all duration-200">VOLTAR</button>
   </div>
  </div><!-- Tela de Créditos -->
  <div id="creditsScreen" class="hidden flex-col items-center justify-center min-h-full">
   <div class="bg-void-dark border-2 border-void-blue rounded-lg p-8 max-w-md" style="box-shadow: 0 0 20px rgba(0, 240, 255, 0.3);">
    <h2 class="text-3xl font-bold text-void-blue mb-6 text-center">CRÉDITOS</h2>
    <div class="text-void-blue space-y-4 text-center">
     <div>
      <h3 class="text-xl font-bold text-white mb-2">Voidline Tetris</h3>
      <p>Uma experiência cósmica de Tetris</p>
     </div>
     <div>
      <h4 class="font-bold text-white">Desenvolvido por:</h4>
      <p>Canva Code AI</p>
     </div>
     <div>
      <h4 class="font-bold text-white">Música:</h4>     /       *musica*/
      <p>Sintetizada com Web Audio API</p>
     </div>
     <div>
      <h4 class="font-bold text-white">Inspirado em:</h4>
      <p>O vazio cósmico e as formas geométricas perfeitas</p>
     </div>
    </div><button id="creditsMusicButton" onclick="toggleMusic()" class="bg-purple-600 text-white px-6 py-3 font-bold rounded mt-4 w-full hover:bg-purple-500 transition-all duration-200">🎵 Música OFF</button> <button id="backFromCredits" onclick="showMenu()" class="bg-void-blue text-void-dark px-6 py-3 font-bold rounded mt-2 w-full hover:bg-cyan-300 transition-all duration-200">VOLTAR</button>
   </div>
  </div><!-- Tela do Jogo -->
  <div id="gameScreen" class="hidden">
   <h1 id="t">Voidline</h1>
   <div id="fundo" class="container">
    <div class="coluna1 w-40 flex flex-col">
     <h3 id="levelLabel">NÍVEL</h3>
     <p id="levelDisplay" class="text-right">0</p>
     <h3 id="linesLabel">LINHAS</h3>
     <p id="linesDisplay" class="text-right">0</p>
     <h3 id="scoreLabel">PONTUAÇÃO</h3>
     <p id="scoreDisplay" class="score text-right">000000</p><input type="text" id="in01" placeholder="Comando (ex: 'restart')">
     <div class="flex flex-col gap-1"><button onclick="sendCommand()">ENVIAR</button> <button onclick="generateLore()">✨ GERAR LORE</button> <button id="pauseButton" onclick="togglePause()">⏸️ PAUSAR</button> <button id="musicButton" onclick="toggleMusic()">🎵 Música OFF</button> <button onclick="showMenu()" class="bg-red-600 hover:bg-red-500">🏠 MENU</button>
     </div>
    </div>
    <div class="coluna2">    /*coluna 2 game canvas    */
     <canvas id="gameCanvas" class="main-canvas" width="300" height="600"></canvas>
    </div>
    <div class="coluna3 w-48 flex flex-col">
     <h3>PRÓXIMA PEÇA</h3>
     <canvas id="nextCanvas" class="next-canvas mb-4" width="120" height="120"></canvas>
     <h3>LORE DA PEÇA</h3>
     <div id="loreDisplay" class="caixa-texto text-left">
      Pressione "GERAR LORE" para criar uma história sobre a peça atual!
      <h3>LORE DA PEÇA</h3>
      </div>
    </div>
   </div>
  </div>
  <script>    /*botões*/
        const defaultConfig = {
            game_title: "Voidline",
            level_label: "NÍVEL",
            lines_label: "LINHAS",
            score_label: "PONTUAÇÃO",
            menu_title: "VOIDLINE TETRIS",
            start_button: "INICIAR JOGO",
            controls_button: "CONTROLES",
            credits_button: "CRÉDITOS",
            back_button: "VOLTAR",
            primary_color: "#00F0FF",
            background_color: "#000000",
            surface_color: "#1a1a2e",
            text_color: "#00FF99",
            secondary_color: "#0A0A1F"
        };

        const canvas = document.getElementById('gameCanvas');
        const ctx = canvas.getContext('2d');
        const nextCanvas = document.getElementById('nextCanvas');
        const nextCtx = nextCanvas.getContext('2d');

        const COLS = 10;
        const ROWS = 20;
        const BLOCK_SIZE = 30;

        let board = Array(ROWS).fill().map(() => Array(COLS).fill(0));
        let score = 0;
        let lines = 0;
        let level = 0;
        let gameOver = false;
        let isPaused = false;
        let currentPiece = null;
        let nextPiece = null;
        let dropCounter = 0;
        let dropInterval = 1000;
        let lastTime = 0;

        const PIECES = {    /*  peças tetris*/
            'I': [[1,1,1,1]],
            'O': [[1,1],[1,1]],
            'T': [[0,1,0],[1,1,1]],
            'S': [[0,1,1],[1,1,0]],
            'Z': [[1,1,0],[0,1,1]],
            'J': [[1,0,0],[1,1,1]],
            'L': [[0,0,1],[1,1,1]]
        };

        const COLORS = {   /* cores da peça*/
            'I': '#00F0FF',
            'O': '#FFD700',
            'T': '#9D00FF',
            'S': '#00FF00',
            'Z': '#FF0000',
            'J': '#0000FF',
            'L': '#FF8C00'
        };

        const PIECE_NAMES = {  /* nome da  peça */
            'I': 'Linha',
            'O': 'Quadrado',
            'T': 'T',
            'S': 'S',
            'Z': 'Z',
            'J': 'J',
            'L': 'L'
        };

        let currentScreen = 'menu';
        let musicPlaying = false;

        // Sistema de navegação entre telas
        function showScreen(screenName) {
            const screens = ['menuScreen', 'controlsScreen', 'creditsScreen', 'gameScreen'];
            screens.forEach(screen => {
                const element = document.getElementById(screen);
                if (screen === screenName + 'Screen') {
                    element.classList.remove('hidden');
                    element.classList.add('flex');
                } else {
                    element.classList.add('hidden');
                    element.classList.remove('flex');
                }
            });
            currentScreen = screenName;
        }

        function showMenu() {      /* função do menu*/
            showScreen('menu');
            if (gameOver || isPaused) {
                gameOver = false;
                isPaused = false;
                // Reset pause button
                const pauseButton = document.getElementById('pauseButton');
                pauseButton.textContent = '⏸️ PAUSAR';
                pauseButton.classList.remove('bg-green-600', 'hover:bg-green-500');
                pauseButton.classList.add('bg-void-blue', 'hover:bg-cyan-300');
            }
        }

        function showControls() {
            showScreen('controls');
        }

        function showCredits() {
            showScreen('credits');
        }

        function startGame() {
            showScreen('game');
            restartGame();
        }

        // Sistema de música simplificado com Web Audio API
        let audioContext = null;
        let musicInterval = null;
        let currentNote = 0;

        // Melodia do Tetris em frequências (Hz)
        const tetrisMelody = [
            659.25, 493.88, 523.25, 587.33, 523.25, 493.88, 440.00, 440.00,
            523.25, 659.25, 587.33, 523.25, 493.88, 493.88, 523.25, 587.33,
            659.25, 523.25, 440.00, 440.00, 440.00, 493.88, 523.25, 587.33,
            698.46, 880.00, 783.99, 698.46, 659.25, 659.25, 523.25, 659.25,
            587.33, 523.25, 493.88, 493.88, 523.25, 587.33, 659.25, 523.25,
            440.00, 440.00
        ];

        function initAudio() {    /* função de audio */
            try {
                if (!audioContext) {
                    audioContext = new (window.AudioContext || window.webkitAudioContext)();
                    console.log('Contexto de áudio criado');
                }
               
                if (audioContext.state === 'suspended') {
                    audioContext.resume();
                    console.log('Contexto de áudio resumido');
                }
               
                return true;
            } catch (error) {
                console.error('Erro ao inicializar áudio:', error);
                return false;
            }
        }

        function playNote(frequency, duration = 0.3) {
            if (!audioContext) return;
           
            try {
                const oscillator = audioContext.createOscillator();
                const gainNode = audioContext.createGain();
               
                oscillator.connect(gainNode);
                gainNode.connect(audioContext.destination);
               
                oscillator.frequency.setValueAtTime(frequency, audioContext.currentTime);
                oscillator.type = 'square';
               
                gainNode.gain.setValueAtTime(0.1, audioContext.currentTime);
                gainNode.gain.exponentialRampToValueAtTime(0.01, audioContext.currentTime + duration);
               
                oscillator.start(audioContext.currentTime);
                oscillator.stop(audioContext.currentTime + duration);
               
                console.log('Tocando frequência:', frequency);
            } catch (error) {
                console.error('Erro ao tocar nota:', error);
            }
        }

        function updateMusicButtons() {
            const buttons = [
                document.getElementById('menuMusicButton'),
                document.getElementById('musicButton'),
                document.getElementById('controlsMusicButton'),
                document.getElementById('creditsMusicButton')
            ];
           
            const text = musicPlaying ? '🎵 Música ON' : '🎵 Música OFF';
            buttons.forEach(button => {
                if (button) {
                    button.textContent = text;
                }
            });
        }

        function toggleMusic() {
            console.log('Toggle música clicado, estado atual:', musicPlaying);
           
            if (!musicPlaying) {
                console.log('Tentando iniciar música...');
                const initialized = initAudio();
                if (initialized) {
                    startSimpleMusic();
                    musicPlaying = true;
                    updateMusicButtons();
                    console.log('Música iniciada com sucesso!');
                } else {
                    console.log('Falha ao inicializar música');
                }
            } else {
                console.log('Parando música...');
                stopSimpleMusic();
                musicPlaying = false;
                updateMusicButtons();
                console.log('Música parada');
            }
        }

        function startSimpleMusic() {
            try {
                console.log('Iniciando música simples...');
                stopSimpleMusic();
               
                currentNote = 0;
               
                // Tocar uma nota a cada 500ms
                musicInterval = setInterval(() => {
                    if (musicPlaying && audioContext) {
                        const frequency = tetrisMelody[currentNote];
                        playNote(frequency, 0.4);
                        currentNote = (currentNote + 1) % tetrisMelody.length;
                    }
                }, 500);
               
                console.log('Música simples iniciada!');
            } catch (error) {
                console.error('Erro ao iniciar música simples:', error);
            }
        }

        function stopSimpleMusic() {
            try {
                console.log('Parando música simples...');
               
                if (musicInterval) {
                    clearInterval(musicInterval);
                    musicInterval = null;
                }
               
                console.log('Música simples parada');
            } catch (error) {
                console.error('Erro ao parar música simples:', error);
            }
        }

        function togglePause() {
            if (gameOver) return;
           
            isPaused = !isPaused;
            const pauseButton = document.getElementById('pauseButton');
           
            if (isPaused) {
                pauseButton.textContent = '▶️ CONTINUAR';
                pauseButton.classList.add('bg-green-600', 'hover:bg-green-500');
                pauseButton.classList.remove('bg-void-blue', 'hover:bg-cyan-300');
               
                // Mostrar overlay de pause
                ctx.fillStyle = 'rgba(0, 0, 0, 0.75)';
                ctx.fillRect(0, 0, canvas.width, canvas.height);
                ctx.fillStyle = '#00F0FF';
                ctx.font = 'bold 40px Inter';
                ctx.textAlign = 'center';
                ctx.fillText('PAUSADO', canvas.width / 2, canvas.height / 2);
                ctx.font = '16px Inter';
                ctx.fillText('Clique CONTINUAR para retomar', canvas.width / 2, canvas.height / 2 + 40);
            } else {
                pauseButton.textContent = '⏸️ PAUSAR';
                pauseButton.classList.remove('bg-green-600', 'hover:bg-green-500');
                pauseButton.classList.add('bg-void-blue', 'hover:bg-cyan-300');
            }
        }

        function createPiece() {
            const pieces = Object.keys(PIECES);
            const type = pieces[Math.floor(Math.random() * pieces.length)];
            return {
                type: type,
                shape: PIECES[type],
                color: COLORS[type],
                x: Math.floor(COLS / 2) - Math.floor(PIECES[type][0].length / 2),
                y: 0
            };
        }

        function drawBlock(ctx, x, y, color) {    /*função de desenhar*/
            ctx.fillStyle = color;
            ctx.fillRect(x * BLOCK_SIZE, y * BLOCK_SIZE, BLOCK_SIZE, BLOCK_SIZE);
            ctx.strokeStyle = '#000';
            ctx.lineWidth = 2;
            ctx.strokeRect(x * BLOCK_SIZE, y * BLOCK_SIZE, BLOCK_SIZE, BLOCK_SIZE);
        }

        function drawBoard() {     /*desenhar */
            ctx.fillStyle = '#0A0A1F';
            ctx.fillRect(0, 0, canvas.width, canvas.height);

            for (let y = 0; y < ROWS; y++) {
                for (let x = 0; x < COLS; x++) {
                    if (board[y][x]) {
                        drawBlock(ctx, x, y, board[y][x]);
                    }
                }
            }
        }

        function drawPiece(piece, context = ctx, offsetX = 0, offsetY = 0) {
            piece.shape.forEach((row, y) => {
                row.forEach((value, x) => {
                    if (value) {
                        drawBlock(context, piece.x + x + offsetX, piece.y + y + offsetY, piece.color);
                    }
                });
            });
        }

        function drawNextPiece() {
            nextCtx.fillStyle = '#0A0A1F';
            nextCtx.fillRect(0, 0, nextCanvas.width, nextCanvas.height);

            if (nextPiece) {
                const offsetX = Math.floor((4 - nextPiece.shape[0].length) / 2);
                const offsetY = Math.floor((4 - nextPiece.shape.length) / 2);
               
                nextPiece.shape.forEach((row, y) => {
                    row.forEach((value, x) => {
                        if (value) {
                            drawBlock(nextCtx, x + offsetX, y + offsetY, nextPiece.color);
                        }
                    });
                });
            }
        }

        function collision(piece, offsetX = 0, offsetY = 0) {
            for (let y = 0; y < piece.shape.length; y++) {
                for (let x = 0; x < piece.shape[y].length; x++) {
                    if (piece.shape[y][x]) {
                        const newX = piece.x + x + offsetX;
                        const newY = piece.y + y + offsetY;
                       
                        if (newX < 0 || newX >= COLS || newY >= ROWS) {
                            return true;
                        }
                        if (newY >= 0 && board[newY][newX]) {
                            return true;
                        }
                    }
                }
            }
            return false;
        }

        function merge() {
            currentPiece.shape.forEach((row, y) => {
                row.forEach((value, x) => {
                    if (value) {
                        const boardY = currentPiece.y + y;
                        const boardX = currentPiece.x + x;
                        if (boardY >= 0) {
                            board[boardY][boardX] = currentPiece.color;
                        }
                    }
                });
            });
        }

        function rotate(piece) {
            const newShape = piece.shape[0].map((_, i) =>
                piece.shape.map(row => row[i]).reverse()
            );
            const oldShape = piece.shape;
            piece.shape = newShape;
           
            if (collision(piece)) {
                piece.shape = oldShape;
            }
        }

        function clearLines() {
            let linesCleared = 0;
           
            for (let y = ROWS - 1; y >= 0; y--) {
                if (board[y].every(cell => cell !== 0)) {
                    board.splice(y, 1);
                    board.unshift(Array(COLS).fill(0));
                    linesCleared++;
                    y++;
                }
            }

            if (linesCleared > 0) {
                lines += linesCleared;
                score += [0, 100, 300, 500, 800][linesCleared] * (level + 1);
                level = Math.floor(lines / 10);
                dropInterval = Math.max(100, 1000 - (level * 50));
                updateDisplay();
            }
        }

        function updateDisplay() {
            document.getElementById('scoreDisplay').textContent = score.toString().padStart(6, '0');
            document.getElementById('linesDisplay').textContent = lines;
            document.getElementById('levelDisplay').textContent = level;
        }

        function drop() {
            if (!collision(currentPiece, 0, 1)) {
                currentPiece.y++;
            } else {
                merge();
                clearLines();
                currentPiece = nextPiece;
                nextPiece = createPiece();
               
                if (collision(currentPiece)) {
                    gameOver = true;
                    showGameOver();
                }
            }
        }

        function showGameOver() {
            ctx.fillStyle = 'rgba(0, 0, 0, 0.75)';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            ctx.fillStyle = '#00F0FF';
            ctx.font = 'bold 30px Inter';
            ctx.textAlign = 'center';
            ctx.fillText('GAME OVER', canvas.width / 2, canvas.height / 2 - 20);
            ctx.font = '16px Inter';
            ctx.fillText('Digite "restart" para jogar novamente', canvas.width / 2, canvas.height / 2 + 20);
        }

        function update(time = 0) {
            if (gameOver || isPaused) {
                requestAnimationFrame(update);
                return;
            }

            const deltaTime = time - lastTime;
            lastTime = time;
            dropCounter += deltaTime;

            if (dropCounter > dropInterval) {
                drop();
                dropCounter = 0;
            }

            drawBoard();
            if (currentPiece) {
                drawPiece(currentPiece);
            }
            drawNextPiece();

            requestAnimationFrame(update);
        }

        function sendCommand() {
            const input = document.getElementById('in01');
            const command = input.value.toLowerCase().trim();
           
            if (command === 'pause') {
                togglePause();
                input.value = '';
                return;
            }
           
            if (command === 'restart') {
                restartGame();
                input.value = '';
                return;
            }

            input.value = '';
        }

        function restartGame() {
            board = Array(ROWS).fill().map(() => Array(COLS).fill(0));
            score = 0;
            lines = 0;
            level = 0;
            gameOver = false;
            isPaused = false;
            dropInterval = 1000;
            currentPiece = createPiece();
            nextPiece = createPiece();
            updateDisplay();
           
            // Reset pause button
            const pauseButton = document.getElementById('pauseButton');
            pauseButton.textContent = '⏸️ PAUSAR';
            pauseButton.classList.remove('bg-green-600', 'hover:bg-green-500');
            pauseButton.classList.add('bg-void-blue', 'hover:bg-cyan-300');
        }

        function generateLore() {
            if (!currentPiece) return;
           
            const loreDisplay = document.getElementById('loreDisplay');
            loreDisplay.textContent = 'Gerando lore...';
           
            const pieceName = PIECE_NAMES[currentPiece.type];
            const lores = {
                'I': `A Linha Infinita: Dizem que esta peça atravessou o vazio cósmico por milênios. Sua forma perfeita representa a eternidade e o equilíbrio. Quando cai, ela traz consigo a promessa de ordem no caos.`,
                'O': `O Cubo Primordial: Nascido no centro do universo, o Quadrado é a forma mais estável conhecida. Sua simetria perfeita é um símbolo de harmonia. Lendas dizem que quem domina o Cubo, domina o destino.`,
                'T': `O Tridente Estelar: Forjado nas estrelas mais antigas, o T carrega o poder de três direções. É a peça dos estrategistas, capaz de se adaptar a qualquer situação. Seu centro brilha com sabedoria ancestral.`,
                'S': `A Serpente do Vazio: Sinuosa e imprevisível, a peça S desliza pelo tabuleiro como uma criatura viva. Ela representa a mudança e a transformação. Dizem que traz boa sorte aos corajosos.`,
                'Z': `O Raio Invertido: Nascido de uma tempestade cósmica, o Z corta o espaço com sua forma angular. É a peça dos revolucionários, que desafiam a ordem estabelecida. Seu poder é caótico, mas necessário.`,
                'J': `O Gancho Celestial: Forjado pelos guardiões do cosmos, o J é uma ferramenta de precisão. Sua curva elegante permite alcançar o impossível. Mestres do Tetris dizem que ele é a chave para a perfeição.`,
                'L': `A Lâmina Luminosa: Afiada como a luz de mil sóis, a peça L corta através das trevas. Ela representa coragem e determinação. Aqueles que a dominam são lembrados como lendas.`
            };

            setTimeout(() => {
                loreDisplay.textContent = lores[currentPiece.type] || 'Uma peça misteriosa do vazio...';
            }, 500);
        }

        document.addEventListener('keydown', (e) => {
            if (gameOver || isPaused || !currentPiece) return;

            switch(e.key) {
                case 'ArrowLeft':
                    if (!collision(currentPiece, -1, 0)) {
                        currentPiece.x--;
                    }
                    break;
                case 'ArrowRight':
                    if (!collision(currentPiece, 1, 0)) {
                        currentPiece.x++;
                    }
                    break;
                case 'ArrowDown':
                    drop();
                    break;
                case 'ArrowUp':
                    rotate(currentPiece);
                    break;
                case ' ':
                    while (!collision(currentPiece, 0, 1)) {
                        currentPiece.y++;
                    }
                    drop();
                    break;
            }
        });

        document.getElementById('in01').addEventListener('keypress', (e) => {
            if (e.key === 'Enter') {
                sendCommand();
            }
        });

        async function onConfigChange(config) {
            const title = config.game_title || defaultConfig.game_title;
            const levelLabel = config.level_label || defaultConfig.level_label;
            const linesLabel = config.lines_label || defaultConfig.lines_label;
            const scoreLabel = config.score_label || defaultConfig.score_label;
            const menuTitle = config.menu_title || defaultConfig.menu_title;
            const startButton = config.start_button || defaultConfig.start_button;
            const controlsButton = config.controls_button || defaultConfig.controls_button;
            const creditsButton = config.credits_button || defaultConfig.credits_button;
            const backButton = config.back_button || defaultConfig.back_button;

            // Atualizar textos do jogo
            document.getElementById('t').textContent = title;
            document.getElementById('levelLabel').textContent = levelLabel;
            document.getElementById('linesLabel').textContent = linesLabel;
            document.getElementById('scoreLabel').textContent = scoreLabel;

            // Atualizar textos do menu
            document.getElementById('menuTitle').textContent = menuTitle;
            document.getElementById('startButton').textContent = startButton;
            document.getElementById('controlsButton').textContent = controlsButton;
            document.getElementById('creditsButton').textContent = creditsButton;
            document.getElementById('backFromControls').textContent = backButton;
            document.getElementById('backFromCredits').textContent = backButton;
        }

        if (window.elementSdk) {
            window.elementSdk.init({
                defaultConfig,
                onConfigChange,
                mapToCapabilities: (config) => ({
                    recolorables: [],
                    borderables: [],
                    fontEditable: undefined,
                    fontSizeable: undefined
                }),
                mapToEditPanelValues: (config) => new Map([
                    ["game_title", config.game_title || defaultConfig.game_title],
                    ["level_label", config.level_label || defaultConfig.level_label],
                    ["lines_label", config.lines_label || defaultConfig.lines_label],
                    ["score_label", config.score_label || defaultConfig.score_label],
                    ["menu_title", config.menu_title || defaultConfig.menu_title],
                    ["start_button", config.start_button || defaultConfig.start_button],
                    ["controls_button", config.controls_button || defaultConfig.controls_button],
                    ["credits_button", config.credits_button || defaultConfig.credits_button],
                    ["back_button", config.back_button || defaultConfig.back_button]
                ])
            });
        }

        currentPiece = createPiece();
        nextPiece = createPiece();
        updateDisplay();
        update();
        
</script>

    </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'99a072c335a0cd6d',t:'MTc2MjM4ODY3MC4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
