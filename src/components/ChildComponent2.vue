<template>
  <div>
    <h2>Detail Obat 2</h2>
    <button @click="emitData">Tampilkan Info Obat 2</button>
  </div>
</template>

<script>
export default {
  methods: {
    emitData() {
      this.$emit('data-emitted', 'Informasi lengkap tentang Obat 2');
    },
    tampilkanInfo() {
      console.log('Metode pada Obat 2 dipanggil!');
    }
  }
};
</script>
