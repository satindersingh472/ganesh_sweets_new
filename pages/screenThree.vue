<template>
  <!--this page is for drinks-->
  <div class="grid align-center">
    <v-container fluid class="grid align-center">
      <h3 class="primary--text text-center text-h1 font-weight-bold">DRINKS</h3>
      <v-row class="mt-5">
        <v-col
          cols="6"
          class="mt-3"
          v-for="(item, index) in items"
          :key="index"
        >
          <v-row>
            <v-col cols="6">
              <v-card class="rounded-pill" flat>
                <v-img
                  width="100%"
                  height="500px"
                  contain
                  :src="imagePath(`${item['image_name']}`)"
                  :alt="`image of ${item['name']}`"
                ></v-img>
              </v-card>
            </v-col>
            <v-col
              align-self="center"
              cols="6"
            >
              <p class="primary--text text-h1 font-weight-bold ">{{ item["name"] }}</p>
              <p class="text-h3 font-weight-medium">
                {{ item["description"] }}
              </p>
              <p class="text-h2 font-weight-bold" >{{ item["price"] }}</p>
            </v-col>
          </v-row>
        </v-col>
      </v-row>

      <h3 class="primary--text text-center text-h1 mt-10 font-weight-bold">SPECIAL PRODUCTS</h3>
      <v-row class="mt-5">
        <v-col cols="6" class="mt-3" v-for="(special, index) in specials" :key="index">
          <v-row>
            <v-col cols="6">
              <v-card class="rounded-pill" flat>
                <v-img
                  width="100%"
                  :src="imagePath(`${special['image_name']}`)"
                  :alt="`image of ${special['name']}`"
                ></v-img>
              </v-card>
            </v-col>
            <v-col
              align-self="center"
              cols="6"
            >
              <p class="primary--text text-h1 font-weight-bold  ">{{ special["name"] }}</p>
              <p v-for="(desc, index) in special['description']" :key="index" class="text-h3 font-weight-bold" >
                {{ desc }}
              </p>
              <p class="text-h2 font-weight-bold" >{{ special["price"] }}</p>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  head: {
    title: "Drinks",
  },

  data() {
    return {
      imagePath: (image_name) =>
        require(`@/assets/images/drinks/${image_name}`),
      items: [
        {
          name: "Kesar Milk Badam",
          image_name: "kesar-milk-badam.png",
          price: "$4.50",
          description:
            "Milk loaded with goodness of almonds and saffron.",
        },
        {
          name: "Elaichi Milk Badam",
          image_name: "milk-badam-elaichi.png",
          price: "$4.00",
          description: "Almonds blended with elaichi milk.",
        },
        {
          name: "Dudh Patti",
          image_name: "ganeshCup.png",
          price: "$3.49",
          description: "Made with milk, sugar and tea leaves(chai ki patti).",
        },
        {
          name: "Masala Chai",
          image_name: "ganeshCup.png",
          price: "$2.49",
          description:
            "Tea in milk and water with a mixture of herbs and spices.",
        },
        {
          name:"Elaichi Chai",
          image_name:"elaichi_chai.png",
          price:"$2.50",
          description:"Elaichi(cardamom) chai made with milk and sugar"
        },
        {
          name: "Coffee",
          image_name: "ganeshCup.png",
          price: "$2.49",
          description: "Indian style coffee made with milk and sugar.",
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
          description: ["Large $6.50 each", "Small $4.50 each"],
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
