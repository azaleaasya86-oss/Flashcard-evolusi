<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flashcard Evolusi Biologi Azalea Asya</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #e3f2fd 0%, #f3e5f5 100%);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 25px 20px;
            color: #333;
        }
        
        .personal-title {
            text-align: center;
            margin-bottom: 15px;
            width: 100%;
            max-width: 900px;
            background: linear-gradient(to right, #7b1fa2, #2196f3);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .personal-title h1 {
            font-size: 2.5rem;
            margin-bottom: 5px;
            font-weight: 800;
        }
        
        .personal-title p {
            color: #5d5d5d;
            font-size: 1.1rem;
        }
        
        .instructions {
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 12px;
            padding: 18px;
            margin-bottom: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            max-width: 900px;
            width: 100%;
            border-left: 6px solid #7b1fa2;
        }
        
        .instructions h3 {
            color: #7b1fa2;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .instructions p {
            margin-bottom: 8px;
            line-height: 1.5;
            color: #555;
        }
        
        .card-counter {
            background: linear-gradient(to right, #7b1fa2, #2196f3);
            color: white;
            padding: 10px 25px;
            border-radius: 25px;
            font-weight: bold;
            margin-bottom: 25px;
            font-size: 1.1rem;
            box-shadow: 0 4px 10px rgba(123, 31, 162, 0.3);
        }
        
        .flashcard-container {
            perspective: 1500px;
            width: 100%;
            max-width: 900px; /* Lebar kontainer diperbesar */
            height: 480px; /* Tinggi kartu DIPERPANJANG */
            margin-bottom: 35px;
        }
        
        .flashcard {
            width: 100%;
            height: 100%;
            position: relative;
            transform-style: preserve-3d;
            transition: transform 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            cursor: pointer;
            border-radius: 25px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.25);
        }
        
        .flashcard.flipped {
            transform: rotateY(180deg);
        }
        
        .card-front, .card-back {
            position: absolute;
            width: 100%;
            height: 100%;
            backface-visibility: hidden;
            border-radius: 25px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 50px; /* Padding diperbesar untuk ruang teks lebih luas */
            overflow-y: auto;
        }
        
        .card-front {
            background: linear-gradient(135deg, #7b1fa2 0%, #4527a0 100%);
            color: white;
        }
        
        .card-back {
            background: linear-gradient(135deg, #2196f3 0%, #0d47a1 100%);
            color: white;
            transform: rotateY(180deg);
        }
        
        .card-label {
            position: absolute;
            top: 20px;
            left: 25px;
            font-size: 1rem;
            opacity: 0.9;
            font-weight: bold;
            letter-spacing: 1px;
        }
        
        .card-front .card-label {
            background-color: rgba(255, 255, 255, 0.25);
            padding: 8px 15px;
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.4);
        }
        
        .card-back .card-label {
            background-color: rgba(0, 0, 0, 0.25);
            padding: 8px 15px;
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.3);
        }
        
        .question, .answer {
            font-size: 1.9rem; /* Ukuran font sedikit diperbesar */
            text-align: center;
            line-height: 1.6; /* Jarak antar baris diperlebar */
            font-weight: 600;
            max-width: 95%;
            padding: 10px;
        }
        
        .answer {
            font-weight: 500;
            font-size: 1.8rem;
        }
        
        .hint {
            position: absolute;
            bottom: 25px;
            font-size: 0.95rem;
            opacity: 0.9;
            font-style: italic;
            background-color: rgba(0, 0, 0, 0.2);
            padding: 5px 15px;
            border-radius: 15px;
        }
        
        .controls {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 35px;
            flex-wrap: wrap;
        }
        
        .btn {
            padding: 15px 30px;
            border: none;
            border-radius: 50px;
            font-size: 1.05rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 10px;
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
            min-width: 160px;
            justify-content: center;
        }
        
        .btn:hover {
            transform: translateY(-4px);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
        }
        
        .btn:active {
            transform: translateY(0);
        }
        
        .btn-prev {
            background-color: #5d5d5d;
            color: white;
        }
        
        .btn-flip {
            background-color: #7b1fa2;
            color: white;
        }
        
        .btn-next {
            background-color: #2196f3;
            color: white;
        }
        
        .btn-show-all {
            background-color: #ff9800;
            color: white;
        }
        
        .card-list {
            width: 100%;
            max-width: 900px;
            background-color: rgba(255, 255, 255, 0.98);
            border-radius: 18px;
            padding: 25px;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.12);
            margin-bottom: 35px;
            max-height: 450px;
            overflow-y: auto;
            display: none;
            border: 1px solid #e0e0e0;
        }
        
        .card-list h3 {
            color: #7b1fa2;
            margin-bottom: 20px;
            text-align: center;
            font-size: 1.8rem;
            padding-bottom: 15px;
            border-bottom: 2px solid #f0f0f0;
        }
        
        .card-item {
            background: linear-gradient(to right, #f9f9f9, #ffffff);
            border-left: 6px solid #2196f3;
            margin-bottom: 15px;
            padding: 20px;
            border-radius: 12px;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 3px 8px rgba(0, 0, 0, 0.05);
        }
        
        .card-item:hover {
            background: linear-gradient(to right, #e8f4fd, #f0f8ff);
            transform: translateX(8px) translateY(-3px);
            box-shadow: 0 6px 15px rgba(33, 150, 243, 0.15);
            border-left-color: #7b1fa2;
        }
        
        .card-item h4 {
            color: #2c3e50;
            margin-bottom: 8px;
            font-size: 1.2rem;
        }
        
        .card-item p {
            color: #666;
            font-size: 1rem;
            line-height: 1.5;
        }
        
        @media (max-width: 992px) {
            .flashcard-container {
                height: 450px;
                max-width: 95%;
            }
            
            .question, .answer {
                font-size: 1.7rem;
            }
        }
        
        @media (max-width: 768px) {
            .personal-title h1 {
                font-size: 2.2rem;
            }
            
            .flashcard-container {
                height: 420px;
            }
            
            .question, .answer {
                font-size: 1.6rem;
                line-height: 1.5;
            }
            
            .controls {
                gap: 15px;
            }
            
            .btn {
                padding: 12px 25px;
                min-width: 140px;
                font-size: 1rem;
            }
        }
        
        @media (max-width: 576px) {
            body {
                padding: 20px 15px;
            }
            
            .personal-title h1 {
                font-size: 1.9rem;
            }
            
            .flashcard-container {
                height: 400px;
            }
            
            .card-front, .card-back {
                padding: 35px 25px;
            }
            
            .question, .answer {
                font-size: 1.5rem;
                line-height: 1.4;
            }
            
            .controls {
                flex-direction: column;
                align-items: center;
            }
            
            .btn {
                width: 100%;
                max-width: 280px;
            }
            
            .instructions {
                padding: 15px;
            }
        }
    </style>
</head>
<body>
    <!-- JUDUL PRIBADI YANG DIMINTA -->
    <div class="personal-title">
        <h1>📇 Flashcard Evolusi Biologi Azalea Asya</h1>
        <p>Kartu belajar interaktif berdasarkan materi kelas 12</p>
    </div>
    
    <div class="instructions">
        <h3>📋 Cara Menggunakan:</h3>
        <p>1. <strong>Klik kartu</strong> atau tombol "Balik Kartu" untuk melihat jawaban</p>
        <p>2. Gunakan tombol <strong>"Sebelumnya"</strong> dan <strong>"Selanjutnya"</strong> untuk berpindah kartu</p>
        <p>3. Klik <strong>"Lihat Semua Kartu"</strong> untuk daftar lengkap dan memilih kartu tertentu</p>
    </div>
    
    <div class="card-counter" id="cardCounter">Kartu 1 dari 8</div>
    
    <!-- KONTAINER KARTU YANG SUDAH DIPERPANJANG -->
    <div class="flashcard-container">
        <div class="flashcard" id="flashcard">
            <div class="card-front">
                <div class="card-label">PERTANYAAN</div>
                <div class="question" id="question">Apa pengertian inti dari evolusi dalam biologi?</div>
                <div class="hint">Klik untuk membalik kartu</div>
            </div>
            <div class="card-back">
                <div class="card-label">JAWABAN</div>
                <div class="answer" id="answer">Evolusi adalah <strong>perubahan sifat-sifat terwariskan</strong> (morfologi/fisiologi) dalam suatu <strong>populasi</strong> dari generasi ke generasi, yang didorong oleh variasi, reproduksi, dan seleksi.</div>
                <div class="hint">Klik untuk kembali ke pertanyaan</div>
            </div>
        </div>
    </div>
    
    <div class="controls">
        <button class="btn btn-prev" id="prevBtn">⬅ Sebelumnya</button>
        <button class="btn btn-flip" id="flipBtn">🔄 Balik Kartu</button>
        <button class="btn btn-next" id="nextBtn">Selanjutnya ➡</button>
        <button class="btn btn-show-all" id="showAllBtn">📋 Lihat Semua Kartu</button>
    </div>
    
    <div class="card-list" id="cardList">
        <h3>Daftar Semua Kartu Flashcard</h3>
        <!-- Daftar kartu akan diisi oleh JavaScript -->
    </div>

    <script>
        // Data flashcard
        const flashcards = [
            {
                question: "Apa pengertian inti dari evolusi dalam biologi?",
                answer: "Evolusi adalah <strong>perubahan sifat-sifat terwariskan</strong> (morfologi/fisiologi) dalam suatu <strong>populasi</strong> dari generasi ke generasi, yang didorong oleh variasi, reproduksi, dan seleksi."
            },
            {
                question: "Apa dua mekanisme utama yang mendorong terjadinya evolusi?",
                answer: "1. <strong>Hanyutan genetik</strong>: perubahan acak pada frekuensi sifat dalam populasi kecil.<br>2. <strong>Seleksi alam</strong>: proses di mana sifat yang menguntungkan untuk bertahan hidup dan bereproduksi menjadi lebih umum dalam populasi."
            },
            {
                question: "Apa saja faktor yang dapat mengganggu keseimbangan frekuensi gen menurut Hukum Hardy-Weinberg?",
                answer: "Perkawinan tak acak, migrasi (arus gen), hanyutan genetik, seleksi alam, mutasi, serta rekombinasi dan seleksi."
            },
            {
                question: "Apa faktor penentu utama terbentuknya spesies baru?",
                answer: "<strong>Isolasi</strong>, yang mencegah perkawinan antarspesies. Dibagi menjadi:<br>- <strong>Isolasi Geografi</strong>: dipisahkan oleh bentang alam (gunung, laut).<br>- <strong>Isolasi Reproduksi</strong>: isolasi ekologi, musim, tingkah laku, mekanik, dan gamet."
            },
            {
                question: "Apa yang dapat dipelajari dari contoh evolusi ngengat Biston betularia di Inggris saat Revolusi Industri?",
                answer: "Evolusi: 1) Terjadi pada tingkat <strong>populasi</strong>, bukan individu, 2) Memerlukan variasi genetik sebagai <strong>'bahan mentah'</strong>, 3) Bersifat <strong>selektif</strong>, diarahkan oleh faktor lingkungan."
            },
            {
                question: "Apa perbedaan utama antara teori evolusi Lamarck dan Darwin?",
                answer: "<strong>Lamarck</strong>: Sifat yang didapat selama hidup dapat diwariskan (use and disuse).<br><strong>Darwin</strong>: Seleksi alam bekerja pada variasi yang sudah ada; individu dengan sifat lebih adaptif akan bertahan dan bereproduksi."
            },
            {
                question: "Apa itu 'homologi organ tubuh' dan bagaimana hal itu menjadi petunjuk evolusi?",
                answer: "Homologi organ adalah struktur dasar yang sama pada organisme berbeda (contoh: tangan manusia, sayap burung, kaki depan kuda), yang menunjukkan <strong>nenek moyang bersama</strong> meskipun fungsinya sekarang berbeda."
            },
            {
                question: "Sebutkan 3 dari 5 prinsip penting evolusi yang disebutkan dalam materi!",
                answer: "1. Laju evolusi bervariasi.<br>2. Spesies baru berasal dari bentuk sederhana.<br>3. Evolusi bisa regresif (kompleks → sederhana).<br>4. Evolusi terjadi dalam populasi.<br>5. Evolusi tidak selalu dari sederhana ke kompleks."
            }
        ];

        // Variabel state
        let currentCardIndex = 0;
        const flashcardElement = document.getElementById('flashcard');
        const questionElement = document.getElementById('question');
        const answerElement = document.getElementById('answer');
        const cardCounterElement = document.getElementById('cardCounter');
        const cardListElement = document.getElementById('cardList');
        const flipBtn = document.getElementById('flipBtn');
        const prevBtn = document.getElementById('prevBtn');
        const nextBtn = document.getElementById('nextBtn');
        const showAllBtn = document.getElementById('showAllBtn');

        // Fungsi untuk memperbarui tampilan kartu
        function updateCard() {
            questionElement.innerHTML = flashcards[currentCardIndex].question;
            answerElement.innerHTML = flashcards[currentCardIndex].answer;
            cardCounterElement.textContent = `Kartu ${currentCardIndex + 1} dari ${flashcards.length}`;
            
            // Reset kartu ke sisi depan
            flashcardElement.classList.remove('flipped');
            
            // Update state tombol
            prevBtn.disabled = currentCardIndex === 0;
            prevBtn.style.opacity = currentCardIndex === 0 ? '0.5' : '1';
            
            nextBtn.disabled = currentCardIndex === flashcards.length - 1;
            nextBtn.style.opacity = currentCardIndex === flashcards.length - 1 ? '0.5' : '1';
        }

        // Fungsi untuk membalik kartu
        function flipCard() {
            flashcardElement.classList.toggle('flipped');
        }

        // Fungsi untuk menampilkan daftar semua kartu
        function showAllCards() {
            if (cardListElement.style.display === 'block') {
                cardListElement.style.display = 'none';
                showAllBtn.textContent = '📋 Lihat Semua Kartu';
            } else {
                cardListElement.style.display = 'block';
                showAllBtn.textContent = '✖️ Tutup Daftar';
                renderCardList();
            }
        }

        // Fungsi untuk merender daftar kartu
        function renderCardList() {
            cardListElement.innerHTML = '<h3>Daftar Semua Kartu Flashcard</h3>';
            
            flashcards.forEach((card, index) => {
                const cardItem = document.createElement('div');
                cardItem.className = 'card-item';
                cardItem.innerHTML = `
                    <h4>Kartu ${index + 1}: ${card.question.substring(0, 70)}...</h4>
                    <p>${card.answer.replace(/<[^>]*>/g, '').substring(0, 120)}...</p>
                `;
                
                cardItem.addEventListener('click', () => {
                    currentCardIndex = index;
                    updateCard();
                    cardListElement.style.display = 'none';
                    showAllBtn.textContent = '📋 Lihat Semua Kartu';
                });
                
                cardListElement.appendChild(cardItem);
            });
        }

        // Event Listeners
        flashcardElement.addEventListener('click', flipCard);
        flipBtn.addEventListener('click', flipCard);
        
        prevBtn.addEventListener('click', () => {
            if (currentCardIndex > 0) {
                currentCardIndex--;
                updateCard();
            }
        });
        
        nextBtn.addEventListener('click', () => {
            if (currentCardIndex < flashcards.length - 1) {
                currentCardIndex++;
                updateCard();
            }
        });
        
        showAllBtn.addEventListener('click', showAllCards);

        // Navigasi dengan keyboard
        document.addEventListener('keydown', (event) => {
            if (event.key === 'ArrowLeft' && currentCardIndex > 0) {
                currentCardIndex--;
                updateCard();
            } else if (event.key === 'ArrowRight' && currentCardIndex < flashcards.length - 1) {
                currentCardIndex++;
                updateCard();
            } else if (event.key === ' ' || event.key === 'Enter') {
                flipCard();
                event.preventDefault();
            } else if (event.key === 'Escape' && cardListElement.style.display === 'block') {
                cardListElement.style.display = 'none';
                showAllBtn.textContent = '📋 Lihat Semua Kartu';
            }
        });

        // Inisialisasi
        updateCard();
        renderCardList();
    </script>
</body>
</html>