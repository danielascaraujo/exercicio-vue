<script>
export default {
  data() {
    return {
      numero1: 0,
      numero2: 0,
      operacao: '+',
    };
  },
  computed: {
    resultado() {
      switch (this.operacao) {
        case '+':
          return this.numero1 + this.numero2;
        case '-':
          return this.numero1 - this.numero2;
        case '*':
          return this.numero1 * this.numero2;
        case '/':
          return this.numero1 / this.numero2;
        default:
          return 0;
      }
    },
  },
};
</script>

<template>
  <div>
    <input type="number" v-model.number="numero1" />
      <select v-model="operacao">
        <option value="+">Soma</option>
        <option value="-">Subtração</option>
        <option value="*">Multiplicação</option>
        <option value="/">Divisão</option>
      </select>
    <input type="number" v-model.number="numero2" />
    <p>Resultado: {{ resultado }}</p>
  </div>
</template>

<style scoped>

</style>
