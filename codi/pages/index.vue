<template>
  <v-container fluid>
    <v-row>
      <v-col color="white" class="block block1" align="center">
        Hola
      </v-col>
    </v-row>

    <v-row>
      <v-col class="block2 block" align="center">
        com et dius?
      <v-text-field v-model="nom" color="aquamarine" style="max-width:400px" 
      outlined rounded></v-text-field>
      </v-col>
    </v-row>

    <v-row>
      <v-col class="block block3" align="center" >
        quina feina tens?
      <v-text-field v-model="feina" color="white" style="width: 400px" 
      outlined rounded ></v-text-field>
      </v-col>
    </v-row>

    <v-row>
      <v-col class="block block4" align="center">
        quin e-mail tens?
      <v-text-field v-model="correu" color="aquamarine" style="width: 400px" 
      outlined rounded ></v-text-field>
      </v-col>
    </v-row>

    <v-row>
      <v-col class="block block5" align="center">
        quin telèfon tens?
      <v-text-field v-model="telefon" color="white" style="width: 400px" 
      outlined rounded ></v-text-field>
      </v-col>
    </v-row> 

    <v-row>
      <v-col class="block block5" align="center">
        quina edat tens?
      <v-text-field v-model="edat" color="aquamarine" style="width: 400px" 
      outlined rounded ></v-text-field>
      </v-col>
    </v-row>

    <v-row>
      <v-col class="block block6"  align="center">
        <p v-if="totPle" style="max-width:400px; text-align:left">
        {{ nom }} és {{ feina }}  i té {{ anys }}.
        Podeu contactar amb ell al telèfon {{ telefon }} o bé del 
        correu electronic {{ correu }}
      </p>
      <p v-else>Cal que emplenis el formulari sencer</p>
      {{ elTextFinal }}
      <v-text-field v-model="contacte" color="white" style="width: 400px" ></v-text-field>
      </v-col>
    </v-row> 

  </v-container>
</template>

<style>
.block{
  min-height:70 vh;
  padding-top:20vh;
  padding-bottom: 20vh;
  font-size: 10vh;
  color: white;
}
.block1{
  background-color: aquamarine;
}
.block2{
  background-color: rgb(130, 158, 74);
}
.block3{
  background-color: aquamarine;
}
.block4{
  background-color: rgb(130, 158, 74);
}
.block5{
  background-color: aquamarine;
}
.block6{
  background-color: rgb(130, 158, 74)e;
}
</style>



<script> 
export default {
  data(){
    return{
      nom:"",
      edat:"",
      feina:"",
      correu:"",
      telefon:"",
    }
  },
  computed:{
    elTextFinal(){
      return this.nom
            +" és "
            +this.edat
            +" i té "
            +this.feina
            +" Podeu contactar-hi a través del telèfon "
            +this.correu
            +" o del correu "
            + this.telefon
            +" . "

    },
    totPle(){
      return this.nom != "" 
      && this.edat != ""
      && this.feina != "" 
      && this.correu != "" 
      && this.telefon != "" 
      && this.contacte != "" 
    }

  }

}
</script>
