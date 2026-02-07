---
# the default layout is 'page'
title: "About"
permalink: /about/
layout: single
author_profile: true
---


<div class="cyber-terminal">
  <div class="terminal-header">
    <div class="left">
      <span class="dot red"></span>
      <span class="dot yellow"></span>
      <span class="dot green"></span>
      <span class="title">About - secure shell</span>
    </div>
    <div class="right">ACTIVE</div>
  </div>

  <div class="terminal-body">
    <div id="console"></div><span class="cursor"></span>
  </div>
</div>

<style>
:root {
  --bg: #0b0d10;
  --panel: #111418;
  --border: #1f2933;
  --blue: #4fc3f7;
  --green: #2ecc71;
  --red: #ff5f56;
  --yellow: #ffbd2e;
}

.cyber-terminal {
  background: linear-gradient(180deg, #0b0d10, #07090c);
  border: 1px solid var(--border);
  border-radius: 10px;
  box-shadow: 0 30px 80px rgba(0,0,0,.85);
  font-family: 'JetBrains Mono', monospace;
  color: #e5e7eb;
  margin: 40px 0;
  overflow: hidden;
}

/* HEADER */
.terminal-header {
  background: linear-gradient(180deg, #141820, #0d1117);
  border-bottom: 1px solid #1f2933;
  padding: 10px 14px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 11px;
  letter-spacing: 1.2px;
}

.left {
  display: flex;
  align-items: center;
  gap: 6px;
}

.dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
}
.red { background: var(--red); }
.yellow { background: var(--yellow); }
.green { background: var(--green); }

.title {
  margin-left: 10px;
  color: #9ca3af;
}

.right {
  color: var(--green);
  font-size: 10px;
}

/* BODY */
.terminal-body {
  padding: 26px;
  min-height: 480px;
  font-size: 13.8px;
  line-height: 1.7;
  background:
    radial-gradient(circle at top, rgba(79,195,247,.08), transparent 55%);
}

/* TEXT */
.prompt {
  color: var(--blue);
  font-weight: 600;
}

.cmd {
  color: #fff;
}

.out {
  color: #d1d5db;
}

.sys {
  color: #f87171;
}

/* CURSOR */
.cursor {
  display: inline-block;
  width: 2px;
  height: 16px;
  background: #e5e7eb;
  margin-left: 4px;
  animation: blink .9s infinite;
}

@keyframes blink {
  50% { opacity: 0; }
}

@media (max-width: 600px) {
  .terminal-body {
    font-size: 11.5px;
    padding: 16px;
  }
}
</style>

<script>
(function () {
  const log = [
    { t: 'sys', v: '[+] Initializing Environment...\n[+] Secure channel established.\n\n' },

    { t: 'prompt', v: 'X0ph3nt@redops:~$ ' },
    { t: 'cmd', v: 'whoami' },
    { t: 'out', v: '\nI’m Abdulaziz Alsalahi, an offensive cybersecurity specialist with a passion for understanding how systems break.\n\n' },

    { t: 'prompt', v: 'X0ph3nt@redops:~$ ' },
    { t: 'cmd', v: 'uname -a' },
    { t: 'out', v: '\nx0ph3nt\n\n' },

    { t: 'prompt', v: 'X0ph3nt@redops:~$ ' },
    { t: 'cmd', v: 'cat status.txt' },
    { t: 'out', v:
` 
• Learning
• Breaking
• Repeating
\n`
    },

    { t: 'prompt', v: 'X0ph3nt@redops:~$ ' },
    { t: 'cmd', v: './philosophy' },
    { type: 'out', v: '\nTo secure the future, we must master the exploit.\n[+] MISSION: UNSTOPPABLE\n[+] STATUS: TRY HARDER.\n' }
  ];

  const c = document.getElementById('console');
  let i = 0, j = 0;

  function run() {
    if (i >= log.length) return;

    if (j === 0) {
      const s = document.createElement('span');
      s.id = 'l' + i;
      s.className =
        log[i].t === 'prompt' ? 'prompt' :
        log[i].t === 'cmd' ? 'cmd' :
        log[i].t === 'sys' ? 'sys' : 'out';
      c.appendChild(s);
    }

    const span = document.getElementById('l' + i);
    const text = log[i].v;

    span.innerHTML += text[j] === '\n' ? '<br>' : text[j];
    j++;

    if (j < text.length) {
      setTimeout(run, 28);
    } else {
      i++; j = 0;
      setTimeout(run, 140);
    }
  }

  setTimeout(run, 700);
})();
</script>