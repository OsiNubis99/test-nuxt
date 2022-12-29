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
        {
          hid: "og:title",
          name: "og:title",
          content: "test",
        },
        {
          hid: "og:description",
          property: "og:description",
          content: "test de " + this.name,
        },
        {
          hid: "og:type",
          property: "og:type",
          content: "website",
        },
        {
          hid: "og:url",
          property: "og:url",
          content: "http://ec2-44-212-0-107.compute-1.amazonaws.com:3001/",
        },
        {
          hid: "og:title",
          property: "og:title",
          content: "test",
        },
        {
          hid: "og:description",
          property: "og:description",
          content: "Test de Foto",
        },
        {
          hid: "og:image",
          property: "og:image",
          content:
            "https://chgsdev.shareity.com/campaign/" + this.name + ".png",
        },
        {
          hid: "twitter:image",
          property: "twitter:image",
          content:
            "https://chgsdev.shareity.com/campaign/" + this.name + ".png",
        },
      ],
      // 			`<!-- Primary Meta Tags -->
      // <meta name="description" content="With Meta Tags you can edit and experiment with your content then preview how your webpage will look on Google, Facebook, Twitter and more!">

      // <!-- Open Graph / Facebook -->
      // <meta property="og:type" content="website">
      // <meta property="og:url" content="https://metatags.io/">
      // <meta property="og:title" content="Meta Tags — Preview, Edit and Generate">
      // <meta property="og:description" content="With Meta Tags you can edit and experiment with your content then preview how your webpage will look on Google, Facebook, Twitter and more!">
      // <meta property="og:image" content="https://metatags.io/assets/meta-tags-16a33a6a8531e519cc0936fbba0ad904e52d35f34a46c97a2c9f6f7dd7d336f2.png">

      // <!-- Twitter -->
      // <meta property="twitter:card" content="summary_large_image">
      // <meta property="twitter:url" content="https://metatags.io/">
      // <meta property="twitter:title" content="Meta Tags — Preview, Edit and Generate">
      // <meta property="twitter:description" content="With Meta Tags you can edit and experiment with your content then preview how your webpage will look on Google, Facebook, Twitter and more!">
      // <meta property="twitter:image" content="https://metatags.io/assets/meta-tags-16a33a6a8531e519cc0936fbba0ad904e52d35f34a46c97a2c9f6f7dd7d336f2.png">
      // `
    };
  },
};
</script>
