<script setup>
import { ref } from 'vue';

const showModal = ref(false)
const menuNavigation = ref(true)
</script>

<template>
    <nav class="navContainer">
        <div class="menu">
            <div class="logoContainer">
                <img class="menuLogo" src="/mainIcons/M-logo.png" alt="logo">
            </div>
            <nav class="computer-nav">
                <a href="https://mort5554.github.io/portfolio-vue/#:~:text=Passionate%20Web%20Developer%20%7C%20Creating%20Engaging%20Digital%20Experiences">Home</a>
                <a href="https://mort5554.github.io/portfolio-vue/#:~:text=Engaging%20Digital%20Experiences-,SKILLS,-Vue.js">My skills</a>
                <a href="https://mort5554.github.io/portfolio-vue/#:~:text=using%20so%20far%3A-,MY%20PROJECTS,-Introducing%20a%20dynamic">Projects</a>
                <a href="https://mort5554.github.io/portfolio-vue/#:~:text=ssss-,Made%20By%20%40mort5554">Contact</a>
            </nav>
            <div class="burgerContainer">
                <button @click="showModal=!showModal, menuNavigation = !menuNavigation" :class="menuNavigation == false ? `hamburger is-active` :  `hamburger`">
                    <div class="bar"></div>
                </button>
            </div>
        </div>
        <nav v-show="showModal" class="mobile-nav">
            <div class="openModalFromLeft">
                <a href="https://mort5554.github.io/portfolio-vue/#:~:text=Passionate%20Web%20Developer%20%7C%20Creating%20Engaging%20Digital%20Experiences">Home</a>
            </div>
            <div class="openModalFromRight">     
                <a href="https://mort5554.github.io/portfolio-vue/#:~:text=Engaging%20Digital%20Experiences-,SKILLS,-Vue.js">My skills</a>
            </div> 
            <div class="openModalFromLeft">
                <a href="https://mort5554.github.io/portfolio-vue/#:~:text=using%20so%20far%3A-,MY%20PROJECTS,-Introducing%20a%20dynamic">Projects</a>
            </div>
            <div class="openModalFromRight">
                <a href="https://mort5554.github.io/portfolio-vue/#:~:text=ssss-,Made%20By%20%40mort5554">Contact</a>
            </div>
        </nav>
    </nav>
    <div class="space"></div>
</template>

<style scoped>
*{
    font-family: "Apple Chancery, cursive";
    font-weight: bold;
}
.space{
    width: 100%;
    height: 150px;
}
.navContainer{
    position: absolute;
    width: 100%;
    background-color: rgb(252, 227, 242);
}
.menu{
    display: flex;
    align-items: center;
    justify-content: space-around;
    margin: auto;
    width: 100%;
    gap: 30px;
}
.menuLogo{
    height: 330%;
    align-self: center;
    justify-content: center;
    margin-top: 30px;
    margin-left: 40px;
}
.computer-nav{
    display: flex;
    align-items: center;
    box-sizing: border-box;
    margin-left: 60px;
    width: 40%;
    text-wrap: nowrap;
}
@media(max-width: 835px){
    .computer-nav{
        display: none;
    }
}
/*@media (max-width: 914px) {
    .computer-nav{
        padding-right: 70px;
    }
}*/
.computer-nav a{
    width: 100%;
    margin: 20px;
    text-decoration: none;
    font-size: 22px;
    color: rgb(85, 85, 85);
    cursor: pointer;
}
.computer-nav a:hover{
    color: rgba(168, 168, 168, 0.726);
}
.logoContainer{
    width: 40%;
    height: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
}
.burgerContainer{
    width: 30%;
    height: 95px;
    display: flex;
    justify-content: center;
}
.hamburger{
    position: relative;
    display: block;
    width: 35px;
    cursor: pointer;

    appearance: none;
    background-color: rgba(0, 0, 0, 0.0);
    outline: none;
    border: none;
}
.hamburger .bar, .hamburger:after, .hamburger:before{
    content: '';
    display: block;
    width: 120%;
    height: 4px;
    background-color: black;
    margin: 4px 0px;
    transition: 0.4s;
}
.hamburger.is-active:before{
    transform: rotate(-45deg) translate(-9px, 6px);
}
.hamburger.is-active:after{
    transform: rotate(45deg) translate(-5px, -2px);
}
.hamburger.is-active .bar{
    opacity: 0;
}
.mobile-nav a:hover{
    background-color: rgba(255, 190, 232, 0.87);
    color: rgba(0, 0, 0, 0.705);
}
.mobile-nav{
    position: absolute;
    justify-content: center;
    width: 100%;
}
.mobile-nav a{
    display: flex;
    text-align: center;
    align-self: center;
    height: 70px;
    align-items: center;
    justify-content: center;
    width: 100%;
    border: solid rgba(253, 165, 222, 0.9) 9px ;
    color: black;
    font-size: large;
    text-decoration: none;
    background-color: rgb(255, 190, 232);
    animation: slideDown 0.5s ease-in-out;
    transform-origin: left;
    box-sizing: border-box;
}
.openModalFromLeft{
    animation: slideFromLeft 0.5s ease-in-out;
    transform-origin: left;
}
@keyframes slideFromLeft{
    from{
        transform: scaleX(0%)
    }
    to{
        transform: scaleX(100%);
    }
}
.openModalFromRight{
    animation: slideFromRight 0.5s ease-in-out;
    transform-origin: right;
}
@keyframes slideFromRight{
    from{
        transform: scaleX(0%)
    }
    to{
        transform: scaleX(100%);
    }
}
@media(min-width: 836px){
    .hamburger{
        display: none;
    }
    .bar{
        display: none;
    }
    .mobile-nav{
        display: none;
    }
}
.mainPage,
.contact{
    font-weight: bold;
    margin-left: 20px;
    cursor: pointer;
}
.link{
    text-decoration: none;
    color: black;
    transition: transform 0.3s;
}
.link:hover{
    transform: translateY(-7px);
    color: rgb(77, 76, 76);
}
</style>
