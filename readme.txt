!-------------------------------------------------------------------------------------------------------------
!-- tab menu ---------- tab menu ที่อยู่ด้านบน----------------------------------------------!
<header class="style_tab_menu">
  <div class="logo">
    <img src="mainpage/Lianli_logo.png" alt="Logo">
  </div>

  .style_tab_menu {
  width: 100%;
  height: 60px;
  background-color: white;

  box-shadow: 0px 8px 10px 1px rgba(0, 0, 0, 0.15);

  display: flex;
  align-items: center;
  justify-content: space-between;

  padding: 0 40px;

  position: sticky;
  top: 0;
  z-index: 1000;
}
!-------------------------------------------------------------------------------------------------------------
!-------------------------------------------------------------------------------------------------------------

!-- lianli logo ---------- logo ที่อยู่ใน tab menu----------------------------------------------!

.logo {
  display: flex;
  align-items: center;
}

.logo img {
  height: 35px;
  width: auto;
  display: block;
}
!-------------------------------------------------------------------------------------------------------------
!-------------------------------------------------------------------------------------------------------------


!-- ข้อความที่อยู่ใน logo --------------------------------------------------------!

.menu-list {
  display: flex;
  align-items: center;
  gap: 30px;

  list-style: none;
  margin: 0;
  padding: 0;
}

.menu-list li {
  display: flex;
  align-items: center;
}

.menu-list a {
  color: #111;
  text-decoration: none;
  font-size: 16px;
  font-weight: 500;

  transition: color 0.3s ease;
}
!-------------------------------------------------------------------------------------------------------------
!-------------------------------------------------------------------------------------------------------------

!-- ภาพปกต้อนรับ --------------------------------------------------------!
.hero {
  position: relative;
  height: 100vh;
  overflow: hidden;
}

/* รูป */
.hero-img {
  width: 100%;
  height: 100%;
  object-fit: cover; /* สำคัญมาก */
}

!-- ทำให้ภาพปกมืดลง --------------------------------------------------------!
.hero::after {
  content: "";
  position: absolute;
  inset: 0;
  background: rgba(0,0,0,0.4);


!-- ข้อความในภาพหน้าปก --------------------------------------------------------!
  /* text */
.hero-content {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: white;
  text-align: center;
  z-index: 1;
  font-size: 32px;
}

/* section ถัดไป */
.content {
  background: white;
  padding: 100px 40px;
}
}
!-------------------------------------------------------------------------------------------------------------
!-------------------------------------------------------------------------------------------------------------

!-- สร้างตารางสำหรับเลือกประเภทของสินค้า --------------------------------------------------------!
.product-grid {
  width: 90%;
  max-width: 800px;
  margin: 30px auto;

  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: 160px;
  gap: 14px;
}

!-- กำหนดเส้นกล่อง --------------------------------------------------------!
.box {
  border: 6px solid #d9552f;
  border-radius: 4px;
  background: white;
  box-shadow: 4px 4px 8px rgba(0,0,0,0.25);

  padding: 22px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  overflow: hidden;
}
!-- ข้อความในกล่อง --------------------------------------------------------!
.box h2 {
  margin: 0;
  color: #d9552f;
  font-family: 'Afacad', sans-serif;
  font-size: 36px;
  line-height: 0.95;
  font-weight: 400;
}

!-- ภาพในกล่อง --------------------------------------------------------!
.box img {
  max-width: 100%;
  max-height: 100%;
  object-fit: contain;
}
!-- ภาพในกล่อง(ที่มีขนาดใหญ่เกินไป) --------------------------------------------------------!
.box .imgbiger {
  max-width: 50%;
  max-height: 100%;
  object-fit: contain;
}

!-- ขนาดของแต่ละกล่อง --------------------------------------------------------!
.big-wide {
  grid-column: span 2;
  grid-row: span 1;
}

.tall {
  grid-column: span 1;
  grid-row: span 2;
  flex-direction: column;
  align-items: flex-start;
}

.small {
  grid-column: span 1;
  grid-row: span 2;
  flex-direction: column;
  align-items: flex-start;
}

.wide {
  grid-column: span 2;
  grid-row: span 1;
}

.long {
  grid-column: span 2;
  grid-row: span 1;
}

.medium {
  grid-column: span 2;
  grid-row: span 1;
  flex-direction: column;
}

!-- ทำให้สีกล่องค่อยๆเปลี่ยนเมื่อเอาเมาส์ไปแตะ --------------------------------------------------------!
.box {
  transition: all 0.25s ease;
}

.box:hover {
  background-color: #d9552f; /* สีส้ม */
}

.box:hover h2 {
  color: white; /* ตัวอักษรขาว */
}

!-- เอาเส้นใต้ลิ้นออก --------------------------------------------------------!
.box,
.box:hover,
.box:focus,
.box:active {
  text-decoration: none;
}
!-------------------------------------------------------------------------------------------------------------
!-------------------------------------------------------------------------------------------------------------


!-- ทำ animetion ค่อยๆเลื่อนขึ้น --------------------------------------------------------!
.reveal {
  opacity: 0;
  transform: translateY(40px);
  transition: opacity 0.6s ease, transform 0.6s ease;
}

.reveal.show {
  opacity: 1;
  transform: translateY(0);
}
!-------------------------------------------------------------------------------------------------------------
!-------------------------------------------------------------------------------------------------------------

!-- หัวข้อหลัก --------------------------------------------------------!
.section-title {
  display: flex;
  align-items: center;
  gap: 0px;
  margin: 0px 0 0px;
}

!-- หัวข้อย่อย --------------------------------------------------------!
.section-title-minor {
  gap: 16px;
  margin: 30px ;
  margin-left: 160px;
  font-size: 24px;
  color: #d9552f;
  margin-top: 60px;
  }

