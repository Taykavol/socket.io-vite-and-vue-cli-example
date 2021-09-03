<script setup>
import {io} from 'socket.io-client'
// io is works!
const socket = io("ws://localhost:4000/", {});
socket.on("connect", () => {
  // Works great!
  alert(`connect ${socket.id}`)
});

socket.on("disconnect", () => {
  console.log("disconnect");
});

</script>

<template>
  <img alt="Vue logo" src="./assets/logo.png" />
</template>

<style>

</style>

