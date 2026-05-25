<template>

<div class="wrapper">
<section class="experience">

  <div class="title">
   <p>Experienta</p>
  </div>

  <div class="info">
    <p>2024 — prezent</p>

    <div class="status">
      <div class="role"><p>Proiecte personale & auto-didact</p></div>
      <div class="company"><p>Independent</p></div>
      <div class="desc"><p>Dezvoltarea proiectelor personale pentru consolidarea cunoștințelor, urmărirea cursurilor online și tutorialelor pentru aprofundarea tehnologiilor web — HTML, CSS, JavaScript, Vue.js.</p></div>
    </div>
  </div>

</section>
</div>

</template>

<style scoped>


.wrapper{

 width: 100%;
 display: flex;
 align-items: center;
 max-width: 1400px;


}

.experience {
  width: 80%;
  margin:50px auto;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
  gap:40px;
 
}

  


.info {
  display: flex;
  gap: 100px;
}

.status {
  display: flex;
  flex-direction: column;
  gap:30px;
}

.title p { color: #a09e9a; }
.info  p { color: #a09e9a; }
.role p { color: #1a1917; font-weight: 500; }
.company p { color: #6b6860; }
.desc p { color: #6b6860; }
</style>