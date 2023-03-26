<template>
  <div >
    <div class="actions" >
      <h3 @click="showDetails = !showDetails"> {{ post1.title }} </h3>
    </div>
    <div v-if="showDetails" class="details">
      <img src="../assets/images/all_joins.png" alt="">
      <p>There are multiple types of joines, but I will show you only some of them. Above is a good visualization of what the joins are</p>
      <img src="../assets/images/join.png" alt="">
      <code> 
        SELECT * FROM naruto
        JOIN bleach
	      ON naruto.id=bleach.anime_id 
      </code>
      <p> the REGULAR JOIN I created above adds all columns, but only enough rows in a TABLE with the LEAST amount of ROWS. naruto has 10 rows, but bleach has 6, so the total rows that will be shown will only be 6. THIS IS THE SAME AS AN INNER JOIN. <span>IF I WANTED TO GET ALL ROWS THEN I WOULD NEED TO CHANGE JOIN TO FULL JOIN</span> </p>
      <code>

      </code>
      <br>
      
      <img src="../assets/images/remaining_joins.png" alt="">
      <code> 
      SELECT * FROM naruto
      INNER JOIN bleach
        ON naruto.id=bleach.anime_id
      </code>

      SELECT * FROM naruto
      LEFT JOIN bleach
        ON naruto.id=bleach.anime_id
        <code>

      SELECT * FROM naruto
      LEFT OUTER JOIN bleach
        ON naruto.id=bleach.anime_id
      </code>

      SELECT * FROM naruto
      RIGHT JOIN bleach
        ON naruto.id=bleach.anime_id
      <code>

      SELECT * FROM naruto
      RIGHT OUTER JOIN bleach
        ON naruto.id=bleach.anime_id
      </code>
      <br>
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
      "title": "JOINS AND MORE JOINS",
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

  span {
    color: blue;
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