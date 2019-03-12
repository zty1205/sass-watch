<template>
  <div class="home">
    Name: {{ desc }}

    <div>
      <button @click="onAdd">添加</button>
      <button style="margin-left: 10px;" @click="onSet">设置</button>
    </div>

    <div v-for="val in arr" :key="val"> {{ val }}</div>
    <div>
      <button @click="onArrAdd1">添加index</button>
      <button style="margin-left: 10px;" @click="onArrAdd2">添加push</button>
      <button style="margin-left: 10px;" @click="onArrSet1">设置</button>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'home',
  data() {
    return {
      n1: "hello ",
      num: 1,
      n2: " zty",
      arr: [1,2,3]
    }
  },
  computed: {
    desc() {
      return this.n1 + this.num + this.n2
    }
  },
  methods: {
    onAdd() {
      this.num++
    },
    onSet() {
      this.n2 = " vue"
    },
    onArrAdd1() {
      this.arr[3] = 4
    },
    onArrAdd2() {
       this.arr.push(4)
    },
    onArrSet1() {
      this.arr[1] = 222
    }
  }
}
</script>

<style lang="scss" scoped>
  .home {
    margin-top: 100px;
    padding-top: 20px;
  }
</style>

