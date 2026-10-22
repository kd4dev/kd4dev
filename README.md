<div align="center">

# ⚡ Kedar Baswade
### Full-Stack & Backend Systems Engineer • ML/DL • Competitive Programmer

<a href="https://github.com/kd4dev">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=20&duration=2500&pause=1000&color=E7B832&center=true&vCenter=true&width=640&lines=Software+Engineer+%E2%80%A2+Backend+%26+Distributed+Systems;CS+(Artificial+Intelligence)+%40+VIT+Pune+(CGPA+8.82);LeetCode+Knight+(Peak+Rating%3A+1931+%7C+1000%2B+Solved);Building+Explainable+AI+(SHAP)+%26+Microservices;Event-Driven+Workflows+with+Zero-Polling+Architecture" alt="Typing SVG" />
</a>

<br/>

[![Portfolio](https://img.shields.io/badge/Portfolio-kedarbaswade.vercel.app-e7b832?style=for-the-badge&logo=vercel&logoColor=white)](https://kedarbaswade.vercel.app/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Kedar_Baswade-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kedar-baswade-784b95404/)
[![LeetCode Knight](https://img.shields.io/badge/LeetCode-Knight%20(1931)-FFA116?style=for-the-badge&logo=leetcode&logoColor=white)](https://leetcode.com/kd4dev/)
[![Codeforces](https://img.shields.io/badge/Codeforces-Pupil%20(1209)-1F8ACB?style=for-the-badge&logo=codeforces&logoColor=white)](https://codeforces.com/profile/kedarbaswade2802)
[![Email](https://img.shields.io/badge/Email-kedarbaswade2802@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:kedarbaswade2802@gmail.com)

</div>

---

### 🖥️ `$ whoami --verbose`

```yaml
identity:
  name: Kedar Baswade
  role: Full-Stack & Backend Systems Engineer
  education:
    degree: B.Tech in Computer Science (Artificial Intelligence)
    institution: Vishwakarma Institute of Technology (VIT), Pune
    cgpa: "8.82 / 10.0"
  competitive_programming:
    leetcode: Knight (Max Rating 1931 | 1000+ Problems Solved)
    codeforces: Pupil (Max Rating 1209)
  engineering_principles:
    - "Event-driven durable workflows > Wasteful cron polling"
    - "Microservices with strict contract validation & mock fallback resilience"
    - "Glass-box Explainable AI (SHAP) > Untrusted black boxes"
    - "Atomic I/O transactions & multi-document ACID safety"
```

---

### 🏗️ Interactive Architectural Showcases

Click each project below to reveal the **System Architecture Blueprint & Data Flow**:

<details open>
<summary><b>🔍 CampusFind — Lost & Found Recovery Platform (Next.js, MongoDB, Clerk, Vitest)</b></summary>
<br/>

> **Core Problem:** Campus lost-and-found is plagued by false claims, exposed personal numbers, and unverified handovers.  
> **Solution:** A stateful recovery pipeline secured by dual-party OTP validation and zero-leak in-app communications.

```
[Student Reports Item] ──► [Claim Filed with Proof] ──► [Owner Verification & Approval]
                                                                   │
                                                                   ▼
[Verified Handover Done] ◄── [Success] ◄── [6-Digit OTP Handover (30m Expiry, 3-Lockout)]
```

- **Architecture Highlights:** 8 normalized Mongoose models, server action boundaries, Clerk webhook user sync, and 20+ automated Vitest regression suites.
- 🔗 **Links:** [Source Code](https://github.com/kd4dev/campus-find) • [Live Production App](https://campus-find-blond.vercel.app)

</details>

<details open>
<summary><b>⚡ SubDub — Scalable Subscription Management Backend (Node.js, Express, Upstash, Arcjet)</b></summary>
<br/>

> **Core Problem:** Traditional recurring renewal checkers rely on persistent cron workers continuously polling the DB, wasting compute.  
> **Solution:** Serverless, event-driven durable workflows that sleep until target countdown intervals without background processes.

```
[Subscription Created] ──► [MongoDB ACID Transaction] ──► [Upstash Workflow Init]
                                                                  │
                                                          (Durable Sleep)
                                                                  │
[Nodemailer Dispatch] ◄── [Triggered: T-7d, T-5d, T-2d, T-1d] ◄───┘
```

- **Architecture Highlights:** 15+ versioned REST endpoints, bcrypt credential hashing, Arcjet token-bucket rate limiting + bot defense shield.
- 🔗 **Links:** [Source Code](https://github.com/kd4dev/backend-of-a-scalable-subscription-model)

</details>

<details open>
<summary><b>📊 Loan Approval Explainer — Explainable AI (XAI) Platform (FastAPI, Express, scikit-learn, SHAP)</b></summary>
<br/>

> **Core Problem:** ML credit scoring models act as black boxes; rejected applicants are never told *why* they were denied.  
> **Solution:** Decoupled microservice architecture marrying an Express API gateway with a FastAPI ML service producing per-applicant SHAP feature weights.

```
[Client Request] ──► [Express Gateway (Port 5000)] ──► [FastAPI Model Service (Port 8000)]
                           │ (Audit Log & Query History)         │
                           ▼                                     ▼
                      [MongoDB]                       [Random Forest / Logistic Reg]
                                                                 │
[SHAP Attribution Breakdown] ◄───────────────────────────────────┴── [TreeExplainer Kernel]
```

- **Architecture Highlights:** Reusable preprocessing pipeline on UCI Credit dataset, instant top-k contributing feature vectors, and mock-mode fallback for offline testing.
- 🔗 **Links:** [Source Code](https://github.com/kd4dev/loan_)

</details>

<details>
<summary><b>💻 Terminal Todo Manager — CLI & Keyboard-Driven TUI (Node.js, Ink, Commander)</b></summary>
<br/>

> **Core Problem:** CLI tools frequently corrupt flat-file state during unexpected terminal exits or concurrent writes.  
> **Solution:** Clean three-tier architecture (CLI/TUI ➔ Service Layer ➔ Repository) backed by atomic temporary-file-and-rename disk writes.

- **Architecture Highlights:** Interactive keyboard navigation powered by Ink (React inside terminal), query filtering across priorities, tags, and due dates.
- 🔗 **Links:** [Source Code](https://github.com/kd4dev/CLI-based-Todo)

</details>

---

### 🛠️ Technical Arsenal

<table>
  <tr>
    <td width="20%"><b>Languages</b></td>
    <td>
      <img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white" />
      <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
      <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
      <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
      <img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white" />
    </td>
  </tr>
  <tr>
    <td width="20%"><b>Backend & Web</b></td>
    <td>
      <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white" />
      <img src="https://img.shields.io/badge/Express.js-000000?style=flat-square&logo=express&logoColor=white" />
      <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white" />
      <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
      <img src="https://img.shields.io/badge/REST_APIs-005571?style=flat-square" />
      <img src="https://img.shields.io/badge/Microservices-232F3E?style=flat-square" />
      <img src="https://img.shields.io/badge/Clerk_Auth-6C47FF?style=flat-square&logo=clerk&logoColor=white" />
      <img src="https://img.shields.io/badge/Upstash_Workflow-00E599?style=flat-square&logo=upstash&logoColor=black" />
    </td>
  </tr>
  <tr>
    <td width="20%"><b>Databases & ORM</b></td>
    <td>
      <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
      <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" />
      <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" />
      <img src="https://img.shields.io/badge/Drizzle_ORM-C5F74F?style=flat-square&logo=drizzle&logoColor=black" />
      <img src="https://img.shields.io/badge/Mongoose-880000?style=flat-square" />
    </td>
  </tr>
  <tr>
    <td width="20%"><b>Machine Learning & XAI</b></td>
    <td>
      <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white" />
      <img src="https://img.shields.io/badge/SHAP-Explainable_AI-FF6F00?style=flat-square" />
      <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white" />
      <img src="https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white" />
      <img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white" />
    </td>
  </tr>
  <tr>
    <td width="20%"><b>Testing & DevOps</b></td>
    <td>
      <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" />
      <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
      <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" />
      <img src="https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white" />
      <img src="https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white" />
      <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white" />
    </td>
  </tr>
</table>

---

### 📊 Competitive Programming & Activity Telemetry

<div align="center">
  <table border="0">
    <tr>
      <td width="50%" align="center">
        <a href="https://leetcode.com/kd4dev/">
          <img src="https://leetcard.jacoblin.cool/kd4dev?theme=dark&font=IBM%20Plex%20Mono&ext=contest" alt="LeetCode Knight Rating" width="100%" />
        </a>
      </td>
      <td width="50%" align="center">
        <a href="https://github.com/kd4dev">
          <img src="https://github-readme-stats.vercel.app/api?username=kd4dev&show_icons=true&theme=radical&hide_border=true&count_private=true" alt="GitHub Stats" width="100%" />
        </a>
      </td>
    </tr>
    <tr>
      <td width="50%" align="center">
        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=kd4dev&layout=compact&theme=radical&hide_border=true" alt="Top Languages" width="100%" />
      </td>
      <td width="50%" align="center">
        <img src="https://github-readme-streak-stats.herokuapp.com/?user=kd4dev&theme=radical&hide_border=true" alt="GitHub Streak" width="100%" />
      </td>
    </tr>
  </table>
</div>

---

### 🏆 Milestones & Leadership

- 🏅 **LeetCode Knight**: Solved **1000+** algorithmic challenges with a peak contest rating of **1931**.
- ⚔️ **Codeforces Pupil**: Peak rating of **1209**.
- 🚀 **Hackathon Team Lead**: Spearheaded backend design, task delegation, and cross-service integration at **ODDO** and **Barclays** hackathons.
- 🎃 **Hacktoberfest 2024**: Recognized as a **Super Contributor**.

---

### 📬 Connect With Me

<div align="center">

[![Portfolio](https://img.shields.io/badge/Portfolio-Visit%20Website-e7b832?style=for-the-badge&logo=google-chrome&logoColor=white)](https://kedarbaswade.vercel.app/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kedar-baswade-784b95404/)
[![GitHub](https://img.shields.io/badge/GitHub-Follow%20%40kd4dev-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/kd4dev)
[![Gmail](https://img.shields.io/badge/Gmail-Send%20Message-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:kedarbaswade2802@gmail.com)

<br/>

```bash
# Terminal contact card
curl -sL https://kedarbaswade.vercel.app
```

</div>
