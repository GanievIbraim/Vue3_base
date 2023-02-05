<template>
	<p>{{ arr[0] }}</p>
  <p>{{ arr[1] }}</p>
  <p>{{ arr[2] }}</p>
  <p>{{ arr[3] }}</p>
  <p>> RESULT: {{ num[0] + num[1] + num[2] }}</p>
</template>

<script>
export default {
	data() {
	  return {
		  arr: ['> 25%', '> 50%', '> 100%', '> COMPLETE!'],
      num: [1, 2, 3],
	  }
  } 
}

</script>
