# DADS5001_MiniProject
<h1>Introduction</h1>
  Dataset : https://www.kaggle.com/datasets/muhammadehsan02/126-years-of-historical-olympic-dataset/data <br>
  <br>
  &nbsp;&nbsp;&nbsp;&nbsp;ข้อมูลที่เรากำลังสำรวจนี้ จะเป็นการศึกษาปัจจัยต่างๆ ที่มีผลต่อการแข่งขันของนักกีฬา ไม่ว่าจะเป็นส่วนสูง น้ำหนัก และอายุ โดย Dataset<br> ที่นำมาใช้งานมีข้อมูล
  ของชื่อ วันเกิด น้ำหนัก ส่วนสูง การได้รับเหรียญรางวัล อันดับผลการแข่งขัน รายการที่แข่นขัน ประเภทของกีฬาที่แข่งขัน<br> ประเทศ ตัวย่อของประเทศ ปีที่แข่งขัน และรหัสของนักกีฬา 

  <br>![image](https://github.com/user-attachments/assets/2fda9398-1bdc-41ca-bfaa-e795b81b415a)

   &nbsp;&nbsp;&nbsp;&nbsp;<I>รูปที่ 1 รูปแสดง data ที่ยังไม่ผ่านการ clean และ fill data ที่หายไป</I>

  ![image](https://github.com/user-attachments/assets/5dd24eca-3941-42fb-af22-e64461ce67fe)
  
   &nbsp;&nbsp;&nbsp;&nbsp;<I>รูปที่ 2 รูปแสดง data ที่ยังไม่ผ่านการ clean และ fill data ที่หายไป</I>



<h1>Preparation</h1>

  <h3>Download Data</h3><br>  
  
  ![image](https://github.com/user-attachments/assets/afad997d-ca00-4b4e-a1e1-560df655835a) 
  
  &nbsp;&nbsp;&nbsp;&nbsp;<I>รูปที่ 3 รูปแสดง data ที่ยังไม่ผ่านการ clean และ fill data ที่หายไป</I>
  
  <h3>Checked match data (prepare to join)</h3><br>
  
  ![image](https://github.com/user-attachments/assets/a3d40338-70d4-4bfb-9414-78a5eb29752b)

  &nbsp;&nbsp;&nbsp;&nbsp;<I>รูปที่ 4 รูปแสดง code ที่ใช้ในการ Check match data</I>
  
  <h3>Merge Data</h3><br>
  
  ![image](https://github.com/user-attachments/assets/cfbfa404-4205-4153-b4a3-010d0fa55e57) 

  &nbsp;&nbsp;&nbsp;&nbsp;<I>รูปที่ 5 รูปแสดง code ที่ใช้ในการ Merge data</I>
  
  <h3>Fill and Fix the missing weight and height</h3><br>
  
  ![image](https://github.com/user-attachments/assets/40455fdd-5c44-4f12-b8c5-14b2093e3fb3)

  &nbsp;&nbsp;&nbsp;&nbsp;<I>รูปที่ 6 รูปแสดง code ที่ใช้ในการ Fill และ Fix data ทีขาดหายหรือมีค่าเป็นช่วง</I>
  
  <h3>Drop the data that is DNF DSQ etc.</h3><br>
  
  ![image](https://github.com/user-attachments/assets/03a1d247-4945-49c6-9139-b1c588593954)

  &nbsp;&nbsp;&nbsp;&nbsp;<I>รูปที่ 7 รูปแสดง code ที่ใช้ในการ Drop data ใน column ที่มีค่าเป็น DNF DSQ etc.</I>
  
  ![image](https://github.com/user-attachments/assets/eb20c486-1d9b-47bd-9741-15a9ce811124)

  &nbsp;&nbsp;&nbsp;&nbsp;<I>รูปที่ 8 รูปแสดง data หลังผ่านการ Preparation เรียบร้อยแล้ว</I>


<h1>Analysis</h1>
  หลังจากทำการ clean data ที่ไม่จำเป็น และ fill data ที่ขาดหาย plot กราฟที่แสดงถึงจำนวนของนักกีฬาที่ลงแข่งในแต่ละกีฬา<br>เพื่อเลือกกลุ่มตัวอย่างของกีฬาที่จะนำมาวิเคราะห์
  
  ![image](https://github.com/user-attachments/assets/e9c6921c-ac5e-4ffa-aa58-5ac1e5a6f7db)

  &nbsp;&nbsp;&nbsp;&nbsp;<I>กราฟที่ 1 กราฟแสดงจำนวนของนักกีฬาที่ลงแข่งในแต่ละกีฬา</I>

  จากกราฟเราเลือกกีฬา sports = ['Athletics', 'Swimming', 'Rowing', 'Football', 'Sailing', 'Ice Hockey', 'Shooting', 'Artistic Gymnastics']
  เนื่องจากมีปริมาณนักกีฬาที่เยอะ และเลือก Artistic Gymnastics เพราะส่วนสูง และ น้ำหนักมีความแตกต่างจากกีฬาอื่นอย่างชัดเจน(หุ่นของนักกีฬามีความเฉพาะเจาะจง)<br>

  ![image](https://github.com/user-attachments/assets/df819bb7-4535-45d5-9e37-31e429c6d7a3)
  
  &nbsp;&nbsp;&nbsp;&nbsp;<I>กราฟที่ 2 กราฟแสดงความสูงเฉลี่ยของนักกีฬาที่ได้รับเหรียญรางวัลเทียบกับนักกีฬาที่ไม่ได้รับเหรียญรางวัล</I>
  
  กราฟนี้เปรียบเทียบความสูงเฉลี่ยของนักกีฬาทั้งสองกลุ่ม ผลลัพธ์แสดงให้เห็นว่าความสูงเฉลี่ยของนักกีฬาที่ได้รับเหรียญและไม่ได้รับเหรียญมีความใกล้เคียงกันมาก ซึ่งบ่งชี้ว่าความสูงอาจไม่ใช่ปัจจัยสำคัญที่ส่งผลต่อความสำเร็จในการแข่งขันกีฬา

  ![image](https://github.com/user-attachments/assets/efa9d700-3890-4cea-b099-7644032ef7d6)
  
  &nbsp;&nbsp;&nbsp;&nbsp;<I>กราฟที่ 3 กราฟแสดงน้ำหนักเฉลี่ยของนักกีฬาที่ได้รับเหรียญรางวัลเทียบกับนักกีฬาที่ไม่ได้รับเหรียญรางวัล</I>

  กราฟนี้แสดงให้เห็นว่าน้ำหนักของนักกีฬาทั้งสองกลุ่มก็มีค่าเฉลี่ยใกล้เคียงกัน เช่นเดียวกับความสูง ทำให้สรุปได้ว่าน้ำหนักก็ไม่ใช่ปัจจัยสำคัญในการได้รับเหรียญรางวัล

  ![image](https://github.com/user-attachments/assets/b03ca5fe-18d8-401b-ad65-67512601d753)

 
  &nbsp;&nbsp;&nbsp;&nbsp;<I>กราฟที่ 4 กราฟแสดงอายุเฉลี่ยของนักกีฬาที่ได้รับเหรียญรางวัลเทียบกับนักกีฬาที่ไม่ได้รับเหรียญรางวัล</I>

  กราฟนี้แสดงอายุเฉลี่ยของนักกีฬาที่ได้รับเหรียญและไม่ได้รับเหรียญ ผลลัพธ์แสดงให้เห็นว่าอายุเฉลี่ยของทั้งสองกลุ่มก็ใกล้เคียงกัน โดยอาจบ่งชี้ว่าในกลุ่มนักกีฬาที่เข้าสู่การแข่งขันโอลิมปิกแล้ว อายุไม่ได้เป็นปัจจัยที่มีความสำคัญต่อการได้รับเหรียญรางวัล

  ![image](https://github.com/user-attachments/assets/04919c40-2943-46df-8f9c-ef54125d59c7)
  
  &nbsp;&nbsp;&nbsp;&nbsp;<I>กราฟที่ 5 กราฟแสดงน้ำหนักและส่วนสูงของนักกีฬาที่ได้รับเหรียญรางวัลเทียบกับนักกีฬาที่ไม่ได้รับเหรียญรางวัล</I>

  กราฟนี้แสดงพล็อตแบบสามมิติที่เพิ่มอายุเป็นตัวแปรที่แสดงเป็นขนาดและสีของจุดข้อมูล ผลลัพธ์ยังแสดงให้เห็นว่าส่วนสูง น้ำหนัก และอายุของนักกีฬาทั้งสองกลุ่มมีค่าใกล้เคียงกัน
  
  
  ![visualization (1)](https://github.com/user-attachments/assets/d2f51fd9-b81c-46cb-8cfc-da94a4c4163b) 
  
  &nbsp;&nbsp;&nbsp;&nbsp;<I>กราฟที่ 6 กราฟแสดง น้ำหนัก ส่วนสูง และอายุของนักกีฬาที่ได้เหรียญ(บน) และไม่ได้เหรียญ(ล่าง) โดยอายุจะแสดงเป็นขนาดของจุดข้อมูลและสีของข้อมูล</I>

  กราฟนี้ใช้พล็อตจุด (scatter plot) เพื่อแสดงให้เห็นความสัมพันธ์ระหว่างน้ำหนักและส่วนสูง โดยการเปรียบเทียบกลุ่มนักกีฬาที่ได้รับเหรียญและไม่ได้รับเหรียญ ซึ่งกราฟนี้ยังแสดงให้เห็นอีกครั้งว่าไม่มีความสัมพันธ์ชัดเจนระหว่างน้ำหนักและส่วนสูงกับการได้รับเหรียญ

  ![image](https://github.com/user-attachments/assets/e7450c25-8883-467e-b67f-44391564078c)
  
  &nbsp;&nbsp;&nbsp;&nbsp;<I>กราฟที่ 7 ตารางแสดง correlation ของค่าต่างที่เกี่ยวข้อง</I>

  กราฟนี้แสดงความสัมพันธ์ระหว่างตัวแปรต่าง ๆ (ส่วนสูง น้ำหนัก อายุ) โดยค่าความสัมพันธ์ (correlation) ที่ได้แสดงให้เห็นว่า<br>ไม่มีความสัมพันธ์ที่เด่นชัดระหว่างตัวแปรเหล่านี้กับการได้รับเหรียญรางวัล ทำให้สรุปได้ว่าสิ่งเหล่านี้ไม่ใช่ปัจจัยหลักที่ส่งผลต่อ<br>ความสำเร็จของนักกีฬา
  <br>

<h1>Summary</h1>
  จากการศึกษาข้อมูลและวิเคราะห์ผ่านกราฟทำให้ได้ข้อสรุปว่า ส่วนสูง น้ำหนัก และอายุ ไม่ส่งผลต่อการได้รับเหรียญรางวัลโดยรวม <br>
  แม้ในกีฬาที่ส่วนสูงและน้ำหนักอาจมีผลต่อการแข่ง เช่น กรีฑา(Athletics) โดยนักกีฬามืออาชีพที่ช่วงขาที่ยาวมีข้อได้เปรียบเป็นอย่างมาก<br>
  แต่เนื่องจากในการแข่งขัน Olympic นั้นได้มีการคัดนักกีฬามาแล้ว ทำให้ส่วนสูงและน้ำหนักมีความต่างกันที่น้อย หรือเหมาะสมกับกีฬาที่แข่งแล้ว <br>
  ทำให้การได้เหรียญรางวัลไม่ได้ขึ้นอยู่กับ ส่วนสูง น้ำหนัก และอายุ เป็นหลัก ถ้าข้อมูลของนักกีฬาเก็บไปจนถึงก่อนรอบคัดเลือกเข้าแข่งขัน <br>
  อาจได้ข้อสรุปบางอย่างที่น่าสนใจมากกว่านี้
  