!-- เส้นคั่นข้างหน้า --------------------------------------------------------!
  .bar {
  margin: 40px; 
  margin-left: 130px; 
  width: 8px;
  height: 80px;
  background: #d9552f;
}
!-------------------------------------------------------------------------------------------------------------
!-------------------------------------------------------------------------------------------------------------


!-- วางรูปภาพทั่วไป --------------------------------------------------------!
.image-container{
    display: flex;
    justify-content: center;
    width: 100%;
    padding: 20px;
    box-sizing: border-box;
    margin: 60px auto 0 auto;
}

/* รูปภาพ */
.image-container img{
    width: 100%;
    max-width: 700px;   /* ขนาดสูงสุดบนจอใหญ่ */
    height: auto;       /* รักษาสัดส่วนรูป */
    display: block;
}
.image-container-big{
    display: flex;
    justify-content: center;   /* จัดกึ่งกลางแนวนอน */
    align-items: center;       /* จัดกึ่งกลางแนวตั้ง (ถ้าต้องการ) */
    width: 100%;
    padding: 20px;
    box-sizing: border-box;
    margin-top: 10px;
}

/* รูปภาพ */
.image-container-big img{
    width: 100%;
    max-width: 500px;   /* ขนาดสูงสุดบนจอใหญ่ */
    height: auto;       /* รักษาสัดส่วนรูป */
    display: block;
}
!-------------------------------------------------------------------------------------------------------------
!-------------------------------------------------------------------------------------------------------------

!-- ข้อความกึ่งกลางขนาดใหญ่ --------------------------------------------------------!
.text-center{
    display: flex;
    justify-content: center;
    align-items: center;

    text-align: center;

    font-size: 64px;   /* ขนาดฟอนต์ */
    color: #d9552f;      /* สีตัวอักษร */
    margin-top: 60px;
    margin-bottom: 60px;
    font-weight: bold; /* ความหนา */
}
!-------------------------------------------------------------------------------------------------------------
!-------------------------------------------------------------------------------------------------------------

!-- สร้างกล่องสำหรับใส่ภาพและข้อความลงไปได้ --------------------------------------------------------!
.diagram-box{
  position: relative;
  width: 100%;
  max-width: 900px;
  margin: auto;
}

.diagram-box img{
    width: 70%;
    display: block;
    margin: auto;
}

.diagram-svg{
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
}
!-------------------------------------------------------------------------------------------------------------
!-------------------------------------------------------------------------------------------------------------

!-- ข้อความเล็กๆตรงกลาง --------------------------------------------------------!
.Construction-text {
  text-align: center;   /*  จัดข้อความให้อยู่กลาง */
  margin-top: 80px;     /* เว้นจากด้านบน */
  margin-bottom: -60px;
  font-size: 24px;
  font-family: 'Afacad', sans-serif;
  font-weight: bold;
  color :#D65A31;
}
!-------------------------------------------------------------------------------------------------------------
!-------------------------------------------------------------------------------------------------------------

!-- ตกแต่งตาราง --------------------------------------------------------!
.Table-head-text {
  text-align: center;   /*  จัดข้อความให้อยู่กลาง */
  margin-top: 80px;     /* เว้นจากด้านบน */
  margin-bottom: -80px;
  font-size: 24px;
  font-family: 'Afacad', sans-serif;
  font-weight: bold;
  color :#D65A31;
}

table {
  border-collapse: collapse;
  width: 40%;
  font-family: Arial, sans-serif;
  margin: 0 auto;   /* ทำให้ตารางอยู่กึ่งกลาง */
  margin-top: 90px;     /* เว้นจากด้านบน */
}

th {
  background-color: #D65A31;
  color: white;
}

th, td {
  border: 1px solid #ddd;
  padding: 10px;
  text-align: center;
}

tr:nth-child(even) {
  background-color: #f9f9f9;
}
!-------------------------------------------------------------------------------------------------------------
!-------------------------------------------------------------------------------------------------------------


!-- ใส่เป็น product หลายอันต่อกัน --------------------------------------------------------!
.product-container{
    display: flex;
    justify-content: center;
    align-items: flex-start;
    margin-top: 60px;
    gap: 40px;

    flex-wrap: wrap;
}
.product{
    text-align: center;
}

.product img{
    width: 250px;
    height: auto;
    display: block;
}

.product p{
    margin-top: 15px;
    font-size: 20px;
    color: #d9552f;
}
!-------------------------------------------------------------------------------------------------------------
!-------------------------------------------------------------------------------------------------------------

!-- ข้อความแบบมีจุดปลา --------------------------------------------------------!
.list-container {
  display: flex;
  gap: 60px; /* ระยะห่างระหว่าง 2 ฝั่ง */
      color :#D65A31;
      justify-content: center;
      margin-top: 80px;
}
.list-container ul li{
  list-style-type: disc;
  padding-left: 20px;
  font-family: 'Afacad', sans-serif;
  font-size: 20px;
}
!-------------------------------------------------------------------------------------------------------------
!-------------------------------------------------------------------------------------------------------------



!-- วงกลมสีแยกความเมหาะสม --------------------------------------------------------!
  /* ● สีเขียว */
  .ball-green {
    background: #72b34a;
    border-radius: 50%;
  }

  /* ○ สีเหลือง */
  .ball-yellow {
    background: #ffe600;
    border-radius: 50%;
  }

  /* ▲ สีแดง */
  .ball-red {
    background: red;
    border-radius: 50%;
  }

  /* ✕ สีดำ */
  .ball-black {
    background: black;
    border-radius: 50%;
  }
!-------------------------------------------------------------------------------------------------------------
!-------------------------------------------------------------------------------------------------------------