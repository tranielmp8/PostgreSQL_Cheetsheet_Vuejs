<template>
  <div class="container">
    <Hero />
    <div class="sql-container">
      <h1>SNIPPETS</h1>
      <Create />
      <Insert />
      <Select />
      <Where />
      <Count />
      <Groupby />
      <Joins />
      <Tips />
    </div>
  </div>
  
</template>

<script>
import Create from '../components/Create.vue';
import Hero from '../components/Hero.vue';
import Insert from '../components/Insert.vue';
import Select from '../components/Select.vue';
import Where from '../components/Where.vue';
import Count from '../components/Count.vue';
import Groupby from '../components/Groupby.vue'
import Joins from '../components/Joins.vue'
import Tips from '../components/Tips.vue'
export default {
  components: {
      Create, 
      Hero, 
      Insert, 
      Select,
      Where,
      Count,
      Groupby,
      Joins,
      Tips
    },
  setup () {
    
  }
}
</script>

<style scoped>

.container {
  text-align: center;
}

.sql-container{
  text-align: center;
  background: #eee;
  padding: .7rem;
  border-radius: 7px;
  margin: 2rem auto;
  width: 100%;
}

</style>