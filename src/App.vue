<script>

export default {
  data() {
    return {
      numero1: '',
      numero2: '',
      total:''
    }
  },

  computed: {
    resultado() {
      switch(this.total) {
        case 'adicao':
          return this.numero1 + this.numero2
        case 'subtrair':
          return this.numero1 - this.numero2
        case 'multiplicar':
          return this.numero1 * this.numero2
        case 'dividir':
          return this.numero1 / this.numero2
        }
    }
  }
}
</script>

<template>

  <div class="container">
    <header>
      <div class="row mt-5 p-5 text-center">
        <h1>Calculadora Aritimética</h1>
      </div>
    </header>

    <div class="row">
      <div class="col-md-3">
        <select class="form-control form-control-lg text-center" v-model="total">
          <option disabled value="">Selecione a operação</option>
          <option value="adicao">Adição</option>
          <option value="subtrair">Subtração</option>
          <option value="multiplicar">Multiplicação</option>
          <option value="dividir">Divisão</option>
        </select>
      </div>
      <div class="col-md-3">
        <input type="number" min="0" placeholder="Número 1" class="form-control form-control-lg text-center" v-model.number="numero1">
      </div>
      <div class="col-md-3">
        <input type="number" min="0" placeholder="Número 2" class="form-control form-control-lg text-center" v-model.number="numero2">
      </div>
      <div class="col-md-3">
        <h4 class="mt-2">Resultado: {{ resultado }}</h4>
      </div>
    </div>
  </div>

</template>

<style scoped>
</style>
