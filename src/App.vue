<template>
  <h1>{{ title }}</h1>
  <p>Welcome...</p>
  <teleport to=".modals" v-if="showModal">
    <CompModal @close='toggleModal'>
      <template v-slot:links>
        <a href="#">sign up now</a>
        <a href="#">more info</a>
      </template>
      <h1>Ninja Giavay!</h1>
      <p>Grap your ninja swag for have parise!</p>
    </CompModal>
  </teleport>

  <div v-if="showModalTwo">
    <CompModal @close='toggleModalTwo'>
      <h1>Ninja Giavay!</h1>
      <p>Grap your ninja swag for have parise!</p>
    </CompModal>
  </div>
  <button @click="toggleModal">open modal</button>
  <button @click="toggleModalTwo">open modal 2</button>
</template>

<script>
import CompModal from "./components/CompModal";
export default {
  name: "App",
  data() {
    return {
      title: "My First Vue App :)",
      showModal: false,
      showModalTwo:false

    };
  },
  components: {
    CompModal,
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal
    },
    toggleModalTwo() {
      this.showModalTwo = !this.showModalTwo
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1 {
  border: 1px solid black;
  display: inline-block;
  padding-bottom: 10px;
  border: none;
}
a{
  text-decoration: none;
  color: #333;
  padding: 8px;
  border: 1px solid #eee;
  border-radius: 4px;
  margin: 10px;
  background: greenyellow;
}
</style>
