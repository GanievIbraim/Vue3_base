<template>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <p>> Hello!</p>
    <p>> Нажмите на кнопку!</p>
  </div>

  <a :href="link"><button  @click="show_1()">1</button></a>
  <a :href="link" :target="tar"><button  @click="show_2()">2</button></a>

</template>

<script>

export default {
	data() {
    return {
      link: "https://learn.javascript.ru/introduction-browser-events",
      count: 0,
      tar: "_blank",
	  }
  },

  methods: {
    show_1: function() {
        this.link = "#no_scroll";
	  },
    show_2: function() {
      if (this.count > 0) {
        this.link = "#no_scroll";
        this.tar = "_self";
      }
      this.count += 1;
	  }
  }
}

</script>
