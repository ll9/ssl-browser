<template>
  <Page>
    <ActionBar title="Welcome to NativeScript-Vue!"/>
    <StackLayout>
      <WebView :src="src" ref="ww3" style="height: 250;" />
      <TextField placeholder="enter url" v-model="urlRequest"/>
      <Button @tap="loadUrl"/>
    </StackLayout>
  </Page>
</template>

<script >
export default {
  data() {
    return {
      msg: "Hello World!",
      urlRequest: "",
      src: "https://www.google.com/"
    };
  },
  methods: {
    loadUrl() {
      this.src = this.urlRequest;
    }
  }
};
</script>

<style scoped>
ActionBar {
  background-color: #53ba82;
  color: #ffffff;
}

.message {
  vertical-align: center;
  text-align: center;
  font-size: 20;
  color: #333333;
}
</style>
