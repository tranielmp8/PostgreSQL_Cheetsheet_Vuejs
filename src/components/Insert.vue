<template>
  <div >
    <div class="actions" >
      <h3 @click="showDetails = !showDetails"> {{ post1.title }} </h3>
    </div>
    <div v-if="showDetails" class="details">
      <img src="../assets/images/insert1.png" alt="">
      <code> {{ post1.code }} </code>
      <br>
      <h4>Select Specific columns in a Table</h4>
      <img src="../assets/images/insert2.png" alt="">
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
        "id": 2,
        "title": "Insert data into table",
        "code": "INSERT INTO naruto(name, village, power, age, rank)values ('naruto','leaf','shadow clone',12,'genin')"
      })
    const post2 = ref({
      "id": 3,
      "title": "Insert multiple lines of values",
      "code": "INSERT INTO naruto(name, village, power, age, rank)\nvalues\n('jiraiya', 'leaf', 'rasengan', 50, 'sage'),\n('sakura', 'leaf', 'creation rebirth', 12, 'genin'),\n('gaara', 'sand', 'sand binding coffin', 12, 'jinchuriki'),\n('kankuro', 'sand', 'salamander', 12, 'genin'),\n('temari', 'sand', 'dust wind technique', 12, 'genin'),\n('zabuza', 'mist', 'water prison technique', 26, 'anbu'),\n('kisame', 'mist', 'five feeding sharks', 29, 'jounin'),\n('killer bee', 'cloud', 'tailed beast ball', 36, 'jinchuriki'),\n('darui', 'cloud', 'black panther', 26, 'jounin')"
      },)

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