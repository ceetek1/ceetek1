<!-- ░░ HEADER ░░ -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,100:0f5132&height=190&section=header&text=Charles%20Chukwurah&fontColor=39FF14&fontSize=50&fontAlignY=36&desc=~%2Fceetek1%20%24%20build%20--with%20curiosity&descAlignY=56&descSize=18&animation=twinkling" alt="Charles Chukwurah banner" width="100%" />
</p>

<p align="center">
  <a href="https://ceetek1.up.railway.app/">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=22&duration=2800&pause=900&color=39FF14&center=true&vCenter=true&width=640&height=48&lines=%24+whoami;Software+Engineering+student+%40+PAU;Exploring+AI+%2F+Machine+Learning;Shipping+with+Python%2C+TypeScript%2C+C%2B%2B+%26+Rust;Open+to+opportunities+%E2%80%94+let's+talk!" alt="Typing intro" />
  </a>
</p>

<p align="center">
  <a href="https://ceetek1.up.railway.app/"><img src="https://img.shields.io/badge/Portfolio-ceetek1.up.railway.app-39FF14?style=for-the-badge&logo=railway&logoColor=39FF14&labelColor=0d1117" alt="Portfolio" /></a>
  <a href="https://www.linkedin.com/in/chukwurah-charles-652775377"><img src="https://img.shields.io/badge/LinkedIn-Connect-39FF14?style=for-the-badge&logo=linkedin&logoColor=39FF14&labelColor=0d1117" alt="LinkedIn" /></a>
  <a href="mailto:charles.chukwurah@pau.edu.ng"><img src="https://img.shields.io/badge/Email-Say%20hi-39FF14?style=for-the-badge&logo=gmail&logoColor=39FF14&labelColor=0d1117" alt="Email" /></a>
</p>

---

### `$ whoami`

```bash
charles@ceetek1:~$ cat about.json
{
  "name":     "Charles Chukwurah",
  "role":     "Software Engineering student @ Pan-Atlantic University (PAU)",
  "focus":    ["AI / Machine Learning", "Backend systems", "Full-stack apps"],
  "status":   "Open to internships and engineering roles",
  "contact":  "charles.chukwurah@pau.edu.ng"
}
```

---

### `$ cat stack.txt`

<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=python,ts,react,cpp,rust,java,fastapi,postgres,docker,git&theme=dark&perline=10" alt="Tech stack: Python, TypeScript, React, C++, Rust, Java, FastAPI, Postgres, Docker, Git" />
  </a>
</p>

---

### `$ ./featured --project officelog`

