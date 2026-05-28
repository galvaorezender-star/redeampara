<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
    <title>Memória Dueto - Jogo da Memória para Duas Pessoas</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            user-select: none;
        }

        body {
            min-height: 100vh;
            background: linear-gradient(145deg, #1a472a 0%, #0e2a1a 100%);
            font-family: 'Segoe UI', 'Poppins', 'Quicksand', system-ui, -apple-system, 'Inter', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        /* Container principal */
        .game-container {
            max-width: 1300px;
            width: 100%;
            background: rgba(255, 248, 225, 0.15);
            backdrop-filter: blur(3px);
            border-radius: 64px;
            padding: 20px 25px 30px;
            box-shadow: 0 25px 45px rgba(0, 0, 0, 0.4), inset 0 1px 2px rgba(255, 255, 255, 0.2);
            transition: all 0.2s ease;
        }

        /* Painel de pontuação e turno */
        .score-panel {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 20px;
            margin-bottom: 35px;
        }

        .player-card {
            flex: 1;
            background: #fef7e0;
            border-radius: 48px;
            padding: 18px 20px;
            text-align: center;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
            transition: transform 0.2s, box-shadow 0.2s, border 0.2s;
            border: 3px solid transparent;
        }

        .player-card.active-turn {
            border-color: #ffb347;
            background: #fff5e6;
            transform: scale(1.02);
            box-shadow: 0 0 0 4px rgba(255, 180, 71, 0.5), 0 12px 28px black;
        }

        .player-name {
            font-size: 1.8rem;
            font-weight: 800;
            letter-spacing: 1px;
            background: linear-gradient(135deg, #2c5e2e, #1d3e1a);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.05);
        }

        .player-score {
            font-size: 3rem;
            font-weight: 900;
            color: #d68b2c;
            line-height: 1;
            margin: 10px 0 5px;
            text-shadow: 2px 2px 0 #ffe0a3;
        }

        .turn-indicator {
            font-size: 1rem;
            font-weight: bold;
            background: #f2c94c;
            display: inline-block;
            padding: 6px 18px;
            border-radius: 40px;
            color: #2c2c2c;
        }

        /* Área do tabuleiro */
        .board {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 18px;
            justify-items: center;
            align-items: center;
            margin: 20px 0 25px;
        }

        /* Cartas lindas e vivas */
        .card {
            width: 100%;
            aspect-ratio: 3 / 4;
            max-width: 140px;
            background: radial-gradient(circle at 30% 25%, #fff9e8, #ffefcf);
            border-radius: 28px;
            cursor: pointer;
            transition: all 0.25s cubic-bezier(0.2, 0.9, 0.4, 1.1);
            box-shadow: 0 15px 20px -8px rgba(0, 0, 0, 0.4);
            position: relative;
            transform-style: preserve-3d;
            transform: rotateY(0deg);
        }

        /* Estrutura de frente/verso */
        .card-inner {
            position: relative;
            width: 100%;
            height: 100%;
            text-align: center;
            transition: transform 0.4s ease-in-out;
            transform-style: preserve-3d;
            border-radius: 28px;
        }

        .card.flipped .card-inner {
            transform: rotateY(180deg);
        }

        .card-front, .card-back {
            position: absolute;
            width: 100%;
            height: 100%;
            backface-visibility: hidden;
            border-radius: 28px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            font-weight: bold;
            box-sizing: border-box;
        }

        .card-front {
            background: linear-gradient(145deg, #ffdd99, #ffcc77);
            transform: rotateY(180deg);
            color: #a55820;
            text-shadow: 2px 2px 0 rgba(0,0,0,0.1);
            border: 2px solid #ffb347;
            box-shadow: inset 0 0 0 3px rgba(255,215,130,0.8);
        }

        .card-back {
            background: repeating-linear-gradient(45deg, #ffb882, #ffb882 12px, #ffa559 12px, #ffa559 24px);
            border-radius: 28px;
            border: 2px solid #f5e2b0;
            color: #fff2d0;
            font-size: 2.6rem;
            font-weight: bold;
            display: flex;
            flex-direction: column;
            gap: 6px;
        }
        .card-back::before {
            content: "?";
            font-size: 3.5rem;
            opacity: 0.8;
            font-weight: 800;
        }
        .card-back::after {
            content: "🐾";
            font-size: 1.8rem;
            opacity: 0.7;
        }

        /* estados especiais */
        .card.matched {
            filter: drop-shadow(0 0 12px #ffd966);
            opacity: 0.7;
            cursor: default;
            transform: scale(0.97);
            filter: grayscale(0.2) brightness(1.05);
            pointer-events: none;
        }
        .card.matched .card-front {
            background: linear-gradient(145deg, #b5d3a0, #9cc97a);
            color: #3c6e2f;
            border-color: gold;
        }

        .card.disabled-temp {
            pointer-events: none;
            filter: brightness(0.96);
        }

        /* Botão reset + mensagens */
        .action-area {
            display: flex;
            justify-content: center;
            gap: 25px;
            margin-top: 15px;
            flex-wrap: wrap;
        }

        .btn {
            background: #fdd48d;
            border: none;
            font-size: 1.2rem;
            font-weight: bold;
            padding: 12px 28px;
            border-radius: 60px;
            cursor: pointer;
            transition: 0.15s linear;
            color: #3b2a1f;
            box-shadow: 0 6px 0 #b97f2e;
            font-family: inherit;
        }
        .btn:active {
            transform: translateY(2px);
            box-shadow: 0 3px 0 #b97f2e;
        }

        .message {
            text-align: center;
            background: #2d2b1fcc;
            backdrop-filter: blur(8px);
            padding: 10px 20px;
            border-radius: 60px;
            color: #ffefc0;
            font-weight: bold;
            font-size: 1.2rem;
            margin-top: 20px;
        }

        /* Modal de entrada dos jogadores */
        .modal {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.75);
            backdrop-filter: blur(8px);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 1000;
            transition: all 0.2s;
        }
        .modal-card {
            background: #fff7e8;
            max-width: 450px;
            width: 90%;
            border-radius: 64px;
            padding: 35px 30px;
            text-align: center;
            box-shadow: 0 30px 40px black;
            border: 1px solid #ffc857;
        }
        .modal-card h2 {
            font-size: 2rem;
            color: #4a6a2f;
            margin-bottom: 25px;
        }
        .modal-card input {
            display: block;
            width: 100%;
            margin: 18px 0;
            padding: 14px 18px;
            font-size: 1.2rem;
            border-radius: 48px;
            border: 2px solid #e1b87c;
            background: white;
            outline: none;
            font-family: inherit;
        }
        .modal-card button {
            background: #ffb347;
            font-size: 1.3rem;
            padding: 12px 30px;
            border: none;
            border-radius: 48px;
            font-weight: bold;
            margin-top: 15px;
            cursor: pointer;
        }

        @media (max-width: 650px) {
            .board {
                gap: 12px;
            }
            .player-name {
                font-size: 1.2rem;
            }
            .player-score {
                font-size: 2.2rem;
            }
            .card-front, .card-back {
                font-size: 2rem;
            }
        }

        footer {
            text-align: center;
            font-size: 0.7rem;
            margin-top: 15px;
            opacity: 0.7;
            color: #efe3c1;
        }
    </style>
</head>
<body>

<div class="game-container" id="gameContainer" style="display: none;">
    <div class="score-panel">
        <div class="player-card" id="player1Card">
            <div class="player-name" id="p1Name">Jogador 1</div>
            <div class="player-score" id="p1Score">0</div>
            <div class="turn-indicator" id="p1TurnBadge"></div>
        </div>
        <div class="player-card" id="player2Card">
            <div class="player-name" id="p2Name">Jogador 2</div>
            <div class="player-score" id="p2Score">0</div>
            <div class="turn-indicator" id="p2TurnBadge"></div>
        </div>
    </div>
    <div class="board" id="board"></div>
    <div class="action-area">
        <button class="btn" id="resetGameBtn">🔄 Reiniciar Jogo</button>
        <button class="btn" id="newPlayersBtn">👥 Trocar Jogadores</button>
    </div>
    <div class="message" id="statusMsg">Clique nas cartas! Combine os pares.</div>
    <footer>✨ Memória Dueto - Turnos alternados, quem faz mais pares vence! ✨</footer>
</div>

<!-- Modal inicial para nomes -->
<div id="nameModal" class="modal">
    <div class="modal-card">
        <h2>🎴 Bem-vindos ao Dueto da Memória</h2>
        <input type="text" id="player1NameInput" placeholder="Nome do Jogador 1" autocomplete="off">
        <input type="text" id="player2NameInput" placeholder="Nome do Jogador 2" autocomplete="off">
        <button id="startGameBtn">✨ Começar Jogo ✨</button>
        <div style="margin-top: 16px; font-size: 0.9rem;">🌈 Jogo para 2 pessoas: acerte um par e jogue novamente, erre e passa a vez!</div>
    </div>
</div>

<script>
    // ---------- Configuração do jogo ----------
    // Conjunto de ícones bonitos e modernos (tema nature/divertido)
    const ICON_SET = [
        "🐶", "🐱", "🐭", "🐹", "🐰", "🦊", "🐻", "🐼",
        "🐨", "🐯", "🦁", "🐮", "🐷", "🐸", "🐙", "🦄"
    ];
    
    let gameBoard = [];         // array de objetos: { id, icon, matched, flipped, cardElement, pairId }
    let cardsElements = [];
    let currentPlayer = 0;      // 0 = jogador1, 1 = jogador2
    let players = ["Jogador 1", "Jogador 2"];
    let scores = [0, 0];
    let lockBoard = false;      // trava enquanto animação ou checagem
    let firstCard = null;
    let secondCard = null;
    let timeoutId = null;
    let totalPairs = 8;          // 8 pares -> 16 cartas
    let matchedCount = 0;
    let gameActive = true;

    // DOM elements
    const boardDiv = document.getElementById('board');
    const p1NameSpan = document.getElementById('p1Name');
    const p2NameSpan = document.getElementById('p2Name');
    const p1ScoreSpan = document.getElementById('p1Score');
    const p2ScoreSpan = document.getElementById('p2Score');
    const p1TurnBadge = document.getElementById('p1TurnBadge');
    const p2TurnBadge = document.getElementById('p2TurnBadge');
    const statusMsgDiv = document.getElementById('statusMsg');
    const resetBtn = document.getElementById('resetGameBtn');
    const newPlayersBtn = document.getElementById('newPlayersBtn');
    const gameContainer = document.getElementById('gameContainer');
    const nameModal = document.getElementById('nameModal');
    const startBtn = document.getElementById('startGameBtn');
    const p1Input = document.getElementById('player1NameInput');
    const p2Input = document.getElementById('player2NameInput');

    // Função auxiliar para embaralhar (Fisher-Yates)
    function shuffleArray(arr) {
        for (let i = arr.length - 1; i > 0; i--) {
            const j = Math.floor(Math.random() * (i + 1));
            [arr[i], arr[j]] = [arr[j], arr[i]];
        }
        return arr;
    }

    // Inicializar ou reiniciar o tabuleiro (mantém os nomes atuais)
    function initGame(keepScores = false) {
        // cancelar qualquer timeout pendente
        if (timeoutId) clearTimeout(timeoutId);
        lockBoard = false;
        firstCard = null;
        secondCard = null;
        matchedCount = 0;
        gameActive = true;
        
        if (!keepScores) {
            scores = [0, 0];
            updateScoresUI();
        }
        
        // criar pares embaralhados
        let selectedIcons = ICON_SET.slice(0, totalPairs);
        let deck = [];
        for (let i = 0; i < totalPairs; i++) {
            deck.push({ pairId: i, icon: selectedIcons[i] });
            deck.push({ pairId: i, icon: selectedIcons[i] });
        }
        deck = shuffleArray(deck);
        
        // construir estrutura gameBoard
        gameBoard = deck.map((item, idx) => ({
            id: idx,
            pairId: item.pairId,
            icon: item.icon,
            matched: false,
            flipped: false,
            element: null
        }));
        
        // renderizar as cartas no DOM
        renderBoard();
        
        // atualizar interface de turno
        updateTurnUI();
        statusMsgDiv.innerHTML = `🎲 Vez de ${players[currentPlayer]}! Encontre um par e jogue novamente.`;
    }
    
    function renderBoard() {
        boardDiv.innerHTML = '';
        cardsElements = [];
        gameBoard.forEach((card, index) => {
            const cardDiv = document.createElement('div');
            cardDiv.className = 'card';
            if (card.matched) cardDiv.classList.add('matched');
            if (card.flipped) cardDiv.classList.add('flipped');
            
            const inner = document.createElement('div');
            inner.className = 'card-inner';
            
            const front = document.createElement('div');
            front.className = 'card-front';
            front.textContent = card.icon;
            const back = document.createElement('div');
            back.className = 'card-back';
            
            inner.appendChild(front);
            inner.appendChild(back);
            cardDiv.appendChild(inner);
            
            cardDiv.addEventListener('click', (e) => {
                e.stopPropagation();
                if (!gameActive) return;
                if (lockBoard) return;
                if (card.matched) return;
                if (card.flipped) return;
                if (secondCard !== null && firstCard !== null) return; // esperando reset
                handleCardClick(index);
            });
            
            boardDiv.appendChild(cardDiv);
            card.element = cardDiv;
            cardsElements.push(cardDiv);
        });
    }
    
    function updateSingleCardUI(cardIdx) {
        const card = gameBoard[cardIdx];
        const el = card.element;
        if (!el) return;
        if (card.matched) {
            el.classList.add('matched');
            el.classList.remove('flipped');
        } else if (card.flipped) {
            el.classList.add('flipped');
            el.classList.remove('matched');
        } else {
            el.classList.remove('flipped');
            el.classList.remove('matched');
        }
    }
    
    function handleCardClick(clickedIdx) {
        if (lockBoard) return;
        const clickedCard = gameBoard[clickedIdx];
        if (clickedCard.matched) return;
        if (clickedCard.flipped) return;
        
        // Se já existe primeira carta virada e segunda é nula, ou vice versa
        if (firstCard === null) {
            // vira primeira carta
            flipCardOpen(clickedIdx);
            firstCard = clickedIdx;
        } 
        else if (secondCard === null && firstCard !== clickedIdx) {
            flipCardOpen(clickedIdx);
            secondCard = clickedIdx;
            // verificar par
            lockBoard = true;
            checkMatch();
        }
        else if (secondCard === null && firstCard === clickedIdx) {
            // mesma carta, ignora
            return;
        }
    }
    
    function flipCardOpen(idx) {
        if (gameBoard[idx].flipped) return;
        gameBoard[idx].flipped = true;
        updateSingleCardUI(idx);
    }
    
    function flipCardClose(idx) {
        if (!gameBoard[idx].flipped) return;
        gameBoard[idx].flipped = false;
        updateSingleCardUI(idx);
    }
    
    function checkMatch() {
        const card1 = gameBoard[firstCard];
        const card2 = gameBoard[secondCard];
        const isMatch = (card1.pairId === card2.pairId);
        
        if (isMatch) {
            // acertou: marca como matched e incrementa pontuação do jogador atual
            card1.matched = true;
            card2.matched = true;
            updateSingleCardUI(firstCard);
            updateSingleCardUI(secondCard);
            matchedCount++;
            
            // soma ponto para o jogador atual
            scores[currentPlayer]++;
            updateScoresUI();
            
            // verifica se acabou o jogo
            if (matchedCount === totalPairs) {
                endGame();
                lockBoard = false;
                firstCard = null;
                secondCard = null;
                return;
            }
            
            // jogador ganha ponto e continua jogando (não muda turno)
            statusMsgDiv.innerHTML = `🎉 ${players[currentPlayer]} acertou! +1 ponto. Jogue novamente! 🎉`;
            // limpar seleções, mas mantém turno
            firstCard = null;
            secondCard = null;
            lockBoard = false;
            // atualizar UI de turno (mesmo jogador continua)
            updateTurnUI();
        } 
        else {
            // erro: mostra mensagem e depois de 0.8s desvira, troca turno
            statusMsgDiv.innerHTML = `❌ ${players[currentPlayer]} errou! Vez de ${players[currentPlayer === 0 ? 1 : 0]}. ❌`;
            // bloquear cliques durante o delay
            lockBoard = true;
            timeoutId = setTimeout(() => {
                // desvirar as duas cartas se não estiverem matched
                if (!gameBoard[firstCard].matched) flipCardClose(firstCard);
                if (!gameBoard[secondCard].matched) flipCardClose(secondCard);
                // trocar turno
                currentPlayer = currentPlayer === 0 ? 1 : 0;
                updateTurnUI();
                // reset temporário
                firstCard = null;
                secondCard = null;
                lockBoard = false;
                timeoutId = null;
                // mensagem de nova vez
                statusMsgDiv.innerHTML = `🎲 Agora é a vez de ${players[currentPlayer]}. Boa sorte!`;
            }, 800);
        }
    }
    
    function updateScoresUI() {
        p1ScoreSpan.innerText = scores[0];
        p2ScoreSpan.innerText = scores[1];
    }
    
    function updateTurnUI() {
        // remove classe active dos dois
        const p1CardDiv = document.getElementById('player1Card');
        const p2CardDiv = document.getElementById('player2Card');
        p1CardDiv.classList.remove('active-turn');
        p2CardDiv.classList.remove('active-turn');
        
        if (currentPlayer === 0) {
            p1CardDiv.classList.add('active-turn');
            p1TurnBadge.innerText = "🔵 SUA VEZ";
            p2TurnBadge.innerText = "";
        } else {
            p2CardDiv.classList.add('active-turn');
            p2TurnBadge.innerText = "🔴 SUA VEZ";
            p1TurnBadge.innerText = "";
        }
        // Atualiza nomes se tiver alteração (já estão setados)
    }
    
    function endGame() {
        gameActive = false;
        let winnerMsg = "";
        if (scores[0] > scores[1]) {
            winnerMsg = `🏆 Vitória de ${players[0]} com ${scores[0]} pontos! 🏆`;
        } else if (scores[1] > scores[0]) {
            winnerMsg = `🏆 Vitória de ${players[1]} com ${scores[1]} pontos! 🏆`;
        } else {
            winnerMsg = `🤝 Empate! ${players[0]} e ${players[1]} fizeram ${scores[0]} pontos cada. 🤝`;
        }
        statusMsgDiv.innerHTML = `✨ FIM DE JOGO! ✨ ${winnerMsg} ✨ Clique em Reiniciar para nova partida.`;
        lockBoard = true; // impede novos cliques
    }
    
    function resetGameSession() {
        if (timeoutId) clearTimeout(timeoutId);
        lockBoard = false;
        firstCard = null;
        secondCard = null;
        gameActive = true;
        // reinicia placar e tabuleiro mantendo nomes
        scores = [0, 0];
        updateScoresUI();
        currentPlayer = 0;   // jogador 1 começa
        initGame(true);      // true para manter os scores já zerados (keepScores mas passamos false antes? melhor usar initGame com reset total)
        // Mas initGame(keepScores=false) vai zerar scores novamente, porém chamamos antes e já zeramos, melhor chamar initGame sem keepScores mas já zerei
        // Para evitar duplicidade, chamo initGame com keepScores false mas scores já está 0,0 então ok
        // O initGame(false) zera scores novamente e recria deck
        // Para garantir, chamamos:
        // Mas precisamos resetar matchedCount, etc.
        // Vamos simplesmente chamar initGame(false)
        initGame(false);
        statusMsgDiv.innerHTML = `🔄 Jogo reiniciado! Vez de ${players[0]}. Faça pares!`;
    }
    
    function changePlayers() {
        // mostrar modal e esconder jogo
        gameContainer.style.display = "none";
        nameModal.style.display = "flex";
        // limpar inputs e preencher com os atuais se desejar (opcional)
        p1Input.value = players[0];
        p2Input.value = players[1];
        // qualquer timeout pendente cancelar
        if (timeoutId) clearTimeout(timeoutId);
    }
    
    function startGameWithNames() {
        let name1 = p1Input.value.trim();
        let name2 = p2Input.value.trim();
        if (name1 === "") name1 = "Mestre(a)🐣";
        if (name2 === "") name2 = "Desbravador(a)🦊";
        players[0] = name1;
        players[1] = name2;
        p1NameSpan.innerText = players[0];
        p2NameSpan.innerText = players[1];
        
        // resetar pontuações e estado
        scores = [0, 0];
        currentPlayer = 0;
        updateScoresUI();
        // iniciar o jogo do zero
        initGame(false);
        // esconder modal e mostrar container
        nameModal.style.display = "none";
        gameContainer.style.display = "block";
        // atualizar mensagem
        statusMsgDiv.innerHTML = `🎴 Partida iniciada! ${players[0]} vs ${players[1]}. ${players[0]} começa!`;
        updateTurnUI();
    }
    
    // Event listeners
    resetBtn.addEventListener('click', () => {
        if (!gameContainer.style.display === 'block') return;
        resetGameSession();
    });
    
    newPlayersBtn.addEventListener('click', () => {
        changePlayers();
    });
    
    startBtn.addEventListener('click', () => {
        startGameWithNames();
    });
    
    // Permitir iniciar com enter nos inputs
    p1Input.addEventListener('keypress', (e) => { if (e.key === 'Enter') startGameWithNames(); });
    p2Input.addEventListener('keypress', (e) => { if (e.key === 'Enter') startGameWithNames(); });
    
    // Inicialmente mostrar modal e garantir que nenhum jogo ativo
    gameContainer.style.display = "none";
    nameModal.style.display = "flex";
    
    // pré definição para demonstração (opcional)
    p1Input.value = "Aventureiro(a)";
    p2Input.value = "Explorador(a)";
</script>
</body>
</html>
