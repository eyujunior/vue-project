<template>
  <ul>
    <resource-item
      v-for="res in storedResources"
      :key="res.id"
      :link="res.link"
      :description="res.description"
      :title="res.title"
    ></resource-item>
  </ul>
</template>

<script>
import ResourceItem from './components/Resources/ResourceItem';

export default {
  components: {
    ResourceItem
  },
  data() {
    return {
      storedResources: [
        {
          id: 'official Guide',
          title: 'Official Guide',
          description: 'the official documentation for vue.js',
          link: 'https.//vuejs.org'
        },
        {
          id: 'google',
          title: 'Google',
          description: 'learn to google',
          link: 'https.//google.com'
        }
      ]
    };
  }
};
</script>

<style>
* {
  box-sizing: border-box;
}
html {
  font-family: 'roboto', 'sans-serif';
}
body {
  margin: 0;
}
</style>
