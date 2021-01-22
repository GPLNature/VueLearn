<template>
  <nav>
    <div id="append" @click="append">
        <p>커미션 추가</p>
    </div>
    <div id="remove" @click="remove">
        <p>커미션 삭제</p>
    </div>
  </nav>
  <footer>
    <div id="cr">Copyright 2021. 문준상. All rights reserved.</div>
  </footer>
  <router-view/>
</template>
<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'App',
  methods: {
    append () {
      this.$router.push('/')
      console.log(this.$router.currentRoute)
    },
    remove () {
      this.$router.push('/remove')
      console.log(this.$router.currentRoute)
    }
  }
})
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

html, body
{
  background: rgb(83, 83, 83);
}

footer
{
  position: absolute;
  width:100%;
  height: 50px;
  bottom: 0;
  left: 0;
  background:rgb(83, 83, 83);
  text-align: center;
}

footer #cr
{
  width: 100%;
  padding: 5px 0px;
  position: absolute;
  text-align: center;
  background:#333333;
  color: azure;
  bottom: 0;
  font-size: 14px;
  -webkit-user-select: none;
}

nav
{
  top: 0;
  left: 0;
  position: absolute;
  width: 100%;
  background: #292929;
  height: 46px;
}

nav div
{
  position: relative;
  width: 100px;
  color: azure;
  border-radius: 5px;
  float: left;
}

nav div p
{
  font-size: 14px;
  -webkit-user-select: none;
}

nav div:hover
{
  background:rgb(107, 107, 107);
}

section
{
  position:relative;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
}
</style>
