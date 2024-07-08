<template>
  <div class="cards-wrapper">
    <div v-for="(card, index) in cards" :key="index" class="card-container">
      <q-card class="my-card" >
        <q-img src="../assets/img/foto-nutri.png" class="card-image">
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
  data(){
    return{
      cards:[
        {
          imagem:'../assets/img/foto-nutri.png',
          titulo:"Laura Marques",
          descricao: "A Dra. Luiza Souza me ajudou a transformar minha alimentação e melhorar minha saúde em apenas três meses!"
        },
        {
          imagem:'../assets/img/foto-nutri.png',
          titulo:"Joana Lima",
          descricao: "Com a orientação da Dra. Luiza, consegui atingir meu peso ideal de maneira saudável e sustentável!"
        },
        {
          imagem:'../assets/img/foto-nutri.png',
          titulo:"Thaís Oliveira",
          descricao: "A Dra. Luiza é incrível! Suas dicas são práticas e realmente funcionam no dia a dia!"
        },
        {
          imagem:'../assets/img/foto-nutri.png',
          titulo:"Maria da Silv",
          descricao: "Recomendo a Dra. Luiza para todos que desejam uma mudança positiva na alimentação e saúde!"
        },
      ]
    }
  }

}
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

  margin:  35px 15px 15px 15px;
}
.card-image {
  height: 300px; /* Definindo altura da imagem */
}
</style>
