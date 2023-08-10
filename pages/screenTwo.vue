<template>
  <!-- this page is for snacks -->
  <div class="grid align-center">
    <v-container fluid class="grid align-center" >
      <h3 class="primary--text text-center text-h3">SNACKS</h3>

      <v-row class="mt-3">
        <v-col cols="6" v-for="(item, index) in items" :key="index">
          <v-row>
            <v-col cols="6">
              <v-card rounded="pill" >
                <v-img
                width="100%"
                :src="imagePath(`${item['image_name']}`)"
                :alt="`image of ${item['name']}`"
              ></v-img>
              </v-card>
            </v-col>
            <v-col align-self="center" class=" font-weight-bold text-h4" cols="6">
                <p class="primary--text" >{{ item["name"] }}</p>
                <p class="text-h6 font-weight-regular" >{{ item['description'] }}</p>
                <p>{{ item['price'] }}</p>

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
        require(`@/assets/images/snacks/${image_name}`),
      items: [
        {
          name: "Bread Pakoda",
          image_name: "bread_pakoda.png",
          price:"$1.60 Each",
          description: "Bread slices dipped in spiced gram flour batter and fried.",
        },
        {
            name:"Kadi Chawal",
            image_name:"Kadi_chawal.png",
            price:"",
            description:""
        },
        {
            name:"Aloo Poori",
            image_name:"aloo_poori.png",
            price:"",
            description:""
        },
        {
            name:"Chaat Papdi",
            image_name:"chaat_papdi.png",
            price:"",
            description:""
        },
        {
            name:"Gobi Pakoda",
            image_name:"gobi_pakoda.png",
            price:"",
            description:""
        },
        {
            name:"Mix Pakoda",
            image_name:"mix_pakoda.png",
            price:"",
            description:""
        },
        {
            name:"Mini Samosa",
            image_name:"mini_samosa.png",
            price:"",
            description:""
        },
        {
            name:"Paneer Pakoda",
            image_name:"paneer_pakoda.png",
            price:"",
            description:""
        },
        {
            name:"Pao Bhaji",
            image_name:"pao_bhaji.png",
            price:"",
            description:""
        },
        {
            name:"Puri Chana",
            image_name:"puri_chana.png",
            price:"",
            description:""
        },
        {
            name:"Samosa Chana",
            image_name:"samosa_chana.png",
            price:"",
            description:""
        },
        {
          name:"Samosa",
          image_name:"samosa.png",
          price:"",
          description:""
        }
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/scss/global.scss";
// @import "@/assets/variables.scss";

</style>
