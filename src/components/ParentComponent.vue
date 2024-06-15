<template>
  <div>
    <h1>Daftar Obat</h1>
    <obat-detail1 ref="obat1" @data-emitted="handleDataEmitted" />
    <obat-detail2 ref="obat2" @data-emitted="handleDataEmitted" />
    <div v-if="emittedData">
      <p>Informasi Diterima: {{ emittedData }}</p>
    </div>
    <info-slot>
      <p>Informasi tambahan melalui slot.</p>
    </info-slot>
    <button @click="panggilMetodeAnak">Panggil Metode Anak</button>
  </div>
</template>

<script>
import ObatDetail1 from './ChildComponent1.vue';
import ObatDetail2 from './ChildComponent2.vue';
import InfoSlot from './SlotComponent.vue';

export default {
  components: {
    ObatDetail1,
    ObatDetail2,
    InfoSlot
  },
  data() {
    return {
      emittedData: null
    };
  },
  methods: {
    handleDataEmitted(data) {
      this.emittedData = data;
    },
    panggilMetodeAnak() {
      this.$refs.obat1.tampilkanInfo();
      this.$refs.obat2.tampilkanInfo();
    }
  }
};
</script>
