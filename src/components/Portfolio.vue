<script setup>
import { reactive } from "vue";
import { Icon } from "@iconify/vue";

const portfolios = reactive([
  {
    year: "2023",
    projects: [
      {
        title: "E-Office Automation",
        description:
          "เป็นระบบจัดการสำนักงานเศรษฐกิจการเกษตร ซึ่งจะประกอบด้วยระบบย่อยคือ ระบบบริหารเอกสารอิเล็กทรอนิกส์ และระบบสารบรรณอิเล็กทรอนิกส์",
        detail: [
          "วางแผน Task ร่วมกับคนในทีม",
          "ออกแบบ Database ร่วมกับคนในทีม",
          "ขึ้นโครงสร้าง UI หน้า Frontend",
          "สร้าง Component ที่จำเป็น",
          "Support, Review code และแก้ไขปัญหาต่างๆ",
        ],
        technology: ["Nuxt.js", "Node.js", "PostgreSQL"],
        link: "",
      },
      {
        title: "XFAS",
        description:
          "ระบบให้บริการข้อมูลดิจิตอลทางอากาศ ที่จะช่วยให้คุณสร้างธุรกิจได้กว้างไกล เเค่ระบุขนาดพื้นที่ วันเวลา และตำแหน่งที่ตั้งของคุณ",
        detail: [
          "วางแผน Task ให้กับคนในทีม",
          "ขึ้นโครงสร้าง UI หน้า Frontend",
          "จัดทำระบบ Backoffice และ API ต่างๆ",
          "Review code และแก้ไขปัญหาต่างๆ",
          "Deploy",
        ],
        technology: ["Nuxt.js", "Laravel", "MySQL"],
        link: "https://xfas.ksta.co/",
      },
      {
        title: "Thai Wara",
        description:
          'Thai Wara "ยืนหนึ่งในตะวันออกกลาง" พร้อมผลักดันสินค้าไทย ให้กลุ่มประเทศตะวันออกกลาง',
        detail: ["ขึ้นโครงสร้าง UI หน้า Frontend", "สร้าง Component ต่างๆ"],
        technology: ["Vue.js"],
        link: "https://thaiwara.ksta.co/",
      },
      {
        title: "SUT",
        description: "เป็นระบบของหน่วยงาน มหาวิทยาลัยเทคโนโลยีสุรนารี",
        detail: [
          "จัดทําหน้าแบบฟอร์มพิจารณา",
          "แผนงานและแบบฟอร์มพิจารณา",
          "Integrate API",
          "Support และแก้ไขปัญหาต่างๆ",
        ],
        technology: ["Vue.js", "Laravel", "MySQL"],
        link: "https://sut-web.ksta.co/",
      },
      {
        title: "Bear Wash F-Card",
        description:
          "เป็นระบบจัดการหลังบ้านของ Bear Wash เกี่ยวกับประเภทบัตรต่างๆ และการตั้งค่าโปรโมชั่น รวมถึงการ Topup, Discount, Event และการตรวจสอบยอดเงิน",
        detail: [
          "ปรับ Database ให้เหมาะสมกับระบบ",
          "เพิ่มหน้าจัดการ Topup Promotion",
          "เพิ่มหน้าจัดการ Discount Promotion",
          "เพิ่มหน้าจัดการ Event Promotion",
          "เพิ่มหน้าจัดการประเภทบัตร",
          "เพิ่มหน้าจัดการบัตร",
          "เพิ่มหน้า Log Activity",
          "Support และแก้ไขปัญหาต่างๆ",
        ],
        technology: ["Laravel", "MySQL"],
        link: "https://sut-web.ksta.co/",
      },
    ],
  },
  {
    year: "2022",
    projects: [
      {
        title: "นิทรารมณ์",
        description:
          "เป็น Application ช่วยจัดการการนอนหลับ ที่สามารถวิเคราะห์ผลการเปรียบเทียบการนอนของผู้ใช้ย้อนหลัง 7 วัน และยังมีการให้คำแนะนำเกี่ยวกับการนอนของผู้ใช้งาน",
        detail: [
          "จัดทําในส่วนของ iOS หน้า login with social (Facebook/Google)",
          "จัดทำระบบ Backoffice และ API ต่างๆ",
          "จัดทำหน้า Register view",
          "Support และแก้ไขปัญหาต่างๆ",
        ],
        technology: ["SwiftUi", "Laravel", "Vue.js", "MySQL"],
        link: "",
      },
      {
        title: "ระบบ Franchise Portal",
        description:
          "เป็นระบบของ โครงการ PTTOR(Cafe Amazon) ที่สามารถการจัดการข้อมูลร้านค้า, จัดการผู้บริหาร, จัดการข้อมูลพนักงาน, การสั่งซื้อ(E-Order), หลักสูตร, ข่าวสารและบทความต่างๆ และอื่นๆ",
        detail: [
          "จัดทําในส่วนของ Frontend ในเมนูที่ได้รับมอบหมายและแก้ไขปัญหาที่พบ",
          "Deploy ขึ้นระบบ Salesforce",
        ],
        technology: ["Vue.js", "MySQL"],
        link: "https://pttororg1--devpro1.sandbox.my.site.com/FranchisePortal2/FranchisePortalLogin",
      },
      {
        title: "AEON METAVERSE Virtual Party 2022",
        description:
          "เป็นกิจกรรมที่ทาง AEON จัดขึ้นตอนขึ้นปีใหม่ โดยจะให้ทำกิจกรรมสั้นๆขึ้นมา คือ การแข่งขันเล่นเกมบน เว็บไซต์ ในเว็บจะสามารถแต่งตัวละครของแต่ละคนได้ และจะแบบการเเข่งขั้นออกเป็นกลุ่มสีต่างๆ เกมจะเป็นเกมในรูปแบบคล้ายๆ Cookie run และในเว็บไซต์จะแสดงตาราง Ranking คะแนน รายบุคคลหรือตามกลุ่มสีได้",
        detail: [
          "จัดทําในส่วน Frontend หน้าโปรไฟล์",
          "Ranking board",
          "Integrate API ที่เกี่ยวข้องกับหน้าโปรไฟล์หรือ Ranking board",
          "Deploy",
        ],
        technology: ["Laravel", "MySQL"],
        link: "",
      },
      {
        title: "Thai Trade USA",
        description:
          "เป็นระบบแสดงข้อมูล Event หรือ ข่าวสารต่างๆ ของ The Department of International Trade Promotion",
        detail: [
          "ออกแบบ Database",
          "Frontend",
          "Backoffice",
          "Backend",
          "Deploy",
        ],
        technology: ["Vue.js", "Laravel", "MySQL"],
        link: "https://thaitradeusa.com/",
      },
      {
        title: "Powerpod Fitness Club",
        description:
          "เป็นเว็บไซต์ที่จะวิเคราะห์ผลการวัดผลทางกายภาพของลูกค้า และแสดงออกมาเป็น Report ทำให้กับทาง Powerpod Fitness Club เป็นโรงยิมสำหรับผู้สูงอายุ คนป่วย และคนอ้วน ในสังคมญี่ปุ่น",
        detail: [
          "ออกแบบ Database",
          "Frontend",
          "Backoffice",
          "Backend",
          "Deploy",
        ],
        technology: ["Vue.js", "Laravel", "MySQL"],
        link: "https://powerpodfitness.ksta.co",
      },
      {
        title: "PMUC MediPod System",
        description: "",
        detail: [
          "จัดทําในส่วน Frontend หน้าจัดการ Meeting (CRUD)",
          "จัดการหน้า Calendar",
          "Integrate API ที่เกี่ยวข้อง",
        ],
        technology: ["Laravel", "MySQL"],
        link: "https://pmuc.ksta.co",
      },
      {
        title: "OSCC Consulting",
        description:
          "ระบบให้คำปรึกษาและพัฒนาผู้ปฏิบัติงานคุ้มครองเด็กและผู้ถูกกระทำด้วยความรุนแรงใรครอบครัว",
        detail: [
          "รับผิดชอบด้าน API ด้วย Laravel",
          "จัดทําในส่วน Login, Chat, ฟอร์มสร้างเคสต่างๆของระบบ",
          "Integrate API ที่เกี่ยวข้อง",
          "แก้ไขปัญหาที่พบ",
        ],
        technology: ["Vue.js", "Laravel", "Pusher", "MySQL"],
        link: "https://pmuc.ksta.co",
      },
      {
        title: "TN Logistic System (Driver phase 2)",
        description:
          "เป็นระบบจัดการ การรับส่งตู้คอนเทรนเนอร์ ไปยังปลายทาง โดยจะมีขั้นตอนการทำงานต่างๆ ตั้งแต่ สร้าง Order เลือก Carrier, รถ, คนขับ จนไปถึงการออกใบวางบิลที่ Export ออกมาเป็น PDF file พร้อมระบบส่ง Email ไปยังผู้ให้บริการที่ได้เลือกไว้ เพื่อแจ้งเตือนตามขั้นตอนต่างๆ ของระบบ ทำให้กับหน่วยงานเอกชน",
        detail: ["ออกแบบ Database", "Frontend", "Backend", "Deploy"],
        technology: ["Vue.js", "Laravel", "MySQL"],
        link: "https://tnlogistic.ksta.co",
      },
    ],
  },
  {
    year: "2021",
    projects: [
      {
        title: "Gosure Online",
        description: "เป็นระบบซื้อประกันรถยนต์ออนไลน์",
        detail: [
          "จัดทําในส่วน Front-end หน้า Landing page",
          "หน้ารายการหรือรายละเอียดบทความ",
          "Integrate API ที่เกี่ยวข้อง",
        ],
        technology: ["Vue.js", "Laravel", "MySQL"],
        link: "",
      },
      {
        title: "ASB Marketing System",
        description: "เป็นระบบจัดการเช่าพื้นที่ในการขายของ",
        detail: [
          "จัดทําในส่วน หน้า Login",
          "หน้ารายการเมนูต่างๆ",
          "หน้าจัดการและค้นหาสมาชิก",
          "Integrate API ที่เกี่ยวข้อง",
        ],
        technology: ["Laravel", "MySQL"],
        link: "",
      },
      {
        title: "Biodiversity Big data",
        description:
          "เว็บไซต์แสดงข้อมูลทรัพยากรชีวภาพจากฐานข้อมูล ThaiBiodiversity / ข้อมูลทรัพยากรชีวภาพที่มีศักยภาพทางเศรษฐกิจ ของทางสํานักงานพัฒนาเศรษฐกิจจากฐานชีวภาพ(BEDO)",
        detail: [
          "จัดทําในส่วนหน้า Landing page",
          "หน้าแสดงรายละเอียดข้อมูลทรัพยากรชีวภาพ",
          "Integrate API ที่เกี่ยวข้อง",
        ],
        technology: ["Vue.js", "Laravel", "MySQL"],
        link: "http://www.nbbch.org/",
      },
      {
        title: "MVTV Authen Streaming",
        description: "",
        detail: ["จัดทํา CRUD ของเมนู Partner management"],
        technology: ["Laravel", "MySQL"],
        link: "https://auth.sky-cdn.com/",
      },
    ],
  },
  {
    year: "2020",
    projects: [
      {
        title: "Consmix Sales",
        description: "",
        detail: [
          "สร้างฟังก์ชั่นออกใบคํา สั่งซื้อ Order และ Export ออกมาเป็น PDF filee",
        ],
        technology: ["Laravel", "MySQL"],
        link: "",
      },
      {
        title: "TN Logistic System",
        description:
          "เป็นระบบจัดการ การรับส่งตู้คอนเทรนเนอร์ ไปยังปลายทาง โดยจะมีขั้นตอนการทำงานต่างๆ ตั้งแต่ สร้าง Order เลือก Carrier, รถ, คนขับ จนไปถึงการออกใบวางบิลที่ Export ออกมาเป็น PDF file พร้อมระบบส่ง Email ไปยังผู้ให้บริการที่ได้เลือกไว้ เพื่อแจ้งเตือนตามขั้นตอนต่างๆ ของระบบ ทำให้กับหน่วยงานเอกชน",
        detail: ["ออกแบบ Database", "Frontend", "Backend", "Deploy"],
        technology: ["Vue.js", "Laravel", "MySQL"],
        link: "",
      },
      {
        title: "TCDC Connect by CEA",
        description:
          "เป็นเว็บไซต์ที่รวบรวมรายชื่อนักออกแบบในไทยและผลงานต่างๆของพวกเขา จัดทำให้กับทาง  CONNECT by CEA ที่เป็นส่วนหนึ่งในงานบริการภาคธุรกิจและการออกแบบของสำนักงานส่งเสริมเศรษฐกิจสร้างสรรค์(สศส.)",
        detail: [
          "ออกแบบ Database",
          "Frontend",
          "Backoffice",
          "Backend",
          "Facebook API",
          "Deploy",
        ],
        technology: ["Vue.js", "Laravel", "MySQL"],
        link: "https://connect.cea.or.th/",
      },
      {
        title: "ระบบจัดการโครงการวิจัยกรมแพทย์ทหารบก(irbrta)",
        description:
          "เป็นระบบจัดทำโครงการวิจัยต่างๆ ภายในหน่วยงาน ของทาง สำนักงานพิจารณาโครงการวิจัย กรมแพทย์ทหารบก",
        detail: ["Frontend", "Backoffice", "Backend"],
        technology: ["Vue.js", "Laravel", "MySQL"],
        link: "https://irbrta-research.com/",
      },
      {
        title: "ระบบฐานข้อมูลกลางคุณลักษณะเฉพาะสิ่งสิ่อุปกรณ์สายแพทย์",
        description:
          "เป็นระบบค้นหาข้อมูลกลางคุณลักษณะเฉพาะสิ่งอุปกรณ์สายแพทย์ และ Export ใบสั่งพิมพ์ของอุปกรณ์สายแพทย์ออกมาเป็น PDF file ของทาง กรมแพทย์ทหารบก",
        detail: [
          "ออกแบบ Database",
          "Frontend",
          "Backoffice",
          "Backend",
          "Deploy",
        ],
        technology: ["Vue.js", "Laravel", "MySQL"],
        link: "https://rtamed.com/",
      },
      {
        title: "ระบบรายงานผู้บาดเจ็บหรือเสียชีวิตจากการตกน้ำ จมน้ำ",
        description:
          "เป็นระบบจัดการรายงานผู้บาดเจ็บหรือเสียชีวิตจากการตกน้ำ จมน้ำ ทำให้กับ กองป้องกันการบาดเจ็บ กรมควบคุมโรค กระทรวงสาธารณสุข",
        detail: [
          "จัดทํา และแก้ไขในส่วนของ ฟอร์มการกรอกข้อมูล หน้าแสดงรายการผู้บาดเจ็บ หรือเสียชีวิตจากการตกน้ํา",
          "ทํา API บันทึกฟอร์มข้อมูลและดึงข้อมูลรายการ",
        ],
        technology: ["Vue.js", "Laravel", "MySQL"],
        link: "http://dip.ddc.moph.go.th/satdrowning/#/login",
      },
    ],
  },
]);
</script>

