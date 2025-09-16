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
import { ref } from "vue";

const documentos = ref([
    {
        nome: "Documento de Visão",
        descricao: "Define o escopo do projeto, os objetivos e as necessidades dos stakeholders. É essencial para alinhar expectativas e direcionar o desenvolvimento do sistema.",
        link: "https://drive.google.com/file/d/1VCTzq0u5C3OVWNCr85BOnT2Dn3A-uP-K/view?usp=sharing",
    },
    {
        nome: "Diagrama de Caso de Uso",
        descricao: "Ilustra graficamente as interações entre usuários (atores) e as funcionalidades do sistema (casos de uso). Ele é importante para esclarecer como o sistema será usado e as funcionalidades necessárias.",
        link: "https://drive.google.com/file/d/19R69Uqo_zYm99a8gAEcGTkIgTM9GDvUp/view?usp=sharing",
    },
    {
        nome: "Diagrama de Classes",
        descricao: "Mostra a estrutura estática do sistema, representando classes, atributos, métodos e relacionamentos entre elas. Ele é importante para orientar a implementação do sistema em código.",
        link: "https://drive.google.com/file/d/1uzK6LJJE7HchpLnffyJAgwiX871MioiE/view?usp=sharing",
    },
    {
        nome: "DER (Diagrama Entidade-Relacionamento)",
        descricao: "Modelo visual que representa os principais dados do sistema e como se relacionam. Ele é importante para projetar a estrutura do banco de dados, garantindo integridade e eficiência.",
        link: "https://drive.google.com/file/d/1X__63c01iUs6hlPnIvdyJIhGYq58VO0I/view?usp=sharing",
    },
    {
        nome: "Workflow (Fluxo de Trabalho)",
        descricao: "Representa a sequência de passos, tarefas e decisões em um processo específico. Ele é importante para otimizar processos, melhorar a eficiência e esclarecer responsabilidades e fluxo de informação.",
        link: "https://drive.google.com/file/d/14p-PBiLz-m_rOEoQcWJoPmIui09bPkNd/view?usp=sharing",
    },
    {
        nome: "MVP (Minimum Viable Product)",
        descricao: "É a versão mais simples do produto com funcionalidades essenciais para atender usuários iniciais. Ele é importante para validar a ideia no mercado real com o mínimo de esforço e risco.",
        link: "https://www.figma.com/proto/h2oNYljQ2sjmtySNZZdi8s/MVP---Dungeons-and-Quiz?node-id=49-170&p=f&t=erxlZ4do3X5morWe-1&scaling=scale-down-width&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=49%3A170&authuser=2",
    }
]);

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