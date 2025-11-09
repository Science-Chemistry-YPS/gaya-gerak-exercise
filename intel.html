<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Petualangan Gerak & Gaya</title>
    <!-- Memuat Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Menggunakan font Inter -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;900&display=swap" rel="stylesheet">
    <style>
        /* Mengatur font default ke Inter */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #0f172a; /* bg-slate-900 */
            color: #f1f5f9; /* text-slate-100 */
            /* Mencegah seleksi teks yang mengganggu */
            user-select: none;
        }

        /* Gradient untuk judul */
        .game-title {
            background-image: linear-gradient(to right, #fde047, #f472b6, #60a5fa);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        /* Tombol kotak pertanyaan */
        .question-box {
            transition: all 0.3s ease;
            cursor: pointer;
            border-radius: 0.75rem; /* rounded-xl */
            font-weight: 900; /* font-black */
            font-size: 1.875rem; /* text-3xl */
            display: flex;
            justify-content: center;
            align-items: center;
            aspect-ratio: 1 / 1; /* Membuat kotak tetap persegi */
            color: #ffffff;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.4);
        }
        .question-box:hover {
            transform: scale(1.05) rotate(2deg);
            box-shadow: 0 10px 20px rgba(0,0,0,0.3);
        }
        .question-box.answered {
            cursor: not-allowed;
            opacity: 0.7;
            transform: scale(0.95);
        }

        /* Warna kotak berdasarkan poin */
        .points-5 { background-color: #22c55e; } /* green-500 */
        .points-10 { background-color: #3b82f6; } /* blue-500 */
        .points-15 { background-color: #eab308; } /* yellow-500 */
        .points-20 { background-color: #ec4899; } /* pink-500 */
        
        /* Status jawaban di kotak */
        .answered-true {
            background-color: #16a34a; /* green-600 */
            font-size: 1.25rem; /* text-xl */
            line-height: 1.5rem;
            text-shadow: none;
        }
        .answered-false {
            background-color: #dc2626; /* red-600 */
            font-size: 1.25rem; /* text-xl */
            line-height: 1.5rem;
            text-shadow: none;
        }

        /* Papan Skor */
        .score-card {
            transition: all 0.3s ease;
            border: 4px solid transparent;
        }
        .score-card.active-turn {
            transform: scale(1.05);
            border-color: #fde047; /* yellow-300 */
            box-shadow: 0 0 20px #fde047;
        }
        
        /* Modal (Popup) */
        .modal {
            display: none; /* Sembunyi secara default */
            position: fixed;
            z-index: 50;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0, 0, 0, 0.7);
            /* Efek backdrop blur */
            backdrop-filter: blur(8px);
            -webkit-backdrop-filter: blur(8px);
            
            /* Tengahkan modal */
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        /* Konten Modal */
        .modal-content {
            position: relative;
            background-color: #1e293b; /* bg-slate-800 */
            border-radius: 0.75rem; /* rounded-xl */
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
            max-width: 90%;
            width: 700px;
            /* Tambahkan max-height untuk layar kecil */
            max-height: 90vh;
            display: flex;
            flex-direction: column;
        }
        
        .modal-body {
            overflow-y: auto; /* Buat isi modal bisa di-scroll jika perlu */
        }
        
        /* Tombol Pilihan Jawaban */
        .option-button {
            transition: all 0.2s ease;
            border: 2px solid #334155; /* border-slate-700 */
        }
        .option-button:hover {
            background-color: #334155; /* hover:bg-slate-700 */
            transform: translateY(-2px);
        }
        .option-button:disabled {
            opacity: 0.5;
            cursor: not-allowed;
        }
        
        /* Umpan balik jawaban */
        #feedback-text {
            display: none; /* Sembunyi sampai ada jawaban */
        }
        #feedback-text.correct {
            display: block;
            color: #22c55e; /* text-green-500 */
        }
        #feedback-text.incorrect {
            display: block;
            color: #ef4444; /* text-red-500 */
        }
        
        /* Kontainer Penjelasan (Bukan AI lagi) */
        #explanation-container {
            display: none; /* Sembunyi default */
            border-top: 2px solid #334155; /* border-t-slate-700 */
            background-color: rgba(0,0,0,0.2);
        }
        
        /* Modal Selesai (Konfeti) */
        #confetti-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            overflow: hidden;
            z-index: 100;
        }
        .confetti {
            position: absolute;
            width: 10px;
            height: 10px;
            background-color: #fde047;
            opacity: 0;
            animation: confetti-fall 5s ease-out forwards;
        }
        
        @keyframes confetti-fall {
            0% {
                transform: translateY(-100vh) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateY(100vh) rotate(720deg);
                opacity: 0;
            }
        }
        
        /* Konfeti Mini (Saat Jawaban Benar) */
        #mini-confetti-container {
            position: fixed;
            top: 50%;
            left: 50%;
            width: 1px;
            height: 1px;
            pointer-events: none;
            z-index: 200;
        }
        
        .mini-confetti {
            position: absolute;
            width: 8px;
            height: 8px;
            background-color: #fde047;
            opacity: 0;
            /* Animasi baru yang lebih singkat */
            animation: confetti-burst-short 1.5s ease-out forwards;
        }
        
        @keyframes confetti-burst-short {
            0% {
                transform: translate(0, 0) scale(0) rotate(0deg);
                opacity: 1;
            }
            100% {
                /* Menyebar acak dan memudar */
                transform: translate(var(--x-end), var(--y-end)) scale(1) rotate(720deg);
                opacity: 0;
            }
        }

    </style>
