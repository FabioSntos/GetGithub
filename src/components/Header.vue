<template>
  <header id="header">
    <h2><strong>Github</strong> Search</h2>
    <form>
      <input
        type="text"
        name="profile"
        v-model="profile"
        placeholder="Write your github profile"
      />
      <button @click="getUserProfile">enviar</button>
    </form>
  </header>
</template>

<script>
import axios from 'axios';

export default {
  name: 'Header',
  props: {
    msg: String,
  },
  data() {
    return {
      profile: document.querySelector('imput[name=profile]'),
    };
  },
  methods: {
    getUserProfile(e) {
      e.preventDefault();
      axios
        .get(`https://api.github.com/users/${this.profile}/repos`)
        .then((data) => {
          console.log(data);
        });
    },
  },
};
</script>

<style scoped>
#header {
  width: 80%;
  max-width: 1360px;
  display: flex;
  justify-content: space-between;
  margin: 40px auto;
  font-family: 'Rubik';
}
#header h2 {
  font-style: italic;
  font-weight: 300;
  font-size: 36px;
}
#header strong {
  font-style: initial;
  font-weight: 700;
}
#header input {
  width: 400px;
  height: 40px;
  border: 2px solid #000000;
  padding-left: 10px;
  outline: none;
}
#header button {
  width: 60px;
  height: 40px;
  background-color: #000000;
  border: none;
  cursor: pointer;
}
</style>
