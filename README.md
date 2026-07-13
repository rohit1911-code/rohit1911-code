
<svg viewBox="0 0 1180 610" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="xMidYMid slice">
  <defs>
    <!-- GRADIENTS -->
    <linearGradient id="mainGradient" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#7C3AED;stop-opacity:1">
        <animate attributeName="offset" from="0%" to="100%" dur="8s" repeatCount="indefinite"/>
      </stop>
      <stop offset="50%" style="stop-color:#22D3EE;stop-opacity:1">
        <animate attributeName="offset" from="50%" to="150%" dur="8s" repeatCount="indefinite"/>
      </stop>
      <stop offset="100%" style="stop-color:#10B981;stop-opacity:1">
        <animate attributeName="offset" from="100%" to="200%" dur="8s" repeatCount="indefinite"/>
      </stop>
    </linearGradient>
 
    <radialGradient id="bgGlow1" cx="20%" cy="30%">
      <stop offset="0%" style="stop-color:#7C3AED;stop-opacity:0.15"/>
      <stop offset="100%" style="stop-color:#030712;stop-opacity:0"/>
      <animate attributeName="cy" from="30%" to="50%" dur="6s" repeatCount="indefinite"/>
    </radialGradient>
 
    <radialGradient id="bgGlow2" cx="80%" cy="70%">
      <stop offset="0%" style="stop-color:#22D3EE;stop-opacity:0.12"/>
      <stop offset="100%" style="stop-color:#030712;stop-opacity:0"/>
      <animate attributeName="cx" from="80%" to="85%" dur="7s" repeatCount="indefinite"/>
    </radialGradient>
 
    <linearGradient id="asciiGradient" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" style="stop-color:#7C3AED;stop-opacity:1"/>
      <stop offset="50%" style="stop-color:#22D3EE;stop-opacity:1"/>
      <stop offset="100%" style="stop-color:#10B981;stop-opacity:1">
        <animate attributeName="offset" from="100%" to="120%" dur="6s" repeatCount="indefinite"/>
      </stop>
    </linearGradient>
 
    <linearGradient id="textGradient" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" style="stop-color:#22D3EE;stop-opacity:1"/>
      <stop offset="100%" style="stop-color:#7C3AED;stop-opacity:1">
        <animate attributeName="offset" from="0%" to="100%" dur="4s" repeatCount="indefinite"/>
      </stop>
    </linearGradient>
 
    <!-- FILTERS -->
    <filter id="glow">
      <feGaussianBlur stdDeviation="2" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
 
    <filter id="glowPulse">
      <feGaussianBlur stdDeviation="3" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
      <animate attributeName="stdDeviation" from="2" to="4" dur="2s" repeatCount="indefinite"/>
    </filter>
 
    <filter id="softBlur">
      <feGaussianBlur in="SourceGraphic" stdDeviation="1"/>
    </filter>
 
    <filter id="noise">
      <feTurbulence type="fractalNoise" baseFrequency="0.8" numOctaves="3" result="noise" seed="2"/>
      <feColorMatrix in="noise" type="saturate" values="0.3"/>
    </filter>
 
    <!-- MASKS -->
    <mask id="asciiMask">
      <rect width="1180" height="610" fill="white"/>
      <rect x="0" y="0" width="450" height="610" fill="black" opacity="0"/>
      <animate attributeName="opacity" from="0" to="0.05" dur="6s" repeatCount="indefinite"/>
    </mask>
 
    <mask id="scanlineMask">
      <rect width="1180" height="610" fill="white"/>
      <rect x="0" y="0" width="1180" height="2" fill="black">
        <animate attributeName="y" from="0" to="610" dur="3s" repeatCount="indefinite"/>
      </rect>
    </mask>
 
    <mask id="textReveal">
      <rect width="600" height="300" fill="white"/>
      <rect x="0" y="0" width="0" height="300" fill="black">
        <animate attributeName="width" from="0" to="600" dur="4s" begin="1s" fill="freeze"/>
      </rect>
    </mask>
  </defs>
 
  <!-- BACKGROUND -->
  <rect width="1180" height="610" fill="#030712"/>
  <rect width="1180" height="610" fill="url(#bgGlow1)"/>
  <rect width="1180" height="610" fill="url(#bgGlow2)"/>
 
  <!-- SUBTLE NOISE -->
  <rect width="1180" height="610" fill="url(#noise)" opacity="0.02"/>
 
  <!-- ANIMATED PARTICLES -->
  <circle cx="100" cy="100" r="1.5" fill="#22D3EE" opacity="0.4">
    <animate attributeName="cy" from="100" to="600" dur="8s" repeatCount="indefinite"/>
    <animate attributeName="opacity" from="0" to="0.4" dur="1s" repeatCount="indefinite"/>
  </circle>
  <circle cx="300" cy="500" r="1" fill="#7C3AED" opacity="0.3">
    <animate attributeName="cy" from="500" to="50" dur="10s" repeatCount="indefinite"/>
  </circle>
  <circle cx="1100" cy="200" r="1.2" fill="#10B981" opacity="0.35">
    <animate attributeName="cx" from="1100" to="900" dur="9s" repeatCount="indefinite"/>
  </circle>
 
  <!-- LEFT SECTION: ASCII ART -->
  <g id="asciiSection">
    <!-- ASCII Container with float animation -->
    <g transform="translate(60, 100)">
      <animateTransform attributeName="transform" type="translate" 
        values="60, 100; 60, 95; 60, 100" dur="4s" repeatCount="indefinite" additive="sum"/>
      
      <!-- ASCII Art -->
      <text x="0" y="0" font-family="'Courier New', monospace" font-size="12" font-weight="bold" fill="url(#asciiGradient)" letter-spacing="2" opacity="0.95">
        <tspan x="0" dy="20">   ╔═══════════════╗</tspan>
        <tspan x="0" dy="20">   ║  👨‍💻  ROHIT  ║</tspan>
        <tspan x="0" dy="20">   ║   AI • ML     ║</tspan>
        <tspan x="0" dy="20">   ║   FULLSTACK   ║</tspan>
        <tspan x="0" dy="20">   ╚═══════════════╝</tspan>
        <tspan x="0" dy="25">   &lt;code&gt;</tspan>
        <tspan x="0" dy="20">   ✦ Python</tspan>
        <tspan x="0" dy="20">   ✦ React.js</tspan>
        <tspan x="0" dy="20">   ✦ ML/AI</tspan>
        <tspan x="0" dy="25">   &lt;/code&gt;</tspan>
      </text>
 
      <!-- ASCII Glow -->
      <rect x="-10" y="-30" width="280" height="290" fill="none" stroke="url(#mainGradient)" stroke-width="1.5" opacity="0.3" filter="url(#glowPulse)"/>
    </g>
 
    <!-- Scanline Effect -->
    <rect x="0" y="0" width="450" height="610" fill="none" stroke="rgba(34,211,238,0.05)" stroke-width="1" stroke-dasharray="2,2">
      <animate attributeName="stroke-dashoffset" from="0" to="100" dur="2s" repeatCount="indefinite"/>
    </rect>
  </g>
 
  <!-- CENTER DIVIDER -->
  <line x1="450" y1="50" x2="450" y2="560" stroke="rgba(255,255,255,0.08)" stroke-width="1"/>
  <circle cx="450" cy="305" r="3" fill="url(#mainGradient)" opacity="0.6" filter="url(#glowPulse)"/>
 
  <!-- RIGHT SECTION: TERMINAL WINDOW -->
  <g id="terminalSection" transform="translate(500, 60)">
    <!-- Terminal Background Panel -->
    <rect x="0" y="0" width="640" height="520" rx="12" fill="#0F172A" opacity="0.8" stroke="rgba(255,255,255,0.08)" stroke-width="1.5"/>
    
    <!-- Shimmer Border -->
    <rect x="0" y="0" width="640" height="520" rx="12" fill="none" stroke="url(#mainGradient)" stroke-width="1" opacity="0" filter="url(#glow)">
      <animate attributeName="opacity" from="0.2" to="0.6" dur="3s" repeatCount="indefinite"/>
    </rect>
 
    <!-- Glass Reflection -->
    <rect x="0" y="0" width="640" height="100" rx="12" fill="white" opacity="0.03"/>
 
    <!-- Terminal Header -->
    <rect x="0" y="0" width="640" height="40" rx="12" fill="rgba(255,255,255,0.03)" stroke-bottom="1px solid rgba(255,255,255,0.08)"/>
    <circle cx="20" cy="20" r="4" fill="#EF4444" opacity="0.7"/>
    <circle cx="40" cy="20" r="4" fill="#FBBF24" opacity="0.7"/>
    <circle cx="60" cy="20" r="4" fill="#10B981" opacity="0.7"/>
    <text x="320" y="25" font-family="'Courier New', monospace" font-size="11" fill="#94A3B8" text-anchor="middle">ROHIT@GITHUB</text>
 
    <!-- Content -->
    <g id="terminalContent" transform="translate(20, 55)">
      <!-- Greeting -->
      <text x="0" y="0" font-family="'Courier New', monospace" font-size="13" font-weight="bold" fill="#22D3EE">
        <tspan>Hi 👋 I'm <tspan fill="url(#textGradient)">Rohit Kumar R</tspan></tspan>
      </text>
 
      <!-- Typing Role with cursor -->
      <text x="0" y="30" font-family="'Courier New', monospace" font-size="12" fill="#F8FAFC">
        <tspan fill="#7C3AED">$ </tspan>
        <tspan id="role">AI Engineer | ML Dev</tspan>
        <tspan fill="#22D3EE" font-weight="bold">
          <animate attributeName="opacity" from="1" to="0" dur="0.8s" repeatCount="indefinite"/>
          │
        </tspan>
      </text>
 
      <!-- Info Items with sequential reveal -->
      <g id="infoItems" opacity="0">
        <animate attributeName="opacity" from="0" to="1" dur="1s" begin="2s" fill="freeze"/>
        
        <text x="0" y="65" font-family="'Courier New', monospace" font-size="11" fill="#94A3B8">
          <tspan fill="#7C3AED">📍 </tspan>Vellore, Tamil Nadu
        </text>
 
        <text x="0" y="85" font-family="'Courier New', monospace" font-size="11" fill="#94A3B8">
          <tspan fill="#7C3AED">🎓 </tspan>B.Tech CSE (AI & ML) - SRMIST
        </text>
 
        <text x="0" y="105" font-family="'Courier New', monospace" font-size="11" fill="#94A3B8">
          <tspan fill="#7C3AED">⚡ </tspan>Building AI solutions with impact
        </text>
 
        <text x="0" y="125" font-family="'Courier New', monospace" font-size="11" fill="#94A3B8">
          <tspan fill="#7C3AED">🌐 </tspan>Portfolio: rohit1911-code.github.io
        </text>
 
        <text x="0" y="145" font-family="'Courier New', monospace" font-size="11" fill="#94A3B8">
          <tspan fill="#7C3AED">📧 </tspan>rsarrsar919@gmail.com
        </text>
      </g>
 
      <!-- Skills Pills -->
      <g id="skills" opacity="0" transform="translate(0, 170)">
        <animate attributeName="opacity" from="0" to="1" dur="1s" begin="3s" fill="freeze"/>
 
        <text x="0" y="0" font-family="'Courier New', monospace" font-size="10" fill="#94A3B8" font-weight="bold">SKILLS</text>
 
        <!-- Skill Pill 1 -->
        <rect x="0" y="15" width="70" height="24" rx="12" fill="rgba(124,58,237,0.15)" stroke="rgba(124,58,237,0.5)" stroke-width="1" filter="url(#glow)">
          <animate attributeName="stroke-width" from="1" to="1.5" dur="2s" repeatCount="indefinite"/>
        </rect>
        <text x="35" y="31" font-family="'Courier New', monospace" font-size="10" fill="#7C3AED" text-anchor="middle" font-weight="bold">Python</text>
 
        <!-- Skill Pill 2 -->
        <rect x="85" y="15" width="70" height="24" rx="12" fill="rgba(34,211,238,0.15)" stroke="rgba(34,211,238,0.5)" stroke-width="1" filter="url(#glow)">
          <animate attributeName="stroke-width" from="1" to="1.5" dur="2.2s" repeatCount="indefinite"/>
        </rect>
        <text x="120" y="31" font-family="'Courier New', monospace" font-size="10" fill="#22D3EE" text-anchor="middle" font-weight="bold">React.js</text>
 
        <!-- Skill Pill 3 -->
        <rect x="170" y="15" width="70" height="24" rx="12" fill="rgba(16,185,129,0.15)" stroke="rgba(16,185,129,0.5)" stroke-width="1" filter="url(#glow)">
          <animate attributeName="stroke-width" from="1" to="1.5" dur="2.4s" repeatCount="indefinite"/>
        </rect>
        <text x="205" y="31" font-family="'Courier New', monospace" font-size="10" fill="#10B981" text-anchor="middle" font-weight="bold">FastAPI</text>
 
        <!-- Skill Pill 4 -->
        <rect x="255" y="15" width="70" height="24" rx="12" fill="rgba(124,58,237,0.15)" stroke="rgba(124,58,237,0.5)" stroke-width="1" filter="url(#glow)">
          <animate attributeName="stroke-width" from="1" to="1.5" dur="2.1s" repeatCount="indefinite"/>
        </rect>
        <text x="290" y="31" font-family="'Courier New', monospace" font-size="10" fill="#7C3AED" text-anchor="middle" font-weight="bold">TensorFlow</text>
 
        <!-- Skill Pill 5 -->
        <rect x="0" y="50" width="70" height="24" rx="12" fill="rgba(34,211,238,0.15)" stroke="rgba(34,211,238,0.5)" stroke-width="1" filter="url(#glow)">
          <animate attributeName="stroke-width" from="1" to="1.5" dur="2.3s" repeatCount="indefinite"/>
        </rect>
        <text x="35" y="66" font-family="'Courier New', monospace" font-size="10" fill="#22D3EE" text-anchor="middle" font-weight="bold">PostgreSQL</text>
 
        <!-- Skill Pill 6 -->
        <rect x="85" y="50" width="70" height="24" rx="12" fill="rgba(16,185,129,0.15)" stroke="rgba(16,185,129,0.5)" stroke-width="1" filter="url(#glow)">
          <animate attributeName="stroke-width" from="1" to="1.5" dur="2.2s" repeatCount="indefinite"/>
        </rect>
        <text x="120" y="66" font-family="'Courier New', monospace" font-size="10" fill="#10B981" text-anchor="middle" font-weight="bold">Git/GitHub</text>
 
        <!-- Skill Pill 7 -->
        <rect x="170" y="50" width="70" height="24" rx="12" fill="rgba(124,58,237,0.15)" stroke="rgba(124,58,237,0.5)" stroke-width="1" filter="url(#glow)">
          <animate attributeName="stroke-width" from="1" to="1.5" dur="2.4s" repeatCount="indefinite"/>
        </rect>
        <text x="205" y="66" font-family="'Courier New', monospace" font-size="10" fill="#7C3AED" text-anchor="middle" font-weight="bold">Docker</text>
      </g>
 
      <!-- Social Icons -->
      <g id="socialIcons" opacity="0" transform="translate(0, 300)">
        <animate attributeName="opacity" from="0" to="1" dur="1s" begin="4s" fill="freeze"/>
 
        <!-- GitHub -->
        <circle cx="25" cy="25" r="18" fill="rgba(34,211,238,0.15)" stroke="rgba(34,211,238,0.4)" stroke-width="1.5" filter="url(#glow)">
          <animate attributeName="r" from="18" to="20" dur="2s" repeatCount="indefinite"/>
        </circle>
        <text x="25" y="31" font-size="14" text-anchor="middle" fill="#22D3EE">🐙</text>
 
        <!-- LinkedIn -->
        <circle cx="70" cy="25" r="18" fill="rgba(124,58,237,0.15)" stroke="rgba(124,58,237,0.4)" stroke-width="1.5" filter="url(#glow)">
          <animate attributeName="r" from="18" to="20" dur="2.2s" repeatCount="indefinite"/>
        </circle>
        <text x="70" y="31" font-size="14" text-anchor="middle" fill="#7C3AED">in</text>
 
        <!-- Email -->
        <circle cx="115" cy="25" r="18" fill="rgba(16,185,129,0.15)" stroke="rgba(16,185,129,0.4)" stroke-width="1.5" filter="url(#glow)">
          <animate attributeName="r" from="18" to="20" dur="2.4s" repeatCount="indefinite"/>
        </circle>
        <text x="115" y="31" font-size="14" text-anchor="middle" fill="#10B981">✉</text>
 
        <!-- Portfolio -->
        <circle cx="160" cy="25" r="18" fill="rgba(34,211,238,0.15)" stroke="rgba(34,211,238,0.4)" stroke-width="1.5" filter="url(#glow)">
          <animate attributeName="r" from="18" to="20" dur="2.1s" repeatCount="indefinite"/>
        </circle>
        <text x="160" y="31" font-size="14" text-anchor="middle" fill="#22D3EE">🌐</text>
      </g>
    </g>
 
    <!-- Bottom Glow -->
    <rect x="0" y="450" width="640" height="70" rx="12" fill="url(#bgGlow1)" opacity="0.2"/>
  </g>
 
  <!-- GLOBAL SCANLINE EFFECT -->
  <rect width="1180" height="610" fill="none" mask="url(#scanlineMask)" stroke="rgba(34,211,238,0.03)" stroke-width="1"/>
 
  <!-- CREDITS -->
  <text x="1170" y="600" font-family="'Courier New', monospace" font-size="8" fill="#475569" text-anchor="end" opacity="0.6">Made with ❤️ | 2026</text>
