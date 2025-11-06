<script setup>
import { ref } from "vue";

const activeTab = ref("intro");

const features = [
  {
    icon: "🌟",
    title: "治愈温馨",
    description: "温暖的视觉风格和动人的音乐，带来心灵的慰藉",
  },
  {
    icon: "👥",
    title: "社交互动",
    description: "与来自世界各地的玩家相遇，建立珍贵的友谊",
  },
  {
    icon: "🗺️",
    title: "探索冒险",
    description: "在七个梦幻国度中自由飞翔，发现隐藏的秘密",
  },
  {
    icon: "🎨",
    title: "自由定制",
    description: "收集各种斗篷、面具和发型，打造独特的角色",
  },
];

const worlds = [
  { name: "晨岛", desc: "新手的起点，学习飞翔的地方" },
  { name: "云野", desc: "广阔的草原和浮岛，充满自由的气息" },
  { name: "雨林", desc: "茂密的森林和神秘的树屋" },
  { name: "霞谷", desc: "竞速赛道和冰雪滑道的欢乐天地" },
  { name: "墓土", desc: "失落的战场，充满挑战" },
  { name: "禁阁", desc: "知识的圣殿，保存着古老的记忆" },
  { name: "暴风眼", desc: "最终的试炼之地" },
];
</script>

<template>
  <div class="sky-intro">
    <!-- Hero Section -->
    <section id="intro" class="hero">
      <div class="hero-content">
        <h1 class="title">欢迎来到光遇的世界</h1>
        <p class="subtitle">Sky: Children of the Light</p>
        <p class="description">
          在这个温馨治愈的社交冒险游戏中，化身为光之子女，<br />
          穿越云端王国，拯救堕落的星灵，点亮希望之光。
        </p>
        <div class="hero-buttons">
          <button class="btn-primary">开始游戏</button>
          <button class="btn-secondary">观看预告</button>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="features">
      <h2 class="section-title">游戏特色</h2>
      <div class="features-grid">
        <div
          v-for="feature in features"
          :key="feature.title"
          class="feature-card"
        >
          <div class="feature-icon">{{ feature.icon }}</div>
          <h3>{{ feature.title }}</h3>
          <p>{{ feature.description }}</p>
        </div>
      </div>
    </section>

    <!-- Worlds Section -->
    <section id="worlds" class="worlds">
      <h2 class="section-title">探索七大国度</h2>
      <div class="worlds-grid">
        <div v-for="world in worlds" :key="world.name" class="world-card">
          <h3>{{ world.name }}</h3>
          <p>{{ world.desc }}</p>
        </div>
      </div>
    </section>

    <!-- Community Section -->
    <section id="community" class="community">
      <h2 class="section-title">加入我们的社区</h2>
      <div class="community-content">
        <div class="stat">
          <div class="stat-number">1亿+</div>
          <div class="stat-label">全球玩家</div>
        </div>
        <div class="stat">
          <div class="stat-number">7+</div>
          <div class="stat-label">梦幻国度</div>
        </div>
        <div class="stat">
          <div class="stat-number">200+</div>
          <div class="stat-label">收集物品</div>
        </div>
      </div>
      <p class="community-text">
        光遇不仅是一款游戏，更是一个温暖的社区。<br />
        在这里，你可以结识天南地北的朋友，分享快乐与感动。
      </p>
    </section>
  </div>
</template>

<style scoped>
.sky-intro {
  width: 100%;
}

/* Hero Section */
.hero {
  min-height: 600px;
  background: linear-gradient(
    180deg,
    rgba(102, 126, 234, 0.1) 0%,
    rgba(118, 75, 162, 0.1) 100%
  );
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 4rem 2rem;
  text-align: center;
}

.hero-content {
  max-width: 800px;
}

.title {
  font-size: 3.5rem;
  font-weight: 800;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin-bottom: 1rem;
}

.subtitle {
  font-size: 1.5rem;
  color: #666;
  margin-bottom: 1.5rem;
  font-weight: 300;
  letter-spacing: 2px;
}

.description {
  font-size: 1.2rem;
  line-height: 1.8;
  color: #555;
  margin-bottom: 2rem;
}

.hero-buttons {
  display: flex;
  gap: 1rem;
  justify-content: center;
  flex-wrap: wrap;
}

.btn-primary,
.btn-secondary {
  padding: 1rem 2.5rem;
  font-size: 1.1rem;
  border: none;
  border-radius: 50px;
  cursor: pointer;
  font-weight: 600;
  transition: all 0.3s ease;
}

.btn-primary {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
}

.btn-primary:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 20px rgba(102, 126, 234, 0.3);
}

.btn-secondary {
  background: white;
  color: #667eea;
  border: 2px solid #667eea;
}

.btn-secondary:hover {
  background: #667eea;
  color: white;
  transform: translateY(-3px);
}

/* Section Styles */
.section-title {
  font-size: 2.5rem;
  text-align: center;
  margin-bottom: 3rem;
  color: #333;
  font-weight: 700;
}

/* Features Section */
.features {
  padding: 5rem 2rem;
  background: white;
}

.features-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
  max-width: 1200px;
  margin: 0 auto;
}

.feature-card {
  padding: 2rem;
  background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
  border-radius: 20px;
  text-align: center;
  transition: all 0.3s ease;
}

.feature-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
}

.feature-icon {
  font-size: 3rem;
  margin-bottom: 1rem;
}

.feature-card h3 {
  font-size: 1.5rem;
  margin-bottom: 1rem;
  color: #333;
}

.feature-card p {
  color: #666;
  line-height: 1.6;
}

/* Worlds Section */
.worlds {
  padding: 5rem 2rem;
  background: linear-gradient(180deg, #ffecd2 0%, #fcb69f 100%);
}

.worlds-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1.5rem;
  max-width: 1200px;
  margin: 0 auto;
}

.world-card {
  padding: 1.5rem;
  background: white;
  border-radius: 15px;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
}

.world-card:hover {
  transform: scale(1.05);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
}

.world-card h3 {
  font-size: 1.3rem;
  color: #667eea;
  margin-bottom: 0.5rem;
}

.world-card p {
  color: #666;
  font-size: 0.95rem;
}

/* Community Section */
.community {
  padding: 5rem 2rem;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  text-align: center;
}

.community .section-title {
  color: white;
}

.community-content {
  display: flex;
  justify-content: center;
  gap: 4rem;
  margin-bottom: 2rem;
  flex-wrap: wrap;
}

.stat {
  text-align: center;
}

.stat-number {
  font-size: 3rem;
  font-weight: 800;
  margin-bottom: 0.5rem;
}

.stat-label {
  font-size: 1.1rem;
  opacity: 0.9;
}

.community-text {
  font-size: 1.2rem;
  line-height: 1.8;
  max-width: 600px;
  margin: 2rem auto 0;
  opacity: 0.95;
}

/* Responsive */
@media (max-width: 768px) {
  .title {
    font-size: 2.5rem;
  }

  .subtitle {
    font-size: 1.2rem;
  }

  .description {
    font-size: 1rem;
  }

  .section-title {
    font-size: 2rem;
  }

  .community-content {
    gap: 2rem;
  }

  .stat-number {
    font-size: 2rem;
  }
}
</style>
