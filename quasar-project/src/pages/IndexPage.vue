<template>
  <q-page class="flex flex-center">
    <q-page-container>
      <div class="custom-gutter">
        <div class="q-col-gutter-md" style="display: flex;">

          <div class="q-col" style="padding: 20px;">
            <div  class="content-wrapper">
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur in est mi. Aliquam faucibus rhoncus
                vehicula. Aenean non hendrerit lectus, at porta nibh. Nullam justo diam, blandit vitae rutrum ac, pulvinar
                id mi. Quisque at lectus in elit lobortis faucibus venenatis ut mauris. Fusce at iaculis lacus, at aliquam
                ex. Pellentesque malesuada cursus libero, vel pulvinar nulla rutrum vel.
              </p>
            </div>
          </div>
          <div class="q-col" style="padding: 20px;">

            <img class="img-home" src="../assets/img/foto-nutri.png" alt="foto do  nutricionista">

          </div>
        </div>
      </div>
    </q-page-container>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'IndexPage'
});
</script>

<style>

.custom-gutter {
  margin-left: auto; /* Para alinhar à direita */
  margin-right: auto; /* Para alinhar à esquerda */
  max-width:75%; /* 80% da largura disponível */
  padding-left: 10%; /* Espaço à esquerda */
  padding-right: 10%; /* Espaço à direita */
  padding-bottom: 10%;
}

.img-home{
  width: 200px;
  border-radius: 40px 10px 40px 10px;
  height: 400px;
}
</style>
