<template>
  <div>
    <h1>{{ this.name }}</h1>
    <p>Path: {{ $route.path }}</p>
    <img
      :src="'https://chgsdev.shareity.com/campaign/' + this.name + '.png'"
      alt="image"
    />
  </div>
</template>
<script>
export default {
  async asyncData({ params }) {
    const name = params.name;
    return { name };
  },
  head() {
    return {
      title: "test de " + this.name,
      meta: [
        { hid: "og-title", property: "og:title", content: "My Title" },
        {
          hid: "og-url",
          property: "og:url",
          content:
            "http://ec2-44-212-0-107.compute-1.amazonaws.com:3001/" + this.name,
        },
        { hid: "og-type", property: "og:type", content: "website" },
        {
          hid: "og-desc",
          property: "og:description",
          content: "test de " + this.name,
        },
        {
          hid: "og-image",
          property: "og:image",
          content:
            "https://chgsdev.shareity.com/campaign/" + this.name + ".png",
        },
        {
          hid: "twitter:type",
          property: "og:type",
          content: "website",
        },
        {
          hid: "twitter:url",
          property: "og:url",
          content: "http://ec2-44-212-0-107.compute-1.amazonaws.com:3001/",
        },
        {
          hid: "twitter:title",
          property: "og:title",
          content: "test",
        },
        {
          hid: "og:description",
          property: "twitter:description",
          content: "Test de Foto",
        },
        {
          hid: "twitter:image",
          property: "twitter:image",
          content:
            "https://chgsdev.shareity.com/campaign/" + this.name + ".png",
        },
      ],
    };
  },
};
</script>
