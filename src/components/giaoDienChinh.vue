<script>
import xeHoi from "@/components/xeHoi.vue";

export default {
  name: 'giaoDienChinh',
  components: {
    xeHoi
  },
  data() {
    return {
      danhSachXeHoi: [
        {
          tenXe: 'KIA sonet',
          mauXe: 'Cam',
          kieuDang: 'SV',
          nhaSX: 'KIA',
          namSX: 2024,
          giaXe:'699,000,000 VNĐ',
          hinhAnh: 'https://drive.gianhangvn.com/image/gianhang-sonet-1-2113290j28834.jpg'
        },
        {
          tenXe: 'KIA seltos',
          mauXe: 'Trắng',
          kieuDang: 'SV',
          nhaSX: 'KIA',
          namSX: 2024,
          giaXe:'869,000,000 VNĐ',
          hinhAnh: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTfL2Fd47eZdyEJrVgkSvzyditkSuMP6L9ukg&s'
        },
        {
          tenXe: 'KIA Sorento',
          mauXe: 'Trắng',
          kieuDang: 'SUV',
          nhaSX: 'KIA',
          namSX: 2024,
          giaXe:'1,650,000,000 VNĐ',
          hinhAnh: 'https://www.carmudi.vn/_next/image/?url=https://static.carmudi.vn/wp-content/uploads/2023-09/XaKy3kfOJm.jpg&w=1200&q=75'
        },
        {
          tenXe: 'KIA carnival',
          mauXe: 'Đen',
          kieuDang: 'SUV',
          nhaSX: 'KIA',
          namSX: 2024,
          giaXe:'2,199,000,000 VNĐ',
          hinhAnh: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQHVEiu2T42WE0-R3P0NvSHoN6Kmr-mE-Ljtg&s'
        },
        {
          tenXe: 'KIA K5',
          mauXe: 'Đen',
          kieuDang: 'Sedan',
          nhaSX: 'KIA',
          namSX: 2024,
          giaXe:'850,000,000 VNĐ',
          hinhAnh: 'https://kiavietnam.com.vn/storage/k5-xam.png'
        },
        {
          tenXe: 'KIA morning',
          mauXe: 'Xanh',
          kieuDang: 'sedan',
          nhaSX: 'KIA',
          namSX: 2024,
          giaXe:'450,000,000 VNĐ',
          hinhAnh: 'https://i1-vnexpress.vnecdn.net/2022/05/06/kiamorningxline11656616j1jpg-1651831445.jpg?w=500&h=300&q=100&dpr=1&fit=crop&s=mKSLm0Rf7Or4aBAPu0mLUQ&t=image'
        },
        {
          tenXe: 'KIA sportage',
          mauXe: 'xanh',
          kieuDang: 'SUV',
          nhaSX: 'KIA',
          namSX: 2024,
          giaXe:'769,000,000 VNĐ',
          hinhAnh: 'https://kiavietnam.com.vn/storage/kia-viet-nam/hinh-anh/suv-1.png'
        },
        {
          tenXe: 'KIA soluto',
          mauXe: 'Đỏ',
          kieuDang: 'sedan',
          nhaSX: 'KIA',
          namSX: 2024,
          giaXe:'480,000,000 VNĐ',
          hinhAnh: 'https://kiavietnam.com.vn/storage/soluto-pngicon.png'
        },
      ]
    };
  },
  methods: {
    xeHienThi() {
      console.log('Xe đã được chọn');
    },
  }
}
</script>

