<template>
  <div class="container">
    <Hero />
    <div class="sql-container">
      <Create />
      <Insert />
      <Select />
      <Where />
      <Count />
      <Groupby />
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
export default {
  components: {
      Create, 
      Hero, 
      Insert, 
      Select,
      Where,
      Count,
      Groupby
    },
  setup () {
    
  }
}
</script>

<style scoped>

.sql-container{
  background: #eee;
  padding: .7rem;
  border-radius: 7px;
  margin: 2rem auto;
}

</style>