<template>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <p>> Hello!</p>
    <p>> Нажмите на кнопку, чтобы изменить переменную visible!</p>
    <p v-if="visible">> Вы видите этот абзац, при этом visible = true.</p>
    <p v-if="!visible">> Вы видите этот абзац, при этом visible = false.</p>
  </div>

  <button  @click="show">1</button>

</template>

<script>

export default {
	data() {
    return {
      visible: false,
	  }
  },

  methods: {
    show: function() {
      this.visible = !(this.visible) &&  true;
    }
  }
}

</script>