<template>
  <div class="container">
    <header class="header">
      <nav class="menu">
        <ul>
          <div class="logo">
            <img src="https://imgcdn.tapchicongthuong.vn/cartime-media/22/11/16/logo_kia.jpg" alt="KIA">
          </div>
          <h1 class="ten-showroom">KIA An Nguyen</h1>
          <li><a href="#">Trang chủ</a></li>
          <li><a href="#san-pham">Sản phẩm</a></li>
          <li><a href="#gioi-thieu">Giới thiệu</a></li>
          <li><a href="#lien-he">Liên hệ</a></li>
        </ul>
      </nav>
    </header>
    <h1>Danh Mục Sản Phẩm</h1>
    <main id="san-pham" class="display-xe">
      <div class="cacXe">
        <xeHoi v-for="(xeHoi, index) in danhSachXeHoi"
               :key="index"
               :tenXe="xeHoi.tenXe"
               :mauXe="xeHoi.mauXe"
               :kieuDang="xeHoi.kieuDang"
               :nhaSX="xeHoi.nhaSX"
               :namSX="xeHoi.namSX"
               :hinhAnh="xeHoi.hinhAnh"
               :giaXe="xeHoi.giaXe"
               @xeDuocChon="xeHienThi">
        </xeHoi>
      </div>
    </main>
    <div id="gioi-thieu" class="gioi-thieu">
      <img src="https://vieclam123.vn/ckfinder/userfiles/images/images/quyen-loi-danh-rieng-cho-nhan-vien-tu-van-website.jpg" alt="KIA">
      <div class="text-introduce">
        <h1>ShowRoom KIA đồng hành cùng bạn</h1>
        <h2>TƯ VẤN TẬN TÌNH</h2>
        <p>Đội ngũ tư vấn được đào tạo chuyên nghiệp, giàu kinh nghiệm luôn sẵn lòng giúp quý khách tìm được chiếc xe ưng ý.</p>
        <h2>GIÁ ƯU ĐÃI - GIAO XE SỚM</h2>
        <p>Đại Lý KIA luôn cam kết mang lại mức giá ưu đãi nhất cho quý khách với thời gian giao xe sớm tại khu vực Miền Bắc.</p>
        <h2>BẢO HÀNH TIÊU CHUẨN TOÀN CẦU</h2>
        <p>Cung cấp phụ tùng ô tô KIA chính hãng. Quý khách hãy yên tâm và tin rằng xe KIA mua tại KIA luôn được chăm sóc kĩ lưỡng.</p>
      </div>
    </div>
    <footer id="lien-he" class="footer">
      <h2>Thông tin liên hệ</h2>
      <ul>
        <li>Địa chỉ: 102 Nguyễn Huy Tưởng, Thanh Xuân, TP. Hà Nội</li>
        <li>Điện thoại: 0826-460-777</li>
        <li>Email: annguyen186305@gmail.com</li>
        <li>Website: www.company.com</li>
      </ul>
    </footer>
  </div>
</template>

<style scoped>
.container{
  display: flex;
  flex-direction: column;
  height: 150vh;
  width: 100vw;
  background-color: #f5f5f5;
  overflow: hidden;
}
.display-xe {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
  background-color: #f5f5f5;
}

.cacXe {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
  max-width: 1200px;
  margin: auto;
  padding: 20px;
  background-color: #fff;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}
.logo img {
  height: 50px;
}
.menu {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 20px;
  background-color: lightblue;
}
.menu ul {
  justify-content: center;
  display: flex;
  list-style: none;
  padding: 0;
  margin: 0;
}

.menu ul li {
  margin: 10px 40px;
}

.menu ul li a {
  color: black;
  font-size: 25px;
  text-decoration: none;
  font-weight: bold;
  transition: color 0.3s;
}

.menu ul li a:hover {
  color: blue;
}
.ten-showroom {
  margin: 10px;
  color: red;
  font-size: 30px;
  font-weight: bold;
  text-transform: uppercase;
}
.footer {
  background-color: #333;
  color: white;
  padding: 20px;
  text-align: center;
  margin-top: auto;
}

.footer h2 {
  margin: 0 0 10px;
  font-size: 35px;
}

.footer ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.footer ul li {
  margin: 5px 0;
}
.gioi-thieu{
  display: flex;
}
.text-introduce {
  max-width: 800px;
  margin: auto;
  text-align: left;
  padding: 20px;
  background-color: #fff;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}
img.gioi-thieu{
  height: 400px;
  width: 600px;
}
</style>
