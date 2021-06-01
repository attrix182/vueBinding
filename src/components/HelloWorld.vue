<template>
  <v-container class="form">
    <v-row class="text-center">
      <v-col>
        <v-text-field
          v-model="name"
          :rules="nameRules"
          :counter="10"
          label="Name"
          required
        ></v-text-field>
      </v-col>
    </v-row>

    <v-row class="text-center">
      <v-col>
        <v-text-field
          v-model="lastname"
          :rules="nameRules"
          :counter="10"
          label="Lastname"
          required
        ></v-text-field>
      </v-col>
    </v-row>

    <v-row class="text-center">
      <v-col>
        <v-text-field
          v-model="image"
          :counter="500"
          label="URL Image"
          required
        ></v-text-field>
      </v-col>
    </v-row>
    <br />
    
    <v-card class="mx-auto" max-width="400" v-if="image && name && lastname" >
      <v-img
        class="white--text align-end"
        height="200px"
        v-bind:src="image"
      >
   
        <v-card-title></v-card-title>
      </v-img>

      <v-card-subtitle> <h1>Bienvenido</h1></v-card-subtitle>

      <v-card-text class="text--primary">
        <div> <h2>{{ name }} {{ lastname }}</h2></div>

    
      </v-card-text>

      <v-card-actions>

      </v-card-actions>
    </v-card>

  </v-container>

</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    name: String,
    lastname: String,
    image:String,
  },

  data: () => ({
    valid: false,
    firstname: "",
    lastname: "",
    nameRules: [
      (v) => !!v || "Name is required",
      (v) => v.length <= 10 || "Max 10 characters",
    ],
  }),
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.form {
  max-width: 300px;
}
</style>