> **[OfficeLog](https://github.com/ceetek1/officelog)**: a tamper-proof attendance log for workers.
> Scan a rotating QR code at the entrance and confirm with Face ID. Your phone then shows a receipt: on time, or how many minutes late.

<p>
  <img src="https://img.shields.io/badge/FastAPI-0d1117?style=flat-square&logo=fastapi&logoColor=39FF14" alt="FastAPI" />
  <img src="https://img.shields.io/badge/PostgreSQL-0d1117?style=flat-square&logo=postgresql&logoColor=39FF14" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/React-0d1117?style=flat-square&logo=react&logoColor=39FF14" alt="React" />
  <img src="https://img.shields.io/badge/TypeScript-0d1117?style=flat-square&logo=typescript&logoColor=39FF14" alt="TypeScript" />
  <img src="https://img.shields.io/badge/WebAuthn%20Passkeys-0d1117?style=flat-square&logo=webauthn&logoColor=39FF14" alt="WebAuthn passkeys" />
  <img src="https://img.shields.io/badge/Docker-0d1117?style=flat-square&logo=docker&logoColor=39FF14" alt="Docker" />
  <img src="https://img.shields.io/badge/Railway-0d1117?style=flat-square&logo=railway&logoColor=39FF14" alt="Railway" />
</p>

<details>
<summary><b>▶ How a clock-in works</b> (click to expand)</summary>

<br/>

```mermaid
sequenceDiagram
    autonumber
    participant TV as 📺 Entrance TV
    participant P as 📱 Worker's phone
    participant API as ⚙️ FastAPI server
    participant DB as 🗄️ Postgres
    TV->>TV: Show QR (changes every 5s) + 6-digit code (every 30s)
    P->>TV: Scan the code
    P->>P: Confirm with Face ID (WebAuthn passkey)
    P->>API: Clock in with code + passkey
    API->>API: Code is current? Passkey matches the registered phone?
    API->>DB: Save the time as a new entry (records are never edited)
    API-->>P: Receipt: time + on time / minutes late
```

</details>

<details>
<summary><b>▶ How the code is put together</b> (click to expand)</summary>

<br/>

```mermaid
flowchart LR
    subgraph Clients
        Phone[📱 Worker / manager phone]
        MD[💻 Managing director]
        TV[📺 Entrance TV]
    end
    subgraph Image[🐳 One Docker image]
        SPA[React + TypeScript app]
        API[FastAPI backend]
    end
    DB[(Postgres)]
    Clients -- "pages" --> SPA
    Clients -- "/api/*" --> API
    API -- "restricted app role" --> DB
```

**Engineering decisions I'm proud of:**

- 🧪 **Pure attendance rules.** `app/rules/` never touches the database or the framework, and a test enforces it.
- ⏱️ **Injectable time.** Business code takes a `Clock` instead of calling `datetime.now()`, so tests can replay any moment of any day.
- 🔐 **Server-side roles.** Every endpoint declares its roles, and a test walks every router to check them.
- 📜 **Append-only history.** Paper-sheet corrections are added as new entries, and an activity log records every important action.

📖 [Read the architecture doc →](https://github.com/ceetek1/officelog/blob/main/docs/architecture.md)

</details>

---

### `$ ls ~/projects`

<details>
<summary><b>▶ More things I've built</b> (click to expand)</summary>

<br/>

| Project | What it is | Stack |
| --- | --- | --- |
| [Store_Man](https://github.com/ceetek1/Store_Man) | A command-line key-value store | C++ |
| [mini-ledger](https://github.com/ceetek1/mini-ledger) | Learning how banking systems actually move money | — |
| [movierecomender](https://github.com/ceetek1/movierecomender) | A machine-learning movie recommender (learning project) | ML |
| [visma](https://github.com/ceetek1/visma) | Visitor management: registers visitors, purpose, host, and check-in/out times | — |
| [simi](https://github.com/ceetek1/simi) | Student CGPA planner | — |
| [ConflictBridge_App](https://github.com/ceetek1/ConflictBridge_App) | App project | Python |
| [Tasktion_App](https://github.com/ceetek1/Tasktion_App) | App project | Python |
| [Latonia-website](https://github.com/ceetek1/Latonia-website) | Website | JavaScript |
| [My_portfolio](https://github.com/ceetek1/My_portfolio) | Source for my portfolio site | JavaScript |

</details>

---

### `$ git log --stats`

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=ceetek1&show_icons=true&hide_border=true&bg_color=0d1117&title_color=39FF14&icon_color=39FF14&text_color=c9d1d9&ring_color=39FF14&rank_icon=github" alt="GitHub stats" height="165" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=ceetek1&layout=compact&hide_border=true&bg_color=0d1117&title_color=39FF14&text_color=c9d1d9&langs_count=6" alt="Top languages" height="165" />
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=ceetek1&hide_border=true&background=0d1117&ring=39FF14&fire=39FF14&currStreakLabel=39FF14&sideLabels=c9d1d9&currStreakNum=c9d1d9&sideNums=c9d1d9&dates=8b949e&stroke=30363d" alt="GitHub streak" />
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/ceetek1/ceetek1/output/github-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/ceetek1/ceetek1/output/github-snake.svg" />
    <img alt="Snake eating my contribution graph" src="https://raw.githubusercontent.com/ceetek1/ceetek1/output/github-snake-dark.svg" />
  </picture>
</p>

---

### `$ ./contact.sh`

<details>
<summary><b>▶ Recruiter quick-start</b> (click to expand)</summary>

<br/>

```bash
charles@ceetek1:~$ ./contact.sh --help
  --portfolio   https://ceetek1.up.railway.app
  --linkedin    linkedin.com/in/chukwurah-charles-652775377
  --email       charles.chukwurah@pau.edu.ng
  --start-here  github.com/ceetek1/officelog   # best example of my work
```

I'm open to internships and engineering roles. Email is the fastest way to reach me.

</details>

<!-- ░░ FOOTER ░░ -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f5132,100:0d1117&height=110&section=footer" alt="" width="100%" />
</p>
