<template>
  <div >
    <p>click {{count}} times, count is {{evenorodd}}</p>
    <button @click="increment">+</button>
    <button @click="decrement">-</button>
    <button @click="incrementIfOdd">increment if odd</button>
    <button @click="incrementAsync">increment async</button>
  </div>
</template>

<script>
export default {
  data () {
    return {
      count: 0
    }
  },
  methods: {
    increment () {
      const count = this.count
      this.count = count + 1
    },
    decrement () {
      const count = this.count
      this.count = count - 1
    },
    incrementIfOdd () {
      const count = this.count
      if (count % 2 === 1) {
        this.count = count + 1
      }
    },
    incrementAsync () {
      setTimeout(() => {
        const count = this.count
        this.count = count + 1
      }, 1000)
    }
  },
  computed: {
    evenorodd () {
      return this.count % 2 === 0 ? '偶数' : '奇数'
    }
  }
}
</script>

<style>

</style>
