<script>
export default {
  data () {
    return {
      planet: null,
      count: 0
    }
  },

  async fetch () {
    this.planet = await this.$axios.$get('https://swapi.dev/api/planets/1/')
  }
}
</script>

<template>
  <div class="planet">
    <h1>Not found</h1>
    <h2>{{ planet.name }}</h2>
    <pre>{{ planet }}</pre>
    <br>
    <p>
      Count: {{ count }} <button @click="count++">+1</button>
    </p>
  </div>
</template>