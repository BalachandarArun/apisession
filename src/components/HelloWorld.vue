<template>
  <div>{{ name }}</div>
    <div>{{ propname }}</div>
  <div>{{ msg }}</div>
  <div>{{ title }}</div>
  <p>Message is: {{ message }}</p>
  <input v-model="message" placeholder="edit me" />
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
    title: String
  },

  beforeMount(){
    console.log("Before Mounted");
  },

  mounted(){
    console.log("Component mounted");
  },

  data(){
    return{
      name: "Hello People Whatsappuu..",
      message: ''
    }
  },

  computed : {
    propname(){
      return this.name.toUpperCase();
    }
  }
}
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
</style>
