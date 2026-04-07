@import url("https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap");

* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    font-family: "Inter", sans-serif;
}

body {
    background: transparent;
    overflow: hidden;
}

/* 🎯 HUD */
.hud {
    position: absolute;
    left: 50%;
    bottom: 2vh;
    transform: translateX(-50%);
    width: 24rem;
    display: flex;
    flex-direction: column;
    gap: 0.8rem;
}

/* 🔫 AMMO */
.ammo-card {
    align-self: center;
    padding: 0.45rem 1rem;
    border-radius: 999px;
    background: rgba(15, 15, 25, 0.6);
    backdrop-filter: blur(12px);
    border: 1px solid rgba(255,255,255,0.08);
    box-shadow: 
        0 0 15px rgba(0, 150, 255, 0.3),
        inset 0 0 10px rgba(255,255,255,0.05);
    display: flex;
    align-items: center;
    gap: 0.5rem;
}

.ammo-card img {
    width: 1rem;
    filter: drop-shadow(0 0 5px rgba(0,150,255,0.7));
}

.ammo-value {
    color: #fff;
    font-size: 1.3rem;
    font-weight: 800;
}

/* 📊 PANEL */
.stats-panel {
    padding: 0.9rem;
    border-radius: 1rem;
    background: rgba(20, 20, 35, 0.6);
    backdrop-filter: blur(14px);
    border: 1px solid rgba(255,255,255,0.08);
    box-shadow: 
        0 0 20px rgba(0,0,0,0.5),
        inset 0 0 10px rgba(255,255,255,0.05);
    display: flex;
    flex-direction: column;
    gap: 0.6rem;
}

/* 📈 ROW */
.stat-row {
    display: flex;
    flex-direction: column;
    gap: 0.3rem;
}

/* 🧠 LABEL + ICON */
.stat-meta {
    display: flex;
    align-items: center;
    gap: 0.4rem;
    color: #eaefff;
}

.stat-meta img {
    width: 1rem;
    opacity: 0.9;
}

.stat-label {
    font-size: 0.65rem;
    font-weight: 600;
    letter-spacing: 0.08em;
}

.stat-value {
    margin-left: auto;
    font-size: 0.8rem;
    font-weight: 800;
}

/* 📊 BAR */
.bar-track {
    width: 100%;
    height: 0.6rem;
    border-radius: 999px;
    overflow: hidden;
    background: rgba(255,255,255,0.06);
    border: 1px solid rgba(255,255,255,0.08);
}

.bar-fill {
    height: 100%;
    transition: width 0.2s ease;
}

/* ❤️ HEALTH */
.stat-row.health .bar-fill {
    background: linear-gradient(90deg, #ff3d5a, #ff7a45);
    box-shadow: 0 0 12px rgba(255,70,90,0.6);
}

/* 🛡️ ARMOR */
.stat-row.armor .bar-fill {
    background: linear-gradient(90deg, #3fa7ff, #00e0ff);
    box-shadow: 0 0 12px rgba(0,150,255,0.6);
}
