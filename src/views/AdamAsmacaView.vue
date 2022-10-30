<template>
  <div class="about">

{{selected}}

    <Sekil :word="selected" :letter="letter"> </Sekil>
    <HataliHarfVue :word="selected" :letter="letter"> </HataliHarfVue>
    <DogruHarf :word="selected" :letter="letter"></DogruHarf>

  </div>
</template>

<script>

import Sekil from "@/components/AdamAsmaca/Sekil.vue"
import HataliHarfVue from "@/components/AdamAsmaca/HataliHarf.vue";
import DogruHarf from "@/components/AdamAsmaca/DogruHarf.vue";

export default {
  components: {
    Sekil,
    HataliHarfVue,
    DogruHarf
  },
  data() {
    return {
      words: ["Vuslat", "Ceyda", "Ayla", "Kardelen", "Nevbahar", "Kumru"],
      selected: null,
      letter: null
    }
  },
  created() {
    this.selected = this.words[this.getRandom(1, this.words.length - 1)]
    document.addEventListener('keydown', this.onKeyDown);
  },
  methods: {
    onKeyDown(e) {

      if (e.keyCode >= 65 && e.keyCode <= 90) {
        this.letter = e.key;
      }

    },
    getRandom(min, max) {
      return Math.floor(Math.random() * (max - min + 1)) + min;
    }
  },
  unmounted() {
    document.removeEventListener('keydown', this.onKeyDown);
  },
}

</script>