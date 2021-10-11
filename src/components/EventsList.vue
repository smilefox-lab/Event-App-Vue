<template>
  <div class="evets container">
    <h2 class="subtitle is-3">Check out our upcoming events</h2>
    <div class="columns is-multiline">
      <div
        v-for="event in events"
        :event="event"
        :key="event.id"
        class="column is-one-quarter"
      >
        <router-link :to="'/event/' + event.id">
          <EventCard :event="event" />
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
import EventCard from "./EventCard.vue";
export default {
  components: {
    EventCard,
  },
  data() {
    return {
      event: {},
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
    };
  },
};
</script>

<style lang="scss" scoped>
.events {
  margin-top: 100px;
  text-align: center;
}
</style>