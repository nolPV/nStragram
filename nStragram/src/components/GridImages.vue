<template>
  <div id="grid-images">

  </div>
</template>

<script>

import axios from 'axios';   // install via npm it's can call it's name

export default {
  name: "GridImages",
  data: () => {
    return {
      avatarImg:
        "https://pbs.twimg.com/profile_images/1277260776688857088/jY226Ilz_400x400.jpg",
      postImg:
        "https://pbs.twimg.com/profile_images/1277260776688857088/jY226Ilz_400x400.jpg",
      usernames: ["Elon", "Peter", "Lisa"],
      apis: null
    }
  },
  mounted: function() {
    axios
        .get('https://dog.ceo/api/breed/pomeranian/images/random/10')
        .then(response => this.apis = response.data.message)
  }
}
</script>

<style>
#grid-images {
  display: flex;
  flex-flow: row wrap;
  justify-content: space-around;
}
</style>
