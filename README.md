<!DOCTYPE html>
<html lang="pt-br">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meus objetivos do ano</title>
    <link rel="stylesheet" href="style.css">
</head>const botoes = document.querySelectorAll(".botao");
const textos = document.querySelectorAll(".aba-conteudo");

for (let i = 0; i < botoes.length; i++) {
    botoes[i].onclick = function () {

        for (let j = 0; j < botoes.length; j++) {
            botoes[j].classList.remove("ativo");
            textos[j].classList.remove("ativo");
        }

        botoes[i].classList.add("ativo");
        textos[i].classList.add("ativo");
    }
}

const contadores = document.querySelectorAll(".contador");
const tempoObjetivo1 = new Date("2020-10-05T00:00:00");
const tempoObjetivo2 = new Date("2023-12-05T00:00:00");
const tempoObjetivo3 = new Date("2023-12-30T00:00:00");
const tempoObjetivo4 = new Date("2024-02-01T00:00:00");

const tempos = [tempoObjetivo1, tempoObjetivo2, tempoObjetivo3, tempoObjetivo4];


function calculaTempo(tempoObjetivo) {
    let tempoAtual = new Date();
    let tempoFinal = tempoObjetivo - tempoAtual;
    let segundos = Math.floor(tempoFinal / 1000);
    let minutos = Math.floor(segundos / 60);
    let horas = Math.floor(minutos / 60);
    let dias = Math.floor(horas / 24);

    segundos %= 60;
    minutos %= 60;
    horas %= 24;
    if (tempoFinal > 0) {
        return [dias, horas, minutos, segundos];
    } else {
        return [0, 0, 0, 0];
    }
}

function atualizaCronometro() {
    document.getElementById("dias0").textContent = calculaTempo(tempos[0])[0];
    document.getElementById("horas0").textContent = calculaTempo(tempos[0])[1];
    document.getElementById("min0").textContent = calculaTempo(tempos[0])[2];
    document.getElementById("seg0").textContent = calculaTempo(tempos[0])[3];

    for (let i = 0; i < contadores.length; i++) {
        // contadores[i].textContent = calculaTempo(tempos[i]);   
    }
}

function comecaCronometro() {
    atualizaCronometro();
    setInterval(atualizaCronometro, 1000);
}

comecaCronometro();const botoes = document.querySelectorAll(".botao");
const textos = document.querySelectorAll(".aba-conteudo");

for (let i = 0; i < botoes.length; i++) {
    botoes[i].onclick = function () {

        for (let j = 0; j < botoes.length; j++) {
            botoes[j].classList.remove("ativo");
            textos[j].classList.remove("ativo");
        }

        botoes[i].classList.add("ativo");
        textos[i].classList.add("ativo");
    }
}

const contadores = document.querySelectorAll(".contador");
const tempoObjetivo1 = new Date("2020-10-05T00:00:00");
const tempoObjetivo2 = new Date("2023-12-05T00:00:00");
const tempoObjetivo3 = new Date("2023-12-30T00:00:00");
const tempoObjetivo4 = new Date("2024-02-01T00:00:00");

const tempos = [tempoObjetivo1, tempoObjetivo2, tempoObjetivo3, tempoObjetivo4];


function calculaTempo(tempoObjetivo) {
    let tempoAtual = new Date();
    let tempoFinal = tempoObjetivo - tempoAtual;
    let segundos = Math.floor(tempoFinal / 1000);
    let minutos = Math.floor(segundos / 60);
    let horas = Math.floor(minutos / 60);
    let dias = Math.floor(horas / 24);

    segundos %= 60;
    minutos %= 60;
    horas %= 24;
    if (tempoFinal > 0) {
        return [dias, horas, minutos, segundos];
    } else {
        return [0, 0, 0, 0];
    }
}

function atualizaCronometro() {
    document.getElementById("dias0").textContent = calculaTempo(tempos[0])[0];
    document.getElementById("horas0").textContent = calculaTempo(tempos[0])[1];
    document.getElementById("min0").textContent = calculaTempo(tempos[0])[2];
    document.getElementById("seg0").textContent = calculaTempo(tempos[0])[3];

    for (let i = 0; i < contadores.length; i++) {
        // contadores[i].textContent = calculaTempo(tempos[i]);   
    }
}

function comecaCronometro() {
    atualizaCronometro();
    setInterval(atualizaCronometro, 1000);
}

comecaCronometro();

