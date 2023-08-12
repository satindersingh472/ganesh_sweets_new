<template>
  <!-- this page is for snacks -->
  <div class="grid align-center">
    <v-container fluid class="grid align-center">
      <h3 class="primary--text text-center  font-weight-bold text-h1">SWEETS</h3>

      <v-row class="mt-5">
        <v-col
          cols="6"
          class="mt-3"
          v-for="(item, index) in items"
          :key="index"
        >
          <v-row>
            <v-col cols="6">
              <v-card class="rounded-pill" elevation="10" >
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
              <p
                v-for="(desc, index) in item['description']"
                :key="index"
                class="font-weight-bold text-h4"
              >
                {{ desc }}
              </p>
              <p class="text-h3 font-weight-bold">{{ item["price"] }}</p>
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
    title: "Sweets",
  },
  data() {
    return {
      imagePath: (image_name) =>
        require(`@/assets/images/sweets/${image_name}`),
      items: [
        {
          name: "Special Barfi",
          image_name: "special_burfi.png",
          price: "$10.99/lb",
          description: [],
        },
        {
          name: "Kaju Barfi",
          image_name: "kaju_barfi.png",
          price: "$13.99/lb",
          description: [],
        },
        {
          name: "Malai Barfi",
          image_name: "malai_barfi.png",
          price: "$12.99/lb",
          description: [],
        },
        {
          name: "Besan Barfi",
          image_name: "besan_barfi.png",
          price: "$8.99/lb",
          description: [],
        },
        {
          name: "Kashmiri Barfi",
          image_name: "kashmiri_barfi.png",
          price: "$12.99/lb",
          description: [],
        },
        {
          name: "Milk Cake",
          image_name: "milk_cake.png",
          price: "$12.49/lb",
          description: [],
        },
        {
          name: "Patisa",
          image_name: "patisa.png",
          price: "$10.99/lb",
          description: [],
        },
        {
          name: "Angoori Petha",
          image_name: "angoori_petha.png",
          price: "$9.99/lb",
          description: [],
        },
        {
          name: "Jalebi",
          image_name: "jalebi.png",
          price: "",
          description: ["Classic $5.99/lb", "Paneer $11.99/lb"],
        },
        {
          name: "Laddu",
          image_name: "desi_ghee_laddu.png",
          price: "",
          description: [
            "Besan $6.99/lb",
            "Boondi $5.99/lb",
            "Desi Ghee $7.49/lb",
            "Motichoor $5.99/lb",
          ],
        },
        {
          name: "Desi Ghee Pinni",
          image_name: "atta_desi_ghee_pini.png",
          price: "",
          description: [
            "Alsi $12.99/lb",
            "Atta $12.99/lb",
            "Besan Pinni $12.99/lb",
          ],
        },
        {
          name: "Gulab Jamun",
          image_name: "gulab_jamun.png",
          price: "",
          description: [
            "Hot $0.99/each",
            "Regular $7.99/lb",
            "Malai Jamun $8.99/lb",
          ],
        },
        {
          name: "Rasgulla",
          image_name: "rasgulla.png",
          price: "",
          description: [
            "Rasgulla $7.99/lb",
            "Small white $7.99/lb",
            "Pink Malai $8.99/lb",
          ],
        },
        {
          name: "Panjeeri",
          image_name: "panjiri.png",
          price: "",
          description: ["Atta $11.99/lb", "Sooji $11.99/lb", "Besan $11.99/lb"],
        },
        {
          name: "Sevian/Badana",
          image_name: "badana_seviyan.png",
          price: "$5.99/lb",
          description: [],
        },
        {
          name: "Wedding Bhaji",
          image_name: "wedding_bhaji.png",
          price: "$5.99/lb",
          description: [
            "Includes Gur para, Shakar para, Mithi seerni, Namkeen sevian, Mathi, Matri",
          ],
        },
        {
          name: "Rasmalai",
          image_name: "rasmalai.png",
          price: "$11.99/lb",
          description: [],
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
