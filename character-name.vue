<template>
  <article>
      <h2> - {{ name }}</h2>
      <input type="text" v-model="text" placeholder="How said it?">
      <p> {{ text }} </p>
      <button v-on:click="answer">Answer</button>
  </article>
</template>

<script>
export default {
    props: {
        name: String
    },
    data: () => {
        return {
            text: ''
        }
    },
    methods: {
        answer:function() {
            alert(this.text);
        }
    }
}
</script>

<style>

</style>