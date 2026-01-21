
<html lang="th" class="h-full">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>คณิตศาสตร์ ป.5</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="/_sdk/element_sdk.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Kanit:wght@300;400;500;600;700&amp;display=swap" rel="stylesheet">
  <style>
    body {
      box-sizing: border-box;
    }
    * {
      font-family: 'Kanit', sans-serif;
    }
    .topic-card {
      transition: all 0.3s ease;
    }
    .topic-card:hover {
      transform: translateY(-4px);
    }
    .btn-option {
      transition: all 0.2s ease;
    }
    .btn-option:hover:not(:disabled) {
      transform: scale(1.02);
    }
    .correct-animation {
      animation: correctPulse 0.5s ease;
    }
    .wrong-animation {
      animation: wrongShake 0.5s ease;
    }
    @keyframes correctPulse {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.05); }
    }
    @keyframes wrongShake {
      0%, 100% { transform: translateX(0); }
      25% { transform: translateX(-5px); }
      75% { transform: translateX(5px); }
    }
    .star {
      animation: starBounce 0.6s ease infinite;
    }
    @keyframes starBounce {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.2); }
    }
    .progress-fill {
      transition: width 0.5s ease;
    }
    .kawaii-bg {
      position: relative;
      overflow: hidden;
    }
    .kawaii-pattern {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      opacity: 0.2;
      pointer-events: none;
    }
    .floating-icon {
      position: absolute;
      animation: float 6s ease-in-out infinite;
      font-size: 3rem;
      opacity: 0.4;
    }
    @keyframes float {
      0%, 100% { transform: translateY(0px) rotate(0deg); }
      50% { transform: translateY(-25px) rotate(8deg); }
    }
    .bow-decoration {
      display: inline-block;
      font-size: 1.8rem;
      animation: bowBounce 2s ease-in-out infinite;
      margin: 0 8px;
    }
    @keyframes bowBounce {
      0%, 100% { transform: scale(1) rotate(-5deg); }
      50% { transform: scale(1.15) rotate(5deg); }
    }
  </style>
  <style>@view-transition { navigation: auto; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
 </head>
 <body class="h-full">
  <div id="app-container" class="h-full overflow-auto kawaii-bg" style="background: linear-gradient(135deg, #FFB6D9 0%, #D5AAFF 50%, #A8D8FF 100%);"><!-- Kawaii Decorations -->
   <div class="kawaii-pattern"><!-- Bows -->
    <div class="floating-icon" style="top: 8%; left: 5%;">
     🎀
    </div>
    <div class="floating-icon" style="top: 12%; right: 8%; animation-delay: 1s;">
     🎀
    </div>
    <div class="floating-icon" style="top: 55%; right: 12%; animation-delay: 2.5s;">
     🎀
    </div>
    <div class="floating-icon" style="top: 18%; left: 50%; animation-delay: 2.2s;">
     🎀
    </div>
    <div class="floating-icon" style="top: 78%; left: 15%; animation-delay: 3.5s;">
     🎀
    </div><!-- Hearts and Stars -->
    <div class="floating-icon" style="top: 22%; left: 12%; animation-delay: 2s;">
     💖
    </div>
    <div class="floating-icon" style="top: 32%; right: 18%; animation-delay: 0.5s;">
     ⭐
    </div>
    <div class="floating-icon" style="top: 62%; left: 8%; animation-delay: 1.8s;">
     💝
    </div>
    <div class="floating-icon" style="top: 88%; right: 10%; animation-delay: 0.8s;">
     ✨
    </div>
    <div class="floating-icon" style="top: 58%; right: 5%; animation-delay: 1.2s;">
     💫
    </div><!-- Flowers -->
    <div class="floating-icon" style="top: 42%; left: 8%; animation-delay: 1.5s;">
     🌸
    </div>
    <div class="floating-icon" style="top: 72%; right: 15%; animation-delay: 3s;">
     🌺
    </div>
    <div class="floating-icon" style="top: 38%; right: 88%; animation-delay: 2.8s;">
     🌸
    </div><!-- Sanrio Style Characters -->
    <div class="floating-icon" style="top: 28%; left: 85%; animation-delay: 1.3s; font-size: 2.5rem;">
     🐰
    </div>
    <div class="floating-icon" style="top: 48%; left: 92%; animation-delay: 2.7s; font-size: 2.5rem;">
     🐱
    </div>
    <div class="floating-icon" style="top: 68%; left: 78%; animation-delay: 1.9s; font-size: 2.5rem;">
     🐧
    </div>
    <div class="floating-icon" style="top: 15%; right: 85%; animation-delay: 3.2s; font-size: 2.5rem;">
     🦄
    </div>
   </div><!-- หน้าหลัก - เลือกหัวข้อ -->
   <div id="home-screen" class="min-h-full p-4 md:p-8">
    <div class="max-w-4xl mx-auto" style="position: relative; z-index: 1;"><!-- Header -->
     <div class="text-center mb-8">
      <div class="inline-block bg-white/30 backdrop-blur-sm rounded-full px-6 py-2 mb-4"><span class="text-white text-lg">📚 ระดับชั้น ป.5</span>
      </div>
      <div class="bg-white/40 backdrop-blur-md rounded-2xl px-8 py-4 mb-4 inline-block border-4 border-white/50" style="box-shadow: 0 8px 32px rgba(255, 182, 217, 0.3);"><span class="bow-decoration">🎀</span>
       <div class="inline-block">
        <div class="text-white text-xl font-semibold mb-1" style="text-shadow: 2px 2px 4px rgba(0,0,0,0.1);">
         👧 เด็กหญิง วนิศา สัมมาเมฆ
        </div>
        <div class="text-white/90 text-sm">
         ชั้นประถมศึกษาปีที่ 5
        </div>
       </div><span class="bow-decoration" style="animation-delay: 0.5s;">🎀</span>
      </div>
      <h1 id="main-title" class="text-3xl md:text-5xl font-bold text-white mb-3" style="text-shadow: 3px 3px 6px rgba(0,0,0,0.2);">คณิตศาสตร์ ป.5</h1>
      <p id="welcome-text" class="text-white/95 text-lg">เลือกหัวข้อที่ต้องการฝึก</p>
     </div><!-- Topic Grid -->
     <div class="grid grid-cols-2 md:grid-cols-3 gap-4 md:gap-6"><button onclick="startTopic('addition')" class="topic-card bg-gradient-to-br from-orange-400 to-orange-600 rounded-2xl p-6 text-white shadow-xl hover:shadow-2xl">
       <div class="text-4xl mb-3">
        ➕
       </div>
       <div class="font-semibold text-lg">
        การบวก
       </div>
       <div class="text-sm text-white/80">
        เลขหลายหลัก
       </div></button> <button onclick="startTopic('subtraction')" class="topic-card bg-gradient-to-br from-blue-400 to-blue-600 rounded-2xl p-6 text-white shadow-xl hover:shadow-2xl">
       <div class="text-4xl mb-3">
        ➖
       </div>
       <div class="font-semibold text-lg">
        การลบ
       </div>
       <div class="text-sm text-white/80">
        เลขหลายหลัก
       </div></button> <button onclick="startTopic('multiplication')" class="topic-card bg-gradient-to-br from-green-400 to-green-600 rounded-2xl p-6 text-white shadow-xl hover:shadow-2xl">
       <div class="text-4xl mb-3">
        ✖️
       </div>
       <div class="font-semibold text-lg">
        การคูณ
       </div>
       <div class="text-sm text-white/80">
        สูตรคูณ &amp; โจทย์
       </div></button> <button onclick="startTopic('division')" class="topic-card bg-gradient-to-br from-purple-400 to-purple-600 rounded-2xl p-6 text-white shadow-xl hover:shadow-2xl">
       <div class="text-4xl mb-3">
        ➗
       </div>
       <div class="font-semibold text-lg">
        การหาร
       </div>
       <div class="text-sm text-white/80">
        หารลงตัว &amp; เศษ
       </div></button> <button onclick="startTopic('fraction')" class="topic-card bg-gradient-to-br from-pink-400 to-pink-600 rounded-2xl p-6 text-white shadow-xl hover:shadow-2xl">
       <div class="text-4xl mb-3">
        🍕
       </div>
       <div class="font-semibold text-lg">
        เศษส่วน
       </div>
       <div class="text-sm text-white/80">
        บวก ลบ เศษส่วน
       </div></button> <button onclick="startTopic('wordproblem')" class="topic-card bg-gradient-to-br from-teal-400 to-teal-600 rounded-2xl p-6 text-white shadow-xl hover:shadow-2xl">
       <div class="text-4xl mb-3">
        📝
       </div>
       <div class="font-semibold text-lg">
        โจทย์ปัญหา
       </div>
       <div class="text-sm text-white/80">
        คิดวิเคราะห์
       </div></button>
     </div><!-- Footer -->
     <div class="text-center mt-8 text-white/80 text-sm">
      🎯 ฝึกทำโจทย์ทุกวัน เก่งคณิตศาสตร์แน่นอน! 🎀
     </div>
    </div>
   </div><!-- หน้าทำข้อสอบ -->
   <div id="quiz-screen" class="min-h-full p-4 md:p-8 hidden">
    <div class="max-w-2xl mx-auto" style="position: relative; z-index: 1;"><!-- Progress Bar -->
     <div class="bg-white/30 rounded-full h-4 mb-6 overflow-hidden">
      <div id="progress-bar" class="progress-fill bg-yellow-400 h-full rounded-full" style="width: 0%"></div>
     </div><!-- Quiz Card -->
     <div class="bg-white rounded-3xl shadow-2xl p-6 md:p-8"><!-- Header -->
      <div class="flex justify-between items-center mb-6"><button onclick="goHome()" class="text-gray-500 hover:text-gray-700 flex items-center gap-2"> <span>←</span> กลับ </button>
       <div id="topic-badge" class="bg-purple-100 text-purple-700 px-4 py-1 rounded-full font-medium"></div>
       <div id="score-display" class="text-lg font-bold text-green-600"><span id="current-score">0</span> คะแนน
       </div>
      </div><!-- Question Number -->
      <div class="text-center mb-4"><span class="text-gray-500">ข้อที่ <span id="question-number">1</span> / <span id="total-questions">10</span></span>
      </div><!-- Question -->
      <div id="question-container" class="text-center mb-8">
       <div id="question-text" class="text-2xl md:text-4xl font-bold text-gray-800 mb-4"></div>
       <div id="question-hint" class="text-gray-500 text-sm"></div>
      </div><!-- Answer Options -->
      <div id="options-container" class="grid grid-cols-2 gap-4 mb-6"></div><!-- Feedback -->
      <div id="feedback-container" class="hidden text-center p-4 rounded-xl mb-4">
       <div id="feedback-icon" class="text-4xl mb-2"></div>
       <div id="feedback-text" class="font-medium"></div>
       <div id="feedback-explanation" class="text-sm text-gray-600 mt-2"></div>
      </div><!-- Next Button --> <button id="next-btn" onclick="nextQuestion()" class="hidden w-full bg-gradient-to-r from-purple-500 to-pink-500 text-white py-4 rounded-xl font-semibold text-lg hover:opacity-90 transition-opacity"> ข้อถัดไป → </button>
     </div>
    </div>
   </div><!-- หน้าผลลัพธ์ -->
   <div id="result-screen" class="min-h-full p-4 md:p-8 hidden flex items-center justify-center">
    <div class="bg-white rounded-3xl shadow-2xl p-8 max-w-md w-full text-center" style="position: relative; z-index: 1;">
     <div class="text-6xl mb-4"><span id="result-emoji">🎉</span>
     </div>
     <h2 id="result-title" class="text-2xl font-bold text-gray-800 mb-2">ยอดเยี่ยมมาก!</h2>
     <p id="result-message" class="text-gray-600 mb-6"></p>
     <div class="bg-gradient-to-r from-purple-500 to-pink-500 rounded-2xl p-6 text-white mb-6">
      <div class="text-5xl font-bold mb-2"><span id="final-score">0</span>/<span id="final-total">10</span>
      </div>
      <div class="text-white/80">
       คะแนนที่ได้
      </div>
     </div>
     <div id="stars-container" class="flex justify-center gap-2 mb-6"><!-- Stars will be added here -->
     </div>
     <div class="flex gap-4"><button onclick="startTopic(currentTopic)" class="flex-1 bg-purple-500 text-white py-3 rounded-xl font-semibold hover:bg-purple-600 transition-colors"> 🔄 เล่นอีกครั้ง </button> <button onclick="goHome()" class="flex-1 bg-gray-200 text-gray-700 py-3 rounded-xl font-semibold hover:bg-gray-300 transition-colors"> 🏠 หน้าหลัก </button>
     </div>
    </div>
   </div>
  </div>
  <script>
    // Configuration
    const defaultConfig = {
      app_title: 'คณิตศาสตร์ ป.5',
      welcome_message: 'เลือกหัวข้อที่ต้องการฝึก',
      primary_color: '#FFB6D9',
      secondary_color: '#D5AAFF',
      text_color: '#5a5a5a',
      button_color: '#ffb4d1',
      accent_color: '#ffd93d'
    };

    let config = { ...defaultConfig };

    // Game State
    let currentTopic = '';
    let currentQuestion = 0;
    let score = 0;
    let totalQuestions = 10;
    let questions = [];
    let answered = false;

    // Topic Names
    const topicNames = {
      addition: 'การบวก',
      subtraction: 'การลบ',
      multiplication: 'การคูณ',
      division: 'การหาร',
      fraction: 'เศษส่วน',
      wordproblem: 'โจทย์ปัญหา'
    };

    // Initialize SDK
    async function initSDK() {
      if (window.elementSdk) {
        await window.elementSdk.init({
          defaultConfig,
          onConfigChange: async (newConfig) => {
            config = { ...defaultConfig, ...newConfig };
            applyConfig();
          },
          mapToCapabilities: (cfg) => ({
            recolorables: [
              {
                get: () => cfg.primary_color || defaultConfig.primary_color,
                set: (v) => { cfg.primary_color = v; window.elementSdk.setConfig({ primary_color: v }); }
              },
              {
                get: () => cfg.secondary_color || defaultConfig.secondary_color,
                set: (v) => { cfg.secondary_color = v; window.elementSdk.setConfig({ secondary_color: v }); }
              },
              {
                get: () => cfg.text_color || defaultConfig.text_color,
                set: (v) => { cfg.text_color = v; window.elementSdk.setConfig({ text_color: v }); }
              },
              {
                get: () => cfg.button_color || defaultConfig.button_color,
                set: (v) => { cfg.button_color = v; window.elementSdk.setConfig({ button_color: v }); }
              },
              {
                get: () => cfg.accent_color || defaultConfig.accent_color,
                set: (v) => { cfg.accent_color = v; window.elementSdk.setConfig({ accent_color: v }); }
              }
            ],
            borderables: [],
            fontEditable: undefined,
            fontSizeable: undefined
          }),
          mapToEditPanelValues: (cfg) => new Map([
            ['app_title', cfg.app_title || defaultConfig.app_title],
            ['welcome_message', cfg.welcome_message || defaultConfig.welcome_message]
          ])
        });
        config = { ...defaultConfig, ...window.elementSdk.config };
      }
      applyConfig();
    }

    function applyConfig() {
      const title = config.app_title || defaultConfig.app_title;
      const welcome = config.welcome_message || defaultConfig.welcome_message;
      const primary = config.primary_color || defaultConfig.primary_color;
      const secondary = config.secondary_color || defaultConfig.secondary_color;
      const textColor = config.text_color || defaultConfig.text_color;
      const buttonColor = config.button_color || defaultConfig.button_color;
      const accent = config.accent_color || defaultConfig.accent_color;

      document.getElementById('main-title').textContent = title;
      document.getElementById('welcome-text').textContent = welcome;
      
      const container = document.getElementById('app-container');
      container.style.background = `linear-gradient(135deg, ${primary} 0%, ${secondary} 50%, #A8D8FF 100%)`;
      
      const quizCard = document.querySelector('#quiz-screen .bg-white');
      if (quizCard) {
        quizCard.querySelectorAll('.text-gray-800').forEach(el => el.style.color = textColor);
      }
      
      const nextBtn = document.getElementById('next-btn');
      if (nextBtn) {
        nextBtn.style.background = `linear-gradient(to right, ${buttonColor}, ${secondary})`;
      }
      
      const progressBar = document.getElementById('progress-bar');
      if (progressBar) {
        progressBar.style.backgroundColor = accent;
      }
    }

    // Question Generators
    function generateAddition() {
      const questions = [];
      for (let i = 0; i < totalQuestions; i++) {
        const a = Math.floor(Math.random() * 9000) + 1000;
        const b = Math.floor(Math.random() * 9000) + 1000;
        const answer = a + b;
        const options = generateOptions(answer);
        questions.push({
          text: `${a.toLocaleString()} + ${b.toLocaleString()} = ?`,
          answer: answer,
          options: options,
          explanation: `${a.toLocaleString()} + ${b.toLocaleString()} = ${answer.toLocaleString()}`
        });
      }
      return questions;
    }

    function generateSubtraction() {
      const questions = [];
      for (let i = 0; i < totalQuestions; i++) {
        const a = Math.floor(Math.random() * 9000) + 5000;
        const b = Math.floor(Math.random() * (a - 1000)) + 1000;
        const answer = a - b;
        const options = generateOptions(answer);
        questions.push({
          text: `${a.toLocaleString()} - ${b.toLocaleString()} = ?`,
          answer: answer,
          options: options,
          explanation: `${a.toLocaleString()} - ${b.toLocaleString()} = ${answer.toLocaleString()}`
        });
      }
      return questions;
    }

    function generateMultiplication() {
      const questions = [];
      for (let i = 0; i < totalQuestions; i++) {
        const a = Math.floor(Math.random() * 90) + 10;
        const b = Math.floor(Math.random() * 90) + 10;
        const answer = a * b;
        const options = generateOptions(answer);
        questions.push({
          text: `${a} × ${b} = ?`,
          answer: answer,
          options: options,
          explanation: `${a} × ${b} = ${answer.toLocaleString()}`
        });
      }
      return questions;
    }

    function generateDivision() {
      const questions = [];
      for (let i = 0; i < totalQuestions; i++) {
        const b = Math.floor(Math.random() * 11) + 2;
        const quotient = Math.floor(Math.random() * 90) + 10;
        const a = b * quotient;
        const options = generateOptions(quotient);
        questions.push({
          text: `${a.toLocaleString()} ÷ ${b} = ?`,
          answer: quotient,
          options: options,
          explanation: `${a.toLocaleString()} ÷ ${b} = ${quotient}`
        });
      }
      return questions;
    }

    function generateFraction() {
      const questions = [];
      for (let i = 0; i < totalQuestions; i++) {
        const denom = [2, 3, 4, 5, 6, 8, 10][Math.floor(Math.random() * 7)];
        const isAddition = Math.random() > 0.5;
        
        if (isAddition) {
          const num1 = Math.floor(Math.random() * (denom - 1)) + 1;
          const num2 = Math.floor(Math.random() * (denom - num1)) + 1;
          const answer = num1 + num2;
          const options = generateFractionOptions(answer, denom);
          questions.push({
            text: `${num1}/${denom} + ${num2}/${denom} = ?`,
            answer: `${answer}/${denom}`,
            options: options,
            explanation: `เมื่อตัวส่วนเท่ากัน ให้บวกเฉพาะตัวเศษ: ${num1} + ${num2} = ${answer}`
          });
        } else {
          const num1 = Math.floor(Math.random() * (denom - 2)) + 3;
          const num2 = Math.floor(Math.random() * (num1 - 1)) + 1;
          const answer = num1 - num2;
          const options = generateFractionOptions(answer, denom);
          questions.push({
            text: `${num1}/${denom} - ${num2}/${denom} = ?`,
            answer: `${answer}/${denom}`,
            options: options,
            explanation: `เมื่อตัวส่วนเท่ากัน ให้ลบเฉพาะตัวเศษ: ${num1} - ${num2} = ${answer}`
          });
        }
      }
      return questions;
    }

    function generateWordProblem() {
      const templates = [
        {
          generate: () => {
            const apples = Math.floor(Math.random() * 50) + 20;
            const oranges = Math.floor(Math.random() * 50) + 20;
            const answer = apples + oranges;
            return {
              text: `สมชายมีแอปเปิ้ล ${apples} ผล และส้ม ${oranges} ผล สมชายมีผลไม้ทั้งหมดกี่ผล?`,
              answer: answer,
              options: generateOptions(answer),
              explanation: `แอปเปิ้ล + ส้ม = ${apples} + ${oranges} = ${answer} ผล`
            };
          }
        },
        {
          generate: () => {
            const total = Math.floor(Math.random() * 900) + 500;
            const spent = Math.floor(Math.random() * (total - 100)) + 100;
            const answer = total - spent;
            return {
              text: `แม่ค้ามีเงิน ${total.toLocaleString()} บาท ซื้อของไป ${spent.toLocaleString()} บาท เหลือเงินกี่บาท?`,
              answer: answer,
              options: generateOptions(answer),
              explanation: `เงินเดิม - เงินที่ใช้ = ${total.toLocaleString()} - ${spent.toLocaleString()} = ${answer.toLocaleString()} บาท`
            };
          }
        },
        {
          generate: () => {
            const perBox = Math.floor(Math.random() * 20) + 10;
            const boxes = Math.floor(Math.random() * 8) + 3;
            const answer = perBox * boxes;
            return {
              text: `กล่องหนึ่งมีขนม ${perBox} ชิ้น ถ้ามี ${boxes} กล่อง จะมีขนมทั้งหมดกี่ชิ้น?`,
              answer: answer,
              options: generateOptions(answer),
              explanation: `ขนมต่อกล่อง × จำนวนกล่อง = ${perBox} × ${boxes} = ${answer} ชิ้น`
            };
          }
        },
        {
          generate: () => {
            const students = Math.floor(Math.random() * 6) + 4;
            const perStudent = Math.floor(Math.random() * 10) + 5;
            const total = students * perStudent;
            const answer = perStudent;
            return {
              text: `แบ่งดินสอ ${total} แท่ง ให้นักเรียน ${students} คน เท่าๆ กัน แต่ละคนได้กี่แท่ง?`,
              answer: answer,
              options: generateOptions(answer),
              explanation: `ดินสอทั้งหมด ÷ จำนวนคน = ${total} ÷ ${students} = ${answer} แท่ง`
            };
          }
        },
        {
          generate: () => {
            const price = Math.floor(Math.random() * 40) + 15;
            const quantity = Math.floor(Math.random() * 8) + 3;
            const answer = price * quantity;
            return {
              text: `ปากกาด้ามละ ${price} บาท ซื้อ ${quantity} ด้าม ต้องจ่ายเงินกี่บาท?`,
              answer: answer,
              options: generateOptions(answer),
              explanation: `ราคาต่อด้าม × จำนวน = ${price} × ${quantity} = ${answer} บาท`
            };
          }
        }
      ];
      
      const questions = [];
      for (let i = 0; i < totalQuestions; i++) {
        const template = templates[Math.floor(Math.random() * templates.length)];
        questions.push(template.generate());
      }
      return questions;
    }

    function generateOptions(correctAnswer) {
      const options = [correctAnswer];
      while (options.length < 4) {
        const variance = Math.max(Math.floor(correctAnswer * 0.2), 10);
        const wrong = correctAnswer + (Math.floor(Math.random() * variance * 2) - variance);
        if (wrong > 0 && wrong !== correctAnswer && !options.includes(wrong)) {
          options.push(wrong);
        }
      }
      return shuffleArray(options);
    }

    function generateFractionOptions(correctNum, denom) {
      const options = [`${correctNum}/${denom}`];
      while (options.length < 4) {
        const wrongNum = Math.floor(Math.random() * (denom * 2)) + 1;
        const wrongOption = `${wrongNum}/${denom}`;
        if (wrongNum !== correctNum && !options.includes(wrongOption)) {
          options.push(wrongOption);
        }
      }
      return shuffleArray(options);
    }

    function shuffleArray(array) {
      const arr = [...array];
      for (let i = arr.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [arr[i], arr[j]] = [arr[j], arr[i]];
      }
      return arr;
    }

    // Game Functions
    function startTopic(topic) {
      currentTopic = topic;
      currentQuestion = 0;
      score = 0;
      answered = false;

      switch (topic) {
        case 'addition': questions = generateAddition(); break;
        case 'subtraction': questions = generateSubtraction(); break;
        case 'multiplication': questions = generateMultiplication(); break;
        case 'division': questions = generateDivision(); break;
        case 'fraction': questions = generateFraction(); break;
        case 'wordproblem': questions = generateWordProblem(); break;
      }

      document.getElementById('home-screen').classList.add('hidden');
      document.getElementById('quiz-screen').classList.remove('hidden');
      document.getElementById('result-screen').classList.add('hidden');
      document.getElementById('topic-badge').textContent = topicNames[topic];
      document.getElementById('total-questions').textContent = totalQuestions;

      showQuestion();
    }

    function showQuestion() {
      answered = false;
      const q = questions[currentQuestion];
      
      document.getElementById('question-number').textContent = currentQuestion + 1;
      document.getElementById('current-score').textContent = score;
      document.getElementById('question-text').textContent = q.text;
      document.getElementById('progress-bar').style.width = `${((currentQuestion) / totalQuestions) * 100}%`;
      
      document.getElementById('feedback-container').classList.add('hidden');
      document.getElementById('next-btn').classList.add('hidden');

      const optionsContainer = document.getElementById('options-container');
      optionsContainer.innerHTML = '';

      q.options.forEach((option, index) => {
        const btn = document.createElement('button');
        btn.className = 'btn-option bg-gray-100 hover:bg-gray-200 text-gray-800 py-4 px-6 rounded-xl font-semibold text-lg transition-all';
        btn.textContent = typeof option === 'number' ? option.toLocaleString() : option;
        btn.onclick = () => selectAnswer(option, btn);
        optionsContainer.appendChild(btn);
      });
    }

    function selectAnswer(selected, btnElement) {
      if (answered) return;
      answered = true;

      const q = questions[currentQuestion];
      const isCorrect = selected === q.answer || selected.toString() === q.answer.toString();

      const allBtns = document.querySelectorAll('#options-container button');
      allBtns.forEach(btn => {
        btn.disabled = true;
        const btnValue = btn.textContent.replace(/,/g, '');
        const answerValue = typeof q.answer === 'number' ? q.answer.toString() : q.answer;
        
        if (btnValue === answerValue || btn.textContent === q.answer.toString() || btn.textContent === q.answer.toLocaleString?.()) {
          btn.classList.remove('bg-gray-100', 'hover:bg-gray-200');
          btn.classList.add('bg-green-500', 'text-white');
        } else if (btn === btnElement && !isCorrect) {
          btn.classList.remove('bg-gray-100', 'hover:bg-gray-200');
          btn.classList.add('bg-red-500', 'text-white', 'wrong-animation');
        }
      });

      if (isCorrect) {
        score++;
        btnElement.classList.add('correct-animation');
      }

      const feedbackContainer = document.getElementById('feedback-container');
      feedbackContainer.classList.remove('hidden', 'bg-green-100', 'bg-red-100');
      feedbackContainer.classList.add(isCorrect ? 'bg-green-100' : 'bg-red-100');
      
      document.getElementById('feedback-icon').textContent = isCorrect ? '🎉' : '😢';
      document.getElementById('feedback-text').textContent = isCorrect ? 'ถูกต้อง! เก่งมาก!' : 'ไม่ถูกต้อง ลองใหม่นะ';
      document.getElementById('feedback-text').className = `font-medium ${isCorrect ? 'text-green-700' : 'text-red-700'}`;
      document.getElementById('feedback-explanation').textContent = q.explanation;

      document.getElementById('current-score').textContent = score;
      document.getElementById('next-btn').classList.remove('hidden');
      document.getElementById('next-btn').textContent = currentQuestion < totalQuestions - 1 ? 'ข้อถัดไป →' : 'ดูผลคะแนน 🏆';
    }

    function nextQuestion() {
      currentQuestion++;
      if (currentQuestion < totalQuestions) {
        showQuestion();
      } else {
        showResult();
      }
    }

    function showResult() {
      document.getElementById('quiz-screen').classList.add('hidden');
      document.getElementById('result-screen').classList.remove('hidden');
      document.getElementById('progress-bar').style.width = '100%';

      document.getElementById('final-score').textContent = score;
      document.getElementById('final-total').textContent = totalQuestions;

      const percentage = (score / totalQuestions) * 100;
      let emoji, title, message;

      if (percentage >= 90) {
        emoji = '🏆'; title = 'ยอดเยี่ยมมาก!'; message = 'เก่งสุดๆ เลย! คุณเป็นเทพคณิตศาสตร์!';
      } else if (percentage >= 70) {
        emoji = '🎉'; title = 'ดีมาก!'; message = 'ทำได้ดีมากเลย! ฝึกต่อไปนะ!';
      } else if (percentage >= 50) {
        emoji = '👍'; title = 'พอใช้ได้!'; message = 'ฝึกเพิ่มอีกนิด จะเก่งขึ้นแน่นอน!';
      } else {
        emoji = '💪'; title = 'พยายามต่อไป!'; message = 'อย่าท้อนะ ฝึกบ่อยๆ แล้วจะเก่งขึ้น!';
      }

      document.getElementById('result-emoji').textContent = emoji;
      document.getElementById('result-title').textContent = title;
      document.getElementById('result-message').textContent = message;

      const starsContainer = document.getElementById('stars-container');
      starsContainer.innerHTML = '';
      const starCount = Math.ceil((score / totalQuestions) * 5);
      for (let i = 0; i < 5; i++) {
        const star = document.createElement('span');
        star.className = 'text-4xl';
        star.textContent = i < starCount ? '⭐' : '☆';
        if (i < starCount) {
          star.classList.add('star');
          star.style.animationDelay = `${i * 0.1}s`;
        }
        starsContainer.appendChild(star);
      }
    }

    function goHome() {
      document.getElementById('home-screen').classList.remove('hidden');
      document.getElementById('quiz-screen').classList.add('hidden');
      document.getElementById('result-screen').classList.add('hidden');
    }

    // Initialize
    initSDK();
  </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9c133efed0b6732e',t:'MTc2ODk2MTEyMS4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
