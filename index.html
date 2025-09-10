<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
    <title>4키 리듬게임</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700&family=Noto+Sans+KR:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-color: #1a1a2e;
            --lane-color: #16213e;
            --line-color: #0f3460;
            --text-color: #e94560;
            --judgement-line-color: #f9f9f9;
            --note-d: #ff6b6b;
            --note-f: #48dbfb;
            --note-j: #feca57;
            --note-k: #1dd1a1;
        }

        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: var(--bg-color);
            font-family: 'Inter', 'Noto Sans KR', sans-serif;
            color: white;
            overflow: hidden;
        }

        #game-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
        }

        #game-screen {
            position: relative;
            width: 320px;
            height: 600px;
            background-color: var(--lane-color);
            border: 2px solid var(--line-color);
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
        }

        .lane {
            position: absolute;
            width: 80px;
            height: 100%;
            border-right: 1px solid var(--line-color);
        }
        .lane:last-child { border-right: none; }
        #lane-0 { left: 0px; }
        #lane-1 { left: 80px; }
        #lane-2 { left: 160px; }
        #lane-3 { left: 240px; }

        .note {
            position: absolute;
            width: 70px;
            height: 25px;
            left: 5px;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.3);
            z-index: 5;
            transition: opacity 0.1s;
        }
        
        .long-note-tail {
            position: absolute;
            width: 60px;
            left: 10px;
            border-radius: 8px;
            z-index: 4;
            opacity: 0.8;
            transition: opacity 0.1s, box-shadow 0.2s;
        }

        .long-note-tail.release-glow {
            box-shadow: 0 0 25px 8px white;
        }

        .note-d, .tail-d { background: linear-gradient(145deg, var(--note-d), #d45a5a); }
        .note-f, .tail-f { background: linear-gradient(145deg, var(--note-f), #3cbad6); }
        .note-j, .tail-j { background: linear-gradient(145deg, var(--note-j), #d9ad4b); }
        .note-k, .tail-k { background: linear-gradient(145deg, var(--note-k), #18b089); }

        #judgement-line {
            position: absolute;
            bottom: 80px;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--note-d), var(--note-f), var(--note-j), var(--note-k));
            box-shadow: 0 0 15px var(--judgement-line-color);
            z-index: 10;
        }

        #key-indicators {
            position: absolute;
            bottom: 0;
            width: 100%;
            height: 80px;
            display: flex;
        }

        .key {
            width: 80px;
            height: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 28px;
            font-weight: bold;
            color: rgba(255, 255, 255, 0.5);
            transition: all 0.1s ease;
            user-select: none;
            -webkit-user-select: none;
            cursor: pointer;
        }

        .key.active {
            background-color: rgba(255, 255, 255, 0.2);
            color: white;
            transform: scale(1.05);
        }

        #ui-container {
            width: 320px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 20px;
            font-weight: bold;
            text-shadow: 0 2px 4px rgba(0,0,0,0.5);
        }
        
        .controls-right {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        #speed-control {
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        #speed-control button {
            width: 30px;
            height: 30px;
            font-size: 20px;
            font-weight: bold;
            border-radius: 50%;
            border: 2px solid var(--line-color);
            background-color: var(--lane-color);
            color: white;
            cursor: pointer;
        }

        #pause-button {
            width: 40px;
            height: 40px;
            font-size: 20px;
            font-weight: bold;
            border-radius: 8px;
            border: 2px solid var(--line-color);
            background-color: var(--lane-color);
            color: white;
            cursor: pointer;
            padding-bottom: 3px; /* Align bars vertically */
        }
        
        #judgement-feedback {
            position: absolute;
            top: 40%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 48px;
            font-weight: bold;
            color: white;
            opacity: 0;
            transition: all 0.3s ease;
            z-index: 20;
            text-shadow: 0 0 10px #000, 0 0 20px #fff;
        }
        
        #judgement-feedback.show {
            opacity: 1;
            transform: translate(-50%, -50%) scale(1.2);
        }
        
        #start-button, #resume-button {
            padding: 15px 30px;
            font-size: 24px;
            font-weight: bold;
            color: var(--bg-color);
            background-color: var(--judgement-line-color);
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.2s ease;
        }
        
        #start-button {
             position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 100;
        }


        #start-button:hover, #resume-button:hover {
            transform: translate(-50%, -50%) scale(1.05);
            box-shadow: 0 0 20px var(--judgement-line-color);
        }

        #pause-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.75);
            z-index: 200;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            gap: 20px;
        }

        #pause-text {
            font-size: 48px;
            font-weight: bold;
            color: white;
            text-shadow: 0 0 15px white;
        }
    </style>
