<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Game Ular Tangga Interaktif</title>
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Font Google Poppins -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700;800&display=swap" rel="stylesheet">
  <!-- FontAwesome Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"/>

  <style>
    body {
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #0f172a 0%, #1e1b4b 50%, #311042 100%);
      min-height: 100vh;
      color: #fff;
    }
    
    /* Grid Board Styling */
    .board-container {
      position: relative;
      width: 100%;
      max-width: 580px;
      aspect-ratio: 1 / 1;
      box-shadow: 0 20px 50px rgba(0,0,0,0.5);
      border-radius: 16px;
      overflow: hidden;
      border: 4px solid #4f46e5;
    }

    .board-grid {
      display: grid;
      grid-template-columns: repeat(10, 1fr);
      grid-template-rows: repeat(10, 1fr);
      width: 100%;
      height: 100%;
    }

    .cell {
      display: flex;
      align-items: flex-start;
      justify-content: flex-start;
      padding: 4px;
      font-size: 0.75rem;
      font-weight: 700;
      position: relative;
    }

    /* Cell Alternating Colors */
    .cell-even { background-color: #f8fafc; color: #334155; }
    .cell-odd { background-color: #e2e8f0; color: #334155; }
    .cell-highlight-even { background-color: #ddd6fe; color: #4c1d95; }
    .cell-highlight-odd { background-color: #c4b5fd; color: #4c1d95; }

    /* SVG Layer Overlay for Snakes & Ladders */
    #svg-overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 10;
    }

    /* Player Pawn Pin */
    .pawn {
      width: 22px;
      height: 22px;
      border-radius: 50%;
      border: 2px solid #ffffff;
      box-shadow: 0 4px 6px rgba(0,0,0,0.4);
      transition: all 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
      position: absolute;
      z-index: 20;
    }

    /* Dice Rolling Animation */
    .dice-roll-anim {
      animation: spinDice 0.5s ease-in-out;
    }
    @keyframes spinDice {
      0% { transform: rotate(0deg) scale(0.8); }
      50% { transform: rotate(180deg) scale(1.2); }
      100% { transform: rotate(360deg) scale(1); }
    }

    /* Glassmorphism Cards */
    .glass-card {
      background: rgba(255, 255, 255, 0.08);
      backdrop-filter: blur(12px);
      border: 1px solid rgba(255, 255, 255, 0.15);
    }
  </style>
</head>
<body class="flex items-center justify-center p-4">

  <!-- ================= HALAMAN RUMAH (LOBBY) ================= -->
  <div id="home-screen" class="w-full max-w-md glass-card rounded-3xl p-8 shadow-2xl text-center space-y-6">
    <!-- Header Title -->
    <div>
      <div class="inline-block p-4 rounded-full bg-gradient-to-tr from-amber-400 to-red-500 shadow-lg mb-3 animate-bounce">
        <i class="fa-solid font-black text-4xl text-white">🎲</i>
      </div>
      <h1 class="text-4xl font-extrabold tracking-wide bg-gradient-to-r from-yellow-300 via-pink-400 to-indigo-300 bg-clip-text text-transparent">
        ULAR TANGGA
      </h1>
      <p class="text-sm text-gray-300 mt-1">Game Papan Klasik Modern & Seru</p>
    </div>

    <!-- Selection Jumlah Pemain -->
    <div class="space-y-3">
      <label class="block text-left text-sm font-semibold text-indigo-200">
        <i class="fa-solid fa-users mr-1"></i> Pilih Jumlah Pemain (Maksimal 4):
      </label>
      <div class="grid grid-cols-3 gap-3">
        <button type="button" onclick="selectPlayerCount(2)" id="btn-count-2" class="count-btn py-3 rounded-xl font-bold bg-indigo-600 border-2 border-indigo-400 text-white shadow-md">
          2 Pemain
        </button>
        <button type="button" onclick="selectPlayerCount(3)" id="btn-count-3" class="count-btn py-3 rounded-xl font-bold bg-gray-800 border-2 border-transparent text-gray-400 hover:bg-indigo-900">
          3 Pemain
        </button>
        <button type="button" onclick="selectPlayerCount(4)" id="btn-count-4" class="count-btn py-3 rounded-xl font-bold bg-gray-800 border-2 border-transparent text-gray-400 hover:bg-indigo-900">
          4 Pemain
        </button>
      </div>
    </div>

    <!-- Input Nama Pemain -->
    <div id="player-inputs" class="space-y-3 text-left">
      <!-- Input dinamis akan di-render di sini oleh JavaScript -->
    </div>

    <!-- Tombol Mulai -->
    <button onclick="startGame()" class="w-full py-4 rounded-2xl bg-gradient-to-r from-emerald-500 to-teal-600 hover:from-emerald-400 hover:to-teal-500 font-extrabold text-lg text-white shadow-xl hover:shadow-emerald-500/40 transform hover:-translate-y-1 transition duration-200">
      <i class="fa-solid fa-play mr-2"></i> MULAI PERMAINAN
    </button>
  </div>


  <!-- ================= HALAMAN PERMAINAN ================= -->
  <div id="game-screen" class="hidden w-full max-w-5xl flex-col lg:flex-row gap-6 items-center lg:items-start justify-center">
    
    <!-- Papan Game -->
    <div class="board-container bg-slate-900">
      <div id="board" class="board-grid"></div>
      <svg id="svg-overlay"></svg>
      <!-- Bidak pemain akan dimasukkan ke sini -->
      <div id="pawns-container"></div>
    </div>

    <!-- Control & Dashboard Sidebar -->
    <div class="w-full lg:w-80 flex flex-col gap-4">
      
      <!-- Card Bar Atas: Informasi & Kembali -->
      <div class="glass-card p-4 rounded-2xl flex items-center justify-between">
        <span class="font-bold text-yellow-400 text-lg"><i class="fa-solid fa-gamepad mr-2"></i>Ular Tangga</span>
        <button onclick="backToHome()" class="px-3 py-1.5 rounded-lg bg-red-500/20 hover:bg-red-500/40 text-red-300 text-xs font-semibold border border-red-500/30 transition">
          <i class="fa-solid fa-house mr-1"></i> Beranda
        </button>
      </div>

      <!-- Card Dadu & Giliran -->
      <div class="glass-card p-6 rounded-2xl text-center space-y-4">
        <div class="text-xs font-semibold uppercase tracking-wider text-gray-400">Giliran Saatin Ini</div>
        <div id="current-player-display" class="text-xl font-extrabold flex items-center justify-center gap-2">
          <!-- Nama Pemain Aktif -->
        </div>

        <!-- Visual Dadu -->
        <div class="py-3 flex justify-center items-center">
          <div id="dice-box" class="w-20 h-20 rounded-2xl bg-gradient-to-tr from-white to-gray-200 text-slate-900 font-extrabold text-4xl flex items-center justify-center shadow-2xl border-2 border-white">
            🎲
          </div>
        </div>

        <!-- Tombol Lempar Dadu -->
        <button id="roll-btn" onclick="rollDice()" class="w-full py-3.5 rounded-xl bg-gradient-to-r from-indigo-500 to-purple-600 hover:from-indigo-400 hover:to-purple-500 text-white font-bold text-md shadow-lg transform active:scale-95 transition">
          <i class="fa-solid fa-dice mr-2"></i> Lempar Dadu
        </button>
      </div>

      <!-- Card Daftar Pemain & Posisi -->
      <div class="glass-card p-4 rounded-2xl space-y-3">
        <div class="text-xs font-semibold uppercase tracking-wider text-gray-400 border-b border-gray-700 pb-2">Posisi Pemain</div>
        <div id="players-list" class="space-y-2">
          <!-- List Pemain -->
        </div>
      </div>

      <!-- Log Aktivitas -->
      <div class="glass-card p-4 rounded-2xl space-y-2">
        <div class="text-xs font-semibold uppercase tracking-wider text-gray-400">Riwayat Perjalanan</div>
        <div id="game-log" class="h-28 overflow-y-auto text-xs space-y-1 text-gray-300 pr-1">
          <p class="text-emerald-400">🎮 Selamat bermain!</p>
        </div>
      </div>

    </div>
  </div>


  <!-- ================= MODAL KEMENANGAN ================= -->
  <div id="win-modal" class="fixed inset-0 bg-black/80 backdrop-blur-sm hidden items-center justify-center z-50 p-4">
    <div class="glass-card bg-slate-900 border-2 border-yellow-400/50 max-w-sm w-full p-6 rounded-3xl text-center space-y-5 animate-bounce-short">
      <div class="text-6xl">🏆</div>
      <h2 class="text-3xl font-black text-yellow-400">PEMENANG!</h2>
      <p id="winner-name" class="text-xl font-bold text-white">Pemain 1</p>
      <p class="text-sm text-gray-300">Berhasil mencapai petak 100 terlebih dahulu!</p>
      <button onclick="backToHome()" class="w-full py-3 rounded-xl bg-gradient-to-r from-amber-500 to-orange-500 text-white font-bold shadow-lg">
        Main Lagi
      </button>
    </div>
  </div>


  <!-- ================= JAVASCRIPT LOGIC ================= -->
  <script>
    // Konfigurasi Warna Pemain
    const PLAYER_COLORS = [
      { name: 'Merah', hex: '#ef4444', border: '#b91c1c' },
      { name: 'Biru', hex: '#3b82f6', border: '#1d4ed8' },
      { name: 'Hijau', hex: '#10b981', border: '#047857' },
      { name: 'Kuning', hex: '#f59e0b', border: '#b45309' }
    ];

    // Data Tangga & Ular (Mulai -> Selesai)
    const LADDERS = {
      4: 14,
      9: 31,
      20: 38,
      28: 84,
      40: 59,
      51: 67,
      63: 81,
      71: 91
    };

    const SNAKES = {
      17: 7,
      54: 34,
      62: 19,
      64: 60,
      87: 24,
      93: 73,
      95: 75,
      99: 78
    };

    // State Permainan
    let playerCount = 2;
    let players = [];
    let currentPlayerIndex = 0;
    let isRolling = false;

    // Inisialisasi awal saat load
    window.onload = () => {
      renderPlayerInputs();
    };

    // Memilih Jumlah Pemain di Lobby
    function selectPlayerCount(count) {
      playerCount = count;
      for (let i = 2; i <= 4; i++) {
        const btn = document.getElementById(`btn-count-${i}`);
        if (i === count) {
          btn.className = "count-btn py-3 rounded-xl font-bold bg-indigo-600 border-2 border-indigo-400 text-white shadow-md";
        } else {
          btn.className = "count-btn py-3 rounded-xl font-bold bg-gray-800 border-2 border-transparent text-gray-400 hover:bg-indigo-900";
        }
      }
      renderPlayerInputs();
    }

    // Render Input Nama Pemain
    function renderPlayerInputs() {
      const container = document.getElementById('player-inputs');
      container.innerHTML = '';
      for (let i = 0; i < playerCount; i++) {
        const color = PLAYER_COLORS[i];
        container.innerHTML += `
          <div>
            <label class="text-xs text-gray-300 font-semibold mb-1 flex items-center">
              <span class="w-3 h-3 rounded-full mr-2 inline-block" style="background-color: ${color.hex}"></span>
              Nama Pemain ${i + 1}
            </label>
            <input type="text" id="input-player-${i}" value="Pemain ${i + 1}" 
              class="w-full bg-slate-800/80 border border-slate-700 rounded-xl px-4 py-2 text-sm text-white focus:outline-none focus:border-indigo-400">
          </div>
        `;
      }
    }

    // Pindah dari Lobby ke Game
    function startGame() {
      players = [];
      for (let i = 0; i < playerCount; i++) {
        const inputVal = document.getElementById(`input-player-${i}`).value.trim();
        players.push({
          id: i,
          name: inputVal || `Pemain ${i + 1}`,
          position: 1, // Mulai dari petak 1
          color: PLAYER_COLORS[i]
        });
      }

      currentPlayerIndex = 0;
      document.getElementById('home-screen').classList.add('hidden');
      document.getElementById('game-screen').classList.remove('hidden');
      document.getElementById('game-screen').classList.add('flex');

      buildBoard();
      drawSnakesAndLadders();
      updateDashboard();
      updatePawnPositions();
      addLog("🚀 Game dimulai! Semua pemain berada di Petak 1.");
    }

    // Kembali ke Lobby
    function backToHome() {
      document.getElementById('win-modal').classList.add('hidden');
      document.getElementById('win-modal').classList.remove('flex');
      document.getElementById('game-screen').classList.add('hidden');
      document.getElementById('game-screen').classList.remove('flex');
      document.getElementById('home-screen').classList.remove('hidden');
      document.getElementById('game-log').innerHTML = '<p class="text-emerald-400">🎮 Selamat bermain!</p>';
    }

    // Membuat Grid Papan 100 Petak (Boustrophedon Zig-zag)
    function buildBoard() {
      const board = document.getElementById('board');
      board.innerHTML = '';

      // Loop dari baris atas (baris 10) sampai bawah (baris 1)
      for (let row = 9; row >= 0; row--) {
        const isEvenRow = row % 2 === 0;
        for (let col = 0; col < 10; col++) {
          let cellNumber;
          if (isEvenRow) {
            // Baris genap: Kiri ke Kanan
            cellNumber = row * 10 + col + 1;
          } else {
            // Baris ganjil: Kanan ke Kiri
            cellNumber = row * 10 + (9 - col) + 1;
          }

          const cell = document.createElement('div');
          const isHighlight = (Math.floor((cellNumber-1)/10) + (cellNumber-1)%10) % 2 === 0;
          cell.className = `cell ${isHighlight ? 'cell-highlight-even' : 'cell-even'} id-cell-${cellNumber}`;
          cell.id = `cell-${cellNumber}`;
          cell.innerHTML = `<span>${cellNumber}</span>`;
          board.appendChild(cell);
        }
      }
    }

    // Menghitung Koordinat Center dari Petak (0-100%)
    function getCellCoords(squareNum) {
      const row = Math.floor((squareNum - 1) / 10);
      const colInRow = (squareNum - 1) % 10;
      const col = (row % 2 === 0) ? colInRow : 9 - colInRow;
      const displayRow = 9 - row;

      return {
        x: (col + 0.5) * 10, // persentase X
        y: (displayRow + 0.5) * 10 // persentase Y
      };
    }

    // Menggambar Visual Ular & Tangga Menggunakan SVG
    function drawSnakesAndLadders() {
      const svg = document.getElementById('svg-overlay');
      svg.innerHTML = `
        <defs>
          <linearGradient id="ladderGrad" x1="0%" y1="0%" x2="100%" y2="100%">
            <stop offset="0%" stop-color="#f59e0b"/>
            <stop offset="100%" stop-color="#d97706"/>
          </linearGradient>
          <linearGradient id="snakeGrad" x1="0%" y1="0%" x2="100%" y2="100%">
            <stop offset="0%" stop-color="#ef4444"/>
            <stop offset="100%" stop-color="#991b1b"/>
          </linearGradient>
        </defs>
      `;

      // Gambar Tangga (Garis Ganda)
      for (const [start, end] of Object.entries(LADDERS)) {
        const c1 = getCellCoords(Number(start));
        const c2 = getCellCoords(Number(end));

        const ladderLine = document.createElementNS('http://www.w3.org/2000/svg', 'line');
        ladderLine.setAttribute('x1', `${c1.x}%`);
        ladderLine.setAttribute('y1', `${c1.y}%`);
        ladderLine.setAttribute('x2', `${c2.x}%`);
        ladderLine.setAttribute('y2', `${c2.y}%`);
        ladderLine.setAttribute('stroke', 'url(#ladderGrad)');
        ladderLine.setAttribute('stroke-width', '8');
        ladderLine.setAttribute('stroke-linecap', 'round');
        ladderLine.setAttribute('opacity', '0.85');
        svg.appendChild(ladderLine);
      }

      // Gambar Ular (Garis Gelombang Lengkung)
      for (const [head, tail] of Object.entries(SNAKES)) {
        const c1 = getCellCoords(Number(head));
        const c2 = getCellCoords(Number(tail));
        
        // Buat path melengkung sederhana
        const midX = (c1.x + c2.x) / 2 + 5;
        const midY = (c1.y + c2.y) / 2 - 5;

        const snakePath = document.createElementNS('http://www.w3.org/2000/svg', 'path');
        const d = `M ${c1.x} ${c1.y} Q ${midX} ${midY} ${c2.x} ${c2.y}`;
        snakePath.setAttribute('d', d);
        snakePath.setAttribute('stroke', 'url(#snakeGrad)');
        snakePath.setAttribute('stroke-width', '6');
        snakePath.setAttribute('fill', 'none');
        snakePath.setAttribute('stroke-linecap', 'round');
        snakePath.setAttribute('stroke-dasharray', '6 3');
        svg.appendChild(snakePath);
      }
    }

    // Memperbarui Posisi Bidak di Atas Papan
    function updatePawnPositions() {
      const container = document.getElementById('pawns-container');
      container.innerHTML = '';

      players.forEach((player) => {
        const coords = getCellCoords(player.position);
        
        // Offset sedikit agar bidak yang berada di petak sama tidak saling menutupi
        const offsetX = (player.id % 2 === 0 ? -1.8 : 1.8);
        const offsetY = (player.id < 2 ? -1.8 : 1.8);

        const pawn = document.createElement('div');
        pawn.className = 'pawn';
        pawn.style.backgroundColor = player.color.hex;
        pawn.style.borderColor = player.color.border;
        pawn.style.left = `calc(${coords.x}% + ${offsetX}%)`;
        pawn.style.top = `calc(${coords.y}% + ${offsetY}%)`;
        pawn.title = `${player.name} (Petak ${player.position})`;

        container.appendChild(pawn);
      });
    }

    // Memperbarui Tampilan Sidebar
    function updateDashboard() {
      const curPlayer = players[currentPlayerIndex];
      const display = document.getElementById('current-player-display');
      display.innerHTML = `
        <span class="w-4 h-4 rounded-full inline-block" style="background-color: ${curPlayer.color.hex}"></span>
        <span style="color: ${curPlayer.color.hex}">${curPlayer.name}</span>
      `;

      const listContainer = document.getElementById('players-list');
      listContainer.innerHTML = '';
      players.forEach((p, idx) => {
        const isTurn = idx === currentPlayerIndex;
        listContainer.innerHTML += `
          <div class="flex items-center justify-between p-2 rounded-xl ${isTurn ? 'bg-indigo-600/30 border border-indigo-500/50' : 'bg-slate-800/40'}">
            <div class="flex items-center gap-2">
              <span class="w-3 h-3 rounded-full" style="background-color: ${p.color.hex}"></span>
              <span class="text-sm font-semibold ${isTurn ? 'text-white' : 'text-gray-400'}">${p.name}</span>
            </div>
            <span class="text-xs font-bold px-2 py-0.5 rounded-md bg-slate-700 text-yellow-300">Petak ${p.position}</span>
          </div>
        `;
      });
    }

    // Lempar Dadu
    function rollDice() {
      if (isRolling) return;
      isRolling = true;

      const diceBox = document.getElementById('dice-box');
      const rollBtn = document.getElementById('roll-btn');
      rollBtn.disabled = true;
      rollBtn.classList.add('opacity-50');

      diceBox.classList.add('dice-roll-anim');

      // Animasi angka acak saat melempar
      let count = 0;
      const interval = setInterval(() => {
        diceBox.innerText = Math.floor(Math.random() * 6) + 1;
        count++;
        if (count > 8) {
          clearInterval(interval);
          const diceResult = Math.floor(Math.random() * 6) + 1;
          diceBox.innerText = diceResult;
          diceBox.classList.remove('dice-roll-anim');
          
          movePlayer(diceResult);
        }
      }, 50);
    }

    // Pergerakan Pemain
    function movePlayer(diceRoll) {
      const player = players[currentPlayerIndex];
      addLog(`🎲 <b>${player.name}</b> mendapat angka <b>${diceRoll}</b>.`);

      let targetPos = player.position + diceRoll;

      // Aturan: Harus pas ke angka 100, jika lebih akan memantul balik
      if (targetPos > 100) {
        const over = targetPos - 100;
        targetPos = 100 - over;
        addLog(`⚠️ Memantul! ${player.name} melewatin petak 100.`);
      }

      // Animasi gerak bertahap
      let currentStep = player.position;
      const stepInterval = setInterval(() => {
        if (currentStep < targetPos) currentStep++;
        else if (currentStep > targetPos) currentStep--;
        
        player.position = currentStep;
        updatePawnPositions();

        if (currentStep === targetPos) {
          clearInterval(stepInterval);
          checkSpecialTiles(player);
        }
      }, 200);
    }

    // Cek Pijakan Tangga / Ular
    function checkSpecialTiles(player) {
      const pos = player.position;

      // Cek Tangga
      if (LADDERS[pos]) {
        const newPos = LADDERS[pos];
        setTimeout(() => {
          player.position = newPos;
          updatePawnPositions();
          updateDashboard();
          addLog(`🪜 <b>Hore!</b> ${player.name} naik tangga dari <b>${pos}</b> ke <b>${newPos}</b>!`);
          finishTurn(player);
        }, 400);
        return;
      }

      // Cek Ular
      if (SNAKES[pos]) {
        const newPos = SNAKES[pos];
        setTimeout(() => {
          player.position = newPos;
          updatePawnPositions();
          updateDashboard();
          addLog(`🐍 <b>Awas!</b> ${player.name} digigit ular dari <b>${pos}</b> turun ke <b>${newPos}</b>.`);
          finishTurn(player);
        }, 400);
        return;
      }

      finishTurn(player);
    }

    // Penyelesaian Giliran & Pindah Pemain
    function finishTurn(player) {
      updateDashboard();

      // Cek Pemenang
      if (player.position === 100) {
        setTimeout(() => {
          showWinner(player);
        }, 300);
        return;
      }

      // Berganti giliran ke pemain berikutnya
      currentPlayerIndex = (currentPlayerIndex + 1) % players.length;
      updateDashboard();

      const rollBtn = document.getElementById('roll-btn');
      rollBtn.disabled = false;
      rollBtn.classList.remove('opacity-50');
      isRolling = false;
    }

    // Tampilkan Modal Pemenang
    function showWinner(player) {
      document.getElementById('winner-name').innerText = player.name;
      document.getElementById('winner-name').style.color = player.color.hex;
      const modal = document.getElementById('win-modal');
      modal.classList.remove('hidden');
      modal.classList.add('flex');
      addLog(`🏆 <b>${player.name} MENANG!</b>`);
    }

    // Helper Catat Log
    function addLog(message) {
      const logContainer = document.getElementById('game-log');
      const p = document.createElement('p');
      p.innerHTML = message;
      logContainer.appendChild(p);
      logContainer.scrollTop = logContainer.scrollHeight;
    }
  </script>
</body>
</html>
