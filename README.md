<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Profile & Stats</title>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f7fc;
      margin: 0;
      padding: 20px;
    }
    h1, h3, h2 {
      text-align: center;
    }
    .tech-section {
      margin: 40px 0;
    }
    .container {
      width: 80%;
      margin: 0 auto;
    }
    button {
      padding: 10px 20px;
      font-size: 16px;
      cursor: pointer;
      background-color: #007BFF;
      color: white;
      border: none;
      border-radius: 5px;
    }
    .button-container {
      text-align: center;
      margin-top: 20px;
    }
    .stats-container {
      width: 70%;
      margin: 0 auto;
    }
    .progress-bar {
      height: 25px;
      width: 100%;
      background-color: #ddd;
      margin: 10px 0;
    }
    .completed {
      background-color: #4CAF50;
    }
    .in-progress {
      background-color: #FF9800;
    }
    .pending {
      background-color: #F44336;
    }
  </style>
</head>
<body>

  <!-- Profile Header -->
  <h1 align="center">Hey there 👋, I'm <span style="color:#00bfff;">Vishal Abhinav</span></h1>
  <h3 align="center">🚀 Software Ops Engineer | DevOps Engineer | IT Engineer | Cloud Engineer | Aspiring Cloud Architect ☁️</h3>

  <!-- Tech Stack Section -->
  <div class="tech-section container">
    <h2>🧠 My Tech Arsenal — *Deep Dive Mode ON 🔍*</h2>
    
    <h3>💻 Languages & Logic – *The Syntax I Think In*</h3>
    <p>🐍 <strong>Python</strong> | 🐹 <strong>GoLang</strong> | ⚡ <strong>SQL / PLSQL / Oracle SQL</strong> | 🐚 <strong>Bash</strong></p>

    <h3>🌐 Full-Stack Fuel – *Crafting Web Wizards*</h3>
    <p>🧩 <strong>Django</strong> | 🔥 <strong>Flask</strong> | 🎨 <strong>HTML/CSS</strong> | 📜 <strong>YAML</strong></p>

    <h3>🧬 Brains Behind the Bots – *Code That Thinks*</h3>
    <p>🤖 <strong>ML Models</strong> | 🧠 <strong>Deep Neural Networks</strong> | 🧩 <strong>AI Agents</strong> | 🔁 <strong>CI/CD for AI</strong></p>

    <h3>🔧 DevOps Wizardry – *Automate. Deploy. Repeat.*</h3>
    <p>🐳 <strong>Docker</strong> | ☸️ <strong>Kubernetes</strong> | 🚀 <strong>GitHub Actions</strong> | 🧰 <strong>Jenkins</strong></p>
    <p>🔄 <strong>GitOps</strong> | ⚙️ <strong>Deployment Architect</strong></p>

    <h3>☁️ Cloud Nomad – *Scaling Skies*</h3>
    <p>☁️ <strong>AWS</strong> | 🌩️ <strong>OCI (Oracle Cloud)</strong> | 🛫 <strong>GCP</strong></p>
  </div>

  <!-- Profile Visit Count -->
  <div class="button-container">
    <button onclick="incrementVisitCount()">Visit Profile</button>
    <p>Profile Visit Count: <span id="visitCount">0</span></p>
  </div>

  <script>
    // Initialize visit count from localStorage or set to 0
    let visitCount = localStorage.getItem("visitCount") || 0;

    // Display the current visit count
    document.getElementById("visitCount").textContent = visitCount;

    // Increment and update the visit count
    function incrementVisitCount() {
      visitCount++;
      localStorage.setItem("visitCount", visitCount);  // Save the updated count to localStorage
      document.getElementById("visitCount").textContent = visitCount;
    }
  </script>

  <!-- Language Usage Percentage Graph -->
  <h2 align="center">Language Usage Percentage</h2>
  <div class="container">
    <canvas id="languageChart" width="400" height="400"></canvas>
  </div>
  <script>
    const ctx = document.getElementById('languageChart').getContext('2d');
    const languageChart = new Chart(ctx, {
      type: 'pie',
      data: {
        labels: ['Python', 'GoLang', 'SQL/PLSQL', 'Bash', 'Django', 'Flask', 'HTML/CSS', 'YAML'],
        datasets: [{
          label: 'Language Usage',
          data: [30, 10, 15, 5, 10, 10, 10, 10],  // Percentage data (can adjust based on usage)
          backgroundColor: ['#FF5733', '#33FF57', '#3357FF', '#F5A623', '#F9E12E', '#6A5ACD', '#FF6347', '#9B59B6'],
          borderColor: ['#FFFFFF', '#FFFFFF', '#FFFFFF', '#FFFFFF', '#FFFFFF', '#FFFFFF', '#FFFFFF', '#FFFFFF'],
          borderWidth: 1
        }]
      }
    });
  </script>

  <!-- Project Status -->
  <h2 align="center">Project Status</h2>
  <div class="stats-container">
    <h3>Completed Projects</h3>
    <div class="progress-bar">
      <div class="completed" style="width: 70%;"></div>
    </div>
    <p>70% completed</p>

    <h3>In-Progress Projects</h3>
    <div class="progress-bar">
      <div class="in-progress" style="width: 20%;"></div>
    </div>
    <p>20% in-progress</p>

    <h3>Pending Projects</h3>
    <div class="progress-bar">
      <div class="pending" style="width: 10%;"></div>
    </div>
    <p>10% pending</p>
  </div>

  <!-- Social Links -->
  <div align="center">
    <p>🔗 Let’s Connect!</p>
    <a href="https://www.linkedin.com/in/vishal-abhinav/" target="_blank">
      <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge"/>
    </a>
    <a href="https://www.hackerrank.com/Vishal_Abhinav?hr_r=1" target="_blank">
      <img src="https://img.shields.io/badge/HackerRank-2EC866?style=for-the-badge&logo=hackerrank&logoColor=white" alt="HackerRank Badge"/>
    </a>
    <a href="https://www.researchgate.net/profile/Vishal-Abhinav/research" target="_blank">
      <img src="https://img.shields.io/badge/ResearchGate-00CCBB?style=for-the-badge&logo=researchgate&logoColor=white" alt="ResearchGate Badge"/>
    </a>
  </div>

  <footer align="center">
    <p>🙏 Maintained with ❤️ by Vishal Abhinav</p>
    <p>🛠️ DevOps Engineer | Problem Solver | Cloud Whisperer</p>
  </footer>

</body>
</html>