<template>
  <div class="mt-3">
    <div v-for="(item, i) in portfolios" :key="i">
      <div class="mb-2">
        <h1
          class="text-2xl font-bold text-gray-800 dark:text-gray-100 flex items-center"
        >
          <Icon
            icon="mdi:calendar"
            class="mr-1 text-gray-800 dark:text-gray-100"
          />
          {{ item.year }}
        </h1>

        <div class="pt-2" v-for="(project, i) in item.projects" :key="i">
          <div class="pl-4 ml-6 border-l-4">
            <h1
              class="text-xl mb-2 font-semibold text-gray-800 dark:text-gray-100 flex items-center"
            >
              {{ project.title }}
              <a
                v-if="project.link"
                :href="project.link"
                target="_blank"
                class="hover:text-blue-500 dark:hover:text-blue-400"
              >
                <Icon
                  icon="ph:link"
                  class="ml-1 shrink cursor-pointer text-2xl dark:text-gray-100"
                />
              </a>
            </h1>

            <div class="mb-2" v-if="project.description">
              &nbsp;&nbsp;&nbsp;{{ project.description }}
            </div>

            <div class="mb-2">
              <span class="font-semibold">เทคโนโลยีที่ใช้ : </span>
              <span
                class="font-semibold"
                v-for="(tech, t) in project.technology"
                :key="t"
              >
                {{ tech
                }}<span v-if="project.technology.length != t + 1">, </span>
              </span>
            </div>

            <div class="mb-2">
              <div class="font-semibold">รายละเอียดงาน</div>
              <div v-for="(desc, i) in project.detail" :key="i">
                <p class="text-gray-800 dark:text-gray-100">- {{ desc }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style></style>
