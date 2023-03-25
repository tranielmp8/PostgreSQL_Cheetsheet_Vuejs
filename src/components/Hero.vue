<template>
  <div>
    <h1>SQL Snippets</h1>
    <p>Structured query language (SQL) is a programming language for storing and processing information in a relational database</p>
    <p>SQL is an important skill to have if you are a DataAnalyst or want to be one.</p>
    <p>I have created a simple webpage with SQL basics you should know using PostgreSQL</p>
    <div>
      <h3>Getting started with Postgres</h3>
      <h3>
        <a href="https://www.postgresql.org/download/" target="_blank">Download PostgreSQL</a>
      </h3>
      <p>make sure to choose your correct operating system before downloaded</p>
      <img src="../assets/images/postgres_download.png" alt="postgres" >
      <h3>NOTE: when downloading postgreSQL you will be prompted to create a password. WRITE IT DOWN</h3>
      <p>To get the postgresAdmin app please click link below</p>
      <h3><a href="https://www.pgadmin.org/download/" target="_blank">PGAdmin</a></h3>
      <img class="pgadmin" src="../assets/images/pgadmin.png" alt="pgadmin">
      <h3>NOTE: you will be prompted to create another password. It can be the same, but REMEMBER THE PASSWORD.  </h3>
      <p>While SQL has so much to offer, I will just provide basic information that I believe everyone should know</p>
      <p>The database I created is about anime. I am a nerd I understand, but who doesn't love anime/manga? Anyways I will create two tables: naruto and bleach. We will work first with Naruto, but once joins get involved you will see my bleach content. See my SQL Snippets Below and have fun. </p>
    </div>
  </div>
</template>

<script>
  export default {
    setup(){


      return{  }
    }
  }
</script>

<style>
.pgadmin {
  max-width: 700px;
}

</style>