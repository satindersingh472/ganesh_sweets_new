<template>
  <!-- this page is for snacks -->
  <div class="grid align-center">
    <v-container fluid class="grid align-center">
      <h3 class="primary--text text-center text-h3">SWEETS</h3>

      <v-row class="mt-3">
        <v-col cols="6" v-for="(item, index) in items" :key="index">
          <v-row>
            <v-col cols="6">
              <v-card rounded="pill">
                <v-img
                  width="100%"
                  :src="imagePath(`${item['image_name']}`)"
                  :alt="`image of ${item['name']}`"
                ></v-img>
              </v-card>
            </v-col>
            <v-col
              align-self="center"
              class="font-weight-bold text-h4"
              cols="6"
            >
              <p class="primary--text text-h3 font-weight-bold">
                {{ item["name"] }}
              </p>
              <!-- <p class="text-h6 font-weight-regular" >{{ item['description'] }}</p> -->
              <p>{{ item["price"] }}</p>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      imagePath: (image_name) =>
        require(`@/assets/images/sweets/${image_name}`),
      items: [
        {
          name: "Special Barfi",
          image_name: "special_burfi.png",
          price: "$10.99 per lbs",
        },
        {
          name: "Kaju Barfi",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/scss/global.scss";
// @import "@/assets/variables.scss";
</style>
