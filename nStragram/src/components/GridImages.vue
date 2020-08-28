<template>
  <div id="grid-images">
    <InstraCard
      v-for="(data, idx) in info"
      :info="data"
      :img="apis[idx]"
      :key="data.username + idx"
    >
    </InstraCard>
  </div>
</template>

<script>
import axios from "axios"; // install via npm it's can call it's name
import InstraCard from "@/components/InstraCard";

export default {
  name: "GridImages",
  data: () => {
    return {
      apis: null,
      info: [
        {
          username: "Munyong",
          avatarImage:
            "https://pbs.twimg.com/profile_images/1277260776688857088/jY226Ilz_400x400.jpg",
          image:
            "https://s.isanook.com/mv/0/rp/r/w850/ya0xa0m1w0/aHR0cHM6Ly9zLmlzYW5vb2suY29tL212LzAvdWQvMjAvMTAwMzU3L3VudGl0bGVkLTEuanBn.jpg",
          numOfLikes: 92,
          numOfComment: 108
        },
        {
          username: "Park",
          avatarImage:
            "https://pbs.twimg.com/profile_images/1277260776688857088/jY226Ilz_400x400.jpg",
          image:
            "https://i0.wp.com/www.korseries.com/wp-content/uploads/2020/08/seo-ye-ji-hair-1.jpg?w=696&ssl=1",
          numOfLikes: 200,
          numOfComment: 321
        },
        {
          username: "Munyong",
          avatarImage:
            "https://pbs.twimg.com/profile_images/1277260776688857088/jY226Ilz_400x400.jpg",
          image:
            "https://s.isanook.com/mv/0/rp/r/w850/ya0xa0m1w0/aHR0cHM6Ly9zLmlzYW5vb2suY29tL212LzAvdWQvMjAvMTAwMzU3L3VudGl0bGVkLTEuanBn.jpg",
          numOfLikes: 92,
          numOfComment: 108
        },
      ]
    };
  },
  mounted: function() {
    axios
      .get("https://dog.ceo/api/breed/pomeranian/images/random/10")
      .then(response => (this.apis = response.data.message));
  },
  components: {
    InstraCard
  }
};
</script>

<style>
#grid-images {
  display: flex;
  flex-flow: row wrap;
  justify-content: space-around;
}
</style>
