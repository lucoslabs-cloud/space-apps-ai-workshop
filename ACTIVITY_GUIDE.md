# Workshop Activity Guide: "Speed Orbit" (8-Minute Challenge)

> **Activity Name:** Speed Orbit: Prompt-to-Prototype Challenge  
> **Duration:** 8 Minutes (1 min prompt setup, 5 mins generation & tweak, 2 mins lightning showcase)  
> **Format:** Individual or pairs (works on any laptop with a browser and an AI chat tool)  
> **Reference Solution:** [`activity_sample_lunar_lander.html`](file:///c:/Users/isam/Desktop/SSC%20Workshop/activity_sample_lunar_lander.html)

---

## 🎯 Activity Objective
Participants will experience the core superpower of **vibe coding**: transforming a conceptual NASA hackathon challenge requirement into a functional, styled, interactive web widget in under 300 seconds.

---

## 📋 Facilitator Instructions (Slide 7)

1. **Minute 0:00 - 1:00 (The Pitch):**
   * Announce: *"You have 5 minutes to generate a working interactive NASA widget. No npm install, no framework setup. Just one prompt into your AI model of choice (Claude, ChatGPT, Gemini, Cursor, or Bolt) and save it as `index.html`."*
   * Tell attendees to pick **one** of the 3 tracks below.

2. **Minute 1:00 - 5:30 (Live Prompting & Coding):**
   * Play background music or keep a countdown timer on the screen.
   * Walk around the room or monitor the workshop chat.
   * Remind attendees: *"If it gives you markdown code blocks, click 'Copy', paste it into Notepad / VS Code, save as `widget.html`, and double-click to view."*

3. **Minute 5:30 - 8:00 (Lightning Showcase):**
   * Ask 1 or 2 attendees to raise their hand or screen-share their generated widget.
   * Highlight what worked well (e.g. SVG graphics, responsive controls, color palettes).
   * If attendees encounter errors, use it as a live teaching moment for the "Refinement Prompt".

---

## 🚀 The 3 Challenge Tracks & Ready-to-Copy Prompts

### Track 1: Artemis Lunar Descent Thruster HUD
* **Challenge:** Create an Apollo/Artemis lunar descent cockpit monitor with an interactive RCS thruster button, fuel gauge, and soft touchdown detection.
* **Master Prompt:**
  ```text
  You are an expert frontend engineer participating in the NASA Space Apps Challenge.
  Write a self-contained, single-file index.html prototype for an Artemis Lunar Lander Descent HUD.

  Requirements:
  1. Theme: NASA mission control cyber-dark (#020617 background, cyan and amber telemetry accents, Orbitron and JetBrains Mono fonts from Google Fonts).
  2. Visual Viewport: An SVG canvas showing a lunar crater surface and a small descent module lander.
  3. Physics Loop (Vanilla JS setInterval): Lunar gravity gently pulls the lander down. A "HOLD TO FIRE RCS THRUSTER" button (or spacebar) accelerates it upward.
  4. Real-time Telemetry: Fuel percentage bar (depletes on thrust), altitude in meters, vertical descent velocity in m/s (turns red if > 2.5 m/s).
  5. Touchdown State: Displays "TOUCHDOWN NOMINAL" if velocity is safe, or "CRASH" if too fast.
  6. Constraints: Zero external dependencies, pure vanilla HTML + CSS + JS. Complete executable code only.
  ```

---

### Track 2: Solar Storm & Flare Early-Warning Radar
* **Challenge:** Create a Space Weather Operations Center radar sweep detecting coronal mass ejections (CMEs) heading toward Earth.
* **Master Prompt:**
  ```text
  You are an expert frontend engineer participating in the NASA Space Apps Challenge.
  Write a self-contained, single-file index.html prototype for a NOAA/NASA Space Weather Radiation Early-Warning Radar.

  Requirements:
  1. Theme: Deep space dark (#050814) with glowing green/amber CRT radar aesthetics and JetBrains Mono typography.
  2. Radar Display: A circular canvas or SVG with a continuous 360-degree rotating sweep line and concentric distance rings (Earth at center, Sun at perimeter).
  3. Blip Detection: Random solar energetic particle blips or CMEs appear and pulse when illuminated by the sweep.
  4. Interactive Controls: A slider for "Solar Flare Class" (C-Class, M-Class, X-Class) that changes alert levels from Green to Flashing Red Warning.
  5. Constraints: Single HTML file, responsive, zero build tools.
  ```

---

### Track 3: ISS Orbital Path & Day/Night Terminator
* **Challenge:** Create a real-time 2D world map showing the orbital track of the International Space Station and the solar terminator (sunlight vs shadow).
* **Master Prompt:**
  ```text
  You are an expert frontend engineer participating in the NASA Space Apps Challenge.
  Write a self-contained, single-file index.html prototype for an ISS Ground Track & Solar Terminator visualizer.

  Requirements:
  1. Theme: High-tech aerospace telemetry console.
  2. Map Display: A stylized SVG 2D world map outline with a sinusoidal orbital ground track curve.
  3. Interactive Controls: A time scrub slider (T-00:00 to T+90:00 min orbital period) that slides the ISS icon along the curve.
  4. Dynamic Indicator: Highlights whether the ISS is currently in "Orbital Day (Solar Arrays Generating Power)" or "Orbital Eclipse (Battery Storage Active)".
  5. Telemetry Cards: Speed (27,600 km/h), Altitude (408 km), Inclination (51.6°).
  6. Constraints: Pure single-file HTML + CSS + JS with SVG.
  ```

---

## 🛠️ Troubleshooting & Live Refinement Prompts

When participants run their first prompt, they might encounter common minor glitches. Share these rapid 1-line follow-up prompts:

| Symptom | Rapid Fix Prompt |
| :--- | :--- |
| **"The buttons don't do anything!"** | *"Fix the event listeners: make sure the button click handler modifies the state and triggers a redraw loop. Return the full corrected file."* |
| **"The layout looks stretched or ugly"** | *"Polish the visual CSS: use modern flexbox/grid, add backdrop-filter blur(12px), glowing box-shadows, and clean borders."* |
| **"The code was cut off by token limit"** | *"Continue generating exactly from line [X] without repeating previous code."* |
