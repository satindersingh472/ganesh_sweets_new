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
            name:"Paneer Pakoda",
            image_name:"paneer_pakoda2.png",
            price:"$11.99/lb",
            description:"Delicious paneer fitters, both cripsy and crunchy."
        },
        {
          name: "Bread Pakoda",
          image_name: "bread_pakoda2.png",
          price:"$1.60 Each",
          description: "Bread slices dipped in spiced gram flour batter and fried.",
        },
        
        {
            name:"Gobi Pakoda",
            image_name:"gobi_pakoda.png",
            price:"$10.99/lb",
            description:"Crisp and tasty fried marinated cauliflower fritters."
        },
        {
            name:"Mix Pakoda",
            image_name:"mix_pakoda2.png",
            price:"$8.99/lb",
            description:"Made with flour, spices & ingredients like onion, veggies."
        },
        {
            name:"Mini Samosa",
            image_name:"mini_samosa.png",
            price:"2 for $1.25",
            description:"Fried pastry with a filling like potatoes and peas."
        },
       
        {
          name:"Samosa",
          image_name:"samosa_2.png",
          price:"$1.25 each",
          description:"Fried pastry with a filling like potatoes and peas."
        },
        {
            name:"Samosa Chana",
            image_name:"samosa_chana.png",
            price:"Reg samosa $6.50/Mini Samosa $5.50" , 
            description:"Crunchy samosa is served with spicy channe(chickpeas)."
        },
        {
        name:"Chaat Papdi",
            image_name:"chaat_papdi.png",
            price:"$5.99",
            description:"The best of Bombay chaat, both sweet and sour."
        },
        {
            name:"Kadi Chawal",
            image_name:"Kadi_chawal.png",
            price:"$6.99/ Available every Tuesday",
            description:"Dish of onion fritters dunked in a spiced yogurt sauce."
        },
      
        
        {
            name:"Pao Bhaji",
            image_name:"pao_bhaji.png",
            price:"$7.99 / Available every Friday",
            description:"Combining soft bread with spicy veggies."
        },
        {
            name:"Aloo Poori",
            image_name:"aloo_poori.png",
            price:"$7.99/ Available every Saturday and Sunday",
            description:"3 Puris, Desi ghee suji halwa, aloo sabji, onion salad"
        },
        {
            name:"Puri Chana",
            image_name:"puri_chana.png",
            price:"$7.99/ Available every Saturday and Sunday",
            description:"3 Puris, Desi ghee suji halwa, channa sabji, onion salad"
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
