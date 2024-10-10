<template>
  <q-page class="constrain q-pa-md">
    <div class="row col-gutter-lg">
      <div class="col-12 col-sm-8">
        <q-card
          v-for="post in posts"
          :key="post.id"
          class="my-card q-mb-md"
          flat
          bordered
        >
          <q-item>
            <q-item-section avatar>
              <q-avatar>
                <img src="https://cdn.quasar.dev/img/boy-avatar.png" />
              </q-avatar>
            </q-item-section>

            <q-item-section>
              <q-item-label>Egidius_k</q-item-label>
              <q-item-label caption> {{ post.location }}</q-item-label>
            </q-item-section>
          </q-item>
          <q-img src="https://cdn.quasar.dev/img/parallax2.jpg" />
          <q-card-section>
            <div class="text-h6">{{ post.caption }}</div>
            <div class="text-caption text-grey">{{ post.date | nicedate }}</div>
          </q-card-section>
          <q-separator />
        </q-card>
      </div>
      <div class="col-4 large-screen-only">
        <q-item class="fixed">
          <q-item-section avatar>
            <q-avatar size="48px">
              <img src="https://cdn.quasar.dev/img/boy-avatar.png" />
            </q-avatar>
          </q-item-section>

          <q-item-section>
            <q-item-label>Egidius_k</q-item-label>
            <q-item-label caption> Kigali, Rwanda</q-item-label>
          </q-item-section>
        </q-item>
      </div>
    </div>
  </q-page>
</template>

<script>
import { date } from "quasar";
export default {
  name: "PageHome",
  data() {
    return {
      posts: [
        {
          id: 1,
          caption: "Golden Gate Bridge",
          date: 1728578307019,
          location: "Kigali, Rwanda",
          imageUrl: "https://cdn.quasar.dev/img/boy-avatar.png",
        },
        {
          id: 2,
          caption: "Golden Gate Bridge",
          date: 1728578307019,
          location: "Kigali, Rwanda",
          imageUrl: "https://cdn.quasar.dev/img/boy-avatar.png",
        },
        {
          id: 3,
          caption: "Golden Gate Bridge",
          date: 1728578307019,
          location: "Kigali, Rwanda",
          imageUrl: "https://cdn.quasar.dev/img/boy-avatar.png",
        },
      ],
    };
  },
  filters: {
    nicedate(value) {
      return date.formatDate(value, "MMMM D h:mm");
    },
  },
};
</script>
<style lang="sass" scoped>
// .card-post
//   .q-img
//     min-width: 200px
</style>
