<template>
	<ul>
      <li v-for="elem in arga">{{ elem }}</li>
    </ul>
</template>

<script>
	export default {
        props: ['arga'],
		data() {
			return {

			}
		}
	}
</script>