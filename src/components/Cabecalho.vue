<template>
    <section class="banner">
        <header>
            <a href="https://unifil.br/" target="blank"><img src="../../public/images/logo-unifil.png" alt="Logo UniFil" height="60" /></a>
            <ul class="menu">
                <a href="#apresentacao"><li>Apresentação</li></a>
                <a href="#quem-somos"><li>Quem Somos</li></a>
                <a href="#tema"><li>Tema do Projeto</li></a>
                <a href="#comunidade"><li>Comunidade</li></a>
                <a href="#documentacao"><li>Documentação</li></a>
                <a href="https://guilherme-mattos-conde.github.io/Dungeons-Quiz/" target="_blank"><li><img src="../../public/images/btn_jogar.png" alt="Jogar"></li></a>
            </ul>
        </header>
        <div>
            <h1>Duelo de Perguntas RPG</h1>
        </div>
    </section>
</template>

<style scoped>
.banner {
    background-image: url("/public/images/banner.png");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: fixed;

    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        background-color: transparent;
        color: white;
        padding: 10px 80px;
        text-align: center;

        img {
            height: 45px;
        }
    }

    .menu {
        display: flex;
        list-style: none;
        justify-content: center;
        align-items: center;

        a {
            text-decoration: none;
            color: rgb(176, 176, 176);
        }

        li {
            margin: 0 8px;
            transition: .5s;
        }
        li:hover {
            color: white;
        }

        a img {
            width: 180px;
            height: auto;
        }
    }

    div {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 550px;

        h1 {
            color: white;
            font-size: 35pt;
        }
    }
}
</style>