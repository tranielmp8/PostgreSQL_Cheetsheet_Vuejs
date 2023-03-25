<template>
  <div >
    <div class="actions" >
      <h3 @click="showDetails = !showDetails"> {{ post1.title }} </h3>
    </div>
    <div v-if="showDetails" class="details">
      <p>There is so much to learn when it comes SQL. Below I have provided some more information that I found helpful. Some of the information could be used for interview questions as well. </p>
      <h4>DDL and DML</h4>
      <p>Think of DDL as defining information or creating/deleting the information</p>
      <p>DML is more of Inserting data inside data or editing created data</p>
      <img src="../assets/images/DDLandDML.png" alt="">
            <br>
      <h4>Operators and More OPERATORS!</h4>
      <img src="../assets/images/arithmetic.png" alt="">
      <img src="../assets/images/logical.png" alt="">
      <img src="../assets/images/comparison.png" alt="">
      <p>NOTE: More operators are available, but the ones I provided above are a good starting point. </p>
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
      "title": "Tips and Information that is super helpful when learning SQL",
      "code": "Select * From naruto"
      })
    const post2 = ref({
        "id": 5,
        "title": "Selecting select columns/fields from table",
        "code": "Select name, village From naruto"
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