<script>
export default {
    methods: {
        downloadFile() {
            const fileUrl = "/cv-jose-gomes.pdf"; // Caminho do arquivo para download (relativo à pasta public)
            const fileName = "cv-jose-gomes.pdf"; // Nome que o arquivo terá ao ser baixado pelo usuário

            const link = document.createElement("a"); // Cria dinamicamente um elemento HTML <a>
            link.href = fileUrl; // Define o atributo href do link para a URL do arquivo
            link.download = fileName; // Define o atributo download com o nome do arquivo

            document.body.appendChild(link); // Adiciona o link ao corpo do documento
            link.click(); // Dispara o clique no link para iniciar o download

            document.body.removeChild(link);
        }
    }
}
</script>

<template>
    <div class="card">
        <div class="card-content">
            <div class="main">
                <h1>José Gomes</h1>
                <h2>&lt;Front-End Developer /&gt;</h2>
                <p>Apaixonado em transformar soluções em código</p>
                <button class="btn4" @click="downloadFile">
                    <a>DOWNLOAD CV</a>
                    <img src="/public//iconArrow.png" alt="">
                </button>
            </div>
        </div>
    </div>
</template>

<style scoped>
.card {
    border-radius: 1.25rem;
    width: 19.8125rem;
    margin: 2.5rem auto;
    background: linear-gradient(to right, #5761B2, #1FC5A8);
}

.card-content {
    color: #FFFFFF;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 1.25rem 1.25rem;
}

/* #f83620 #f9d432 */

.card-content h1 {
    margin-top: 1.875rem;
    font-family: 'Gilroy', 'Inter', sans-serif;
    font-size: 3rem;
    font-weight: 700;
    margin: 0;
}

.card-content h2 {
    font-family: 'Sora', 'Inter', sans-serif;
    font-size: 1.125rem;
    font-weight: 600;
    margin: 0 0 1.25rem;
}

.card-content p {
    font-family: 'Inter', 'Poppins', sans-serif;
    font-size: 1.125rem;
    font-weight: 400;
    margin: 1.875rem 0 1.875rem;
}

/* .btn-cv {
    all: unset;
    outline: none;
    display: flex;
    justify-content: space-between;
    background-color: #1E1E1E;
    color: #FFFFFF;
    width: 13.75rem;
    height: 1.875rem;
    border-radius: 1rem;
    align-items: center;
    margin: 2.5rem auto 0.625rem;
    padding: 0.9375rem;
    cursor: pointer;
}

.btn-cv p {
    all: unset;
    outline: none;
    color: #FFFFFF;
    font-size: 1.125rem;
    font-family: 'Inter', 'Poppins', sans-serif;
    font-weight: 200;
    text-align: center;
    margin: 0;
    cursor: pointer;
}

.btn-cv img {
    all: unset;
    width: 1.5rem;
    height: 1.5rem;
    cursor: pointer;
} */

.btn4 {
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    padding: 10px 20px;
    background-color: #836fff;
    color: #fff;
    font-size: 16px;
    text-align: center;
    width: 100%;
    border: 2px solid transparent;
    cursor: pointer;
    overflow: hidden;
    z-index: 1;
    font-size: 1.125rem;
    font-family: 'Inter', 'Poppins', sans-serif;
    font-weight: 800;
    border-radius: 1rem;
}

.btn4::before {
    content: "";
    position: absolute;
    top: -4px;
    left: -4px;
    right: -4px;
    bottom: -4px;
    background: linear-gradient(92.83deg, #ff9966 0%, #ff5e62 100%);
    z-index: -1;
    filter: blur(4px);
    transform: rotate(0deg);
    transform-origin: center;
    transition: transform 0.4s;
    animation: rotateGradient 4s linear infinite;
}

@keyframes rotateGradient {
    0% {
        transform: rotate(0deg);
    }

    100% {
        transform: rotate(360deg);
    }
}
</style>