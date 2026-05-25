
<template>
<div class="wrapper">
<section class="projects">   


<div class="title">

<h2>Proiectele mele personale:</h2>

</div>

 <div class="search">
        <input v-model="cautare" type="text" placeholder="Caută un proiect..." />
      </div>

<div v-if="loading" class="grid">


 <div class="card skeleton" v-for="n in 6" :key="n"></div>


</div>


<div v-else-if="error" class="error">


 <p>Nu am putut încărca proiectele. Încearcă mai târziu.</p>



</div>

<div v-else class="grid">

  <div class="card" v-for="repo in reposFiltrate" :key="repo.id">
    
  <div class="card-name"><p>{{ repo.name }}</p></div>
  <div class="card-desc"><p>{{ repo.description || 'Fara descriere disponibila'}}</p></div>
  <div class="card-footer">

  <div class="card-lang"><p> {{ repo.language || 'N/A' }}</p></div>
  <div class="card-stats">
     <p>star {{ repo.stargazers_count }}</p>
     <p>fork {{ repo.forks_count }}</p>
 

  </div>
   

  </div>

  <div class="card-link">
    <a :href="repo.html_url" target="_blank">Vezi pe Github</a>

  </div>
  
  
  </div>



</div>

</section>



</div>

</template>


<script setup>

import { ref, onMounted, computed } from 'vue'

const repos=ref([]);
const loading=ref(true);
const error=ref(false);
const cautare=ref('');

const reposFiltrate = computed(() => {
  return repos.value.filter(r =>
    r.name.toLowerCase().includes(cautare.value.toLowerCase())
  )
})

onMounted(async ()=>{


try{

 const res=await fetch('https://api.github.com/users/florincosminalexescu-oss/repos');

 if(!res.ok) throw new Error();
 const data=await res.json();
 repos.value=data.filter(r=> !r.fork)
   .sort((a, b) => new Date(b.updated_at) - new Date(a.updated_at))


}



catch{
  error.value=true;


}

finally{
  loading.value=false;
}



})


</script>


<style scoped>


.wrapper{

  display: flex;
  flex-direction: column;
 max-width: 1400px;


}


.title p {

  color: #a09e9a;
  font-size: 11px;

}


.search input {
  padding: 8px 14px;
  font-size: 14px;
  border: 1px solid #e8e5e0;
  border-radius: 8px;
  outline: none;
  width: 300px;
  background: #ffffff;
  color: #1a1917;
}



.projects{


  display: flex;
  flex-direction: column;
  align-items: flex-start;
  width: 80%;
  margin:60px auto;
  gap:40px;



}


.grid{

display: grid;
 grid-template-columns: repeat(3, 1fr);
  gap: 30px;
  width: 100%;




}



.card {
  background: #ffffff;
  border: 1px solid #e8e5e0;
  border-radius: 8px;
  padding: 30px;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.card-name p {
  font-size: 15px;
  font-weight: 500;
  color: #1a1917;
}

.card-desc p {
  font-size: 13px;
  color: #6b6860;
}

.card-lang p {
  font-size: 12px;
  color: #a09e9a;
}

.card-stats {
  display: flex;
  gap: 1rem;
}

.card-stats p {
  font-size: 12px;
  color: #a09e9a;
}

.card-link a {
  font-size: 13px;
  color: #6b6860;
  text-decoration: none;
}



</style>