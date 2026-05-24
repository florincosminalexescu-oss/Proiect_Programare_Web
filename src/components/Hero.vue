<template>
  <section class="hero">
    <div class="hero-text">
      <p class="hero-subtitle">Disponibil pentru colaborare</p>
      <h1 class="hero-name">Florin Cosmin <br> <em>Alexescu</em></h1>
      <p class="hero-description">
        Student IT cu pasiune pentru tehnologie și rezolvarea problemelor reale
        prin cod. Explorez diverse domenii — de la web la algoritmi — și sunt
        mereu în căutare de proiecte interesante.
      </p>
      <div class="hero-tags">
        <span class="tag">Student IT</span>
        <span class="tag">Problem Solving</span>
        <span class="tag">Open Source</span>
        <span class="tag">GitHub</span>
      </div>
    </div>

    <div class="avatar">
      <img src="/poza.png" alt="Florin Cosmin Alexescu" />
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.hero {
  max-width: 1600px;
  margin: 0 auto;
  display: flex;
  padding: 100px;
  align-items: center;
  justify-content: space-between;
  gap: 4rem;
}

.hero-subtitle {
  font-size: 12px;
  color: #a09e9a;
  margin-bottom: 1rem;
  text-transform: uppercase;
  letter-spacing: 0.1em;
}

.hero-name {
  font-family: 'DM Serif Display', serif;
  font-size: 3.5rem;
  line-height: 1.1;
  color: #1a1917;
  margin-bottom: 1.25rem;
}

.hero-name em {
  font-style: italic;
  color: #6b6860;
}

.hero-description {
  font-size: 16px;
  color: #6b6860;
  max-width: 480px;
  margin-bottom: 2rem;
}

.hero-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
}

.tag {
  font-size: 12px;
  padding: 5px 12px;
  background: #efecea;
  color: #5c5a57;
  border-radius: 999px;
  border: 1px solid #e8e5e0;
}

.avatar {
  width: 180px;
  height: 180px;
  border-radius: 50%;
  overflow: hidden;
  border: 1px solid #e8e5e0;
  flex-shrink: 0;
}

.avatar img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>