<template>
  <div class="mb-20">
      Counter: {{ number }}
      <div>
          <lable for="counter" v-bind:title="number">Counter: </lable>
          <input type="text" v-model="number">
          <button v-on:click="increase">+</button>
          <button v-on:click="decrease">-</button>
          <button v-on:click="increaseten">+10</button>
          <button v-on:click="multiplytwo">x2</button>
      </div>
      
  </div>
</template>

<script>
export default {
    data(){
       return{
           number: 200
       } 
    },
    methods:{
        increase(){
            this.number++
        },
        decrease(){
            this.number--
        },
        increaseten(){  
            this.number++,
            this.number = this.number+9
        },
        multiplytwo(){
            this.number*=2
        },
    }

}
</script>

<style scoped lang="scss">
.mb-20{
    margin-bottom: 20px;
}

</style>