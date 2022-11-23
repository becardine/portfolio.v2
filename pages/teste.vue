<template>
  <div>
    <template v-for="line in lines">
      <div
        v-for="(column, index) in columns"
        :key="index"
        :style="{
          width: size + 'px',
          height: size + 'px',
          background: '#ccc',
          border: '1px solid #eee',
          position: 'absolute',
          top: line * size + 'px',
          left: column * size + 'px',
        }"
      ></div>
    </template>
    <div
      v-for="block in snaker"
      :key="block.id"
      :style="{
        width: size + 'px',
        height: size + 'px',
        background: '#666',
        border: '1px solid #eee',
        position: 'absolute',
        top: line * size,
        left: column * size,
      }"
    ></div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      lines: 20,
      columns: 20,
      size: 20,
      snaker: [{ x: 1, y: 1 }],
    };
  },
};
</script>
<style lang="sass" scoped></style>
