---
title: "Posts"
permalink: /posts/
layout: single
author_profile: true
---

<style>
/* سنستخدم نفس الأساسيات اللي عندك مع تعديلات بسيطة لتناسب المنصات */
#platforms {
  padding: 20px 0;
}

.platforms-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 30px;
  margin-top: 30px;
}

.platform-card {
  background: linear-gradient(145deg, #2a2f3a, #1f242d);
  border: 1px solid rgba(31, 111, 120, 0.25);
  border-radius: 16px;
  overflow: hidden;
  transition: all 0.4s ease;
  position: relative;
  box-shadow: 0 12px 28px rgba(0,0,0,0.35);
}

.platform-card:hover {
  transform: translateY(-8px);
  border-color: rgba(31, 111, 120, 0.6);
  box-shadow: 0 20px 40px rgba(31, 111, 120, 0.18);
}

/* Shine Effect */
.platform-card::after {
  content: "";
  position: absolute;
  top: 0;
  left: -160%;
  width: 55%;
  height: 100%;
  background: linear-gradient(120deg, transparent, rgba(255,255,255,0.06), transparent);
  transform: skewX(-20deg);
}

.platform-card:hover::after {
  animation: shine 1.3s ease;
}

@keyframes shine {
  from { left: -160%; }
  to { left: 160%; }
}

.platform-img-wrapper {
  width: 100%;
  height: 180px;
  background: #1a1e26;
  overflow: hidden;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
}

.platform-img-wrapper img {
  width: 70%; /* ليكون اللوجو متناسق داخل الكرت */
  height: auto;
  filter: drop-shadow(0 0 10px rgba(31, 111, 120, 0.5));
  transition: transform 0.6s ease;
}

.platform-card:hover .platform-img-wrapper img {
  transform: scale(1.1);
}

.platform-info {
  padding: 20px;
  text-align: center;
}

.platform-title {
  font-family: "Courier New", monospace;
  font-weight: bold;
  color: #b6e1e4;
  font-size: 1.4rem;
  margin-bottom: 10px;
  display: block;
  letter-spacing: 2px;
}

.platform-desc {
  font-size: 0.85em;
  color: rgba(234,234,234,0.7);
  display: block;
  margin-bottom: 20px;
  line-height: 1.5;
}

/* Ribbon */
/* Ribbon - Fix Centering */
.platform-ribbon {
  position: absolute;
  top: 18px;            /* تحريك مكان الشريطة قليلاً لتبدو متوازنة */
  right: -35px;         /* ضبط المسافة من اليمين */
  background: #1f6f78;
  color: #eaeaea;
  font-size: 11px;
  font-weight: 800;
  width: 140px;         /* عرض ثابت يضمن توسيط النص */
  text-align: center;   /* توسيط النص داخل العرض الثابت */
  transform: rotate(45deg);
  box-shadow: 0 4px 10px rgba(0,0,0,0.3);
  z-index: 5;
  line-height: 24px;    /* لضمان توسيط النص عمودياً أيضاً */
  text-transform: uppercase;
  letter-spacing: 1px;
}

.enter-link {
  display: flex;
  align-items: center;
  justify-content: center;
  color: #eaeaea;
  text-decoration: none;
  font-size: 0.9em;
  font-weight: 600;
  background: rgba(31, 111, 120, 0.18);
  border: 1px solid rgba(31, 111, 120, 0.4);
  padding: 12px;
  border-radius: 10px;
  transition: all 0.3s ease;
}


.enter-link:hover {
  background: #1f6f78;
  color: #ffffff;
  box-shadow: 0 0 15px rgba(31, 111, 120, 0.4);
  text-decoration: none !important;
}
</style>

<div id="platforms">
  <div class="platforms-grid">

    <div class="platform-card">
      <div class="platform-img-wrapper">
      <span class="platform-ribbon">HTB</span>
        <img src="https://www.hackthebox.com/images/logo-htb.svg" alt="HTB">
      </div>
      <div class="platform-info">
        <span class="platform-title">HackTheBox</span>
        <p class="platform-desc">Advanced penetration testing labs and machine writeups.</p>
        <a href="{{ '/htb/' | relative_url }}" class="enter-link">
          Explore Writeups
        </a>
      </div>
    </div>

    <div class="platform-card">
      <div class="platform-img-wrapper">
      <span class="platform-ribbon">THM</span>
        <img src="https://assets.tryhackme.com/img/logo/tryhackme_logo_full.svg" alt="THM">
      </div>
      <div class="platform-info">
        <span class="platform-title">TryHackMe</span>
        <p class="platform-desc">Step-by-step learning paths and room walkthroughs.</p>
        <a href="{{ '/thm/' | relative_url }}" class="enter-link">
          Explore Writeups
        </a>
      </div>
    </div>

  </div>
</div>