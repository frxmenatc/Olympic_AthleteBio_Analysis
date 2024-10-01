# DADS5001_MiniProject
<h1>Introduction</h1>
  Dataset : https://www.kaggle.com/datasets/muhammadehsan02/126-years-of-historical-olympic-dataset/data
  <p>ข้อมูลที่เรากำลังสำรวจนี้ จะเป็นการศึกษาปัจจัยต่างๆ ที่มีผลต่อการแข่งขันของนักกีฬา ไม่ว่าจะเป็นอายุ ความสูง และน้ำหนัก 

<h1>Preparation</h1>

  1. Download Data![image](https://github.com/user-attachments/assets/afad997d-ca00-4b4e-a1e1-560df655835a)
  2. Checked match data (prepare to join)![image](https://github.com/user-attachments/assets/a3d40338-70d4-4bfb-9414-78a5eb29752b)
  3. Merge Data![image](https://github.com/user-attachments/assets/cfbfa404-4205-4153-b4a3-010d0fa55e57)
  4. Fill and Fix the missing weight and height![image](https://github.com/user-attachments/assets/40455fdd-5c44-4f12-b8c5-14b2093e3fb3)
  5. Drop the data that is DNF DSQ etc.![image](https://github.com/user-attachments/assets/03a1d247-4945-49c6-9139-b1c588593954)

<h1>Analysis</h1>
  หลังจากทำการ clean data ที่ไม่จำเป็น และ fill data ที่ขาดหาย plot กราฟที่แสดงถึงจำนวนของนักกีฬาที่ลงแข่งในแตจ่ละกีฬาเพื่อเลือกกลุ่มตัวอย่างของกีฬาที่จะนำมาวิเคราะห์
  
  ![image](https://github.com/user-attachments/assets/e9c6921c-ac5e-4ffa-aa58-5ac1e5a6f7db)

  จากกราฟเราเลือกกีฬา sports = ['Athletics', 'Swimming', 'Rowing', 'Football', 'Sailing', 'Ice Hockey', 'Shooting', 'Artistic Gymnastics']
  เนื่องจากมีปริมาณนักกีฬาที่เยอะ และเลือก Artistic Gymnastics เพราะส่วนสูง และ น้ำหนักมีความแตกต่างจากกีฬาอื่นอย่างชัดเจน(หุ่นของนักกีฬามีความเฉพาะเจาะจง)<br>

  ![image](https://github.com/user-attachments/assets/df819bb7-4535-45d5-9e37-31e429c6d7a3)
  
  <I> กราฟแสดงความสูงเฉลี่ยของนักกีฬาที่ได้รับเหรียญรางวัลเทียบกับนักกีฬาที่ไม่ได้รับเหรียญรางวัล</I>

  ![image](https://github.com/user-attachments/assets/efa9d700-3890-4cea-b099-7644032ef7d6)
  
  <I> กราฟแสดงน้ำหนักเฉลี่ยของนักกีฬาที่ได้รับเหรียญรางวัลเทียบกับนักกีฬาที่ไม่ได้รับเหรียญรางวัล</I>

  ![image](https://github.com/user-attachments/assets/b03ca5fe-18d8-401b-ad65-67512601d753)


  <I> กราฟแสดงอายุเฉลี่ยของนักกีฬาที่ได้รับเหรียญรางวัลเทียบกับนักกีฬาที่ไม่ได้รับเหรียญรางวัล</I>

  ![image](https://github.com/user-attachments/assets/04919c40-2943-46df-8f9c-ef54125d59c7)
  
  <I> ตารางแสดง correlation ของค่าต่างที่เกี่ยวข้อง</I>
  
  ![visualization (1)](https://github.com/user-attachments/assets/d2f51fd9-b81c-46cb-8cfc-da94a4c4163b) 
  
  <I> กราฟแสดงน้ำหนักและส่วนสูงของนักกีฬาที่ได้รับเหรียญรางวัลเทียบกับนักกีฬาที่ไม่ได้รับเหรียญรางวัล</I>

  ![image](https://github.com/user-attachments/assets/e7450c25-8883-467e-b67f-44391564078c)
  
  <I> กราฟแสดง น้ำหนัก ส่วนสูง และอายุของนักกีฬาที่ได้เหรียญ(บน) และไม่ได้เหรียญ(ล่าง) โดยอายุจะแสดงเป็นขนาดของจุดข้อมูลและสีของข้อมูล</I>

  จากกราฟทั้งหมด ไม่เห็นถึงความสัมพันธ์ของน้ำหนักและส่วนสูงต่อการได้รับเหรียญรางวัลใน Olympic <br>
  ตารางแสดง correlation ก็ไม่มีค่าใดที่แสดงให้เห็นความสัมพันธ์ของตัวแปร น้ำหนัก และ ส่วนสูง ต่อการได้เหรียญรางวัล

<h1>Summary</h1>
  จากการศึกษาข้อมูลและวิเคราะห์ผ่านกราฟทำให้ได้ข้อสรุปว่า ส่วนสูง อายุ และน้ำหนัก ไม่ส่งผลต่อการได้รับเหรียญรางวัลโดยรวม <br>
  แม้ในกีฬาที่ส่วนสูงและน้ำหนักอาจมีผลต่อการแข่ง เช่น กรีฑา(Athletics) โดยนักกีฬามืออาชีพที่ช่วงขาที่ยาวมีข้อได้เปรียบเป็นอย่างมาก<br>
  แต่เนื่องจากในการแข่งขัน Olympic นั้นได้มีการคัดนักกีฬามาแล้ว ทำให้ส่วนสูงและน้ำหนักมีความต่างกันที่น้อย หรือเหมาะสมกับกีฬาที่แข่งแล้ว <br>
  ทำให้การได้เหรียญรางวัลไม่ได้ขึ้นอยู่กับ น้ำหนัก ส่วนสูง และอายุ เป็นหลัก ถ้าข้อมูลของนักกีฬาเก็บไปจนถึงก่อนรอบคัดเลือกเข้าแข่งขัน <br>
  อาจได้ข้อสรุปบางอย่างที่น่าสนใจมากกว่านี้
  


