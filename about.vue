<template>
  <v-container fluid class="pa-5" style="background-color: #f5f5f5;">
    <v-row justify="center">
      <v-col cols="12" md="8">
        <v-card class="elevation-3" max-width="2000px">
          <v-img
            src="https://scontent.fbkk7-2.fna.fbcdn.net/v/t39.30808-6/434863782_1091067162145871_5796633221364377311_n.jpg?stp=cp6_dst-jpg&_nc_cat=109&ccb=1-7&_nc_sid=833d8c&_nc_ohc=eoSqn8JZn2cQ7kNvgGP_BMj&_nc_ht=scontent.fbkk7-2.fna&_nc_gid=A7h2dTaKA_znHAQ-162Up29&oh=00_AYAZd_-9zD8irvrd9qSlDuRzjK0swZViIOK0fTfmuNeyNw&oe=67095201"
            alt="About Us Image"
            height="300px"
            class="elevation-1"
          ></v-img>

          <v-card-title class="headline text-center py-4" style="color: #1e88e5;">
             เกี่ยวกับเรา
          </v-card-title>

          <v-divider></v-divider>

          <v-card-text class="px-5 py-3">
            <v-row>
              <v-col cols="12">
                <p>
                  สวัสดีครับ ผมชื่อ Chatphon ผมเป็นนักพัฒนาซอฟต์แวร์ที่มีความหลงใหลในเทคโนโลยีและการเขียนโปรแกรมมาตั้งแต่เริ่มเข้าสู่สายงานนี้ การเขียนโปรแกรมสำหรับผมไม่ใช่เพียงแค่การเขียนโค้ดหรือสร้างโปรแกรมให้ทำงานได้เท่านั้น แต่เป็นการแก้ปัญหาและสร้างสรรค์สิ่งใหม่ๆ ที่สามารถตอบสนองต่อความต้องการของผู้ใช้งานในโลกที่เปลี่ยนแปลงไปอย่างรวดเร็ว
                  ผมมีประสบการณ์ในการพัฒนาโปรแกรมที่หลากหลาย ทั้งในด้านการสร้างแอปพลิเคชันเว็บและมือถือ การพัฒนาระบบ Backend ที่มั่นคง และการทำงานร่วมกับทีมเพื่อส่งมอบโซลูชันที่มีประสิทธิภาพและใช้งานง่าย ผมมุ่งมั่นที่จะเรียนรู้เทคโนโลยีใหม่ๆ และติดตามเทรนด์การพัฒนาโปรแกรมอย่างต่อเนื่อง เพื่อให้แน่ใจว่างานของผมจะอยู่ในระดับที่ทันสมัยและตอบโจทย์ผู้ใช้งานได้ดีที่สุด
                </p>
                <p>
                  นอกจากการเขียนโปรแกรมแล้ว ผมยังชื่นชอบการแบ่งปันความรู้และประสบการณ์กับผู้อื่น ผ่านการทำงานร่วมกันในโปรเจกต์ต่างๆ และการช่วยเหลือทีมในการแก้ไขปัญหาที่ซับซ้อน ผมเชื่อว่าความสำเร็จในการพัฒนาซอฟต์แวร์ไม่ได้มาจากความสามารถของคนคนเดียว แต่เป็นผลจากความร่วมมือและการสื่อสารที่ดีระหว่างทีม
                  ผมพร้อมที่จะนำความรู้และประสบการณ์ที่มีมาช่วยสร้างสรรค์โปรเจกต์ใหม่ๆ ที่สามารถทำให้โลกดิจิทัลนี้ดียิ่งขึ้น ขอบคุณที่ให้ความสนใจครับ"
                </p>
              </v-col>

              <v-col cols="12">
                <v-card class="elevation-2" color="#e3f2fd" outlined>
                  <v-card-title class="headline" style="color: #1976d2;">
                    Our Mission
                  </v-card-title>
                  <v-card-text>
                    พันธกิจของเราคือการสร้างแพลตฟอร์ม E-commerce ที่เข้าถึงง่ายและทรงพลัง ซึ่งช่วยให้ผู้ใช้สามารถควบคุมประสบการณ์การช้อปปิ้งของตนได้อย่างเต็มที่ด้วยเทคโนโลยีที่ใช้งานง่ายและเชื่อถือได้
                  </v-card-text>
                </v-card>
              </v-col>

              <v-col cols="12" class="text-center pt-4">
                <v-btn color="primary" @click="home" class="mr-4" large>ไปยังหน้าหลัก</v-btn>
                <v-btn color="secondary" @click="contactUs" large>ติดต่อเรา</v-btn>
              </v-col>
            </v-row>
          </v-card-text>

          <v-divider></v-divider>

          <v-card-actions class="justify-center py-4">
            <v-btn icon @click="share">
              <v-icon>mdi-share-variant</v-icon>
            </v-btn>
            <v-btn icon @click="like">
              <v-icon>mdi-thumb-up</v-icon>
            </v-btn>
            <v-btn icon @click="follow">
              <v-icon>mdi-account-plus</v-icon>
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
    home() {
      this.$router.push("/home");
    },
    contactUs() {
      alert("Contact us at: contact@example.com");
    },
    share() {
      alert("Share this page!");
    },
    like() {
      alert("You liked this page!");
    },
    follow() {
      alert("You are now following us!");
    },
  },
};
</script>

