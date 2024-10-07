<template>
    <v-container>
      <v-row>
        <v-col cols="12">
          <v-card>
            <v-card-title>
              ยินดีต้อนรับสู่พื้นที่สร้างสรรค์ของผม!
            </v-card-title>
            <v-card-text>
              ขอบคุณที่สละเวลามาเยี่ยมชมเว็บไซต์พอร์ตโฟลิโอนี้ ที่นี่คุณจะได้พบกับผลงานที่ผมได้สร้างสรรค์ขึ้นด้วยความตั้งใจและความหลงใหลในงานออกแบบและพัฒนา ไม่ว่าจะเป็นโปรเจกต์ทางด้านเว็บไซต์ งานออกแบบกราฟิก หรือโปรเจกต์ส่วนตัวอื่นๆ ทุกชิ้นงานล้วนสะท้อนถึงความพยายามและความมุ่งมั่นในการสร้างสิ่งที่มีคุณค่าและเป็นประโยชน์
              หากคุณสนใจในผลงานหรือมีข้อสงสัยเพิ่มเติม อย่าลังเลที่จะติดต่อผมมาได้เสมอ ไม่ว่าจะเป็นการพูดคุยแลกเปลี่ยนไอเดีย ความร่วมมือในโปรเจกต์ใหม่ หรือแค่ต้องการทำความรู้จัก ผมยินดีเป็นอย่างยิ่งที่ได้รู้จักคุณ
              ขอให้คุณสนุกกับการสำรวจเว็บไซต์นี้ และหวังว่าจะได้มีโอกาสร่วมงานกับคุณในอนาคตครับ!
            </v-card-text>
            <v-card-text>
              Welcome to my creative space! <br>
              Thank you for taking the time to visit this portfolio website. Here, you'll find the works I've passionately crafted, whether it's website projects, graphic design, or other personal endeavors. Every piece reflects my dedication and commitment to creating valuable and meaningful work.
              If you're interested in my work or have any questions, don't hesitate to reach out. Whether it's to exchange ideas, collaborate on a new project, or simply get to know each other, I'm always open to connecting.
              Enjoy exploring this site, and I look forward to the possibility of working with you in the future!
            </v-card-text>
            

            <v-card-actions>
              <v-btn color="primary" @click="about">
                About Us
              </v-btn>
              <v-btn color="secondary" @click="data">
                Members
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script>
  export default {
    methods: {
      about() {
        this.$router.push('/about');
      },

      data() {
        this.$router.push('/data_table');
      },

      logOut() {
        window.sessionStorage.clear();
        this.$router.replace("/login");
      },
    },
  };
  </script>
  
  <style scoped>
  .v-container {
  margin-top: 40px;
  padding: 20px;
  background-color: #f0f4f8; /* พื้นหลังสีฟ้าอ่อน */
  border-radius: 10px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1); /* เพิ่มเงาเบาๆ ให้คอนเทนเนอร์ */
}

/* ปรับแต่งการ์ด */
.v-card {
  border-radius: 12px;
  background-color: #fff;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15); /* เพิ่มเงาให้การ์ด */
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.v-card:hover {
  transform: translateY(-10px); /* ยกการ์ดขึ้นเมื่อ hover */
  box-shadow: 0 12px 30px rgba(0, 0, 0, 0.2); /* เพิ่มเงาเมื่อ hover */
}

/* สไตล์สำหรับ card title */
.v-card-title {
  font-size: 1.8rem;
  font-weight: bold;
  color: #2c3e50;
  text-align: center;
  padding-bottom: 10px;
  position: relative;
  overflow: hidden;
}

.v-card-title::after {
  content: "";
  position: absolute;
  left: 50%;
  bottom: 0;
  width: 100%;
  height: 3px;
  background-color: #3498db;
  transform: translateX(-50%);
  transition: width 0.4s ease;
}

.v-card-title:hover::after {
  width: 50%; /* ลดขนาดเส้นหลังเมื่อ hover */
}

/* ข้อความใน card */
.v-card-text {
  font-size: 1.1rem;
  line-height: 1.7;
  color: #34495e;
  text-align: justify;
  padding: 20px;
  background-color: #ecf0f1;
  border-radius: 10px;
  transition: background-color 0.3s ease;
}

.v-card-text:hover {
  background-color: #e1ecf1; /* เปลี่ยนสีเมื่อ hover */
}

/* ปุ่มใน card-actions */
.v-btn {
  text-transform: none;
  font-size: 1.1rem;
  padding: 10px 20px;
  border-radius: 25px;
  transition: background-color 0.3s ease, transform 0.3s ease;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1); /* เพิ่มเงาให้ปุ่ม */
}

.v-btn:hover {
  transform: translateY(-3px); /* ยกปุ่มขึ้นเล็กน้อย */
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15); /* เพิ่มเงาเมื่อ hover */
}

/* ปุ่มสี primary */
.v-btn[color="primary"] {
  background-color: #3498db;
  color: #fff;
}

.v-btn[color="primary"]:hover {
  background-color: #2980b9; /* ปรับสีเมื่อ hover */
}

/* ปุ่มสี secondary */
.v-btn[color="secondary"] {
  background-color: #e74c3c;
  color: #fff;
}

.v-btn[color="secondary"]:hover {
  background-color: #c0392b; /* ปรับสีเมื่อ hover */
}

  </style>
  