<body>
    <section class="conteudo-principal">
        <h2 class="titulo-principal">Meus Objetivos do ano<span>_</span></h2>
        <div class="conteudo">
            <div class="botoes">
                <button class="botao ativo">Cursos na Alura</button>
                <button class="botao">Criar projetos em Javascript</button>
                <button class="botao">Criar um portfolio</button>
                <button class="botao">Atualizar meu currículo</button>
            </div>
            <div class="abas-textos">
                <div class="aba-conteudo ativo">
                    <h3 class="aba-conteudo-titulo-principal">Estudar 4 cursos na Alura</h3>
                    <h4 class="aba-conteudo-titulo-secundario">Tempo para completar o objetivo</h4>
                    <div class="contador">
                        <div class="contador-digito">
                            <p class="contador-digito-numero">7</p>
                            <p class="contador-digito-texto">dias</p>
                        </div>
                        <div class="contador-digito">
                            <p class="contador-digito-numero">7</p>
                            <p class="contador-digito-texto">horas</p>
                        </div>
                        <div class="contador-digito">
                            <p class="contador-digito-numero">7</p>
                            <p class="contador-digito-texto">min</p>
                        </div>
                        <div class="contador-digito">
                            <p class="contador-digito-numero">7</p>
                            <p class="contador-digito-texto">seg</p>
                        </div>
                    </div>
                </div>
                <div class="aba-conteudo">
                    <h3 class="aba-conteudo-titulo-principal">Criar 5 projetos em Javascript</h3>
                    <h4 class="aba-conteudo-titulo-secundario">Tempo para completar o objetivo</h4>
                    <div class="contador"></div>
                </div>
                <div class="aba-conteudo">
                    <h3 class="aba-conteudo-titulo-principal">Criar um portfolio com os meus 3 melhores projetos</h3>
                    <h4 class="aba-conteudo-titulo-secundario">Tempo para completar o objetivo</h4>
                    <div class="contador"></div>
                </div>const botoes = document.querySelectorAll(".botao");
const textos = document.querySelectorAll(".aba-conteudo");

for (let i = 0; i < botoes.length; i++) {
    botoes[i].onclick = function () {

        for (let j = 0; j < botoes.length; j++) {
            botoes[j].classList.remove("ativo");
            textos[j].classList.remove("ativo");
        }

        botoes[i].classList.add("ativo");
        textos[i].classList.add("ativo");
    }
}

const contadores = document.querySelectorAll(".contador");
const tempoObjetivo1 = new Date("2020-10-05T00:00:00");
const tempoObjetivo2 = new Date("2023-12-05T00:00:00");
const tempoObjetivo3 = new Date("2023-12-30T00:00:00");
const tempoObjetivo4 = new Date("2024-02-01T00:00:00");

const tempos = [tempoObjetivo1, tempoObjetivo2, tempoObjetivo3, tempoObjetivo4];


function calculaTempo(tempoObjetivo) {
    let tempoAtual = new Date();
    let tempoFinal = tempoObjetivo - tempoAtual;
    let segundos = Math.floor(tempoFinal / 1000);
    let minutos = Math.floor(segundos / 60);
    let horas = Math.floor(minutos / 60);
    let dias = Math.floor(horas / 24);

    segundos %= 60;
    minutos %= 60;
    horas %= 24;
    if (tempoFinal > 0) {
        return [dias, horas, minutos, segundos];
    } else {
        return [0, 0, 0, 0];
    }
}

function atualizaCronometro() {
    document.getElementById("dias0").textContent = calculaTempo(tempos[0])[0];
    document.getElementById("horas0").textContent = calculaTempo(tempos[0])[1];
    document.getElementById("min0").textContent = calculaTempo(tempos[0])[2];
    document.getElementById("seg0").textContent = calculaTempo(tempos[0])[3];

    for (let i = 0; i < contadores.length; i++) {
        // contadores[i].textContent = calculaTempo(tempos[i]);   
    }
}

function comecaCronometro() {
    atualizaCronometro();
    setInterval(atualizaCronometro, 1000);
}

comecaCronometro();
                <div class="aba-conteudo">
                    <h3 class="aba-conteudo-titulo-principal">Atualizar meu curriculo com os certificados da Alura</h3>
                    <h4 class="aba-conteudo-titulo-secundario">Tempo para completar o objetivo</h4>
                    <div class="contador"></div>
                </div>
            </div>
        </div>
    </section>
    <script src="main.js"></script>
</body>

</html>
@import url('https://fonts.googleapis.com/css2?family=Chakra+Petch:wght@400;700&display=swap');

