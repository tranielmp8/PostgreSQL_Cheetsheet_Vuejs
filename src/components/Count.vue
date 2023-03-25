<template>
  <div >
    <div class="actions" >
      <h3 @click="showDetails = !showDetails"> {{ post1.title }} </h3>
    </div>
    <div v-if="showDetails" class="details">
      <img src="../assets/images/count1.png" alt="">
      <code> {{ post1.code }} </code>
      <br>
      <h4>Advanced COUNT FUNCTION example</h4>
      <img src="../assets/images/count2.png" alt="">
      <code> {{ post2.code }} </code>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
  
  setup () {
    const showDetails = ref(false)
    const post1 = ref({
      "id": 4,
      "title": "COUNT Function in SQL",
      "code": "SELECT COUNT(*) FROM naruto"
      })
    const post2 = ref({
        "id": 5,
        "title": "Advanced COUNT function",
        "code": "SELECT COUNT(name) FROM naruto WHERE rank='genin'"
      })

    return {showDetails, post1, post2}
  }
}
</script>

<style scoped>
h3 {
    cursor: pointer;

  }
  
  .anime {
    border-bottom: solid #333 10px;
    padding: .5rem;
  }
  .actions {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    border-radius: 7px;
    padding: .7rem;
    background: #333;
    color: #fff;
    box-shadow: 5px 7px 7px rgba(233, 4, 4, 0.438);
    margin: 1rem auto;

  }

  .details {
    display: flex;
    flex-direction: column;
    transition: .3s ease-in;

  }

  code {
    text-align: center;
    padding: .7rem;
  }

</style>