<template>
    <section>
        <h2>Documentação</h2>
        <div class="documentos">
            <div class="documento" v-for="documento in documentos" :key="documento.nome">
                <h3 class="titulo">{{ documento.nome }}</h3>
                <p class="pgf">{{ documento.descricao }}</p>
                <a :href="documento.link" target="blank"><button class="btn">Visualizar</button></a>
            </div>
        </div>
    </section>
</template>

<script setup>
import { documentos } from '@/mocks/documentos';
</script>

<style scoped>
section {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 50px 0;
    background-color: black;
    color: white;

    h2 {
        font-size: 25pt;
    }
}

.documentos {
    display: flex;
    justify-content: center;
    align-items: top;
    flex-wrap: wrap;
    max-width: 1000px;
}

.documento {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    align-items: center;
    margin: 2rem 2rem;
    width: 250px;

    .titulo {
        text-align: center;
        font-size: 13pt;
        margin: 0 10px 0 0;
        font-weight: bold;
    }

    .pgf {
        text-align: justify;
        font-size: 12pt;
        margin: 0;
    }

    .btn {
        background-color: white;
        padding: 5px 10px;
        border: 2px solid black;
        border-radius: 8px;
        font-size: 13pt;
        transition: .5s;
    }

    .btn:hover {
        background-color: rgb(240, 130, 35);
        cursor: pointer;
    }
}
</style>