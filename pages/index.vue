<template>
  <div>
    <v-row>
      <v-col v-for="(link, index) in links" :key="index">
        <v-btn link :to="`/${link}`">
            {{ link }}
        </v-btn>
    </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      links: [
        "screenOne",
        "screenTwo",
        "screenThree",
        "screenFour",
        "complimentary",
        "rough-work"
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
