<script setup>
import ProjectCards from "../data/ProjectsCards.json"
import { ref } from 'vue';

const cards = ref(ProjectCards)
</script>

<template>
  <div class="myProjectsContainer">
    <img src="/mainIcons/bookPageIcon.svg" alt="book Icon" class="projectIcon">
    <h1 class="myProject">MY  PROJECTS</h1>
  </div>
<div class="cardContainer" tabindex="0"> 
  <div class="flip-card" v-for="card in cards" :key="card.id">
    <div class="flip-card-inner">
      <div class="flip-card-front">
        <img :src="`/mainIcons/` + card.img" alt="Project icon" class="notesAppImg">
        <h2>{{ card.frontdescription }}</h2>
      </div>
      <div class="flip-card-back">
        <h1>{{ card.backdescription }}</h1>
        <h1 class="toolsUsed">Tools used:</h1>
        <img :src="`/toolsIcons/` + card.toolsUsed" alt="Tools used icons" class="toolsUsedImg">
      </div>
    </div>
  <div class="links">
    <div class="pinkCircle">ssss</div>
    <a :href="card.pageLink" target="_blank" rel="noreferrer" tabindex="-1"><img src="/mainIcons/open-in-new.svg" class="linkImg"></a>
    <a :href="card.githubLink" target="_blank" rel="noreferrer" tabindex="-1"><img src="/mainIcons/github.svg" class="linkImg"></a>
    </div>
  </div>
  <div class="pinkCircle">ssss</div>
</div>
</template>

<style scoped>
.pinkCircle{
  position: fixed;
  border-radius: 50%;
  height: 50px;
  width: 50px;
  background-color: pink;
}
*{
  font-family: "Apple Chancery, cursive";
}
.cardContainer{
  display: flex;
  justify-content: center;
  margin-top: 50px;
  height: 500px;
}
@media (max-width: 972px) {
  .cardContainer{
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 1100px;
    font-size: small;
  }
  .toolsUsed{
    font-size: small;
  }
  .projectIcon{
    width: 50%;
  }
}
.myProjectsContainer{
  display: flex;
  justify-content: center;
  gap: 2%;
  width: 100%;
  height: 30%;
  margin-top: 80px;

  animation: fade 1s linear;
    animation-timeline: view();
    animation-fill-mode: both;
    animation-duration: 1ms;
}
@keyframes fade{
    0%{
        opacity: 0;
    }
    50%{
        opacity: 0.8;
    }
    100%{
        opacity: 0;
    }
  }
.myProject{
  color: rgb(85, 85, 85);
  font-weight: bold;
  font-size: 200%;
  text-shadow: 2px 2px pink;
}
.projectIcon{
  width: 3%;
}
.flip-card {
  width: 330px;
  height: 300px;
  margin: 50px;
}
.notesAppImg{
  width: 100%;
  height: 150px;
}
.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.6s;
  transform-style: preserve-3d;
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  box-shadow: 5px 5px rgba(128, 128, 128, 0.719);
}
.flip-card:hover .flip-card-inner {
  transform: rotateY(180deg);
}
.flip-card-front, .flip-card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
}

.flip-card-front {
  background-color: #bbb;
  color: black;
}

.flip-card-back {
  padding-top: 20px;
  background-color: #2980b9;
  color: white;
  transform: rotateY(180deg);
  font-size: small;
}
.toolsUsed{
  display: flex;
  margin: 5px;
  margin-left: 20px;
  font-size: x-large;
  font-weight: 400;
}
.toolsUsedImg{
  height: 60px;
}
.links{
  display: flex;
  margin-top: 20px;
  gap: 30px;
  justify-content: center;
}
.linkImg{
  height: 50px;
  width: 50px;
}
</style>