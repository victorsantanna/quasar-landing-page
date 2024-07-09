<template>
  <q-page>
    <q-page-container class="flex flex-center container ">
      <q-page-container class="q-mb-xl">
        <!-- Primeira coluna com informações -->
        <div class="column ">
          <div class="text-center">
            <h2>Contate-nos</h2>
          </div>
          <div class="text-center">
            <q-icon name="fab fa-facebook" size="2.5em" class="q-mx-md" color="secondary" />
            <q-icon name="fab fa-instagram" size="2.5em" class="q-mx-md" color="secondary" />
            <q-icon name="fab fa-google-plus" size="2.5em" class="q-mx-md" color="secondary" />
          </div>
        </div>
      </q-page-container>

      <!-- Segunda coluna com formulário -->
      <q-page-container>
        <div class="column">
          <q-form @submit="submitForm" class="text-center">
            <q-input outlined v-model="formData.nome" label="Nome completo" dense class="q-mb-md" />
            <q-input outlined v-model="formData.email" label="Email" type="email" dense class="q-mb-md" />
            <q-input outlined v-model="formData.Text" label="Digite seu texto"  dense type="textarea" />

            <q-btn color="secondary" label="Enviar" type="submit" class="q-mt-md" />
          </q-form>

        </div>
      </q-page-container>
    </q-page-container>
  </q-page>
</template>

<script>

export default {
  name: 'ContatoForm',


  data() {
    return {
      formData: {
        nome: '',
        email: '',
        Text: ''
      }
    };
  },
  methods: {
    submitForm() {
      console.log('Formulário enviado:', this.formData);

    }
  }
};
</script>

<style scoped>
.column {
  padding: 20px;
}

.q-input,
.q-btn {
  width: 300px;
  max-width: 400px;
}

.q-icon {
  cursor: pointer;
}

</style>
