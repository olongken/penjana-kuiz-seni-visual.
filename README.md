<html lang="ms">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Web App Penjana Kuiz AI Seni Visual</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Penjana Kuiz AI</h1>
    <p>Pendidikan Seni Visual</p>
  </header>
  <main>
    <!-- Halaman Utama -->
    <section id="home-section">
      <button id="startQuizBtn">Mula Jana Kuiz</button>
    </section>
    <!-- Halaman Input Topik -->
    <section id="input-section" style="display: none;">
      <h2>Masukkan Topik atau Pilih Kategori</h2>
      <input type="text" id="topicInput" placeholder="Contoh: Warna, Teknik Lukisan, dsb.">
      <button id="generateQuizBtn">Jana Kuiz</button>
    </section>
    <!-- Halaman Kuiz -->
    <section id="quiz-section" style="display: none;">
      <h2>Kuiz Dijana</h2>
      <div id="quizContainer">
        <!-- Soalan kuiz akan dimasukkan di sini -->
      </div>
      <button id="saveQuestionBtn">Simpan Soalan ke Bank Soalan</button>
    </section>
  </main>
  <script src="script.js"></script>
</body>
</html>
