---
title: "Certifications"
permalink: /certifications/
layout: single
author_profile: true
---

<style>
#certifications {
  padding: 20px 0;
}

.certs-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 30px;
  margin-top: 30px;
}

.cert-card {
  background: linear-gradient(145deg, #2a2f3a, #1f242d);
  border: 1px solid rgba(31, 111, 120, 0.25);
  border-radius: 16px;
  overflow: hidden;
  transition: all 0.4s ease;
  position: relative;
  box-shadow: 0 12px 28px rgba(0,0,0,0.35);
}

/* Subtle Glow */
.cert-card::before {
  content: "";
  position: absolute;
  inset: -2px;
  border-radius: 18px;
  background: linear-gradient(
    120deg,
    transparent,
    rgba(31, 111, 120, 0.35),
    transparent
  );
  opacity: 0;
  z-index: -1;
  transition: opacity 0.4s ease;
}

.cert-card:hover::before {
  opacity: 1;
}

/* Shine (خفيف) */
.cert-card::after {
  content: "";
  position: absolute;
  top: 0;
  left: -160%;
  width: 55%;
  height: 100%;
  background: linear-gradient(
    120deg,
    transparent,
    rgba(255,255,255,0.06),
    transparent
  );
  transform: skewX(-20deg);
}

.cert-card:hover::after {
  animation: shine 1.3s ease;
}

@keyframes shine {
  from { left: -160%; }
  to { left: 160%; }
}

.cert-card:hover {
  transform: translateY(-8px);
  border-color: rgba(31, 111, 120, 0.6);
  box-shadow: 0 20px 40px rgba(31, 111, 120, 0.18);
}

/* Ribbon */
.cert-ribbon {
  position: absolute;
  top: 14px;
  right: -42px;
  background: #1f6f78;
  color: #eaeaea;
  font-size: 10px;
  font-weight: 700;
  padding: 6px 50px;
  transform: rotate(45deg);
  box-shadow: 0 6px 18px rgba(0,0,0,0.45);
  z-index: 2;
}

.cert-ribbon-in-progress {
  position: absolute;
  top: 14px;
  right: -42px;
  background: #7a392f;
  color: #eaeaea;
  font-size: 10px;
  font-weight: 700;
  padding: 6px 50px;
  transform: rotate(45deg);
  box-shadow: 0 6px 18px rgba(0,0,0,0.45);
  z-index: 2;
}

.cert-img-wrapper {
  width: 100%;
  height: 200px;
  background: #1a1e26;
  overflow: hidden;
  position: relative;
}

.cert-img-wrapper img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  filter: grayscale(35%) brightness(0.9);
  transition: transform 0.6s ease, filter 0.6s ease;
}


.cert-img-wrapper::after {
  content: "";
  position: absolute;
  inset: 0;
  background: linear-gradient(
    to bottom,
    transparent 65%,
    rgba(37, 42, 52, 0.92)
  );
}

.cert-info {
  padding: 20px;
}

.cert-badge {
  display: inline-block;
  font-size: 10px;
  text-transform: uppercase;
  letter-spacing: 1px;
  color: #7fb4ba;
  background: rgba(31, 111, 120, 0.15);
  padding: 3px 8px;
  border-radius: 5px;
  margin-bottom: 10px;
}

.cert-name {  
  display: inline-block;
  font-weight: bold; 
  font-size: 10.2px;
  text-transform: uppercase;
  letter-spacing: 1px;
  color: #2ecc71  ;
  background: rgba(46, 204, 113, 0.1);
  padding: 3px 8px;
  border-radius: 5px;
  margin-bottom: 10px;
}

.cert-title {
  font-family: "Courier New", monospace;
  font-weight: bold;
  color: #b6e1e4;
  font-size: 1rem;
  margin-bottom: 6px;
  display: block;
}

.cert-date,
.cert-id {
  font-size: 0.75em;
  color: rgba(234,234,234,0.6);
  display: block;
  margin-bottom: 6px;
  font-style: italic;
}

.view-link {
  margin-top: 14px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #eaeaea;
  text-decoration: none;
  font-size: 0.8em;
  font-weight: 600;
  background: rgba(31, 111, 120, 0.18);
  border: 1px dashed rgba(31, 111, 120, 0.6);
  padding: 10px;
  border-radius: 10px;
  transition: all 0.3s ease;
}

.view-link::after {
  content: " →";
  transition: transform 0.3s ease;
}

.view-link:hover {
  background: rgba(31, 111, 120, 0.45);
  color: #ffffff;
  border-style: solid;
}

.view-link:hover::after {
  transform: translateX(6px);
}
</style>

<div id="certifications">
  <div class="certs-grid">

    <div class="cert-card">
      <div class="cert-ribbon">CERTIFIED</div>

      <div class="cert-img-wrapper">
        <img src="{{ '/assets/img/certs/capt.png' | relative_url }}" alt="CAPT">
      </div>

      <div class="cert-info">
        <span class="cert-badge">Hackviser</span>
        <span class="cert-name">CAPT</span>
        <span class="cert-title">Certified Associate Penetration Tester</span>
        <span class="cert-date">Issued: Nov 28, 2025</span>
        <span class="cert-id">ID: HV-CAPT-E8W5W8K2</span>

        <a href="{{ '/assets/img/certs/capt.png' | relative_url }}" target="_blank" class="view-link">
          View Certification
        </a>
      </div>
    </div>

    <div class="cert-card">
      <div class="cert-ribbon-in-progress">ONGOING</div>

      <div class="cert-img-wrapper">
        <img src="{{ '/assets/img/certs/IN_PROGRESS.png' | relative_url }}" alt="CRTA">
      </div>

      <div class="cert-info">
        <span class="cert-badge">Cyberwarfare</span>
        <span class="cert-name">CRTA</span>
        <span class="cert-title">Certified Red Team Analyist</span>
        <span class="cert-date">Issued: UNKNOWN</span>
        <span class="cert-id">ID: UNKNOWN</span>

        <a href="{{ '/assets/img/certs/IN_PROGRESS.png' | relative_url }}" target="_blank" class="view-link">
          View Certification
        </a>
      </div>
    </div>

    <!-- <div class="cert-card">
      <div class="cert-ribbon-in-progress">ONGOING</div>

      <div class="cert-img-wrapper">
        <img src="{{ '/assets/img/certs/IN_PROGRESS.png' | relative_url }}" alt="eJPT">
      </div>

      <div class="cert-info">
        <span class="cert-badge">INE</span>
        <span class="cert-title">Junior Penetration Tester (eJPT)</span>
        <span class="cert-date">Issued: UNKNOWN</span>
        <span class="cert-id">ID: UNKNOWN</span>

        <a href="{{ '/assets/img/certs/IN_PROGRESS.png' | relative_url }}" target="_blank" class="view-link">
          View Certification
        </a>
      </div>
    </div> -->

  </div>
</div>