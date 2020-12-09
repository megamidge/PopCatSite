<template>
  <q-page class="flex flex-center" @mousedown="doPopDown" @mouseup="doPopUp">
    <q-img v-show="pop" class="popcat" src="/image/popcatpop.png" :ratio="300/338"/>
    <q-img v-show="!pop" class="popcat" src="/image/popcatnot.png" :ratio="300/338"/>
  </q-page>
</template>

<script>
const pops = [
  new Audio('/sound/pop1.mp3'),
  new Audio('/sound/pop2.mp3'),
  new Audio('/sound/pop3.mp3'),
  new Audio('/sound/pop4.mp3'),
  new Audio('/sound/pop5.mp3'),
  new Audio('/sound/pop6.mp3'),
  new Audio('/sound/pop7.mp3'),
  new Audio('/sound/pop8.mp3'),
  new Audio('/sound/pop9.mp3'),
  new Audio('/sound/pop10.mp3'),
  new Audio('/sound/pop11.mp3'),
  new Audio('/sound/pop12.mp3')
]
export default {
  name: 'PageIndex',
  data () {
    return {
      pop: false,
      timeout: null
    }
  },
  methods: {
    doPopDown () {
      this.pop = true
      const index = Math.floor(Math.random() * 12)
      pops[index].play()
    },
    doPopUp () {
      this.pop = false
    }
  }
}
</script>
<style lang="scss" scoped>
.popcat {
  max-width:100vw;
  max-height:100vh;
  height: 100vh;
  width:100vh;
}
</style>
