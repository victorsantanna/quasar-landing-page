<template>
  <div class="cards-wrapper">
    <div v-for="(card) in cards" :key="card.id" class="card-container">
      <q-card class="my-card">
        <q-img :src="card.imagem" class="card-image">
          <div class="absolute-bottom text-h6 text-white">
            {{ card.titulo }}
          </div>
        </q-img>
        <q-card-section>
          {{ card.descricao }}
        </q-card-section>
      </q-card>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          id: 1,
          titulo: "Laura Marques",
          descricao:
            "A Dra. Luiza Souza me ajudou a transformar minha alimentação e melhorar minha saúde em apenas três meses!",
          imagem: "",
        },
        {
          id: 2,
          titulo: "Joana Lima",
          descricao:
            "Com a orientação da Dra. Luiza, consegui atingir meu peso ideal de maneira saudável e sustentável!",
          imagem: "",
        },
        {
          id: 3,
          titulo: "Thaís Oliveira",
          descricao:
            "A Dra. Luiza é incrível! Suas dicas são práticas e realmente funcionam no dia a dia!",
          imagem: "",
        },
        {
          id: 4,
          titulo: "Nayara da Silva",
          descricao:
            "Recomendo a Dra. Luiza para todos que desejam uma mudança positiva na alimentação e saúde!",
          imagem: "",
        },
      ],
    };
  },
  created() {
    // Carregar imagens dinamicamente usando import.meta.url
    this.cards.forEach((card, index) => {
      switch (index % 4) {
        case 0:
          card.imagem = new URL("../assets/img/foto.png", import.meta.url).href;
          break;
        case 1:
          card.imagem = new URL("../assets/img/foto2.png", import.meta.url).href;
          break;
        case 2:
          card.imagem = new URL("../assets/img/foto3.png", import.meta.url).href;
          break;
        case 3:
          card.imagem = new URL("../assets/img/foto4.png", import.meta.url).href;
          break;
        default:
          card.imagem = ""; // Caso haja mais cards do que imagens, isso garante que a imagem será vazia
      }
    });
  },
};
</script>

<style>
.cards-wrapper {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.my-card {
  width: 250px; /* Definindo largura fixa */
  height: 450px; /* Definindo altura fixa */
}

.card-container {
  margin: 35px 15px 15px 15px;
}

.card-image {
  height: 300px; /* Definindo altura da imagem */
}
</style>
