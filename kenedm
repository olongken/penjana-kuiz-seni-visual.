<!DOCTYPE html>
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

/* Gaya asas dengan tema seni interaktif */

body {
  margin: 0;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background: linear-gradient(135deg, #fdfbfb 0%, #ebedee 100%);
  color: #333;
}

header {
  text-align: center;
  padding: 2rem 0;
  background-color: #fff;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

header h1 {
  margin: 0;
  font-size: 2.5rem;
}

header p {
  margin: 0;
  font-size: 1.2rem;
  color: #666;
}

main {
  max-width: 800px;
  margin: 2rem auto;
  padding: 1rem;
  text-align: center;
}

section {
  margin-bottom: 2rem;
}

/* Butang dengan animasi interaktif */
button {
  background-color: #6a1b9a;
  color: #fff;
  border: none;
  padding: 1rem 2rem;
  font-size: 1rem;
  border-radius: 5px;
  cursor: pointer;
  transition: transform 0.2s ease-in-out, background-color 0.2s;
}

button:hover {
  transform: scale(1.05);
}

button:active {
  background-color: #4a148c;
}

/* Gaya input teks */
input[type="text"] {
  width: 80%;
  padding: 0.75rem;
  margin: 1rem 0;
  font-size: 1rem;
  border: 2px solid #ddd;
  border-radius: 5px;
}

// script.js

document.addEventListener("DOMContentLoaded", function() {
  const startQuizBtn = document.getElementById("startQuizBtn");
  const homeSection = document.getElementById("home-section");
  const inputSection = document.getElementById("input-section");
  const generateQuizBtn = document.getElementById("generateQuizBtn");
  const quizSection = document.getElementById("quiz-section");
  const topicInput = document.getElementById("topicInput");
  const quizContainer = document.getElementById("quizContainer");

  // Tindakan untuk memaparkan halaman input topik
  startQuizBtn.addEventListener("click", function() {
    homeSection.style.display = "none";
    inputSection.style.display = "block";
  });

  // Tindakan untuk jana kuiz (di sini menggunakan fungsi simulasi)
  generateQuizBtn.addEventListener("click", function() {
    const topic = topicInput.value.trim();
    if (topic === "") {
      alert("Sila masukkan topik atau kategori.");
      return;
    }

    // Fungsi simulasi untuk menjana kuiz berdasarkan topik
    const simulatedQuiz = generateSimulatedQuiz(topic);

    // Tukar paparan ke halaman kuiz dan paparkan soalan
    inputSection.style.display = "none";
    quizSection.style.display = "block";
    displayQuiz(simulatedQuiz);
  });

  // Fungsi simulasi menjana kuiz (contoh soalan)
  function generateSimulatedQuiz(topic) {
    return [
      {
        question: `Apakah elemen penting dalam topik "${topic}"?`,
        options: ["Warna", "Tekstur", "Bentuk", "Semua di atas"],
        answer: "Semua di atas"
      },
      {
        question: `Siapakah pelukis terkenal yang dikenali dengan penggunaan warna?`,
        options: ["Van Gogh", "Picasso", "Da Vinci", "Rembrandt"],
        answer: "Van Gogh"
      }
    ];
  }

  // Fungsi untuk memaparkan kuiz di dalam div #quizContainer
  function displayQuiz(quizData) {
    quizContainer.innerHTML = "";
    quizData.forEach((item, index) => {
      const questionDiv = document.createElement("div");
      questionDiv.className = "quiz-item";
      questionDiv.innerHTML = `<h3>Soalan ${index + 1}</h3>
        <p>${item.question}</p>`;

      const optionsList = document.createElement("ul");
      item.options.forEach(option => {
        const li = document.createElement("li");
        li.textContent = option;
        li.style.cursor = "pointer";
        li.addEventListener("click", function() {
          // Auto-pemarkahan mudah: paparkan makluman berdasarkan pilihan
          alert(option === item.answer ? "Betul!" : "Cuba lagi!");
        });
        optionsList.appendChild(li);
      });
      questionDiv.appendChild(optionsList);
      quizContainer.appendChild(questionDiv);
    });
  }
});
