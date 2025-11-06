<script setup>
import SkyIntro from "./components/SkyIntro.vue";
</script>

<template>
  <div class="app-container">
    <header class="header">
      <div class="header-content">
        <h1 class="logo">✨ 光遇</h1>
        <nav class="nav">
          <a href="#intro">游戏介绍</a>
          <a href="#features">游戏特色</a>
          <a href="#worlds">世界观</a>
          <a href="#community">社区</a>
        </nav>
      </div>
    </header>

    <main>
      <SkyIntro />
    </main>

    <footer class="footer">
      <p>© 2024 Sky: Children of the Light | Developed by thatgamecompany</p>
      <p class="disclaimer">本网站为粉丝制作的介绍页面，非官方网站</p>
    </footer>
  </div>
</template>

<style scoped>
.app-container {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.header {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  padding: 1.5rem 0;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  position: sticky;
  top: 0;
  z-index: 100;
}

.header-content {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 1.8rem;
  font-weight: 700;
  color: white;
  margin: 0;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}

.nav {
  display: flex;
  gap: 2rem;
}

.nav a {
  color: white;
  text-decoration: none;
  font-weight: 500;
  transition: all 0.3s ease;
  position: relative;
}

.nav a:hover {
  transform: translateY(-2px);
  text-shadow: 0 2px 8px rgba(255, 255, 255, 0.5);
}

.nav a::after {
  content: "";
  position: absolute;
  bottom: -4px;
  left: 0;
  width: 0;
  height: 2px;
  background: white;
  transition: width 0.3s ease;
}

.nav a:hover::after {
  width: 100%;
}

main {
  flex: 1;
}

.footer {
  background: linear-gradient(135deg, #434343 0%, #000000 100%);
  color: white;
  padding: 2rem;
  text-align: center;
  margin-top: 4rem;
}

.footer p {
  margin: 0.5rem 0;
  opacity: 0.9;
}

.disclaimer {
  font-size: 0.85rem;
  opacity: 0.7;
}

@media (max-width: 768px) {
  .header-content {
    flex-direction: column;
    gap: 1rem;
  }

  .nav {
    gap: 1rem;
    font-size: 0.9rem;
  }
}
</style>
