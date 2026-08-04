<h1 align="center">whoami: Anmol Gupta</h1>
<h3 align="center">Offensive Security | Red Teaming | Full-Time CTF Player</h3>

<p align="center">
  <img src="https://img.shields.io/badge/eJPTv3-Certified-red?style=for-the-badge&logo=ine&logoColor=white" />
  <img src="https://img.shields.io/badge/Status-Open_to_Full--Time_Roles-brightgreen?style=for-the-badge" />
</p>

---

### `0x00` root@anmol:~$ cat about.txt

```
> 3rd-year CS undergrad, Cambridge Institute of Technology, Bengaluru (Class of 2027)
> Specializing in offensive security — recon, exploitation, and detection engineering
> eJPTv3 certified | targeting Red Team & Penetration Testing roles
> Full-time CTF player — PicoCTF, TryHackMe
```

---

### `0x01` Flagship Projects

**🛰️ AdaptiveScan** — Continuous Attack Surface Management & Exposure Intelligence
Built to give security teams a live, continuously-updated map of their exposure rather than a point-in-time scan — the shift from periodic pentests to always-on ASM.

**🛡️ SentinelCrypt EDR** — AI-Assisted Ransomware Detection & Response
Endpoint detection tooling that layers ML-driven behavioral analysis on top of traditional signature detection to catch ransomware earlier in the kill chain.
`github.com/saloni1225/ransomware`

---

### `0x02` Field Work

Real recon, not just lab boxes. Structured methodology across live targets:

```bash
$ recon-flow
├── subdomain enum      → httpx
├── vuln scanning        → nuclei, nikto
├── manual analysis       → CSP / header review
└── findings              → misconfigured CSP, exposed unauth APIs, unprotected subdomains
```

Toolbelt: `Burp Suite Pro` `Kali Linux` `Nmap` `Metasploit` `Wireshark` `OWASP ZAP`

---

### `0x03` Currently

```
[+] Learning:      Advanced Penetration Testing, Red Team Ops, Threat Hunting
[+] Collaborating: Security research, OSS security tooling, CTF teams
[+] Ask me about:  Ethical hacking, Python, Linux internals, web app security
```

---

### `0x04` Stats

<p align="center">
  <img src="https://github-readme-stats.shion.dev/api?username=anmoliot&theme=blue_navy&hide_border=false&include_all_commits=true&count_private=true" />
</p>
<p align="center">
  <img src="https://streak-stats.demolab.com/?user=anmoliot&theme=blue_navy&hide_border=false" />
</p>
<p align="center">
  <img src="https://github-readme-stats.shion.dev/api/top-langs/?username=anmoliot&theme=blue_navy&hide_border=false&include_all_commits=true&count_private=true&layout=compact" />
</p>

---

### `0x05` Connect

<p align="center">
  <a href="https://www.linkedin.com/in/anmol-gupta-729b7a269/"><img src="https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="https://cv-anmolgupta.netlify.app"><img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white" /></a>
  <a href="mailto:anmolgupta.nick@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" /></a>
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=anmoliot&icon=0&color=0" />
</p>

# .github/workflows/snake.yml
name: Generate Snake
on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch: {}
  push:
    branches: [ main ]

jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk@v3
        with:
          github_user_name: anmoliot
          outputs: dist/github-contribution-grid-snake.svg
      - uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