</svg>
 
# 🚀 Rohit Kumar R | AI/ML & Web Dev Engineer

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/rohit1911-code/)
[![GitHub](https://img.shields.io/badge/GitHub-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/rohit1911-code)
[![Portfolio](https://img.shields.io/badge/Portfolio-%23FF00FF.svg?style=for-the-badge&logo=firefox&logoColor=white)](https://rohit1911-code.github.io)
[![Email](https://img.shields.io/badge/Email-%23E34234.svg?style=for-the-badge&logo=gmail&logoColor=white)](mailto:rsarrsar919@gmail.com)

**🎓 B.Tech CSE (AI & ML Specialization) @ SRM Institute of Science and Technology**  
**📍 Vellore, Tamil Nadu, India** | **📱 +91 9486477318**

</div>

---

## ✨ About Me

> *Passionate AI/ML Engineer & Full-Stack Developer building intelligent solutions with social impact*

I'm a 3ed-year Computer Science student with expertise in **AI/ML**, **Web Development**, and **IoT**. I specialize in creating end-to-end applications that solve real-world problems—from intelligent assistants to data-driven systems. My recent internships at **Decode Labs** and **SkillCraft Technology** sharpened my skills across AI pipelines and modern web architectures.

---

## 🎯 Current Focus

Building my **Final Year Major Project** with three social-impact candidates:

<table>
<tr>
<td>

### 🏥 AI Elder Care Companion
Smart fall detection & health monitoring for elderly care

</td>
<td>

### 👶 AI Child Development Tracker
Real-time tracking of developmental milestones with parent insights using ML

</td>
<td>

### 🚨 Women Safety SOS App
Instant emergency response system — Web + Mobile

</td>
</tr>
</table>

---

## 💻 Tech Stack

### Languages & Frameworks
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34C26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=java&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)

### AI/ML & Data
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)

### Databases & Backend
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-00758F?style=flat-square&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-13AA52?style=flat-square&logo=mongodb&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)

### DevOps & Tools
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![Render](https://img.shields.io/badge/Render-46E3B7?style=flat-square&logo=render&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD701?style=flat-square&logo=huggingface&logoColor=black)

**Proficiency:** Python (90%) | HTML (90%) | CSS (85%) | SQL/MySQL (85%) | JavaScript (80%) | Java (80%)

---

## 🏆 Recent Experience

### 💼 Internships (June–July 2026)

| Role | Company | Duration | Focus |
|------|---------|----------|-------|
| 🤖 **AI Intern** | Decode Labs | Jun–Jul 2026 | ML Models, Data Pipeline |
| 💻 **Web Dev Intern** | SkillCraft Technology | Jun–Jul 2026 | Full-Stack Development |
| 🌐 **Web Dev Intern** | SaiKet Systems | Jun–Jul 2026 | REST APIs, Backend |

---

## 🚀 Featured Projects

### 1. 🧠 AI-Enhanced Smart Crowd Monitoring & Risk Prediction
**Jan 2026** | Python • ML • REST API • Database

Intelligent system predicting crowd risks in real-time using machine learning models and geospatial analysis.

---

### 2. 🌊 IoT-Based Drainage Monitoring System
**Feb 2026** | ESP8266 • IoT • Embedded Systems

Smart sensors monitoring drainage levels with real-time alerts and predictive overflow detection.

---

### 3. 💬 Rule-Based AI Chatbot
**In Progress** | Python • NLP • AI

Intelligent conversational agent with context awareness and knowledge base integration.

[View Repository](https://github.com/rohit1911-code/Rule-Based-AI-Chatbot)

---

### 4. 📊 Data Classification AI
**Production** | Python • ML • Classification

Advanced ML pipeline for multi-class data classification with model optimization.

[View Repository](https://github.com/rohit1911-code/Data-Classification-AI)

---

### 5. 🎓 Student Management System
**Dec 2025** | Python • MySQL • HTML/CSS

Full-stack student information system with database management and reporting.

---

### 6. 🗳️ E-Voting System
**Oct 2025** | MySQL • HTML • Backend

Secure electronic voting platform with integrity checks and audit trails.

---

### 7. 💳 Billing System
**Aug 2025** | Python • MySQL • CSS

Automated billing and invoice generation with payment tracking.

---

## 🎓 Education & Certifications

### 🎓 Degree
- **B.Tech in Computer Science Engineering** (AI & ML Specialization)
- **SRM Institute of Science and Technology** (2024–2028)
- **CGPA:** 8.5/10

### 📜 Certifications & Programs

| Certification | Issuer | Date |
|--------------|--------|------|
| 🏅 **AI Traineeship** (Letter of Recommendation) | Maiyyam | Oct 2025 |
| 🏅 **Full-Stack MERN Development** | Maiyyam | Completed |
| 🏅 **Tata GenAI Data Analytics Simulation** | Tata Consultancy Services | 2026 |
| 🏅 **Tata GenAI Software Engineering Simulation** | Tata Consultancy Services | 2026 |
| 🏅 **Java Bug Hunt Participation** | Cintel/SRMIST | Mar 2026 |
| 🏅 **Lithos 2K26 Participation** | Unstop | Feb 2026 |
| 🏅 **Adobe India Hackathon** | Team Tech Titans | 2026 |

**Mentor:** Sanjith Baburaj (AI Traineeship Program)

---

## 🌍 Languages

| Language | Proficiency |
|----------|-------------|
| 🇬🇧 English | Proficient |
| 🇮🇳 Tamil | Native |
| 🇮🇳 Telugu | Advanced |
| 🇫🇷 French | Intermediate |

---

## 📊 GitHub Statistics

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=rohit1911-code&theme=tokyonight&show_icons=true&hide_border=true&count_private=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=rohit1911-code&theme=tokyonight&hide_border=true&layout=compact)

</div>

---

## 🎨 Featured Project: Personal Portfolio

A **self-contained HTML portfolio** featuring:
- ✨ Space navy, electric cyan & violet aesthetic
- 🌌 Animated particle background
- 🎨 Glassmorphism design cards
- 🌙 Dark/Light mode toggle
- ⚡ Smooth scroll animations
- 📱 Fully responsive design
- 🚀 Zero dependencies, offline-capable

**[View Live Portfolio](https://rohit1911-code.github.io)**

---

## 🤝 Let's Connect!

I'm always excited to collaborate on **AI/ML projects**, **full-stack applications**, and **socially impactful tech**.

<div align="center">

📧 **Email:** [rsarrsar919@gmail.com](mailto:rsarrsar919@gmail.com)  
💼 **LinkedIn:** [linkedin.com/in/rohit1911-code](https://linkedin.com/in/rohit1911-code/)  
🐙 **GitHub:** [github.com/rohit1911-code](https://github.com/rohit1911-code)  
🌐 **Portfolio:** [rohit1911-code.github.io](https://rohit1911-code.github.io)  
📞 **Phone:** +91 9486477318

</div>

---

<div align="center">

### ⭐ If you found this interesting, consider starring some repos!

**Last Updated:** July 2026 | Made with ❤️ from Vellore, India

</div>
