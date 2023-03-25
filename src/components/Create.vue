<template>
  <div >
    <div class="actions" >
      <h3 @click="showDetails = !showDetails"> {{ post.title }} </h3>
    </div>
    <div v-if="showDetails" class="details">
      <img src="../assets/images/create_table.png" alt="">
      <code> {{ post.code }} </code>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
  
  setup () {
    const showDetails = ref(false)
    const post = ref(
    {
      "id": 1,
      "title": "Create Database Table",
      "code": "CREATE TABLE naruto(id SERIAL PRIMARY KEY,name VARCHAR(50),village VARCHAR(50),power VARCHAR(50),age INTEGER, rank VARCHAR(50))"
      },
    )

    return {showDetails, post}
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