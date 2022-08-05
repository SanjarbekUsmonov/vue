<template>
 <div class="backdrop">
    <div class="modal" :class="{dark: theme ===  'dark'}">
        <h1>{{header}}</h1>
        <p>{{text}}</p>
    </div>
 </div>
</template>
<script>
export default {
 props:['header','text','theme'],

}
</script>
<style scoped>
.modal{
 width: 400px;
 padding: 20px;
 margin: 100px auto;
 background: rgb(214, 212, 212);
 border-radius: 10px;
}
.backdrop{
 top: 0px;
 position: fixed;
 /* background: rgb(192, 190, 190); */
 width: 100%;
 height: 100%;
}
.modal h1{
 color: green;
 border: none;
 padding: 0;
}
.modal p{
 font-style: normal;
}
.modal dark{
 background-color: red;
 color: white;
}
</style>