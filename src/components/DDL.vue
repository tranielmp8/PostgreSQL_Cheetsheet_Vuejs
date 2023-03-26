<template>
  <div >
    <div class="actions" >
      <h3 @click="showDetails = !showDetails"> {{ post1.title }} </h3>
    </div>
    <div v-if="showDetails" class="details">
      <p>
        CREATE, ALTER, TRUNCATE, DROP are apart of the DDL or Data Definition Language.
        Do not practice these unless you have a good understanding of what they can do DDL Defines the database. DANGEROUS because performing one of these statements can drastically change your database even remove it completely with no way of getting it back</p>
      <p>Create DATABASE (db) or CREATE TABLE [table_name]</p>
      <img src="../assets/images/create_table.png" alt="">
      <code> {{ post1.code }} </code>
      <br>
      <h4>Alter can define a new column or change a column. Alter can do many things, but I am just showing 2 basic ALTER statement</h4>
      <img src="../assets/images/alter.png" alt="">
      <code>
        ALTER TABLE bleach
        ADD COLUMN shinigami BOOL

        -- renaming a column
        ALTER TABLE bleach
        RENAME COLUMN shinigami TO is_shinigami
      </code>
      <br>

      <h4>TRUNCATE can completely wipe your database or certain columns. IF statement is written correctly it will keep the TABLE AND VALUES</h4>
      <img src="../assets/images/truncate.png" alt="">
      <code> 
        TRUNCATE TABLE bleach
        IMMEDIATE;
      </code>
      <h4>DELETE will completely remove the TABLE and VALUES. WARNING: cannot get database back</h4>
      <img src="../assets/images/drop.png" alt="">
      <code> 
        DROP TABLE bleach
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
        "title": "DDL - CREATE, ALTER, TRUNCATE, DROP",
        "code": "CREATE TABLE naruto(id SERIAL PRIMARY KEY,name VARCHAR(50),village VARCHAR(50),power VARCHAR(50),age INTEGER, rank VARCHAR(50))"
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