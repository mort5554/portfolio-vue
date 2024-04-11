<script setup>

</script>

<template>
    <footer>
        <div class="footerLogo" tabindex="0" id="contactAnchor">
            <img class="logo" src="/mainIcons/M-logo.png" alt="Logo">
        </div>
        <div class="links">
            <a href="https://github.com/mort5554" target="_blank" rel="noreferrer" tabindex="-1" class="githubLogo"><img src="/mainIcons/github.svg" alt="Github logo" class="githubLink"></a>
            <a href="mailto:kontozwykle013@gmail.com" target="_blank" rel="noreferrer" class="gmailLogo"><img src="/mainIcons/gmail.svg" alt="Gmail Icon" tabindex="-1"></a>
        </div>
        <div class="madeBy">
            <h1>Made By @mort5554</h1>
        </div>
    </footer>
</template>

<style scoped>
footer{
    display: flex;
    flex-direction: column;
    margin-top: 80px;
    height: 350px;
    width: 100%;
    background-color: pink;
}
.footerLogo{
    width: 100%;
    height: 40%;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 30px;
}
.links{
    display: flex;
    justify-content: center;
    height: 25%;
    gap: 50px;
}
.githubLogo{
    width: 5.5%;

}
.gmailLogo{
    width: 5.5%;
}
@media (max-width: 836px) {
    .githubLogo,
    .gmailLogo{
        width: 11%;
    }
}
.githubLink,
.gmailLink{
    position: static;
    cursor: pointer;
}
.madeBy{
    height: 20%;
    display: flex;
    justify-content: center;
    align-items: center;
}
.logo{
    height: 210%;
    margin-top: 45px;
}
</style>