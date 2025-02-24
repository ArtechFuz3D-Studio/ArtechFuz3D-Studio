<p align="center">
    <h1 align="center">Neill Hewitt</h1>
    <h3 align="center">Creative Technologist | Visualization & Simulation Artist | Self-Taught Innovator</h3>
</p>

<p align="center">
    <a href="https://www.linkedin.com/in/neill-hewitt-artechfuz3d"><img alt="Linkedin" src="https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white"></a>
</p>

---

### About Me

I’m Neill—indie developer wielding JavaScript, Three.js, Rogue Engine, Unreal, and Unity, shaping 3D in Blender, crafting audio from scratch—self-taught through chaos: blackouts, pollution, injuries. From film, construction, sales (pre-2019), bonsai grit (2011-2019), a year at Moringa (2020), freelance (2021), and a 3-month gig (2022), I forged a NASA Honorable Mention (‘24)—ROS (cert ‘24) and ML spark my robotics edge. Space, tech, nature fuel me—adversity tempered my steel. I’m built to create for innovative tech teams. Explore my repos below!

---

### Interactive Chaos Particles

<p align="center">
<div style="width: 300px; height: 200px; border: 2px solid #333; background: #1a1a1a; position: relative; overflow: hidden;">
    <canvas id="particleCanvas" width="300" height="200"></canvas>
</div>
</p>

<script>
const canvas = document.getElementById('particleCanvas');
const ctx = canvas.getContext('2d');
let particles = [];

function Particle(x, y) {
    this.x = x;
    this.y = y;
    this.size = Math.random() * 5 + 1;
    this.speedX = Math.random() * 3 - 1.5;
    this.speedY = Math.random() * 3 - 1.5;
}

function init() {
    for (let i = 0; i < 50; i++) {
        particles.push(new Particle(canvas.width / 2, canvas.height / 2));
    }
}

function animate() {
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    for (let i = 0; i < particles.length; i++) {
        ctx.fillStyle = 'rgba(255, 255, 255, 0.8)';
        ctx.beginPath();
        ctx.arc(particles[i].x, particles[i].y, particles[i].size, 0, Math.PI * 2);
        ctx.fill();
        
        particles[i].x += particles[i].speedX;
        particles[i].y += particles[i].speedY;
        
        if (particles[i].x < 0 || particles[i].x > canvas.width) particles[i].speedX = -particles[i].speedX;
        if (particles[i].y < 0 || particles[i].y > canvas.height) particles[i].speedY = -particles[i].speedY;
    }
    requestAnimationFrame(animate);
}

init();
animate();
</script>

---

<p align="center">
    <a href="https://portfolio.artechfuz3d.xyz">🌐 Portfolio</a> | <a href="https://yourusername.itch.io">🎮 itch.io</a>
</p>
