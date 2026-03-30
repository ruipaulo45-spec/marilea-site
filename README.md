<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Marilea Lima</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}

body {
    background: #0f0f0f;
    color: white;
    overflow-x: hidden;
}

/* ANIMAÇÃO */
.fade {
    opacity: 0;
    transform: translateY(30px);
    transition: 1s;
}

.fade.show {
    opacity: 1;
    transform: translateY(0);
}

/* HERO */
.hero {
    height: 100vh;
    background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.9)),
    url('FOTO1.jpg') center/cover no-repeat fixed;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
}

.hero h1 {
    font-size: 3rem;
}

.hero p {
    opacity: 0.8;
    margin-top: 10px;
}

/* BOTÃO */
.btn {
    margin-top: 25px;
    padding: 12px 30px;
    background: #ff4d6d;
    border: none;
    border-radius: 30px;
    color: white;
    font-size: 1rem;
    cursor: pointer;
    transition: 0.3s;
}

.btn:hover {
    transform: scale(1.1);
    background: #ff1f4b;
}

/* SEÇÕES */
section {
    padding: 80px 20px;
    text-align: center;
}

.card {
    max-width: 900px;
    margin: auto;
}

/* GALERIA */
.gallery {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px,1fr));
    gap: 15px;
    margin-top: 20px;
}

.gallery img {
    width: 100%;
    border-radius: 15px;
    transition: 0.4s;
}

.gallery img:hover {
    transform: scale(1.08);
}

/* FRASE */
.quote {
    font-size: 1.4rem;
    line-height: 1.6;
    max-width: 800px;
    margin: auto;
}

/* BOTÃO FINAL */
.final-btn {
    margin-top: 30px;
    padding: 15px 35px;
    background: #ff4d6d;
    border-radius: 30px;
    cursor: pointer;
    display: inline-block;
    transition: 0.3s;
}

.final-btn:hover {
    transform: scale(1.1);
}

/* FOOTER */
footer {
    padding: 20px;
    opacity: 0.6;
}
</style>

</head>

<body>

<!-- MÚSICA -->
<audio autoplay loop>
    <source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_115b9b6b5d.mp3" type="audio/mp3">
</audio>

<!-- HERO -->
<section class="hero">
    <h1 class="fade">Intensa em tudo o que faz</h1>
    <p class="fade">Inspiradora em cada detalhe</p>
    <button class="btn fade" onclick="scrollToSection()">Conhecer mais</button>
</section>

<!-- SOBRE -->
<section id="sobre" class="fade">
    <div class="card">
        <h2>Quem é Marilea</h2>
        <p>
            Marilea é presença, energia e dedicação. Como corretora de seguros de saúde,
            ela cuida de vidas, protege histórias e transforma cada atendimento em algo humano e especial.
        </p>
    </div>
</section>

<!-- PROFISSÃO -->
<section class="fade">
    <div class="card">
        <h2>Profissão & Propósito</h2>
        <p>
            Mais do que vender planos, Marilea entrega cuidado, segurança e tranquilidade.
            Sua intensidade faz dela uma profissional única e inspiradora.
        </p>
    </div>
</section>

<!-- GALERIA -->
<section class="fade">
    <h2>Momentos & Conquistas</h2>
    <div class="gallery">
        <img src="FOTO1.jpg">
        <img src="FOTO2.jpg">
        <img src="FOTO3.jpg">
        <img src="FOTO4.jpg">
    </div>
</section>

<!-- ENERGIA -->
<section class="fade">
    <div class="card">
        <h2>Energia que inspira</h2>
        <p>
            Determinada, ativa e intensa, ela vive com propósito.
            Seja correndo atrás dos objetivos ou aproveitando a vida, ela inspira todos ao redor.
        </p>
    </div>
</section>

<!-- MENSAGEM -->
<section class="fade">
    <div class="quote">
        <p>
            Marilea, você é uma daquelas intensa que faz tudo com tanta dedicação que inspira todo mundo ao redor.<br><br>
            Mesmo de longe, dá pra ver o quanto você é competente e apaixonada pelo que faz.<br><br>
            <strong>A semana é sua, intensa como você! ❤️</strong>
        </p>

        <div class="final-btn" onclick="alert('Você é incrível! ❤️')">
            Enviar carinho 💌
        </div>
    </div>
</section>

<footer>
    Feito com carinho 💖
</footer>

<script>
// SCROLL
function scrollToSection() {
    document.getElementById("sobre").scrollIntoView({ behavior: "smooth" });
}

// ANIMAÇÃO
const elements = document.querySelectorAll('.fade');

window.addEventListener('scroll', () => {
    elements.forEach(el => {
        const top = el.getBoundingClientRect().top;
        if (top < window.innerHeight - 50) {
            el.classList.add('show');
        }
    });
});
</script>

</body>
</html>
