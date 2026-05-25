<template>

<div class="wrapper">
<section class="education">

  <div class="title">
   <p>Educatie</p>
  </div>





   <div class="info">
    <p>2020 — 2024</p>

    <div class="status">
      <div class="role"><p>Liceu</p></div>
      <div class="company"><p>Liceul Teoretic Onisifor Ghibu Sibiu</p></div>
      <div class="desc"><p>Ore la materii fundamentale pentru formarea cunostintelor generale la materii ca informatica,matematica,engleza.</p>
      </div>
    </div>
  </div>


  <div class="info">
    <p>2024 — prezent</p>

    <div class="status">
      <div class="role"><p>Licenta in Inginerie,specializare Calculatoare</p></div>
      <div class="company"><p>Universitatea Lucian Blaga Sibiu</p></div>
      <div class="desc"><p>Cursuri fundamentale: algoritmi și structuri de date, baze de date, rețele de calculatoare, programare orientată obiect, dezvoltare web.</p>
      </div>
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

.education {
  width: 80%;
  margin:50px auto;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
  gap:100px;

  
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