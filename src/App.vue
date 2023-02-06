<template>

  <button  @click="one">{{ visible_1 ? 'HIDE' : 'SHOW' }}</button>
  <p v-if="visible_1" style="color: rgb(238, 87, 87);">Red</p>
  <br>

  <button  @click="two">{{ visible_2 ? 'HIDE' : 'SHOW' }}</button>
  <p v-if="visible_2" style="color: rgb(83, 199, 91);">Green</p>
  <br>

  <button  @click="three" >{{ visible_3 ? 'HIDE' : 'SHOW' }}</button>
  <p v-if="visible_3" style="color: rgb(83, 141, 199);">Blue</p>

  <div id='cmd_head' v-if="false">
  <p>Console</p>
  </div>

  <div id='cmd' v-if="false">
    <p >> Hello :)</p>
  </div>

</template>

<script>

export default {
	data() {
    return {
      visible_1: true,
      visible_2: true,
      visible_3: true,
	  }
  },

  methods: {
    one: function() {
      this.visible_1 = !this.visible_1;
    },
    two: function() {
      this.visible_2 = !this.visible_2;
    },
    three: function() {
      this.visible_3 = !this.visible_3;
    }
  }
}

</script>
