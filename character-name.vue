<template>
  <article>
      <h2> - {{ firstName }} {{ lastName }} </h2>
      <input type="text" v-model="text" placeholder="Who said it?">
      <p> {{ text }} </p>
      <button v-on:click="answer">Answer</button>
  </article>
</template>

<script>
export default {
    props: {
        firstName: String,
        lastName: String
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