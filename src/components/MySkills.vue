<script setup>

</script>

<template>
    <main class="MySkills" tabindex="0">
        <div class="mySkillsHeadline">
            <img class="mySkillsImg" src="/mainIcons/hammer-wrench.svg">
            <h1>SKILLS</h1>
        </div>
        <div class="mySkillsContainer">
            <div class="mySkillsGraph">
                <div class="toolsSkillContainer">
                    <h2 class="toolsSkill">Vue.js</h2>
                    <div class="progressBar">
                        <div class="fillBarVue"></div>
                    </div>
                    <h3 class="procentKnowledge">35%</h3>
                </div>
                <div class="toolsSkillContainer">
                    <h2 class="toolslSkill">HTML</h2>
                    <div class="progressBar">
                        <div class="fillBarHtml"></div>
                    </div>
                    <h3 class="procentKnowledge">80%</h3>
                </div>
                <div class="toolsSkillContainer">
                    <h2 class="toolslSkill">Css</h2>
                    <div class="progressBar">
                        <div class="fillBarCss"></div>
                    </div>
                    <h3 class="procentKnowledge">60%</h3>
                </div>
                <div class="toolsSkillContainer">
                    <h2 class="toolslSkill">Javascript</h2>
                    <div class="progressBar">
                        <div class="fillBarJavascript"></div>
                    </div>
                    <h3 class="procentKnowledge">30%</h3>
                </div>
                <div class="toolsSkillContainer">
                    <h2 class="toolslSkill">Git</h2>
                    <div class="progressBar">
                        <div class="fillBarGit"></div>
                    </div>
                    <h3 class="procentKnowledge">50%</h3>
                </div>
            </div>
            <div class="mySkillsDescription">
                <h1>The tools I have been using so far:</h1>
                <div class="toolsIconsContainer">      
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vuejs/vuejs-original-wordmark.svg" class="icon"/>
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/html5/html5-original-wordmark.svg" class="icon"/>
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg" class="icon"/>
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/css3/css3-original-wordmark.svg" class="icon"/>
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vitejs/vitejs-original.svg" class="icon"/>
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nodejs/nodejs-original.svg" class="icon"/>
                </div>
            </div>
        </div>
    </main>
</template>

<style scoped>
main{
    margin-top: 8%;
    height: 550px;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 5%;
    flex-direction: column;
}
.mySkillsHeadline{
    display: flex;
    height: 50%;
    justify-content: center;
    align-items: center;
    gap: 20%;
}
.mySkillsHeadline h1{
    font-size: 200%;
    font-weight: bold;
    color: rgb(85, 85, 85);
    font-family: "Apple Chancery, cursive";
}
.mySkillsImg{
    width: 30%;
    height: 50%;
}
.mySkillsContainer{
    display: flex;
    width: 100vw;
    height: 100%;
    justify-content: space-around;
}
.toolsSkillContainer{
    margin: 3.5%;
    margin-left: 10%;
    width: 100%;
    height: fit-content;
    display: flex;
    align-items: center;
    gap: 20px;
}
.toolsSkill{
    height: fit-content;
}
.progressBar{
    height: 30px;
    width: 30%;
    background-color: white;
}
.fillBarVue,
.fillBarHtml,
.fillBarCss,
.fillBarJavascript,
.fillBarGit{
    height: 100%;
    background-color: gray;
    border: solid 2px rgb(252, 156, 172);
    
    animation: fillBar 0.5s linear;
    animation-timeline: view();
    animation-name: fillBar;
    animation-fill-mode: both;
    animation-duration: 1ms;
    transform-origin: left;
}
.fillBarVue{
    width: 40%;
}
.fillBarHtml{
    width: 80%;
}
.fillBarCss{
    width: 70%;
}
.fillBarJavascript{
    width: 30%;
}
.fillBarGit{
    width: 50%;
}
@keyframes fillBar{
    0%{
        transform: scaleX(0%);
    }
    30%{
        transform: scaleX(100%);
    }
}
.procentKnowledge{
    margin-left: 5%;
    font-weight: bold;
    color: rgb(83, 83, 83);
}
.mySkillsGraph{
    height: 90%;
    width: 40%;
    background-color: rgb(252, 203, 211);
    border-radius: 5%;
    display: flex;
    flex-direction: column;
}
.mySkillsDescription{
    height: 90%;
    width: 40%;
    background-color: rgb(252, 203, 211);
    border-radius: 5%;
    display: flex;
    align-items: center;
    flex-direction: column;
    padding: 10px;
}
.mySkillsDescription,
h1{
    text-shadow: 2px 2px pink;
    animation: fade linear;
    animation-timeline: watch();
}
.icon{
    height: 30%;
    width: 30%;
    margin: 1.4%;
    animation: rotate 1s linear;
    animation-timeline: view();
    animation-fill-mode: both;
    animation-duration: 1ms;
    rotate: 20;
}
.toolsIconsContainer{
    display: flex;
    flex-wrap: wrap;
    height: 80%;
    width: 90%;
    font-weight: bold;
    font-size: 40px;
    
}
@keyframes rotate{
    0%{
        rotate: 75deg;
    }
    30%{
        rotate: 0deg;
    }
    100%{
        opacity: -75deg;
    }
}
h1,
h2,
h3{
    animation: fade 0.1s linear;
    animation-timeline: view();
    animation-fill-mode: both;
    animation-duration: 1ms;
}
@keyframes fade{
    0%{
        opacity: 0.1;
    }
    40%{
        opacity: 1;
    }
    70%{
        opacity: 1;
    }
    100%{
        opacity: 0.1;
    }
}
</style>