<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,40:1a1a2e,70:e94560,100:f5a623&height=200&section=header&text=KuroShinHQ&fontSize=72&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Systems+thinker.+AI+builder.+Ships+to+production.&descAlignY=60&descSize=18&descColor=f5a623" />

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=15&duration=2500&pause=600&color=F5A623&center=true&vCenter=true&width=750&height=40&lines=Reverse-engineered+a+commercial+LLM+protocol+via+mitmproxy;Scraped+10+products+in+2.5s+with+0%25+bot+detection+rate;Designed+a+custom+8-bit+CPU+ISA+%2B+language+from+scratch;97%2F97+tests+passing+on+a+local+35B+param+LLM+system" alt="Typing SVG" />

<br/><br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/yasin-yagci-dataqa)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/kuroshinhq)
[![Email](https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ulucayto456@gmail.com)
[![Views](https://komarev.com/ghpvc/?username=KuroShinHQ&color=f5a623&style=for-the-badge&label=VIEWS)](https://github.com/KuroShinHQ)

</div>

---

```
╔══════════════════════════════════════════════════════════════════╗
║  > kuroshin --status                                             ║
║                                                                  ║
║  Kuroshin OS v11.33.1  ·  Qwen3-35B-A3B IQ4_XS  ·  ctx=256K    ║
║  ──────────────────────────────────────────────────────────────  ║
║  Iron Inquisitor    97/97 PASS    ████████████████  100.0%       ║
║  Active tools       26/26         ████████████████  100.0%       ║
║  VRAM usage         6.2/8.0 GB    █████████████░░░   77.5%       ║
║  KuroRecon scrape   10 products   ████████████████    2.5s       ║
║  Cloud dependency   $0.00/month   ████████████████  LOCAL        ║
╚══════════════════════════════════════════════════════════════════╝
```

---

## The Story

```
Electrician  ──────────────────────────────►  AI Developer
     ⚡                                              🤖
  read schematics                            read attention maps
  wire circuits                              wire neural nets
  debug with multimeter                      debug with logs
  build with hands                           build with code
```

> Same obsession with how systems work. Different domain.
> **Everything I build is designed for production. Real constraints, real results.**

---

## Projects

<table>
<tr>
<td valign="top" width="50%">

### Kuroshin OS
**Autonomous AI assistant — fully local, $0 cloud**

> **Challenge:** 35B parameter model on 8GB VRAM.
> **Solution:** IQ4_XS quantization + GQA → fits in 6.2GB, 256K context window.
> **Result:** 97/97 tests passing. Outperforms GPT-3.5 on domain tasks.

- 26-tool Telegram agent (market research, scraping, security)
- MIRROR architecture — Thinker-Talker dual-process inner monologue
- RAG memory · KILIÇ-KALKAN v7 security layer
- Multi-agent orchestration via LangGraph

`Python` `llama.cpp` `ChromaDB` `Docker` `Telegram Bot API`

<details>
<summary>🐛 Real debug log — Chancellor crash recovery</summary>

```log
[14:32:11] ERROR   run_tool: market_master timeout (>240s)
[14:32:11] INFO    Sending interim report to Telegram...
[14:32:14] INFO    SYSTEM_PAUSED.flag detected — entering retry loop
[14:32:44] INFO    Chancellor PID 52500 → restart initiated
[14:32:51] INFO    Modules reloaded — sys.modules cache cleared
[14:32:53] SUCCESS market_master online — inject test PASS
```

*Root cause: Python module cache serving stale bytecode after hot-patch.*
*Fix: setsid restart script + chancellor.log TELEGRAM_OUT hook.*

</details>

</td>
<td valign="top" width="50%">

### KuroRecon
**Turkish e-commerce price intelligence toolkit**

> **Challenge:** Playwright flagged as bot on Trendyol/HB within 3 requests.
> **Solution:** `curl_cffi` Chrome124 TLS fingerprint spoof + Akamai bypass.
> **Result:** 0% detection rate. 10 products scraped in 2.5s, $0 infra cost.

- Trendyol · Hepsiburada · Sahibinden · Epey
- Cookie + session management for authenticated access
- Anti-bot: TLS impersonation, delay jitter, browser headers
- CSV/JSON export — drop-in for business reporting

`Playwright` `curl_cffi` `BeautifulSoup` `Python`

<details>
<summary>🐛 Real debug log — Sahibinden 429 bypass</summary>

```log
[12:41:03] INFO    fetch_sahibinden_direct → cookies loaded (44)
[12:41:05] WARNING HTTP 429 — rate limit hit, bot signal detected
[12:41:05] INFO    _sahib_bot_mu(): confidence=0.91 → switching strategy
[12:41:05] INFO    Ping-Pong: sending interim report, sleeping 300s
[12:46:07] INFO    Retry 1/3 — delay jitter: 7.2s
[12:46:15] SUCCESS 142 listings parsed — elapsed: 157.1s
```

*Root cause: Sahibinden CF bot fingerprinting on rapid sequential requests.*
*Fix: Exponential backoff + browser header rotation + Ping-Pong retry.*

</details>

</td>
</tr>
<tr>
<td valign="top" width="50%">

### KuroShinVM
**Custom 8-bit CPU architecture**

> **Challenge:** Design a complete ISA from scratch — registers, opcodes, assembler.
> **Solution:** 5-register system (PC, ACC, X, Y, SP), 11 opcodes, LIFO stack.
> **Result:** Full Fetch-Decode-Execute pipeline. KuroC language. Docker <5s build.

- 256-byte linear address space · 16-byte stack · 16-byte VRAM
- KuroC custom language: hex/decimal, comments, loop constructs
- Cyberpunk Unicode terminal UI with ANSI 256-color scheme
- Roadmap: KuroShinOS microkernel (VFS · IPC · MMU)

`Python` `Docker` `Custom ISA`

</td>
<td valign="top" width="50%">

### AI-Model-Scanner
**ML training experiment analyzer**

> **Challenge:** 9,109 files with inconsistent log formats, no schema.
> **Solution:** Multi-pattern regex engine — 50+ patterns, 6 file formats.
> **Result:** 3,036 experiments extracted. Found: AdamW 89% success, OOM #1 failure.

- Zero external dependencies — pure Python stdlib
- Extracts: model, optimizer, LR, batch size, device, accuracy, loss
- Insight: only 10.3% of training runs succeed without tuning
- Outputs: human-readable TXT + machine-readable JSON

`Python` `Regex` `JSON`

</td>
</tr>
<tr>
<td valign="top" width="50%">

### Kuroshin-CLI
**LLM tool-use protocol reverse-engineering**

> **Challenge:** Commercial LLM tool-calling protocol was undocumented.
> **Solution:** mitmproxy traffic interception → decoded exact JSON schema.
> **Result:** Gemma LoRA fine-tuned on the schema. 85/100 production score at 1/10th cost.

- Decoded parallel multi-tool orchestration JSON format
- LM Studio (gpt-oss-20b) + Ollama (qwen2.5:7b) backends
- Permission system: Plan / Default / AcceptEdits / Bypass
- Real token counting — critical for cost-aware architecture

`mitmproxy` `LM Studio` `Ollama` `Python`

</td>
<td valign="top" width="50%">

### Always Building

```python
while True:
    idea = observe_problem()
    if worth_solving(idea):
        ship(build(idea))
    sleep(0)  # never
```

⭐ Star to follow updates

</td>
</tr>
</table>

---

## Skills

<div align="center">

<sub><b>Languages & Runtimes</b></sub><br/>
<a href="https://skillicons.dev"><img src="https://skillicons.dev/icons?i=python,go,java,nodejs,cpp,cs,bash" /></a>

<br/>

<sub><b>AI · ML · Infrastructure</b></sub><br/>
<a href="https://skillicons.dev"><img src="https://skillicons.dev/icons?i=docker,linux,git,sqlite,pytorch,arduino,vscode" /></a>

<br/>

<sub><b>Creative · Hardware · GameDev</b></sub><br/>
<a href="https://skillicons.dev"><img src="https://skillicons.dev/icons?i=blender,unity,unreal,androidstudio,ae,ps,figma" /></a>

<br/><br/>

![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![curl_cffi](https://img.shields.io/badge/curl__cffi-TLS_spoof-critical?style=flat-square)
![Telegram](https://img.shields.io/badge/Telegram_Bot-26A5E4?style=flat-square&logo=telegram&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-local_LLM-black?style=flat-square)
![ChromaDB](https://img.shields.io/badge/ChromaDB-vector_DB-FF6F00?style=flat-square)
![CUDA](https://img.shields.io/badge/CUDA_11.8-76B900?style=flat-square&logo=nvidia&logoColor=white)
![mitmproxy](https://img.shields.io/badge/mitmproxy-protocol_RE-blueviolet?style=flat-square)
![KiCad](https://img.shields.io/badge/KiCad-PCB_design-314CB0?style=flat-square&logo=kicad&logoColor=white)
![ESP32](https://img.shields.io/badge/ESP32-Espressif-E7352C?style=flat-square&logo=espressif&logoColor=white)

</div>

---

## Currently Exploring

```python
research = {
    "LLM":      "Abliterated Qwen3/Gemma4 on 8GB VRAM — quantization limits vs quality",
    "Arch":     "MIRROR: Thinker-Talker dual-process inner monologue for autonomous agents",
    "Agents":   "Idle loop + emotional state modeling → proactive AI behavior",
    "Bypass":   "nodriver vs camoufox vs curl_cffi — 2026 anti-bot landscape",
    "Business": "Self-sustaining AI tools with $0 infra — scraping as a service model",
}
```

---

## Beyond Code

> *When not shipping code, building something else entirely.*

| Hardware | Creative | Games |
|---|---|---|
| PCB design · KiCad · Proteus · EasyEDA | Digital art · CLIP STUDIO · Live2D | FromSoftware fan (Elden Ring · Sekiro) |
| 3D printing · Ender 3 S1 · PETG/PLA | Motion graphics · After Effects | Colony survival · RimWorld (all DLC) · Kenshi |
| FPV drone tuning · Betaflight | 3D modeling · Blender · Cinema 4D | Indie builder · Stardew · Terraria |
| Electronics sim · Fritzing · Arduino | Game dev · Unity · Unreal | Horror · RE7 · Outlast · Darkest DD |

---

## Stats

<div align="center">

[![trophy](https://github-profile-trophy.vercel.app/?username=KuroShinHQ&theme=dracula&column=7&no-frame=true&no-bg=true&margin-w=6)](https://github.com/ryo-ma/github-profile-trophy)

<br/>

<img height="155" src="https://github-readme-stats.vercel.app/api?username=KuroShinHQ&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&bg_color=0d1117&title_color=f5a623&icon_color=f5a623&text_color=c9d1d9" />
<img height="155" src="https://github-readme-stats.vercel.app/api/top-langs/?username=KuroShinHQ&layout=compact&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=f5a623&text_color=c9d1d9" />

<br/>

[![Streak](https://streak-stats.demolab.com?user=KuroShinHQ&theme=tokyonight&hide_border=true&background=0d1117&ring=f5a623&fire=f5a623&currStreakLabel=f5a623&sideLabels=c9d1d9&dates=c9d1d9)](https://git.io/streak-stats)

<br/>

[![Activity](https://github-readme-activity-graph.vercel.app/graph?username=KuroShinHQ&theme=tokyo-night&bg_color=0d1117&color=f5a623&line=e94560&point=f5a623&area=true&hide_border=true&custom_title=Contribution%20Activity)](https://github.com/Ashutosh00710/github-readme-activity-graph)

<br/>

<img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=KuroShinHQ&theme=tokyonight" width="100%"/>
<img src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=KuroShinHQ&theme=tokyonight" height="150"/>
<img src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=KuroShinHQ&theme=tokyonight" height="150"/>
<img src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=KuroShinHQ&theme=tokyonight" height="150"/>
<img src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=KuroShinHQ&theme=tokyonight&utcOffset=3" height="150"/>

</div>

---

<div align="center">

*Web scraping · AI automation · LLM tooling · Data pipelines · Electronics*

**Got a project? Open an issue or drop an email.**

</div>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:f5a623,50:e94560,100:0d1117&height=130&section=footer&animation=twinkling" />