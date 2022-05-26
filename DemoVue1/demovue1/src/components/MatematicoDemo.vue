<template>
    <div>
      <div>
      <h2> {{result}} </h2>
    </div>
<h1>{{ title }}</h1>
<h2>{{ subtitle }}</h2>
<ul>
<li>{{ items[0] }}</li>
<li>{{ items[1] }}</li>
<li>{{ items[2] }}</li>
</ul>
</div> 
</template>

<style lang="scss" scoped>
  @import url('../assets/styles/typography.scss');
</style>
<script>

export default {
    props: {
      num1: Number,
      num2: Number,
      operacion: String
  },
  data() {
      return {
        result: 0,
        title: 'My list component!',
      subtitle: 'Vue JS basics',
      items: ['Item 1', 'Item 2', 'Item 3']
      }
    },
    methods: {
      calcOperacion: function() {
        switch(this.operacion) {
      case "+":
        console.log(this.operacion);
        this.result = this.num1 + this.num2
        break;
      case "-":
        console.log(this.operacion);
        this.result = this.num1 - this.num2
        break;
      case "*":
        console.log(this.operacion);
        this.result = this.num1 * this.num2
        break;
      case "/":
        console.log(this.operacion);
        this.result = this.num1 / this.num2
        break;
    }
      }
    },
    watch: {
      props: {
        deep: true,
        handler(){
          this.calcOperacion();
        },
        inmediate: true
      }
    }
}
</script>