:root {
    --cor-de-fundo: #1E1E1E;
    --verde: #6FFF57;
    --branco: #FFFFFF;
    --botao-ativo: #3A375E;
    --botao-inativo: rgba(58, 55, 94, 0.5);
    --texto-fundo: rgba(58, 55, 94, 0.3);
}

body {
    background-color: var(--cor-de-fundo);
    color: var(--branco);
    font-family: 'Chakra Petch', sans-serif;
}


.conteudo-principal {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    max-width: 1200px;
    width: 100%;
    margin: 0 auto;
}

.titulo-principal {
    text-align: left;
    width: 100%;
    font-size: 32px;
}

.titulo-principal span {
    color: var(--verde);
}


.botao {
    font-family: 'Chakra Petch', sans-serif;
    background-color: var(--botao-inativo);
    color: var(--branco);
    display: flex;
    justify-content: center;
    padding: 1em;
    font-size: 18px;
    align-items: center;
    width: 100%;
    border-bottom: 4px solid var(--botao-ativo);
    border-left: 2px solid var(--botao-ativo);
    border-right: 2px solid var(--botao-ativo);
    border-top: none;
}

.botao:first-child {
    border-radius: 40px 40px 0 0;
}

.botoes {
    display: block;
}

.botao.ativo {
    background-color: var(--botao-ativo);
    border-bottom: 4px solid var(--verde);
}

.abas-textos {
    background-color: var(--texto-fundo);
    padding: 40px;
    border-radius: 0 0 40px 40px;
}

.aba-conteudo.ativo {
    display: block;
}

.aba-conteudo {
    display: none;
}

.aba-conteudo-titulo-principal {
    font-size: 28px;
    text-align: center;
}

.aba-conteudo-titulo-secundario {
    text-align: center;
    color: var(--verde);
    text-transform: uppercase;
}

.contador {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
}

.contador-digito {
    padding: 0 16px;
    text-align: center;
    min-width: 100px;
}

.contador-digito-numero {
    font-size: 80px;
    margin: 0;

}

.contador-digito-texto {
    color: var(--verde);
    font-size: 20px;
    margin: 0;

}

@media screen and (min-width: 768px) {
    .botoes {
        display: flex;
    }

    .botao:first-child {
        border-radius: 40px 0 0 0;
    }

    .botao:last-child {
        border-radius: 0 40px 0 0;
    }
}
const botoes = document.querySelectorAll(".botao");
const textos = document.querySelectorAll(".aba-conteudo");

for (let i = 0; i < botoes.length; i++) {
    botoes[i].onclick = function () {

        for (let j = 0; j < botoes.length; j++) {
            botoes[j].classList.remove("ativo");
            textos[j].classList.remove("ativo");
        }

        botoes[i].classList.add("ativo");
        textos[i].classList.add("ativo");
    }
}

const contadores = document.querySelectorAll(".contador");
const tempoObjetivo1 = new Date("2020-10-05T00:00:00");
const tempoObjetivo2 = new Date("2023-12-05T00:00:00");
const tempoObjetivo3 = new Date("2023-12-30T00:00:00");
const tempoObjetivo4 = new Date("2024-02-01T00:00:00");

const tempos = [tempoObjetivo1, tempoObjetivo2, tempoObjetivo3, tempoObjetivo4];


function calculaTempo(tempoObjetivo) {
    let tempoAtual = new Date();
    let tempoFinal = tempoObjetivo - tempoAtual;
    let segundos = Math.floor(tempoFinal / 1000);
    let minutos = Math.floor(segundos / 60);
    let horas = Math.floor(minutos / 60);
    let dias = Math.floor(horas / 24);

    segundos %= 60;
    minutos %= 60;
    horas %= 24;
    if (tempoFinal > 0) {
        return [dias, horas, minutos, segundos];
    } else {
        return [0, 0, 0, 0];
    }
}

function atualizaCronometro() {
    document.getElementById("dias0").textContent = calculaTempo(tempos[0])[0];
    document.getElementById("horas0").textContent = calculaTempo(tempos[0])[1];
    document.getElementById("min0").textContent = calculaTempo(tempos[0])[2];
    document.getElementById("seg0").textContent = calculaTempo(tempos[0])[3];

    for (let i = 0; i < contadores.length; i++) {
        // contadores[i].textContent = calculaTempo(tempos[i]);   
    }
}

function comecaCronometro() {
    atualizaCronometro();
    setInterval(atualizaCronometro, 1000);
}

comecaCronometro();
