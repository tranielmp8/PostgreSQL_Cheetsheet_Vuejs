<template>
  <div >
    <div class="actions" >
      <h3 @click="showDetails = !showDetails"> {{ post1.title }} </h3>
    </div>
    <div v-if="showDetails" class="details">
      <p>CRUD is part the DML or Data Manipulation Language Statements </p>
      <p>C for Create or INSERT which I have already shown above. I am showing it again below</p>
      <img src="../assets/images/insert1.png" alt="">
      <code> {{ post1.code }} </code>
      <br>
      <h4>READ goes with the SELECT statement which I have created before also. See below</h4>
      <img src="../assets/images/select_all.png" alt="">
      <br>

      <h4>U for UPDATE which is new. See some queries below</h4>
      <img src="../assets/images/update.png" alt="">
      <p>Notice how I put a WHERE Clause in the update statement? This is to make sure to grable the correct field otherwise every name would have been updated to the statement</p>
      <code> 
        UPDATE bleach
        SET name='Captain Yamamoto'
        WHERE anime_id=5
      </code>

      <h4>D for DELETE edit table by deleting a field within a column</h4>
      <img src="../assets/images/DELETE.png" alt="">
      <code> 
        DELETE FROM bleach
        WHERE name='ichigo'
      </code>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
  
  setup () {
    const showDetails = ref(false)
    const post1 = ref({
        "id": 2,
        "title": "CRUD - DATA Editing",
        "code": "INSERT INTO naruto(name, village, power, age, rank)values ('naruto','leaf','shadow clone',12,'genin')"
      })
    

    return {showDetails, post1}
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