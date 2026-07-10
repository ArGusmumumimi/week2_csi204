# Use Case Diagram - Hotel Booking System

\`\`\`mermaid
graph TB
    Customer((Customer))
    Reception((Receptionist))
    Manager((Manager))
    System((System))

    Customer --> UC1[ค้นหาห้องพัก]
    Customer --> UC2[จองห้องพัก]
    Customer --> UC3[ชำระเงิน]
    Customer --> UC4[ดูประวัติการจอง]
    Customer --> UC5[ยกเลิกการจอง]

    Reception --> UC6[เช็คอิน/เช็คเอาท์]
    Reception --> UC7[ตรวจสอบสถานะห้อง]
    Reception --> UC8[ตรวจสอบการจองล่วงหน้า]

    Manager --> UC9[จัดการข้อมูลห้องพัก]
    Manager --> UC10[ตรวจสอบข้อมูลการจองทั้งหมด]
    Manager --> UC11[ตรวจสอบการยกเลิกเกินกำหนด]

    System --> UC12[ส่งอีเมลยืนยัน]
    System --> UC13[แจ้งเตือนการยกเลิก]
\`\`\`
