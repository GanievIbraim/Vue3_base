<template>
	<div>
    <h1>Квадрат числа {{ num }} = {{ num * num }}</h1>
  </div>

  <div>
    <h1>Сумма чисел {{ num1}}, {{num2}}, {{num3}} = {{ num1 + num2 + num3 }}</h1>
  </div>
</template>

<script>
export default {
	data() {
	  return {
		  num: 11,
      num1: 27,
		  num2: 9,
		  num3: 2003,
	  }
  } 
}

</script>