</head>
<body>

    <div id="game-container">
        <div id="ui-container">
            <div>
                <div id="score">Score: 0</div>
                <div id="combo">Combo: 0</div>
            </div>
            <div class="controls-right">
                <button id="pause-button">II</button>
                <div id="speed-control">
                    <button id="speed-down">-</button>
                    <span id="speed-display">x1.0</span>
                    <button id="speed-up">+</button>
                </div>
            </div>
        </div>
        <div id="game-screen">
            <div class="lane" id="lane-0" data-key="d"></div>
            <div class="lane" id="lane-1" data-key="f"></div>
            <div class="lane" id="lane-2" data-key="j"></div>
            <div class="lane" id="lane-3" data-key="k"></div>
            <div id="judgement-line"></div>
            <div id="judgement-feedback"></div>
            <div id="key-indicators">
                <div class="key" id="key-d" data-key="d">D</div>
                <div class="key" id="key-f" data-key="f">F</div>
                <div class="key" id="key-j" data-key="j">J</div>
                <div class="key" id="key-k" data-key="k">K</div>
            </div>
            <button id="start-button">Start Game</button>
            <div id="pause-overlay" style="display: none;">
                <div id="pause-text">PAUSED</div>
                <button id="resume-button">Resume</button>
            </div>
        </div>
    </div>

    <script>
        // DOM Elements
        const scoreDisplay = document.getElementById('score');
        const comboDisplay = document.getElementById('combo');
        const judgementFeedback = document.getElementById('judgement-feedback');
        const startButton = document.getElementById('start-button');
        const speedDownBtn = document.getElementById('speed-down');
        const speedUpBtn = document.getElementById('speed-up');
        const speedDisplay = document.getElementById('speed-display');
        const keyIndicators = { 'd': document.getElementById('key-d'), 'f': document.getElementById('key-f'), 'j': document.getElementById('key-j'), 'k': document.getElementById('key-k') };
        const pauseButton = document.getElementById('pause-button');
        const pauseOverlay = document.getElementById('pause-overlay');
        const resumeButton = document.getElementById('resume-button');

        // Game State
        let score = 0, combo = 0, notes = [], gameInterval, gameLoopId, isGameRunning = false, isPaused = false;
        let activeLongNotes = { 'd': null, 'f': null, 'j': null, 'k': null };
        let isLaneOccupiedByLongNote = [false, false, false, false];

        // Game Settings
        const BASE_NOTE_SPEED = 2;
        let speedMultiplier = 1.0;
        const SPAWN_INTERVAL = 133;
        const JUDGEMENT_OFFSET = 40; // 판정 위치 조절 (양수 = 더 늦게/아래쪽)
        const JUDGEMENT_LINE_POS = 600 - 80 - 12.5 + JUDGEMENT_OFFSET;
        const KEY_LIST = ['d', 'f', 'j', 'k'];
        const BASE_PERFECT_THRESHOLD = 15, BASE_GREAT_THRESHOLD = 30, BASE_GOOD_THRESHOLD = 50;
        const LONG_NOTE_CHANCE = 0.20;

        // --- Game Functions ---

        function createNote() {
            if (!isGameRunning || isPaused) return;

            const availableLanes = [0, 1, 2, 3].filter(i => !isLaneOccupiedByLongNote[i]);
            if (availableLanes.length === 0) return;

            const keyIndex = availableLanes[Math.floor(Math.random() * availableLanes.length)];
            const key = KEY_LIST[keyIndex];
            const laneElement = document.getElementById(`lane-${keyIndex}`);
            
            const isLongNote = Math.random() < LONG_NOTE_CHANCE;
            
            let note = { key, y: -30, type: 'normal' };
            const noteElement = document.createElement('div');
            noteElement.className = `note note-${key}`;
            laneElement.appendChild(noteElement);
            note.element = noteElement;

            if (isLongNote) {
                note.type = 'long';
                note.duration = Math.random() * 200 + 150;
                note.isHolding = false;
                
                const tailElement = document.createElement('div');
                tailElement.className = `long-note-tail tail-${key}`;
                tailElement.style.height = `${note.duration}px`;
                laneElement.appendChild(tailElement);
                note.tailElement = tailElement;
                note.y = -30 - note.duration;

                isLaneOccupiedByLongNote[keyIndex] = true;
            }
            
            note.element.style.top = `${note.y}px`;
            if (note.tailElement) note.tailElement.style.top = `${note.y + 25}px`;
            notes.push(note);
        }

        function gameLoop() {
            if (!isGameRunning || isPaused) { // Check for pause
                cancelAnimationFrame(gameLoopId);
                return;
            }

            const fallDistance = BASE_NOTE_SPEED * speedMultiplier;
            const currentLateGoodThreshold = BASE_GOOD_THRESHOLD * speedMultiplier; 

            for (let i = notes.length - 1; i >= 0; i--) {
                const note = notes[i];
                note.y += fallDistance;
                note.element.style.top = `${note.y}px`;
                if (note.type === 'long') {
                    note.tailElement.style.top = `${note.y + 25}px`;
                }

                const missLine = JUDGEMENT_LINE_POS + currentLateGoodThreshold;
                const checkPos = note.y;

                if (checkPos > missLine && !note.isHolding) {
                    handleJudgement('MISS');
                    if (activeLongNotes[note.key] === note) {
                        activeLongNotes[note.key] = null;
                    }
                    removeNote(i);
                }
            }
            
            const currentReleaseGlowThreshold = (BASE_GOOD_THRESHOLD * 3.0) * speedMultiplier;
            for (const key in activeLongNotes) {
                const note = activeLongNotes[key];
                if (note && note.isHolding) {
                    const tailEndPos = note.y + 25 + note.duration;
                    const distance = Math.abs(tailEndPos - (JUDGEMENT_LINE_POS + 12.5));
                    if (distance <= currentReleaseGlowThreshold) {
                        note.tailElement.classList.add('release-glow');
                    } else {
                        note.tailElement.classList.remove('release-glow');
                    }
                }
            }

            gameLoopId = requestAnimationFrame(gameLoop);
        }

        function pressKey(key) {
            if (!isGameRunning || isPaused) return;
            
            keyIndicators[key].classList.add('active');

            const earlyGoodThreshold = -(BASE_GOOD_THRESHOLD * 0.5) * speedMultiplier;
            const lateGoodThreshold = BASE_GOOD_THRESHOLD * speedMultiplier;

            for (let i = notes.length - 1; i >= 0; i--) {
                const note = notes[i];
                if (note.key === key) {
                    const rawDistance = note.y - JUDGEMENT_LINE_POS;
                    
                    if (rawDistance >= earlyGoodThreshold && rawDistance <= lateGoodThreshold) {
                        if (note.type === 'normal') {
                            judgeHit(rawDistance);
                            removeNote(i);
                        } else if (note.type === 'long' && !note.isHolding) {
                            judgeHit(rawDistance);
                            note.isHolding = true;
                            activeLongNotes[key] = note;
                            note.element.style.opacity = '0.5';
                            note.tailElement.style.opacity = '1';
                        }
                        break;
                    }
                }
            }
            updateUI();
        }

        function releaseKey(key) {
            if (!KEY_LIST.includes(key)) return;
            keyIndicators[key].classList.remove('active');

            if (!isGameRunning || isPaused) return;

            const activeNote = activeLongNotes[key];
            if (activeNote && activeNote.isHolding) {
                const tailEndPos = activeNote.y + 25 + activeNote.duration;
                const rawDistance = tailEndPos - (JUDGEMENT_LINE_POS + 12.5);

                const earlyReleaseThreshold = -(BASE_GOOD_THRESHOLD * 1.5) * speedMultiplier;
                const lateReleaseThreshold = (BASE_GOOD_THRESHOLD * 3.0) * speedMultiplier;

                if (rawDistance >= earlyReleaseThreshold && rawDistance <= lateReleaseThreshold) {
                    judgeHit(rawDistance);
                } else {
                    handleJudgement('MISS');
                }
                
                const noteIndex = notes.findIndex(note => note === activeNote);
                if (noteIndex > -1) removeNote(noteIndex);
                
                activeLongNotes[key] = null;
                updateUI();
            }
        }
        
        function handleKeyDown(e) {
            if (e.key === 'Escape' && isGameRunning) {
                togglePause();
                return;
            }
            if (e.repeat || !KEY_LIST.includes(e.key)) return;
            pressKey(e.key);
        }
        
        function handleKeyUp(e) {
            releaseKey(e.key);
        }
        
        function judgeHit(rawDistance) {
            const speedBonus = 1 + (speedMultiplier - 1) * 0.5;
            
            const earlyPerfect = -(BASE_PERFECT_THRESHOLD * 0.5) * speedMultiplier;
            const latePerfect = BASE_PERFECT_THRESHOLD * speedMultiplier;
            const earlyGreat = -(BASE_GREAT_THRESHOLD * 0.5) * speedMultiplier;
            const lateGreat = BASE_GREAT_THRESHOLD * speedMultiplier;
            
            if (rawDistance >= earlyPerfect && rawDistance <= latePerfect) { 
                handleJudgement('PERFECT'); 
                score += Math.round(300 * speedBonus); 
            } else if (rawDistance >= earlyGreat && rawDistance <= lateGreat) { 
                handleJudgement('GREAT'); 
                score += Math.round(200 * speedBonus); 
            } else { 
                handleJudgement('GOOD'); 
                score += Math.round(100 * speedBonus); 
            }
        }

        function handleJudgement(judgement) {
            if (judgement === 'MISS') combo = 0;
            else combo++;

            judgementFeedback.textContent = judgement;
            judgementFeedback.className = 'show';
            if (judgement === 'PERFECT') judgementFeedback.style.color = '#ffdd59';
            else if (judgement === 'GREAT') judgementFeedback.style.color = '#48dbfb';
            else if (judgement === 'GOOD') judgementFeedback.style.color = '#1dd1a1';
            else judgementFeedback.style.color = '#ff6b6b';

            setTimeout(() => { judgementFeedback.className = ''; }, 300);
        }
        
        function removeNote(index) {
            const noteToRemove = notes[index];
            if (!noteToRemove) return;

            if (noteToRemove.type === 'long') {
                const keyIndex = KEY_LIST.indexOf(noteToRemove.key);
                if (keyIndex > -1) {
                    isLaneOccupiedByLongNote[keyIndex] = false;
                }
            }

            noteToRemove.element.remove();
            if (noteToRemove.tailElement) noteToRemove.tailElement.remove();
            notes.splice(index, 1);
        }

        function updateUI() {
            scoreDisplay.textContent = `Score: ${score}`;
            comboDisplay.textContent = `Combo: ${combo}`;
        }

        function updateSpeed(change) {
            if (isPaused) return;
            speedMultiplier = Math.max(0.5, Math.min(10.0, speedMultiplier + change));
            speedDisplay.textContent = `x${speedMultiplier.toFixed(1)}`;
        }

        function togglePause() {
            if (!isGameRunning) return;
            isPaused = !isPaused;
            if (isPaused) {
                clearInterval(gameInterval);
                pauseOverlay.style.display = 'flex';
            } else {
                gameInterval = setInterval(createNote, SPAWN_INTERVAL);
                gameLoopId = requestAnimationFrame(gameLoop);
                pauseOverlay.style.display = 'none';
            }
        }

        function startGame() {
            if (isGameRunning) return;
            isGameRunning = true;
            isPaused = false;
            score = 0; combo = 0;
            notes.forEach((note, i) => removeNote(i));
            notes = [];
            activeLongNotes = { 'd': null, 'f': null, 'j': null, 'k': null };
            isLaneOccupiedByLongNote = [false, false, false, false];
            updateUI();
            startButton.style.display = 'none';
            pauseOverlay.style.display = 'none';
            gameInterval = setInterval(createNote, SPAWN_INTERVAL);
            gameLoopId = requestAnimationFrame(gameLoop);
        }

        // --- Event Listeners ---
        startButton.addEventListener('click', startGame);
        pauseButton.addEventListener('click', togglePause);
        resumeButton.addEventListener('click', togglePause);
        window.addEventListener('keydown', handleKeyDown);
        window.addEventListener('keyup', handleKeyUp);
        speedUpBtn.addEventListener('click', () => updateSpeed(0.5));
        speedDownBtn.addEventListener('click', () => updateSpeed(-0.5));

        document.querySelectorAll('.key').forEach(keyElement => {
            const key = keyElement.dataset.key;
            
            keyElement.addEventListener('mousedown', () => pressKey(key));
            keyElement.addEventListener('mouseup', () => releaseKey(key));
            keyElement.addEventListener('mouseleave', () => releaseKey(key));
            
            keyElement.addEventListener('touchstart', (e) => {
                e.preventDefault();
                pressKey(key);
            });
            keyElement.addEventListener('touchend', (e) => {
                e.preventDefault();
                releaseKey(key);
            });
        });

    </script>
</body>
</html>

