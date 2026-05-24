<template>
  <nav class="navbar">
    <div class="navbar-inner">
      <a href="#hero" class="nav-logo">FCA</a>
      <div class="nav-links">
        <a href="#about">Profil</a>
        <a href="#projects">Proiecte</a>
        <a href="#experience">Experiență</a>
        <a href="#education">Educație</a>
      </div>
    </div>
  </nav>
</template>

<script setup>
</script>

<style scoped>
.navbar {
  position: sticky;
  background: #f7f6f4;
  border-bottom: 1px solid #e8e5e0;
  height: 70px;
}

.navbar-inner {
  max-width: 1120px;
  margin: 0 auto;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.nav-logo {
  font-family: 'DM Serif Display', serif;
  font-size: 29px;
  color: #1a1917;
  text-decoration: none;
}

.nav-links {
  display: flex;
  gap: 100px;
}

.nav-links a {
  font-size: 18px;
  color: #6b6860;
  text-decoration: none;
}
</style>

