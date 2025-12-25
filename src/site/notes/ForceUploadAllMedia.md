---
{"dg-publish":true,"permalink":"/force-upload-all-media/","title":"FarGoneE — Force Upload All Media (Hidden System Note)","tags":["system","far-gone-e","assets"],"noteIcon":"global/original_logo.svg","created":"2025-12-09T17:05:56.460+05:00","updated":"2025-12-25T22:51:10.382+05:00"}
---

<canvas

id="space"

style="

margin: 0;

padding: 0;

box-sizing: border-box;

overflow: hidden;

/* background: #000; */

width: 100%;

height: 100%;

background: radial-gradient(ellipse at center, #0a0a1a 0%, #000000 70%);

"

>

<script>

const canvas = document.getElementById("space");

const ctx = canvas.getContext("2d");

  

function resizeCanvas() {

canvas.width = canvas.offsetWidth;

canvas.height = canvas.offsetHeight;

}

  

resizeCanvas();

window.addEventListener("resize", resizeCanvas);

  

/* =======================

STAR CONFIG

======================= */

  

const stars = [];

const maxStars = 80;

  

const STAR_DRAMA = {

minSize: 0.3,

maxSize: 1.8,

  

minOpacity: 0.08,

maxOpacity: 0.85,

  

slowFade: 0.0015,

fastFade: 0.01,

  

minLife: 300,

maxLife: 900,

  

brightChance: 0.06,

giantChance: 0.025,

};

  

const STAR_MODES = {

calm: {

driftSpeed: 0.0006, // very slow atmospheric movement

driftStrength: 0.015, // barely visible

pulseChance: 0.0, // no pulses

fadeMultiplier: 0.5,

},

  

cinematic: {

driftSpeed: 0.001,

driftStrength: 0.03, // gentle breathing

pulseChance: 0.015, // rare bright shimmer

fadeMultiplier: 1.0,

},

  

epic: {

driftSpeed: 0.0014,

driftStrength: 0.06, // still smooth, not flicker

pulseChance: 0.04, // dramatic but rare

fadeMultiplier: 1.3,

},

};

  

let currentStarMode = "cinematic";

  

/* =======================

STAR CREATION

======================= */

  

function createStar(phase = "fadein") {

const isBright = Math.random() < STAR_DRAMA.brightChance;

const isGiant = Math.random() < STAR_DRAMA.giantChance;

  

const size = isGiant

? Math.random() * 2 + 2

: Math.pow(Math.random(), 2) *

(STAR_DRAMA.maxSize - STAR_DRAMA.minSize) +

STAR_DRAMA.minSize;

  

const targetOpacity = isBright

? Math.random() * 0.5 + 0.4

: Math.pow(Math.random(), 2) *

(STAR_DRAMA.maxOpacity - STAR_DRAMA.minOpacity) +

STAR_DRAMA.minOpacity;

  

const fadeSpeed =

Math.random() * (STAR_DRAMA.fastFade - STAR_DRAMA.slowFade) +

STAR_DRAMA.slowFade;

  

return {

x: Math.random() * canvas.width,

y: Math.random() * canvas.height,

  

size,

opacity: phase === "fadein" ? 0 : targetOpacity,

targetOpacity,

  

fadeSpeed,

lifespan:

Math.random() * (STAR_DRAMA.maxLife - STAR_DRAMA.minLife) +

STAR_DRAMA.minLife,

  

age: 0,

phase,

twinkle: Math.random() * Math.PI * 2,

  

drift: Math.random() * Math.PI * 2,

pulse: 0,

};

}

  

/* =======================

STAR UPDATE

======================= */

  

function updateStar(star) {

const mode = STAR_MODES[currentStarMode];

star.age++;

  

// very slow atmospheric drift

star.drift += mode.driftSpeed;

const drift =

Math.sin(star.drift) * mode.driftStrength * star.targetOpacity;

  

// rare pulse (bright stars only)

if (Math.random() < mode.pulseChance && star.targetOpacity > 0.5) {

star.pulse = 0.15 * star.targetOpacity;

}

star.pulse *= 0.92; // smooth decay

  

// fade lifecycle

if (star.phase === "fadein") {

star.opacity += star.fadeSpeed * mode.fadeMultiplier;

if (star.opacity >= star.targetOpacity) {

star.opacity = star.targetOpacity;

star.phase = "stable";

}

}

  

if (star.phase === "fadeout") {

star.opacity -= star.fadeSpeed * mode.fadeMultiplier;

}

  

if (star.age > star.lifespan) {

star.phase = "fadeout";

}

  

// final opacity (NO flicker)

star.opacity = Math.max(

0,

Math.min(star.targetOpacity, star.opacity + drift + star.pulse)

);

}

  

/* =======================

STAR DRAW

======================= */

  

function drawStars() {

for (const star of stars) {

const o = star.opacity;

if (o <= 0) continue;

  

const core = star.size * 0.6;

const halo = star.size * 2.5;

  

// ---- halo (soft glow)

const gradient = ctx.createRadialGradient(

star.x,

star.y,

0,

star.x,

star.y,

halo

);

gradient.addColorStop(0, `rgba(255,255,255,${o * 0.4})`);

gradient.addColorStop(0.4, `rgba(255,255,255,${o * 0.15})`);

gradient.addColorStop(1, "rgba(255,255,255,0)");

  

ctx.fillStyle = gradient;

ctx.beginPath();

ctx.arc(star.x, star.y, halo, 0, Math.PI * 2);

ctx.fill();

  

// ---- core (sharp)

ctx.fillStyle = `rgba(255,255,255,${o})`;

ctx.beginPath();

ctx.arc(star.x, star.y, core, 0, Math.PI * 2);

ctx.fill();

  

// ---- diffraction cross (only bright stars)

if (star.targetOpacity > 0.5) {

ctx.strokeStyle = `rgba(255,255,255,${o * 0.35})`;

ctx.lineWidth = 0.6;

  

const spike = star.size * 3;

  

ctx.beginPath();

ctx.moveTo(star.x - spike, star.y);

ctx.lineTo(star.x + spike, star.y);

ctx.moveTo(star.x, star.y - spike);

ctx.lineTo(star.x, star.y + spike);

ctx.stroke();

}

}

}

  

/* =======================

INIT STARS

======================= */

  

for (let i = 0; i < maxStars; i++) {

const star = createStar("fadein");

star.age = Math.random() * star.lifespan;

stars.push(star);

}

  

/* =======================

COMETS (3D random directions)

======================= */

  

const CAMERA = {

fov: 1,

zNear: 0,

zFar: 2,

};

// ----------------------------

// 3D SPAWN SETTINGS

// ----------------------------

const SPAWN_DISTANCE = Math.max(canvas.width, canvas.height); // spawn outside view

const SPAWN_ANGLE_JITTER = -Math.random() * Math.PI * 10; // full circle

// ----------------------------

const TARGET_JITTER = -Math.random() * 10000; //dom offset toward center

const BASE_SPEED_MIN = 0.008; // slowest comet speed

const BASE_SPEED_MAX = 0.015; // fastest comet speed

const TRAIL_LENGTH_MIN = 150; // min trail segments

const TRAIL_LENGTH_MAX = 600; // max trail segments

  

// ----------------------------

// COMET APPEARANCE

// ----------------------------

const COMET_OPACITY_MIN = 0.3; // faintest comet

const COMET_OPACITY_MAX = 5; // brightest comet

const COMET_SIZE_MIN = 0.4; // smallest comet head

const COMET_SIZE_MAX = 3; // largest comet head

const COMET_COLOR_CHANCE = 0.6; // probability for pink vs cyan

  

// ----------------------------

// OFFSCREEN BUFFER

// ----------------------------

const OFFSCREEN_BUFFER = 2; // how far offscreen before recycling

  

const comets = [];

const cometCount = 100;

const SPAWN_Z_NEAR = CAMERA.zNear;

const SPAWN_Z_FAR = CAMERA.zFar;

  

// ----------------------------

// DIRECTION SETTINGS

  

function createComet() {

// Spawn comets outside the visible canvas

const spawnDistance = Math.max(canvas.width, canvas.height) * 0.001;

  

// Random angle around center

const angle = (Math.random() - 5 * Math.random()) * Math.random() * 1000;

  

const x = Math.cos(angle) * SPAWN_DISTANCE;

const y = Math.sin(angle) * SPAWN_DISTANCE;

const z = Math.random() * (SPAWN_Z_FAR - SPAWN_Z_NEAR) + SPAWN_Z_NEAR;

  

const targetX = 0 + (Math.random() - 0.5) * TARGET_JITTER;

const targetY = 0 + (Math.random() - 0.5) * TARGET_JITTER;

const targetZ =

-20 * Math.random() * (SPAWN_Z_NEAR - SPAWN_Z_FAR) - SPAWN_Z_NEAR;

  

const dx = targetX - x;

const dy = targetY - y;

const dz = targetZ - z;

  

const len = Math.sqrt(dx * dx + dy * dy + dz * dz);

const speed = 4;

// BASE_SPEED_MIN + Math.random() * (BASE_SPEED_MAX - BASE_SPEED_MIN);

  

const vx = (dx / len) * speed;

const vy = (dy / len) * speed;

const vz = (dz / len) * speed;

  

return {

x,

y,

z,

vx: vx,

vy: vy,

vz: vz,

length:

Math.random() * (TRAIL_LENGTH_MAX - TRAIL_LENGTH_MIN) +

TRAIL_LENGTH_MIN,

opacity:

Math.random() * (COMET_OPACITY_MAX - COMET_OPACITY_MIN) +

COMET_OPACITY_MIN,

size:

Math.random() * (COMET_SIZE_MAX - COMET_SIZE_MIN) + COMET_SIZE_MIN,

color: Math.random() > 0.6 ? "rgba(255,0,255," : "rgba(0,255,255,",

trail: [],

};

}

  

function project3D(x, y, z) {

const scale = CAMERA.fov / z;

return {

x: canvas.width / 2 + x * scale,

y: canvas.height / 2 + y * scale,

scale,

};

}

  

// initialize comets

for (let i = 0; i < cometCount; i++) {

comets.push(createComet());

}

  

/* =======================

ANIMATION LOOP

======================= */

function animate() {

ctx.fillStyle = "rgba(0,0,0,0.35)";

ctx.fillRect(0, 0, canvas.width, canvas.height);

  

// Stars

stars.forEach(updateStar);

drawStars();

  

// Comets

comets.forEach((comet, i) => {

// move in 3D

comet.x += comet.vx;

comet.y += comet.vy;

comet.z -= comet.vz;

  

// recycle if behind camera

if (comet.z < CAMERA.zNear) {

comets[i] = createComet();

return;

}

  

// project 3D -> 2D

const p = project3D(comet.x, comet.y, comet.z);

  

// adaptive trail density

const prev = comet.trail[comet.trail.length - 1];

if (prev) {

const dx = p.x - prev.x;

const dy = p.y - prev.y;

const dist = Math.sqrt(dx * dx + dy * dy);

const steps = Math.ceil(dist / 2); // max 2px per segment

  

for (let s = 1; s <= steps; s++) {

const t = s / steps;

comet.trail.push({

x: prev.x + dx * t,

y: prev.y + dy * t,

s: prev.s + (p.scale - prev.s) * t,

});

}

} else {

comet.trail.push({ x: p.x, y: p.y, s: p.scale });

}

  

// limit trail length dynamically by distance

const maxTrail = Math.max(

20,

Math.min(120, comet.length * (comet.z / CAMERA.zFar))

);

while (comet.trail.length > maxTrail) comet.trail.shift();

  

// draw trail

for (let j = 0; j < comet.trail.length; j++) {

const t = comet.trail[j];

const fade = j / comet.trail.length;

ctx.fillStyle = comet.color + fade * comet.opacity + ")";

ctx.beginPath();

ctx.arc(t.x, t.y, comet.size * fade * t.s, 0, Math.PI * 2);

ctx.fill();

}

  

// draw head

ctx.fillStyle = comet.color + comet.opacity + ")";

ctx.beginPath();

ctx.arc(p.x, p.y, comet.size * 1.6 * p.scale, 0, Math.PI * 2);

ctx.fill();

  

// recycle if offscreen

const buffer = 25;

if (

p.x < -buffer ||

p.x > canvas.width + buffer ||

p.y < -buffer ||

p.y > canvas.height + buffer ||

comet.z < CAMERA.zNear

) {

console.log("Recycling comet", i);

comets[i] = createComet();

}

});

  

requestAnimationFrame(animate);

}

  

animate();

  

/* =======================

MODE SWITCH (DEVTOOLS)

======================= */

window.setStarMode = (mode) => {

if (STAR_MODES[mode]) currentStarMode = mode;

};

</script>

</canvas>
<!-- 
══════════════════════════════════════════════════════════
  FAR GONE E  •  FARG'ONIY EXCELLENCE ENGINE
  This note exists only to force Digital Garden to upload 
  every image, video, audio, and vector in /global and /assets
  It is completely hidden from visitors via CSS
══════════════════════════════════════════════════════════
-->

![global/original_logo.jpg](/img/user/global/original_logo.jpg)

<!-- Add every new media file you drop into /global or /assets here in the future.
     One line = guaranteed upload. No visitor ever sees this note. -->

<div class="fargonee-hidden">

FarGoneE — Engineering | Electronics | Education | Excellence  
Pronounced **Farg'oniy** — honoring timeless knowledge from the Fergana Valley.

</div>