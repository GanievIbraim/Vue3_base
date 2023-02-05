<template>
	<div>
  <a :href="href">{{text}}</a>
  </div>
</template>

<script>
export default {
	data() {
	return {
		text: 'Vue3',
		href: 'page.html',
	}
}
}

</script>