</head>
<body class="p-4 md:p-8">

    <!-- --- Wadah untuk Konfeti Mini --- -->
    <div id="mini-confetti-container"></div>

    <!-- --- Wadah untuk Konfeti Akhir --- -->
    <div id="confetti-container"></div>

    <!-- --- Layar Setup Tim --- -->
    <div id="setup-screen" class="max-w-md mx-auto text-center p-8 bg-slate-800 rounded-xl shadow-2xl">
        <!-- Tulisan Selamat Datang -->
        <p class="text-xl font-semibold text-yellow-300 uppercase mb-2">
            Selamat Datang di Kelas IPA <br> Bu Wiwik
        </p>
        <h1 class="text-3xl font-extrabold game-title mb-6">
            Pilih Tim!
        </h1>
        
        <!-- Input API Key SUDAH DIHAPUS -->

        <p class="my-6 text-slate-300">Pilih jumlah tim yang akan bermain:</p>
        <div class="flex justify-center gap-4">
            <button onclick="startGame(2)" class="px-6 py-3 bg-blue-600 hover:bg-blue-700 rounded-lg text-white font-bold text-lg shadow-lg transition duration-200">2 Tim</button>
            <button onclick="startGame(3)" class="px-6 py-3 bg-green-600 hover:bg-green-700 rounded-lg text-white font-bold text-lg shadow-lg transition duration-200">3 Tim</button>
            <button onclick="startGame(4)" class="px-6 py-3 bg-pink-600 hover:bg-pink-700 rounded-lg text-white font-bold text-lg shadow-lg transition duration-200">4 Tim</button>
        </div>
    </div>

    <!-- --- Konten Game (Sembunyi Awalnya) --- -->
    <div id="game-container" class="hidden">
        <!-- Header -->
        <header class="text-center mb-6">
            <h1 class="text-4xl md:text-6xl font-black game-title mt-2">
                Petualangan Gerak & Gaya
            </h1>
        </header>

        <!-- Papan Skor Tim -->
        <div id="scoreboard-container" class="flex flex-wrap justify-center gap-4 mb-8">
            <!-- Papan skor akan dimasukkan oleh JS di sini -->
        </div>

        <!-- Papan Permainan -->
        <main class="max-w-5xl mx-auto grid grid-cols-5 gap-3 md:gap-5">
            <!-- Kategori (hanya visual, tidak bisa diklik) -->
            <div class="question-box bg-slate-700 !text-sm md:!text-lg !font-bold !text-slate-300 p-2 opacity-100">Konsep Gerak</div>
            <div class="question-box bg-slate-700 !text-sm md:!text-lg !font-bold !text-slate-300 p-2 opacity-100">Hukum Newton</div>
            <div class="question-box bg-slate-700 !text-sm md:!text-lg !font-bold !text-slate-300 p-2 opacity-100">Gaya Gesek</div>
            <div class="question-box bg-slate-700 !text-sm md:!text-lg !font-bold !text-slate-300 p-2 opacity-100">Kecepatan & Percepatan</div>
            <div class="question-box bg-slate-700 !text-sm md:!text-lg !font-bold !text-slate-300 p-2 opacity-100">Analisis (HOTS)</div>

            <!-- Pertanyaan akan dimasukkan oleh JS di sini -->
        </main>
        
        <!-- Tombol Reset -->
        <footer class="text-center mt-8">
            <button id="reset-button" onclick="showSetup()" class="px-6 py-2 bg-red-600 hover:bg-red-700 rounded-lg text-white font-bold shadow-lg transition duration-200">
                Mulai Ulang
            </button>
        </footer>
    </div>
    
    <!-- --- Template Papan Skor (untuk di-clone JS) --- -->
    <template id="score-card-template">
        <div class="score-card w-36 md:w-48 p-4 bg-slate-800 rounded-lg shadow-lg text-center">
            <h2 class="text-lg md:text-xl font-bold text-yellow-300 uppercase">Tim 1</h2>
            <p class="text-3xl md:text-5xl font-black text-white">0</p>
        </div>
    </template>

    <!-- --- Modal Pertanyaan --- -->
    <div id="question-modal" class="modal hidden">
        <div class="modal-content">
            <!-- Header Modal -->
            <div class="p-5 border-b border-slate-700">
                <h2 id="modal-points" class="text-3xl font-black text-center"></h2>
            </div>
            
            <!-- Body Modal -->
            <div class="modal-body p-6">
                <!-- Kontainer untuk Gambar (jika ada) -->
                <div id="modal-image-container" class="mb-4 flex justify-center">
                    <!-- SVG atau Gambar akan masuk di sini -->
                </div>
                
                <!-- Teks Pertanyaan -->
                <p id="modal-question-text" class="text-lg md:text-xl text-slate-100 mb-6" style="line-height: 1.6;"></p>
                
                <!-- Pilihan Jawaban -->
                <div id="modal-options-container" class="grid grid-cols-1 md:grid-cols-2 gap-3">
                    <!-- Tombol pilihan akan dimasukkan JS di sini -->
                </div>
                
                <!-- Umpan Balik Jawaban -->
                <div class="mt-6 text-center">
                    <p id="feedback-text" class="text-2xl font-bold"></p>
                </div>
                
                <!-- Penjelasan (bukan AI) -->
                <div id="explanation-container" class="mt-6 p-4 rounded-lg">
                    <h3 class="text-lg font-bold text-blue-400 mb-2 flex items-center">
                        <span class="mr-2">💡</span> Penjelasan
                    </h3>
                    <div id="explanation-text" class="text-sm text-slate-300 overflow-y-auto max-h-32" style="line-height: 1.6;">
                        <!-- Penjelasan akan muncul di sini -->
                    </div>
                </div>
            </div>
            
            <!-- Footer Modal -->
            <div class="p-5 border-t border-slate-700 flex justify-end items-center">
                <!-- Tombol Penjelasan AI SUDAH DIHAPUS -->
                
                <!-- Tombol Tutup -->
                <button id="close-modal-button" onclick="closeModal()" class="px-5 py-2 bg-slate-600 hover:bg-slate-700 rounded-lg text-white font-semibold transition duration-200">
                    Tutup
                </button>
            </div>
        </div>
    </div>
    
    <!-- --- Modal Selesai --- -->
    <div id="finish-modal" class="modal hidden">
        <div class="modal-content text-center p-8 md:p-12">
            <h2 class="text-4xl font-black game-title mb-4">Permainan Selesai!</h2>
            <p id="winner-text" class="text-2xl text-slate-200 mb-6"></p>
            <div id="final-scores-container" class="text-lg text-slate-300 space-y-2 mb-8">
                <!-- Skor akhir tim akan muncul di sini -->
            </div>
            <button onclick="showSetup()" class="px-8 py-3 bg-blue-600 hover:bg-blue-700 rounded-lg text-white font-bold text-lg shadow-lg transition duration-200">
                Main Lagi
            </button>
        </div>
    </div>


    <script>
        // -----------------------------------------------------------------
        // --- DATABASE PERTANYAAN (65% PERHITUNGAN) -----------------------
        // -----------------------------------------------------------------
        // Kategori: [0]Konsep Gerak, [1]Hukum Newton, [2]Gaya Gesek, [3]Kecepatan, [4]Analisis
        
        const questions = [
            // --- POIN 5 (13 Soal Hitungan Total) ---
            { 
                points: 5, category: 0, // HITUNGAN (1)
                question: "Adi berjalan 30 meter ke timur, lalu 10 meter ke barat. Berapa <span class='text-yellow-300'>jarak tempuh</span> Adi?",
                options: ["40 m", "20 m", "30 m", "10 m"],
                answer: "40 m",
                explanation: "<b>Jarak tempuh</b> adalah total lintasan yang dijalani. Jarak = 30 m + 10 m = 40 m. (Jangan keliru dengan <i>perpindahan</i>, yang hasilnya 20 m)."
            },
            { 
                points: 5, category: 1, // HITUNGAN (2)
                question: "Sebuah benda memiliki massa 2 kg. Berapa <span class='text-pink-300'>berat benda</span> tersebut di Bumi? (Gunakan g = 10 m/s²)",
                options: ["20 N", "2 N", "10 N", "5 N"],
                answer: "20 N",
                explanation: "Berat (W) adalah massa (m) dikali percepatan gravitasi (g). Rumus: W = m x g. Maka, W = 2 kg x 10 m/s² = 20 N."
            },
            { 
                points: 5, category: 2, // KONSEP
                question: "Berikut ini adalah cara untuk <span class='text-blue-300'>memperbesar</span> gaya gesek, kecuali...",
                options: ["Menghaluskan permukaan", "Membuat alur pada ban", "Memberi paku pada sepatu pendaki", "Memperkasar permukaan"],
                answer: "Menghaluskan permukaan",
                explanation: "Gaya gesek dipengaruhi oleh kekasaran permukaan. Menghaluskan permukaan (seperti memberi pelumas) akan <b>memperkecil</b> gaya gesek, bukan memperbesarnya."
            },
            { 
                points: 5, category: 3, // HITUNGAN (3)
                question: "Sebuah mobil menempuh jarak 100 meter dalam waktu 5 detik. Berapa <span class='text-green-300'>kelajuan rata-rata</span> mobil itu?",
                options: ["20 m/s", "500 m/s", "25 m/s", "5 m/s"],
                answer: "20 m/s",
                explanation: "Kelajuan (v) adalah jarak (s) dibagi waktu (t). Rumus: v = s / t. Maka, v = 100 m / 5 s = 20 m/s."
            },
            { 
                points: 5, category: 4, // HITUNGAN (4)
                question: "Sebuah gaya 10 N bekerja pada benda bermassa 5 kg. Berapa <span class='text-red-300'>percepatan</span> benda tersebut? (Abaikan gesekan)",
                options: ["2 m/s²", "50 m/s²", "0.5 m/s²", "5 m/s²"],
                answer: "2 m/s²",
                explanation: "Gunakan Hukum II Newton (F = m.a). Untuk mencari percepatan (a), rumusnya adalah a = F / m. Maka, a = 10 N / 5 kg = 2 m/s²."
            },
            
            // --- POIN 10 ---
            { 
                points: 10, category: 0, // KONSEP
                question: "Saat mobil yang melaju kencang tiba-tiba direm, penumpang di dalamnya akan <span class='text-yellow-300'>terdorong ke depan</span>. Peristiwa ini sesuai dengan...",
                options: ["Hukum I Newton", "Hukum II Newton", "Hukum III Newton", "Gaya Gesek"],
                answer: "Hukum I Newton",
                explanation: "Ini adalah contoh Hukum I Newton (Kelembaman). Tubuhmu awalnya sedang bergerak maju bersama mobil. Saat mobil direm, tubuhmu <b>cenderung mempertahankan gerak maju</b>-nya, sehingga kamu terdorong ke depan."
            },
            { 
                points: 10, category: 1, // HITUNGAN (5)
                question: "Gaya 30 N menghasilkan percepatan 5 m/s² pada sebuah balok. Berapa <span class='text-pink-300'>massa</span> balok tersebut?",
                options: ["6 kg", "150 kg", "0.16 kg", "25 kg"],
                answer: "6 kg",
                explanation: "Gunakan Hukum II Newton (F = m.a). Untuk mencari massa (m), rumusnya adalah m = F / a. Maka, m = 30 N / 5 m/s² = 6 kg."
            },
            { 
                points: 10, category: 2, // HITUNGAN (6)
                question: "Dua gaya bekerja pada balok: F1 = 15 N ke kanan dan F2 = 5 N ke kiri. Berapa <span class='text-blue-300'>Resultan Gaya</span> (ΣF) yang bekerja pada balok?",
                options: ["10 N ke kanan", "20 N ke kanan", "10 N ke kiri", "5 N ke kanan"],
                answer: "10 N ke kanan",
                explanation: "Resultan gaya adalah penjumlahan semua gaya. Jika arahnya berlawanan, kita kurangi. (Arah kanan positif, kiri negatif). ΣF = (+15 N) + (-5 N) = 10 N. Hasilnya positif, artinya 10 N ke kanan."
            },
            { 
                points: 10, category: 3, // HITUNGAN (7)
                question: "Sebuah motor bergerak dari 10 m/s menjadi 30 m/s dalam waktu 4 detik. Berapa <span class='text-green-300'>percepatan</span> motor tersebut?",
                options: ["5 m/s²", "10 m/s²", "7.5 m/s²", "20 m/s²"],
                answer: "5 m/s²",
                explanation: "Percepatan (a) = (Kecepatan Akhir - Kecepatan Awal) / waktu. Maka, a = (30 m/s - 10 m/s) / 4 s = 20 m/s / 4 s = 5 m/s²."
            },
            { 
                points: 10, category: 4, // KONSEP
                question: "Saat kamu memukul dinding (aksi), dinding akan memberikan gaya yang <span class='text-red-300'>sama besar dan berlawanan arah</span> ke tanganmu (reaksi), sehingga tanganmu terasa sakit. Ini adalah penerapan...",
                options: ["Hukum III Newton", "Hukum I Newton", "Hukum II Newton", "Gaya Kelembaman"],
                answer: "Hukum III Newton",
                explanation: "Ini adalah contoh Hukum III Newton (Aksi-Reaksi). Gayanya <b>selalu berpasangan</b>, terjadi pada dua benda berbeda, besarnya sama, dan arahnya berlawanan. Aksi: Tangan memukul dinding. Reaksi: Dinding memukul tangan."
            },
            
            // --- POIN 15 ---
            { 
                points: 15, category: 0, // HITUNGAN (8)
                question: "Mobil A bergerak ke timur (60 km/jam) berpapasan dengan mobil B ke barat (40 km/jam). Berapa <span class='text-yellow-300'>kelajuan mobil A menurut mobil B</span>?",
                options: ["100 km/jam", "20 km/jam", "60 km/jam", "40 km/jam"],
                answer: "100 km/jam",
                explanation: "Ini adalah kelajuan relatif. Karena keduanya bergerak berlawanan arah, kelajuan relatifnya dijumlahkan. Menurut B, A bergerak seolah-olah dengan kelajuan 60 km/jam + 40 km/jam = 100 km/jam."
            },
            { 
                points: 15, category: 1, // HITUNGAN (9)
                question: "Balok 5 kg didorong dengan gaya 20 N. Ternyata percepatannya hanya 3 m/s². Berapa besar <span class='text-pink-300'>gaya gesek kinetis</span> (f_k) yang bekerja?",
                options: ["5 N", "15 N", "20 N", "3 N"],
                answer: "5 N",
                explanation: "Gaya bersih (ΣF) = m x a = 5 kg x 3 m/s² = 15 N. Gaya bersih juga sama dengan Gaya Dorong - Gaya Gesek. Jadi, 15 N = 20 N - f_k. Maka f_k = 20 N - 15 N = 5 N."
            },
            { 
                points: 15, category: 2, // KONSEP
                question: "Gaya gesek statis maksimum antara balok 10 kg dan lantai adalah 30 N. Jika balok ditarik dengan gaya horizontal 25 N, apa yang terjadi pada balok?",
                options: ["Balok tetap diam", "Balok bergerak dengan percepatan", "Balok bergerak dengan kecepatan tetap", "Gaya gesek menjadi 25 N dan balok bergerak"],
                answer: "Balok tetap diam",
                explanation: "Gaya gesek statis maksimum adalah 'batas' agar benda bisa bergerak, yaitu 30 N. Karena gaya tarik (25 N) <b>lebih kecil</b> dari batas maksimum (30 N), gaya tarik tersebut belum cukup untuk menggerakkan balok. Balok akan tetap diam."
            },
            { 
                points: 15, category: 3, // KONSEP
                question: "Sebuah batu dilempar vertikal ke atas. Apa yang terjadi pada <span class='text-green-300'>kecepatan dan percepatan</span> batu saat berada di titik puncak?",
                options: ["Kecepatan nol, percepatan tetap (gravitasi)", "Kecepatan nol, percepatan nol", "Kecepatan berkurang, percepatan berkurang", "Kecepatan tetap, percepatan nol"],
                answer: "Kecepatan nol, percepatan tetap (gravitasi)",
                explanation: "Di titik puncak, batu <b>berhenti sesaat</b>, jadi kecepatannya nol. Namun, gravitasi (gaya tarik bumi) <b>selalu bekerja</b> padanya. Jadi, percepatannya tetap (percepatan gravitasi, g ≈ 9.8 m/s² ke bawah)."
            },
            { 
                points: 15, category: 4, // HITUNGAN (10)
                question: "Gaya F pada benda m menghasilkan percepatan 4 m/s². Jika gaya diperbesar menjadi 3F dan massa benda menjadi 2m, berapa <span class='text-red-300'>percepatan baru</span>?",
                options: ["6 m/s²", "4 m/s²", "8 m/s²", "2 m/s²"],
                answer: "6 m/s²",
                explanation: "Awal: a = F/m = 4. Baru: a_baru = (3F) / (2m) = (3/2) x (F/m). Karena (F/m) = 4, maka a_baru = (3/2) x 4 = 12 / 2 = 6 m/s²."
            },

            // --- POIN 20 (HOTS) ---
            { 
                points: 20, category: 0, // HITUNGAN (11)
                question: "Sebuah <span class='text-yellow-300'>pita ticker-timer</span> memiliki frekuensi 50 Hz. Jarak antara dua titik (satu ketukan) adalah 2 cm. Berapa kelajuan benda?",
                options: ["100 cm/s (atau 1 m/s)", "0.02 cm/s", "25 cm/s", "50 cm/s"],
                answer: "100 cm/s (atau 1 m/s)",
                explanation: "Frekuensi 50 Hz artinya 50 ketukan per detik. Waktu antar ketukan (Periode, T) = 1/f = 1/50 detik = 0,02 detik. Kelajuan (v) = jarak / waktu = 2 cm / 0,02 s = 100 cm/s atau 1 m/s."
            },
            { 
                points: 20, category: 1, // HITUNGAN (12)
                question: "Seseorang bermassa 60 kg berada di lift yang bergerak <span class='text-pink-300'>ke bawah</span> dengan percepatan 2 m/s². Berapa berat semu orang itu? (g=10 m/s²)",
                options: ["480 N", "720 N", "600 N", "120 N"],
                answer: "480 N",
                explanation: "Berat Asli (W) = m.g = 600 N. Karena lift ke bawah dipercepat, rumusnya: W - N = m.a. Maka Gaya Normal (N) = W - m.a. N = 600 N - (60 kg x 2 m/s²) = 600 N - 120 N = 480 N. Timbangan akan menunjukkan 480 N."
            },
            { 
                points: 20, category: 2, // KONSEP
                question: "Mengapa setetes air hujan yang jatuh dari awan tinggi tidak menghantam kita secepat peluru, meskipun dipercepat oleh gravitasi?",
                options: ["Karena ada gaya gesek udara (hambatan udara)", "Karena massa air kecil", "Karena awan tidak terlalu tinggi", "Karena air hujan bergerak GLB"],
                answer: "Karena ada gaya gesek udara (hambatan udara)",
                explanation: "Awalnya air hujan dipercepat. Tapi semakin cepat ia jatuh, gaya gesek udara semakin besar. Akhirnya, gaya gesek udara akan sama besar dengan gaya gravitasi, sehingga percepatannya jadi nol. Air hujan lalu jatuh dengan 'kecepatan terminal' (tetap) yang jauh lebih lambat."
            },
            { 
                points: 20, category: 3, // KONSEP
                question: "Dua benda identik, A dan B, didorong dengan gaya yang sama (F) di lantai licin. Massa B tiga kali massa A. Bagaimana perbandingan percepatan A (a_A) dan B (a_B)?",
                options: ["a_A = 3 kali a_B", "a_B = 3 kali a_A", "a_A = a_B", "a_A = 1/3 kali a_B"],
                answer: "a_A = 3 kali a_B",
                explanation: "Dari a = F/m, percepatan (a) berbanding terbalik dengan massa (m). Jika gayanya sama, benda yang massanya lebih kecil (A) akan mengalami percepatan yang lebih besar. Karena m_B = 3 m_A, maka a_A = 3 a_B."
            },
            { 
                points: 20, category: 4, // HITUNGAN (13)
                // Mengubah grafik dan soal
                imageSVG: `
                    <svg width="250" height="200" viewBox="0 0 100 80" xmlns="http://www.w3.org/2000/svg" class="bg-white rounded-lg p-2 mx-auto">
                        <!-- Sumbu Y (v) -->
                        <line x1="10" y1="10" x2="10" y2="70" stroke="black" stroke-width="1"/>
                        <text x="5" y="15" font-size="8" fill="black">v (m/s)</text>
                        <text x="5" y="30" font-size="8" fill="black">10</text>
                        <line x1="10" y1="30" x2="15" y2="30" stroke="grey" stroke-width="0.5"/>
                        <!-- Sumbu X (t) -->
                        <line x1="10" y1="70" x2="90" y2="70" stroke="black" stroke-width="1"/>
                        <text x="88" y="75" font-size="8" fill="black">t (s)</text>
                        <text x="8" y="75" font-size="8" fill="black">0</text>
                        <text x="58" y="75" font-size="8" fill="black">6</text>
                        <line x1="60" y1="70" x2="60" y2="65" stroke="grey" stroke-width="0.5"/>
                        <!-- Garis Grafik (Bentuk Trapesium) -->
                        <line x1="10" y1="30" x2="60" y2="30" stroke="red" stroke-width="2"/>
                        <line x1="10" y1="70" x2="10" y2="30" stroke="red" stroke-width="2"/>
                        <line x1="60" y1="70" x2="60" y2="30" stroke="red" stroke-width="2"/>
                    </svg>
                `,
                question: "Grafik (v-t) di atas menunjukkan gerak sebuah benda. Berapa <span class='text-red-300'>jarak tempuh</span> benda selama 6 detik?",
                options: ["60 meter", "10 meter", "1.67 meter", "600 meter"],
                answer: "60 meter",
                explanation: "Pada grafik v-t, <b>Jarak = Luas di bawah grafik</b>. Grafiknya berbentuk persegi panjang. Luas = panjang x lebar = 6 detik x 10 m/s = 60 meter."
            }
        ];
        
        // Mengacak urutan soal dalam setiap kategori poin
        function shuffleQuestions() {
            const shuffled = [];
            const pointsGroups = [5, 10, 15, 20];
            const categories = 5;
            
            pointsGroups.forEach(points => {
                const questionsByPoints = questions.filter(q => q.points === points);
                // Pastikan ada 5 soal untuk setiap level poin
                if (questionsByPoints.length === categories) {
                    for (let i = 0; i < categories; i++) {
                        const q = questionsByPoints.find(q => q.category === i);
                        shuffled.push(q);
                    }
                }
            });
            return shuffled;
        }
        
        let activeQuestions = [];
        let teamScores = [];
        let currentTeam = 0;
        let questionsAnswered = 0;
        let currentQuestion = null;
        let currentQuestionElement = null;
        
        // Variabel Audio
        let audioContext;
        
        // --- DOM Elements ---
        const modal = document.getElementById('question-modal');
        const modalPoints = document.getElementById('modal-points');
        const modalImageContainer = document.getElementById('modal-image-container');
        const modalQuestionText = document.getElementById('modal-question-text');
        const modalOptionsContainer = document.getElementById('modal-options-container');
        const feedbackText = document.getElementById('feedback-text');
        const closeModalButton = document.getElementById('close-modal-button');
        // Elemen AI diganti menjadi elemen penjelasan umum
        const explanationContainer = document.getElementById('explanation-container');
        const explanationText = document.getElementById('explanation-text');
        
        const setupScreen = document.getElementById('setup-screen');
        const gameContainer = document.getElementById('game-container');
        const scoreboardContainer = document.getElementById('scoreboard-container');
        const board = document.querySelector('main.grid');
        const finishModal = document.getElementById('finish-modal');
        const winnerText = document.getElementById('winner-text');
        const finalScoresContainer = document.getElementById('final-scores-container');

        // -----------------------------------------------------------------
        // --- FUNGSI AUDIO (Baru) -----------------------------------------
        // -----------------------------------------------------------------
        
        function initAudio() {
            // Coba buat AudioContext baru. Diperlukan interaksi pengguna untuk memulai.
            try {
                if (!audioContext) {
                    audioContext = new (window.AudioContext || window.webkitAudioContext)();
                }
            } catch (e) {
                console.error("Web Audio API tidak didukung di browser ini.");
            }
        }
        
        function playSuccessSound() {
            if (!audioContext) return;
            // Membuat suara "ding" (nada C5 lalu E5)
            const oscillator = audioContext.createOscillator();
            const gainNode = audioContext.createGain();
            oscillator.connect(gainNode);
            gainNode.connect(audioContext.destination);
            
            oscillator.type = 'sine';
            gainNode.gain.setValueAtTime(0, audioContext.currentTime);
            gainNode.gain.linearRampToValueAtTime(0.5, audioContext.currentTime + 0.01);
            
            oscillator.frequency.setValueAtTime(523.25, audioContext.currentTime); // C5
            oscillator.frequency.linearRampToValueAtTime(659.25, audioContext.currentTime + 0.1); // E5
            
            gainNode.gain.exponentialRampToValueAtTime(0.00001, audioContext.currentTime + 0.3);
            
            oscillator.start(audioContext.currentTime);
            oscillator.stop(audioContext.currentTime + 0.3);
        }

        function playFailSound() {
            if (!audioContext) return;
            // Membuat suara "buzz" (nada G3 lalu F#3)
            const oscillator = audioContext.createOscillator();
            const gainNode = audioContext.createGain();
            oscillator.connect(gainNode);
            gainNode.connect(audioContext.destination);
            
            oscillator.type = 'triangle'; // Suara 'buzz' yang lebih lembut
            gainNode.gain.setValueAtTime(0, audioContext.currentTime);
            gainNode.gain.linearRampToValueAtTime(0.5, audioContext.currentTime + 0.01);
            
            oscillator.frequency.setValueAtTime(196.00, audioContext.currentTime); // G3
            oscillator.frequency.linearRampToValueAtTime(185.00, audioContext.currentTime + 0.1); // F#3
            
            gainNode.gain.exponentialRampToValueAtTime(0.00001, audioContext.currentTime + 0.4);
            
            oscillator.start(audioContext.currentTime);
            oscillator.stop(audioContext.currentTime + 0.4);
        }

        // -----------------------------------------------------------------
        // --- FUNGSI KONFETI ----------------------------------------------
        // -----------------------------------------------------------------

        function triggerMiniConfetti() {
            const container = document.getElementById('mini-confetti-container');
            const colors = ['#fde047', '#f472b6', '#60a5fa', '#22c55e', '#ffffff'];
            
            for (let i = 0; i < 30; i++) {
                const confetti = document.createElement('div');
                confetti.classList.add('mini-confetti');
                confetti.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                
                // Variabel CSS untuk animasi
                // Menyebar ke arah acak
                const xEnd = (Math.random() * 400 - 200) + 'px';
                const yEnd = (Math.random() * 400 - 200) + 'px';
                confetti.style.setProperty('--x-end', xEnd);
                confetti.style.setProperty('--y-end', yEnd);
                
                // Delay acak agar tidak meledak bersamaan
                confetti.style.animationDelay = Math.random() * 0.1 + 's';
                
                container.appendChild(confetti);
                
                // Hapus elemen setelah animasi selesai
                setTimeout(() => {
                    confetti.remove();
                }, 1500); // 1.5 detik (durasi animasi)
            }
        }
        
        function launchConfetti() {
            const container = document.getElementById('confetti-container');
            const colors = ['#fde047', '#f472b6', '#60a5fa', '#22c55e', '#ec4899', '#ffffff'];
            
            for (let i = 0; i < 100; i++) {
                const confetti = document.createElement('div');
                confetti.classList.add('confetti');
                confetti.style.left = Math.random() * 100 + 'vw';
                confetti.style.animationDelay = Math.random() * 3 + 's';
                confetti.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                // Ukuran acak
                const size = Math.random() * 5 + 5;
                confetti.style.width = size + 'px';
                confetti.style.height = size + 'px';
                
                container.appendChild(confetti);
                
                setTimeout(() => {
                    confetti.remove();
                }, 5000); // Hapus setelah 5 detik
            }
        }


        // -----------------------------------------------------------------
        // --- FUNGSI UTAMA PERMAINAN --------------------------------------
        // -----------------------------------------------------------------

        // Fungsi untuk menampilkan layar setup
        function showSetup() {
            setupScreen.style.display = 'block';
            gameContainer.style.display = 'none';
            finishModal.style.display = 'none';
            
            // Hapus papan skor lama dan kotak soal lama
            scoreboardContainer.innerHTML = '';
            board.innerHTML = `
                <div class="question-box bg-slate-700 !text-sm md:!text-lg !font-bold !text-slate-300 p-2 opacity-100">Konsep Gerak</div>
                <div class="question-box bg-slate-700 !text-sm md:!text-lg !font-bold !text-slate-300 p-2 opacity-100">Hukum Newton</div>
                <div class="question-box bg-slate-700 !text-sm md:!text-lg !font-bold !text-slate-300 p-2 opacity-100">Gaya Gesek</div>
                <div class="question-box bg-slate-700 !text-sm md:!text-lg !font-bold !text-slate-300 p-2 opacity-100">Kecepatan & Percepatan</div>
                <div class="question-box bg-slate-700 !text-sm md:!text-lg !font-bold !text-slate-300 p-2 opacity-100">Analisis (HOTS)</div>
            `;
            
            // Tutup juga modal pertanyaan jika terbuka
            if (modal) modal.style.display = 'none';
        }

        // Fungsi untuk memulai permainan
        function startGame(numTeams) {
            
            // Inisialisasi Audio (harus dipicu oleh interaksi pengguna)
            initAudio();
            
            teamScores = new Array(numTeams).fill(0);
            currentTeam = 0;
            questionsAnswered = 0;
            activeQuestions = shuffleQuestions();
            
            setupScreen.style.display = 'none';
            gameContainer.style.display = 'block';
            finishModal.style.display = 'none';
            
            // Buat Papan Skor
            scoreboardContainer.innerHTML = ''; // Kosongkan dulu
            const template = document.getElementById('score-card-template');
            for (let i = 0; i < numTeams; i++) {
                const clone = template.content.cloneNode(true);
                clone.querySelector('h2').textContent = `Tim ${i + 1}`;
                clone.querySelector('p').textContent = '0';
                clone.firstElementChild.dataset.teamId = i; // Simpan ID tim
                scoreboardContainer.appendChild(clone);
            }
            
            // Buat Papan Pertanyaan
            activeQuestions.forEach((q, index) => {
                const box = document.createElement('div');
                box.classList.add('question-box', `points-${q.points}`);
                box.textContent = q.points;
                box.dataset.index = index; // Simpan index soal
                box.onclick = () => openQuestion(q, box);
                board.appendChild(box);
            });
            
            updateTurnHighLight();
        }
        
        // Menyorot giliran tim
        function updateTurnHighLight() {
            document.querySelectorAll('.score-card').forEach((card, index) => {
                if (index === currentTeam) {
                    card.classList.add('active-turn');
                } else {
                    card.classList.remove('active-turn');
                }
            });
        }
        
        // Membuka modal pertanyaan
        function openQuestion(question, element) {
            if (element.classList.contains('answered')) return; // Jangan buka jika sudah dijawab
            
            currentQuestion = question;
            currentQuestionElement = element;
            
            // Reset modal
            modalPoints.textContent = `Soal ${question.points} Poin`;
            modalPoints.className = `text-3xl font-black text-center points-${question.points}`; // Ganti warna header
            modalQuestionText.innerHTML = question.question; // Pakai innerHTML agar span terbaca
            feedbackText.style.display = 'none';
            // Sembunyikan penjelasan
            explanationContainer.style.display = 'none';
            explanationText.innerHTML = ""; // Kosongkan penjelasan lama
            
            // Tampilkan gambar jika ada
            if (question.imageSVG) {
                modalImageContainer.innerHTML = question.imageSVG;
                modalImageContainer.style.display = 'flex';
            } else {
                modalImageContainer.innerHTML = '';
                modalImageContainer.style.display = 'none';
            }
            
            // Buat tombol pilihan
            modalOptionsContainer.innerHTML = '';
            question.options.forEach(option => {
                const button = document.createElement('button');
                button.classList.add('option-button', 'w-full', 'p-4', 'bg-slate-900', 'rounded-lg', 'text-slate-100', 'font-semibold', 'text-left');
                button.innerHTML = option; // Pakai innerHTML jika ada format khusus
                button.onclick = () => checkAnswer(option, button);
                modalOptionsContainer.appendChild(button);
            });
            
            // Tampilkan modal
            modal.style.display = 'flex';
        }
        
        // Menutup modal
        function closeModal() {
            modal.style.display = 'none';
            
            // Cek apakah permainan selesai
            if (questionsAnswered === activeQuestions.length) {
                showEndGame();
            }
        }
        
        // Memeriksa jawaban
        function checkAnswer(selectedOption) {
            const isCorrect = (selectedOption === currentQuestion.answer);
            
            // Matikan semua tombol pilihan
            modalOptionsContainer.querySelectorAll('button').forEach(btn => {
                btn.disabled = true;
                if (btn.innerHTML === currentQuestion.answer) {
                    btn.classList.add('!bg-green-600', '!border-green-500'); // Tampilkan jawaban benar
                } else if (btn.innerHTML === selectedOption) {
                    btn.classList.add('!bg-red-600', '!border-red-500'); // Tampilkan jawaban salah
                }
            });
            
            // Tampilkan umpan balik
            if (isCorrect) {
                feedbackText.innerHTML = "BENAR! 😊"; // Tambah emoji
                feedbackText.className = "text-2xl font-bold correct";
                updateScore(currentQuestion.points);
                playSuccessSound(); // Mainkan suara benar
                triggerMiniConfetti(); // Tampilkan konfeti mini
                
                // Ubah teks kotak di papan
                currentQuestionElement.innerHTML = "Benar";
                currentQuestionElement.classList.add('answered-true');
            } else {
                feedbackText.innerHTML = "NICE TRY! 😢"; // Tambah emoji
                feedbackText.className = "text-2xl font-bold incorrect";
                updateScore(-currentQuestion.points); // Kurangi poin (minus)
                playFailSound(); // Mainkan suara salah
                
                // Ubah teks kotak di papan
                currentQuestionElement.innerHTML = "Nice try";
                currentQuestionElement.classList.add('answered-false');
            }
            
            // Tandai soal sudah dijawab
            currentQuestionElement.classList.add('answered');
            questionsAnswered++;
            
            // Tampilkan penjelasan (menggantikan tombol AI)
            explanationText.innerHTML = currentQuestion.explanation; // Ambil dari database
            explanationContainer.style.display = 'block'; // Tampilkan
            
            // Ganti giliran tim
            currentTeam = (currentTeam + 1) % teamScores.length;
            updateTurnHighLight();
        }
        
        // Memperbarui skor
        function updateScore(points) {
            teamScores[currentTeam] += points;
            // Update tampilan skor tim yang sedang aktif
            const activeCard = document.querySelector(`.score-card[data-team-id="${currentTeam}"]`);
            if (activeCard) {
                activeCard.querySelector('p').textContent = teamScores[currentTeam];
            }
        }
        
        // Menampilkan layar akhir permainan
        function showEndGame() {
            launchConfetti();
            
            // Tentukan pemenang
            let maxScore = -Infinity;
            let winners = [];
            teamScores.forEach((score, index) => {
                if (score > maxScore) {
                    maxScore = score;
                    winners = [index + 1]; // Tim pemenang baru
                } else if (score === maxScore) {
                    winners.push(index + 1); // Seri
                }
            });
            
            if (winners.length > 1) {
                winnerText.textContent = `Permainan SERI antara Tim ${winners.join(' dan ')}!`;
            } else {
                winnerText.textContent = `Selamat kepada Tim ${winners[0]}!`;
            }
            
            // Tampilkan semua skor akhir
            finalScoresContainer.innerHTML = '';
            teamScores.forEach((score, index) => {
                const scoreText = document.createElement('p');
                scoreText.textContent = `Tim ${index + 1}: ${score} Poin`;
                finalScoresContainer.appendChild(scoreText);
            });
            
            finishModal.style.display = 'flex';
        }
        
        // -----------------------------------------------------------------
        // --- INISIALISASI ------------------------------------------------
        // -----------------------------------------------------------------
        
        // Tampilkan layar setup saat pertama kali dimuat
        document.addEventListener('DOMContentLoaded', showSetup);

    </script>

</body>
</html>
