<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="bg-secondary text-white flex flex-center" shadow-2 style="height: 80px;">
      <q-toolbar >


        <q-toolbar-title class="text-white" style="margin-left: 60px; ">
          <q-avatar>
            <img src="../assets/img/logo-quasar-projeto.png" alt="Logo Projeto" style="filter: invert(100%); width: 60px">
          </q-avatar >
          <router-link to="/" style="text-decoration: none;" class="text-white" >
            Nutricionista Luiza Souza
          </router-link>
        </q-toolbar-title>

        <q-tabs  shrink  v-model="activeTab">
          <router-link to="/" style="text-decoration: none;">
            <q-tab class="text-white" name="Home" label="Home"></q-tab>
          </router-link>
          <router-link to="/portfolionutri" style="text-decoration: none;">
            <q-tab class="text-white" name="tab1" label="PortFolio"></q-tab>
          </router-link>
          <router-link to="/testeimc" style="text-decoration: none;">
            <q-tab name="tab2"  class="text-white" label="Teste IMC" ></q-tab>
          </router-link>
          <router-link to="/contato" style="text-decoration: none;">
            <q-tab name="tab3"  class="text-white" label="Contato"></q-tab>
          </router-link>
        </q-tabs>

      </q-toolbar>
    </q-header>


    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'




export default defineComponent({
  name: 'MainLayout',
  data() {
    return {
      activeTab: 'Home' // Define 'Home' como o tab inicialmente ativo
    };
  }
})
</script>
