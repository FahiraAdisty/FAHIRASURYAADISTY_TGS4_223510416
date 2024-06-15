<template>
  <div>
    <h2>Detail Obat 1</h2>
    <button @click="emitData">Tampilkan Info Obat 1</button>
  </div>
</template>

<script>
export default {
  methods: {
    emitData() {
      this.$emit('data-emitted', 'Informasi lengkap tentang Obat 1');
    },
    tampilkanInfo() {
      console.log('Metode pada Obat 1 dipanggil!');
    }
  }
};
</script>
