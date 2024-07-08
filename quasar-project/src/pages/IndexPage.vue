<template>
  <q-page class="flex flex-center">
    <q-page-container>
      <div class="custom-gutter">
        <div class="q-col-gutter-md" style="display: flex; align-items: center;">
          <div class="q-col" style="padding: 20px;">
            <div class="content-wrapper">
              <p class="text-body1 text-weight-medium  q-pb-xl" shadow-2>
                Olá! Eu sou a Luiza Souza, nutricionista dedicada a ajudar você a alcançar um estilo de vida mais
                saudável e equilibrado.<br> Com anos de experiência na área de nutrição, meu objetivo é proporcionar a
                você
                um atendimento personalizado e de qualidade, focado nas suas necessidades individuais.
                <span class="gradient-border"></span>
              </p>
            </div>
          </div>
          <div class="q-col img-container" style="padding: 20px;">
            <q-img class="img-home" src="../assets/img/foto-nutri.png" alt="foto do  nutricionista">
              <div class="absolute-bottom text-h6 text-white">
                Luiza Souza
              </div>
            </q-img>

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
  margin-left: auto;

  margin-right: auto;

  max-width: 75%;

  padding-left: 10%;

  padding-right: 10%;

}

.img-home {
  width: 250px;
  border-radius: 40px 10px 40px 10px;
  height: 350px;
}



.gradient-border {
  display: inline-block;
  width: 350px;
  height: 15px;
  margin-bottom: 30px;
  border: none;
  background: linear-gradient(to right, #ffffff, #26A69A);
  border-image: linear-gradient(to right, #ffffff, #26A69A);
  border-image-slice: 1;
  border-radius: 80px;
  margin-top: 20px;
}
</style>
