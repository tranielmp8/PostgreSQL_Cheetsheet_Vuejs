<template>
  <div >
    <div class="actions" >
      <h3 @click="showDetails = !showDetails"> {{ post1.title }} </h3>
    </div>
    <div v-if="showDetails" class="details">
      <img src="../assets/images/groupby1.png" alt="">
      <p>NOTE: GROUP BY needs a clause to go with it such as WHERE or HAVING <br> --WHERE Clause comes before GROUP BY and HAVING Clause comes after GROUP BY</p>
      
      <p>2nd NOTE: Please remember when using the GROUP BY the SELECTED columns must match the GROUP BY columns</p>
      <code> {{ post1.code }} </code>
      <br>
      
      <h4> {{ post2.title }} </h4>
      <img src="../assets/images/orderby1.png" alt="">
      <code> {{ post2.code }} </code>
      <br>

      <h4>GROUP BY and ORDER BY Clause</h4>
      <p>ORDER BY can use desc or asc after the column of choice</p>
      <img src="../assets/images/grouporderby.png" alt="">
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
      "id": 8,
      "title": "GROUP BY and ORDER BY Clause uses",
      "code": "SELECT rank FROM naruto WHERE age=12 GROUP BY rank"
      })
    const post2 = ref({
        "id": 9,
        "title": "ORDER BY Clause",
        "code": "Select name, village From naruto"
      })
    const post3 = ref({
        "id": 10,
        "title": "GROUP BY and ORDER BY Clause working together",
        "code": "Select name, village From naruto"
      })

    return {showDetails, post1, post2, post3}
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