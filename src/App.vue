<template>
  <h1>{{ title }}</h1>
  <p>Welcome...</p>
  <div v-if="showModal">
    <CompModal  @close='toggleModal'>
        <h1>snqjsnqjknskqs</h1>
        <p>asma;lsm;ams;ams;lasm</p>
    </CompModal>
  </div>
  <button @click="toggleModal">open modal</button>
</template>

<script>
import CompModal from "./components/CompModal";
export default {
  name: "App",
  data() {
    return {
      title: "My First Vue App :)",
      header:'Sign up for the Giveway!',
      text:'Grap your ninja swag for half price!',
      showModal:false
    };
  },
  components: {
    CompModal,
  },
  methods: {
    toggleModal(){
      this.showModal = !this.showModal
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
</style>
