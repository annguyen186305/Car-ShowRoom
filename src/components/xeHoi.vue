<script>
export default {
  name: 'xeHoi',
  props: {
    tenXe: String,
    mauXe: String,
    kieuDang: String,
    nhaSX: String,
    namSX: Number,
    hinhAnh: String,
    giaXe:String
  },
  methods: {
    xeDuocChon() {
      this.$emit('xeDuocChon');
    }
  }
}
</script>

<template>
  <div class="Xe">
    <button @click="xeDuocChon" type="button">
      <div class="image-container">
        <img :src="hinhAnh" alt="Hình ảnh của xe">
        <div class="info">
          <ul>
            <li>Tên xe: {{ tenXe }}</li>
            <li>Màu xe: {{ mauXe }}</li>
            <li>Kiểu dáng: {{ kieuDang }}</li>
            <li>Nhà sản xuất: {{ nhaSX }}</li>
            <li>Năm sản xuất: {{ namSX }}</li>
          </ul>
        </div>
      </div>
      <span class="gia-xe">{{giaXe}}</span>
    </button>
  </div>
</template>

<style scoped>
.Xe {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 10px;
}

button {
  border: none;
  background: none;
  cursor: pointer;
  position: relative;
}

.image-container {
  position: relative;
}

img {
  width: 200px;
  height: 150px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  transition: transform 0.2s;
}

img:hover {
  transform: scale(1.05);
}

.info {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.7);
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  opacity: 0;
  transition: opacity 0.3s;
  border-radius: 10px;
}

.image-container:hover .info {
  opacity: 1;
}

ul {
  list-style-type: none;
  padding: 0;
  margin: 0;
}

li {
  margin: 5px 0;
}
.gia-xe {
  position: relative;
  background-color: red;
  color: white;

  padding: 5px 10px;
  border-radius: 5px;
  font-weight: bold;
}
</style>
