<template>
  <v-container>
    
<v-divider></v-divider>

<Music/>

<v-divider></v-divider>

    
  </v-container>
</template>

<script>
import Music from "./Music";
export default {
  name: "HelloWorld",
  props: {
    msg: String, 
    Todos: Object,
  },
  data: function () {
    return {
      songs:{},
      loaded: false,
      count: 0,
      colorNb: "blue",
      prenom: "",
      search: "",
      nbDisplay: 3,
      prenoms: ["Steven", "Julien", "Guillaume", "Baptiste"],
    };
  },
  methods: {
    load() {
      this.loaded = true;
    },
    ajouterPrenom() {
      this.prenoms.push(this.prenom);
      this.prenom = "";
      if (this.prenoms.length >= 15) {
        this.colorNb = "red";
      }
    },
    add() {
      this.count++;
    },
    remove() {
      this.count--;
    },
  },
  components: {
    Music,
  },
  computed: {

  },
  watch: {
    
  },
};
</script>
