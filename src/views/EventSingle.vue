<template>
  <div class="event-single">
    <section class="hero is-primary">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">{{ event.name }}</h1>
          <h2 class="subtitle">
            <strong>Date:</strong>{{ event.date }}
            <br />
            <strong>Time:</strong>{{ event.time }}
          </h2>
        </div>
      </div>
    </section>
    <section class="event-content">
      <div class="container">
        <p class="is-size-4 description">{{ event.description }}</p>
        <p class="is-size-4"><strong>Location:</strong>{{ event.location }}</p>
        <p class="is-size-4"><strong>Category:</strong>{{ event.category }}</p>
        <div class="event-images columns is-multiline has-text-centered">
          <div
            v-for="image in event.images"
            :key="image.id"
            class="column is-one-third"
          >
            <img :src="`${image}`" :alt="`${event.name}`" />
          </div>
        </div>
      </div>
    </section>
  </div>
</template>
<script>
export default {
  data() {
    return {
      events: [
        {
          id: 1,
          name: "Charity Ball111",
          category: "Fundraising",
          description:
            "Spend an elegant night of dinner and dancing with us as we raise money for our new rescue farm.",
          featuredImage: "https://placekitten.com/500/500",
          images: [
            "https://placekitten.com/500/500",
            "https://placekitten.com/500/500",
            "https://placekitten.com/500/500",
          ],
          location: "1234 Fancy Ave",
          date: "12-25-2019",
          time: "11:30",
        },
        {
          id: 2,
          name: "Charity Ball222",
          category: "Fundraising",
          description:
            "Spend an elegant night of dinner and dancing with us as we raise money for our new rescue farm.",
          featuredImage: "https://placekitten.com/333/333",
          images: [
            "https://placekitten.com/333/333",
            "https://placekitten.com/333/333",
            "https://placekitten.com/333/333",
          ],
          location: "1234 Fancy Ave",
          date: "13-25-2019",
          time: "11:30",
        },
        {
          id: 3,
          name: "Charity Ball333",
          category: "Fundraising",
          description:
            "Spend an elegant night of dinner and dancing with us as we raise money for our new rescue farm.",
          featuredImage: "https://placekitten.com/222/222",
          images: [
            "https://placekitten.com/222/222",
            "https://placekitten.com/222/222",
            "https://placekitten.com/222/222",
          ],
          location: "1234 Fancy Ave",
          date: "14-25-2019",
          time: "11:30",
        },
        {
          id: 4,
          name: "Charity Ball444",
          category: "Fundraising",
          description:
            "Spend an elegant night of dinner and dancing with us as we raise money for our new rescue farm.",
          featuredImage: "https://placekitten.com/111/111",
          images: [
            "https://placekitten.com/111/111",
            "https://placekitten.com/111/111",
            "https://placekitten.com/111/111",
          ],
          location: "1234 Fancy Ave",
          date: "15-25-2019",
          time: "11:30",
        },
      ],
      event: {},
    };
  },
  created() {
    const ID = this.$route.params.id;
    let event = this.events.find((event) => event.id === ID);
    this.event = event;
  },
};
</script>
<style lang="scss" scoped>
.event-single {
  margin-top: 30px;
}
.hero {
  margin-bottom: 70px;
}
.event-images {
  margin-top: 50px;
}
.description {
  margin-bottom: 30px;
}
</style>