<style scoped>
/* ปรับขอบและเงาของการ์ด */
.v-card {
  border-radius: 15px;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2); /* เพิ่มเงาให้การ์ด */
  transition: transform 0.3s ease, box-shadow 0.3s ease; /* เพิ่มการเปลี่ยนแปลง */
}

.v-card:hover {
  transform: translateY(-10px); /* ยกการ์ดขึ้นเมื่อ hover */
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.3); /* เพิ่มเงาเมื่อ hover */
}

/* ปรับสไตล์ของรูปภาพ */
.v-img {
  border-radius: 15px 15px 0 0;
  filter: brightness(0.95); /* ปรับความสว่างเล็กน้อย */
  transition: filter 0.3s ease;
}

.v-img:hover {
  filter: brightness(1.1); /* เพิ่มความสว่างเมื่อ hover */
}

/* สไตล์ของหัวข้อ */
.v-card-title {
  font-weight: bold;
  font-size: 2rem;
  letter-spacing: 1px;
  color: #1e88e5;
  position: relative;
  overflow: hidden;
}

.v-card-title::after {
  content: "";
  position: absolute;
  left: 50%;
  bottom: 0;
  width: 100%;
  height: 2px;
  background-color: #1e88e5;
  transform: translateX(-50%);
  transition: width 0.4s ease;
}

.v-card-title:hover::after {
  width: 50%; /* ลดความยาวของเส้นเมื่อ hover */
}

/* ปรับสไตล์ของข้อความ */
.v-card-text p {
  font-size: 1.15rem;
  line-height: 1.8;
  color: #424242;
  margin-bottom: 1.5rem;
  text-align: justify;
}

/* ปุ่ม */
.v-btn {
  text-transform: none;
  border-radius: 25px;
  padding: 10px 20px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  transition: background-color 0.3s ease, transform 0.3s ease;
}

.v-btn:hover {
  background-color: #1565c0; /* สีฟ้าเข้มเมื่อ hover */
  transform: translateY(-3px); /* ยกปุ่มขึ้นเล็กน้อยเมื่อ hover */
}

/* ปุ่มใน card-action */
.v-card-actions .v-btn {
  background-color: #ffffff;
  color: #1976d2;
  transition: color 0.3s ease, transform 0.3s ease;
}

.v-card-actions .v-btn:hover {
  color: #0d47a1; /* เปลี่ยนเป็นสีฟ้าเข้มเมื่อ hover */
  transform: scale(1.2); /* ขยายไอคอนเล็กน้อย */
}

/* สไตล์ divider */
.v-divider {
  margin: 20px 0;
  background-color: #bdbdbd;
}

/* ภารกิจการ์ด */
.v-card.elevation-2 {
  transition: box-shadow 0.3s ease;
}

.v-card.elevation-2:hover {
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3); /* เพิ่มเงาเมื่อ hover */
}

/* การจัดวางใน container */
.v-container {
  background-color: #fafafa;
  padding: 50px;
  border-radius: 12px;
}

.v-col {
  padding-bottom: 20px;
}

.v-btn.v-icon {
  color: #1976d2 !important;
}

</style>
