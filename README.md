<div align="center">

# Harie Goutaym D A
### Electrical & Computer Engineering · IoT · Embedded Systems

</div>

---

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-HarieGoutaym-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/harie-goutaym-d-a-67722a36a/)
[![Mail](https://img.shields.io/badge/Email-hariegoutaymda@gmail.com-C9930A?style=for-the-badge&logo=gmail&logoColor=white)](mailto:hariegoutaymda@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-HarieGoutaym-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/HarieGoutaym)

</div>

---

## About

B.Tech in Electrical and Computer Engineering at **Amrita Vishwa Vidyapeetham, Coimbatore** — IoT specialization, 9.0 CGPA.

Most of what I build sits at the boundary of hardware and software. I'm comfortable going from register-level peripheral config on a microcontroller all the way up to a web dashboard or an ML pipeline — and I care about understanding why each layer works, not just that it does. Working toward a graduate degree in Germany in embedded systems or AI.

---

## What I Work With

**Embedded & Hardware**

![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![ESP32](https://img.shields.io/badge/ESP32-003B57?style=flat-square&logo=espressif&logoColor=white)
![PIC16F877A](https://img.shields.io/badge/PIC16F877A-C9930A?style=flat-square&logoColor=white)
![AVR128DA64](https://img.shields.io/badge/AVR128DA64-C9930A?style=flat-square&logoColor=white)
![UART/SPI/I2C](https://img.shields.io/badge/UART%20%7C%20SPI%20%7C%20I2C-444444?style=flat-square)

**Software & Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![HTML/CSS](https://img.shields.io/badge/HTML%20%2F%20CSS-E34F26?style=flat-square&logo=html5&logoColor=white)

**AI / Data**

![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)
![FFT / Wavelet](https://img.shields.io/badge/Signal%20Processing-FFT%20%7C%20Wavelet-8B5E3C?style=flat-square)

**Tools & Platforms**

![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Blynk IoT](https://img.shields.io/badge/Blynk%20IoT-00C58E?style=flat-square)
![MQTT](https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white)
![MPLAB X](https://img.shields.io/badge/MPLAB%20X-EE3124?style=flat-square)

---

## Projects

### [Solar Panel Single-Axis Sun Tracking System](https://github.com/HarieGoutaym/solar-panel-tracker)
**ESP32 · C++ · LDR Differential Sensing · Servo Motor · Wi-Fi Web Dashboard**

Closed-loop solar tracking system that orients a panel along a single axis using LDR differential sensing — two LDRs read left and right light intensity, and the servo drives the panel toward the brighter side when the difference crosses a threshold. Includes real-time voltage and power monitoring from the panel output, motor health diagnostics (stuck servo, jitter, misalignment detection), and a sunset reset that returns the panel to the East position at day end. The entire dashboard is served from the ESP32 as a Wi-Fi access point — no external server, no internet dependency.

---

### [Stepper Sequence Runner — PIC16F877A](https://github.com/HarieGoutaym/pic16f877a-motor-control)
**PIC16F877A · C · 28BYJ-48 · ULN2003A · 4x4 Keypad · SSD1306 OLED · Timer1 Interrupt**

Stepper motor sequence controller where the user builds, saves, and runs multi-step motor programs entirely through a 4x4 keypad. Supports four step types — angle-based, rotation-based, intermittent cycles, and timed runs — each with independent direction and RPM. Execution is Timer1 interrupt-driven (non-blocking), the I2C driver for the SSD1306 OLED is bit-banged from scratch, and the firmware is size-optimized to fit within bootloader flash constraints on the PIC16F877A. All peripheral config at register level — no HAL.

---

### [Anti-Drowsiness Detection System](https://github.com/HarieGoutaym/anti-drowsiness-detection)
**ESP32 · C++ · IR Sensor · MPU6050 · Sensor Fusion · Blynk IoT · HTML Dashboard**

Wearable drowsiness detection built into smart glasses. An IR sensor monitors eyelid closure duration while the MPU6050 tracks head drop and nodding via gyroscope and accelerometer. The ESP32 fuses both signals — relying on either alone would produce too many false positives. When the combined threshold is exceeded, a buzzer/LED alert fires instantly. Live data streams simultaneously to Blynk IoT for mobile monitoring and to an HTML dashboard served directly from the ESP32 over Wi-Fi.

---

### [Secure CLI Password Manager](https://github.com/HarieGoutaym/password-manager-python)
**Python · AES-256-GCM · Argon2id · Per-entry Nonce**

Terminal-based password manager with serious cryptographic foundations. Each credential is encrypted with AES-256-GCM using a unique random 12-byte nonce, so identical passwords never produce identical ciphertexts. The master password is never stored — it goes through Argon2id (memory-hard, GPU-resistant) to derive the 256-bit AES key at runtime. Per-user encrypted vaults, CRUD operations, no plaintext storage anywhere in the pipeline.

---

### [Predictive Maintenance — RUL Estimation & Fault Classification](https://github.com/HarieGoutaym/predictive-maintenance-ml)
**Python · scikit-learn · FFT · DWT (db4, Level 5) · BayesSearchCV · NASA IMS Dataset**

ML pipeline for bearing health monitoring on the NASA IMS dataset (20 kHz vibration data, 8 channels). The core work is a 33-feature extraction pipeline combining FFT statistics (spectral energy, dominant frequency, entropy, band energies) and Discrete Wavelet Transform coefficients across six sub-bands that map to distinct fault frequency ranges. Labels cover both RUL regression (0.0 to 1.0) and 3-class health classification (Normal / Suspect / Failure). Models compared across Random Forest, Gradient Boosting, and XGBoost with hyperparameter tuning via BayesSearchCV. Built with Sarvesh V.

---

## Experience

**Vasantha Advanced Systems** — Embedded Systems Intern
Working on AVR-based embedded development, register-level peripheral interfacing, and firmware design. Focus on building work that holds up under scrutiny — the kind of project you can walk someone through line by line.

**Elgi Ultra Private Limited** — Industrial Induction *(April 2026)*
One-week industrial exposure covering manufacturing systems and automation workflows. Useful context for understanding how embedded control integrates into large-scale production environments.

---

## GitHub Stats

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=HarieGoutaym&amp;show_icons=true&amp;theme=gruvbox&amp;hide_border=true&amp;title_color=C9930A&amp;icon_color=C9930A&amp;text_color=d4b896&amp;bg_color=1a1a1a&amp;cache_seconds=1800" height="165" />
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=HarieGoutaym&amp;layout=compact&amp;theme=gruvbox&amp;hide_border=true&amp;title_color=C9930A&amp;text_color=d4b896&amp;bg_color=1a1a1a&amp;cache_seconds=1800" height="165" />

</div>

<div align="center">

<img src="https://streak-stats.demolab.com/?user=HarieGoutaym&amp;theme=dark&amp;hide_border=true&amp;ring=C9930A&amp;fire=C9930A&amp;currStreakLabel=C9930A&amp;background=1a1a1a&amp;stroke=333333&amp;sideLabels=d4b896&amp;dates=888888" />

</div>

<div align="center">

<img src="https://github-profile-trophy.vercel.app/?username=HarieGoutaym&amp;theme=gruvbox&amp;no-frame=true&amp;no-bg=true&amp;column=6&amp;margin-w=8" />

</div>

---
