<template>
  <div>
	  <h1>Head Tags</h1>
	  <input type="text" v-model="website">
	  <button type="button" @click="getHeadTags">Get head tags</button>
  </div>
</template>

<script setup>
const website = ref('https://wp-bullet.com');

function getHeadTags() {
	const response = $fetch(website.value);
	console.log(response)
}
</script>
