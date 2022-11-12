<template>
  <div class="container">
    <mavon-editor v-model="value" @change="contentChange"/>

    <hr>
    <div>
      <Markdown :content="value"/>
    </div>
  </div>
</template>

<script>
import Markdown from "@/components/Markdown";

export default {
  components: {
    Markdown
  },
  name: "Foo",
  data() {
    return {
      value: "" ,
      renderValue: ''
    };
  },
  methods: {
    contentChange(value, render) {
      this.value = value
      this.renderValue = render
    }
  }
};
</script>

<style lang="scss" scoped>

</style>
