<template>
  <div class="hello">
    <h1>{{ msg }},hello</h1>
    <input type="text" style="width: 200px" @blur="onBlur()" v-bind:focus="onFocus" value="textbox" />
    <div>
      <el-input v-model="textboxvalue"></el-input>
      <font-awesome-icon :icon="['fas', 'square']" />
      <font-awesome-icon :icon="['far', 'square']" />
      <font-awesome-icon :icon="['fab', 'accessible-icon']" />
      <font-awesome-icon :icon="['fas', 'ad']" />
    </div>
    <div>
      <font-awesome-icon icon="chess-knight" />
      <font-awesome-icon icon="chess-knight" size="xs" />
      <font-awesome-icon icon="chess-knight" size="lg" />
      <font-awesome-icon icon="chess-knight" size="2x" />
    </div>
    <div>
      <font-awesome-icon icon="home" fixed-width /> home <br>
      <font-awesome-icon icon="child" fixed-width /> help <br>
      <font-awesome-icon icon="cog" fixed-width /> settings <br>
    </div>
    <div>
      <font-awesome-icon icon="arrow-circle-down" spin />
    </div>
    <div>
      <font-awesome-icon icon="clipboard-list" size="2x" />
      welcome to hangge.com welcome to hangge.com
    </div>
    <div>
      <font-awesome-icon icon="clipboard-list" size="2x" pll="left" />
      welcome to hangge.com welcome to hangge.com
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data: function () {
    return {
      textboxvalue: "1213",
      name: "zhangsan",
    };
  },
  beforeCreate () {
    console.log("beforeCreate");
  },
  methods: {
    validate: function () {
      return true;
    },
    onFocus: function () {
      console.log("text onFocus event.");
    },
    onBlur: function () {
      console.log("textbox onblur event");
    },
  },
  watch: {},
  computed: {},
  created: function () { },
  errorCaptured: function () { },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
