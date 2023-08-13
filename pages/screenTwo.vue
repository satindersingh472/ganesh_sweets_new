<template>
  <!-- this page is for snacks -->
  <div class="grid align-center">
    <v-container class="grid align-center">
      <h3 class="primary--text text-center font-weight-bold text-h1">SNACKS</h3>

      <v-row class="mt-5">
        <v-col
          cols="6"
          class="mt-3"
          v-for="(item, index) in items"
          :key="index"
        >
          <v-row>
            <v-col cols="6">
              <v-card class="rounded-pill" elevation="10">
                <v-img
                  width="100%"
                  :src="imagePath(`${item['image_name']}`)"
                  :alt="`image of ${item['name']}`"
                ></v-img>
              </v-card>
            </v-col>
            <v-col align-self="center" cols="6">
              <p class="primary--text text-h2 font-weight-bold">
                {{ item["name"] }}
              </p>
              <p class="text-h5 font-weight-medium">
                {{ item["description"] }}
              </p>
              <p class="text-h4 font-weight-bold">{{ item["price"] }}</p>
              <p
                v-if="item['availablity'] !== ''"
                class="text-h5 font-weight-bold"
              >
                {{ item["availablity"] }}
              </p>
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
    title: "Snacks",
  },
  data() {
    return {
      imagePath: (image_name) =>
        require(`@/assets/images/snacks/${image_name}`),
      items: [
        {
          name: "Paneer Pakoda",
          image_name: "paneer_pakoda2.png",
          price: "$11.99/lb",
          description: "Delicious paneer fitters, both crispy and crunchy.",
          availablity: "",
        },
        {
          name: "Bread Pakoda",
          image_name: "bread_pakoda.png",
          price: "$1.60 Each",
          description:
            "Bread slices dipped in spiced gram flour batter and fried.",
          availablity: "",
        },

        {
          name: "Gobi Pakoda",
          image_name: "gobi_pakoda.png",
          price: "$10.99/lb",
          description: "Crisp and tasty fried marinated cauliflower fritters.",
          availablity: "",
        },
        {
          name: "Mix Pakoda",
          image_name: "mix_pakoda.png",
          price: "$8.99/lb",
          description:
            "Made with flour, spices & ingredients like onion, veggies.",
          availablity: "",
        },
        {
          name: "Mini Samosa",
          image_name: "mini_samosa.png",
          price: "2 for $1.25",
          description: "Fried pastry with a filling like potatoes and peas.",
          availablity: "",
        },

        {
          name: "Samosa",
          image_name: "samosa.png",
          price: "$1.25 each",
          description: "Fried pastry with a filling like potatoes and peas.",
          availablity: "",
        },
        {
          name: "Samosa Chana",
          image_name: "samosa_chana.png",
          // price: "$6.50-Reg Samosa $5.50-Min Samosa",
          price: " Reg Samosa $6.50 and Mini Samosa $5.50",
          description: "Crunchy samosa is served with spicy channe(chickpeas).",
          availablity: "",
        },
        {
          name: "Chaat Papdi",
          image_name: "chaat_papdi.png",
          price: "$5.99",
          description: "The best of Bombay chat, both sweet and sour.",
          availablity: "",
        },
        {
          name: "Kadi Chawal",
          image_name: "Kadi_chawal.png",
          price: "$6.99 Each Plate",
          description:
            "Dish of onion fritters dunked in a spiced yogurt sauce.",
          availablity: " Available every Tuesday",
        },

        {
          name: "Pao Bhaji",
          image_name: "pao_bhaji.png",
          price: "$7.99 Each Plate",
          description: "Combining soft bread with spicy veggies.",
          availablity: "Available every Friday",
        },
        {
          name: "Aloo Poori",
          image_name: "aloo_poori.png",
          price: "$7.99 Each plate",
          description: "3 Puris, Desi ghee suji halwa, aloo sabji, onion salad",
          availablity: "Available every Saturday and Sunday",
        },
        {
          name: "Puri Chana",
          image_name: "puri_chana.png",
          price: "$7.99 Each plate",
          description:
            "3 Puris, Desi ghee suji halwa, channa sabji, onion salad",
          availablity: "Available every Saturday and Sunday",
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
