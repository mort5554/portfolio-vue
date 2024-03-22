<scipt setup>

</scipt>

<template>
<header>
    <div class="headline" tabindex="0">
        <h1>Passionate Web Developer | Creating Engaging Digital Experiences</h1>
    </div>
    <div class="imgContainer">
        <img src="/mainIcons/LaptopImg.png" alt="Laptop icon" class="laptopImg">
    </div>
    <div class="pinkCircle"></div>
</header>
</template>

<style scoped>
.pinkCircle{
    position: static;
    height: 200px;
    width: 101px;
    border-radius: 50%;
    background-color: pink;
    z-index: -1;
}
header{
    display: flex;
    align-items: center;
    margin: auto;
    flex-direction: column;
    height: 800px;
    width: 100%;
    gap: 20px;
}
.headline{
    display: flex;
    justify-content: center;
    align-content: center;
    margin: auto;
    text-wrap: wrap;
    height: 10%;
    width: 100%;
    text-shadow: 2px 2px pink;
}
@media (max-width: 1010px) {
    .headline{
        margin-left: 5%;
    }
}
h1{
    font-weight: bold;
    font-size: 40px;
    
    animation: fade 2s linear;
    animation-timeline: view();
    animation-fill-mode: both;
    animation-duration: 1ms;
}
@keyframes fade{
    70%{
        opacity: 1;
    }
    65%{
        opacity: 0.8;
    }
    100%{
        opacity: 0;
    }
}
.imgContainer{
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100%;
    width: 100%;
}
.laptopImg{
    display: flex;
    justify-content: center;
    align-items: center;
    height: 70%;
    border: groove 20px pink;
    border-radius: 5%;
    padding: 80px;

    view-timeline-name: --subjectReveal;
    animation-timeline: --subjectReveal;

  animation-name: appear;
  animation-fill-mode: both;
  animation-duration: 1ms;
}
@keyframes appear {
  from {
    opacity: 0;
    transform: scaleX(250%);
  }

  to {
    opacity: 1;
    transform: scaleX(10%);
  }
}
</style>