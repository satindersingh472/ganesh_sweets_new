<template>
  <!--this page is for drinks-->
  <div class="grid align-center">
    <v-container fluid class="grid align-center">
      <h3 class="primary--text text-center text-h3">DRINKS</h3>
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
              <p class="primary--text">{{ item["name"] }}</p>
              <p class="text-h6 font-weight-regular">
                {{ item["description"] }}
              </p>
              <p>{{ item["price"] }}</p>
            </v-col>
          </v-row>
        </v-col>
      </v-row>

      <h3 class="primary--text text-center text-h3">SPECIAL PRODUCTS</h3>
      <v-row class="mt-3">
        <v-col cols="6" v-for="(special, index) in specials" :key="index">
          <v-row>
            <v-col cols="6">
              <v-card rounded="pill">
                <v-img
                  width="100%"
                  :src="imagePath(`${special['image_name']}`)"
                  :alt="`image of ${special['name']}`"
                ></v-img>
              </v-card>
            </v-col>
            <v-col
              align-self="center"
              class="font-weight-bold text-h4"
              cols="6"
            >
              <p class="primary--text">{{ special["name"] }}</p>
              <p v-for="(desc, index) in special['description']" :key="index">
                {{ desc }}
              </p>
              <p>{{ special["price"] }}</p>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
head:{
  title:"Drinks"
},

  data() {
    return {
      imagePath: (image_name) =>
        require(`@/assets/images/drinks/${image_name}`),
      items: [
        {
          name: "Kesar Milk",
          image_name: "kesar-milk.png",
          price: "$6.50",
          description:
            "Kesar Badam Milk is loaded with goodness of almonds and saffron.",
        },
        {
          name: "Elachi Milk Badam",
          image_name: "milk-badam-elachi.png",
          price: "$5.75",
          description: "Indian drink where almonds are blended with milk.",
        },
        {
          name: "Dudh Patti",
          image_name: "dudh_pati.png",
          price: "$3.49",
          description: "Made with milk, sugar and tea leaves (chai ki patti).",
        },
        {
          name: "Masala Chai",
          image_name: "masala_chai.png",
          price: "$2.49",
          description:
            "Tea in milk and water with a mixture of herbs and spices.",
        },
        {
          name: "Coffee",
          image_name: "masala_chai.png",
          price: "$2.49",
          description: "ty",
        },
      ],

      specials: [
        {
          name: "Sabji Container",
          image_name: "sabzi_container.png",
          price: "",
          description: ["1000 ml -$9.99", "500 ml -$6.99", "250 ml -$3.49"],
        },
        {
          name: "Dahi",
          image_name: "dahi.png",
          price: "",
          description: ["1000 ml -$6.99", "500 ml -$4.99", "250 ml -$2.99"],
        },
        {
          name: "Home Made Paneer",
          image_name: "home_made_panner.png",
          price: "$9.49/lb",
          description: [],
        },
        {
          name: "Pure Desi Ghee",
          image_name: "pure_desi_ghee.png",
          price: "",
          description: ["500 gm -$14.99", "2 kg -$49.99"],
        },
        {
          name: "Tamarind",
          image_name: "tamarind.png",
          price: "",
          description: ["Large $6.00 each", "Small $4.00 each"],
        },
        {
          name: "Tawa Roti",
          image_name: "tawa_roti.png",
          price: "",
          description: ["5 for $3.99"],
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/scss/global.scss";
</style>
