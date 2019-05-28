<template>
  <div>
    <h2>The money Game</h2>
    <p>Jack and Jill both won 2 all-access tickets to the Amusement Park </p>
       <p>They both also have $100 each in their pockets and want to play the MG</p>
    <button v-on:click="jack++">Add $1 to Jack</button>
    <button v-on:click="jill++">Add $1 to Jill</button>
    <p>Jack: ${{jack}}</p> <p>Jill: ${{jill}}</p>
    <p>Jack's Total: {{addJack}}</p>
    
    <p>Jill's Total: {{addJill}}</p>
  </div>
</template>

<script>
export default {
  name: 'Test',
  data() {
    return {
     safe: 100,
     jack: 0,
     jill: 0
    }

  },
  computed:{
    addJack: function(){
      console.log('Jack function ran!');
      return '$'+(this.jack + this.safe);
    },
    addJill: function(){
      console.log('Jill function ran!');
      return '$'+(this.jill + this.safe);
    }
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
button {
    background-color: rgb(58, 128, 194); 
    border: none;
    color: white;
    padding: 15px 32px;
    margin: 5px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 18px;
  }
</style>
