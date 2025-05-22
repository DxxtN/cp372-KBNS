# CP372 Data Analytic Project : การวิเคราะห์ข้อมูลยอดขายวิดีโอเกมทั่วโลก

---

จัดทำโดย
1. นางสาวกัลย์สุดา บัวตูม 65102010109
2. นางสาวณัฐนรี ศุขทัตน์ 65102010415

เสนอ : อาจารย์ ผศ.ดร. รัตน์ชัยนันท์ ธรรมสุจริต

---

โครงการนี้เป็นส่วนหนึ่งของรายวิชา CP372 Data Analytics and Business Intelligence ชั้นปีที่ 3 จัดทำขึ้นเพื่อศึกษาความรู้ในเรื่องของการวิเคราะห์ข้อมูลและการใช้เทคโนโลยีด้าน Business Intelligence ในการประมวลผลข้อมูลเพื่อนำมาใช้ในการตัดสินใจและพัฒนาในด้านธุรกิจ โดยใช้เครื่องมือที่มีความเกี่ยวข้อง เช่น Excel หรือ Tableau

ทางคณะผู้จัดทำหวังว่าโครงการนี้จะเป็นประโยชน์ต่อผู้อ่านและนิสิตทุกท่าน ที่มีความสนใจหรือกำลังเรียนรู้ในด้าน Data Analytics และ Business Intelligence หากมีข้อผิดพลาดประการใด คณะผู้จัดทำ ขออภัยมา ณ ที่นี้

---

## สารบัญ
- [Overview](#Overview)
- [Exploratory Data Analysis](#Exploratory-Data-Analysis)
- [In-Depth Analysis](#In-Depth-Analysis)
- [Visualization](#Visualization)

---
## Overview
โครงการนี้เป็นโครงการการวิเคราะห์ข้อมูลยอดขายวิดีโอเกมทั่วโลก มีจุดประสงค์เพื่อให้ผู้จัดทำสามารถนำความรู้ที่ได้จากบทเรียนรายวิชา CP372 มาประยุกต์ใช้กับข้อมูลจริง ซึ่งสามารถฝึกทักษะการคิดวิเคราะห์ การนำเสนอผลลัพธ์ให้อยู่ในรูปแบบที่เข้าใจง่าย และนำไปใช้ประโยชน์ต่อในการทำงานด้านธุรกิจในภายภาคหน้าได้เช่นกัน

ข้อมูลที่ใช้ : https://www.kaggle.com/datasets/gregorut/videogamesales?resource=download

เครื่องมือที่ใช้
- Excel : การเตรียมข้อมูล เช่น การทำความสะอาดข้อมูล การจัดรูปแบบ และการจัดหมวดหมู่ข้อมูล
- Tableau : วิเคราะห์และแสดงผลข้อมูลในรูปแบบภาพ (Visualization)
- Notepad : การบันทึกและอธิบายโค้ดในขั้นตอนต่างๆ
- GitHub : การเก็บรวบรวมข้อมูล

---

## Exploratory Data Analysis 
1. Global Sales (AVG) Vs. Genre
- เกมประเภท Platform, Shooter, และ Role-Playing มีค่าเฉลี่ยยอดขายทั่วโลกสูงที่สุด
- แสดงให้เห็นว่า ผู้เล่นนิยมเล่นเกมประเภท Platform มากที่สุด ซึ่งเกมประเภทนี้สามารถเข้าถึงผู้คนได้ง่ายจริง และมีความโด่งดัง จึงเป็นที่นิยม
- ตัวอย่างเกมประเภท Platform ได้แก่ Mario, Sonic, และ Donkey Kong
![image](https://github.com/user-attachments/assets/92bbd81a-10de-4f30-bdcf-784764395b1f)
---
2. Global Sales (SUM) Vs. Platform
- แพลตฟอร์มที่ได้รับความนิยมมากที่สุด ได้แก่ PS2, X360, PS3, และ Wii
- โดยในอนาคต แพลตฟอร์มเหล่านี้สามารถพัฒนาเป็นแพลตฟอร์ใหม่ๆที่ดีกว่า และยังได้รับความนิยมมากขึ้น เช่น PS4, Nintendo
![image](https://github.com/user-attachments/assets/0c4ef0c7-8697-4c36-a9b5-0b379c298a49)
---
3. [JP Sales & NA Sales (SUM)] Vs. Genre
- กราฟนี้เปรียบเทียบยอดขายของภูมิภาคญี่ปุ่นและอเมริกาเหนือโดยแบ่งตามประเภทเกม
- ในการแสดงผลกราฟ จะแสดงประเภทเกมโดยที่ยอดขายของ JP จะมากกว่า NA 2,000,000 ขึ้นไป
- ผลลัพธ์คือเกมประเภท Role-Playing, Simulation, Misc, etc. ได้รับความนิยมในญี่ปุ่นมากกว่าอเมริกาเหนือ
![image](https://github.com/user-attachments/assets/b8739379-0105-4c6e-a2c7-d23f4fb3dbd6)
---
มีการสร้างField ใหม่ชื่อ JP&NA โดยใช้ Calculate Field เพื่อกรองหาประเภทเกมที่มียอดขายของ JP มากกว่า NA 2,000,000 ขึ้นไป
![image](https://github.com/user-attachments/assets/979a2f7a-557f-4686-a77f-62854ea3e040)

---
4. Global Sales (AVG) Vs. Publisher
- กราฟแสดง 10 อันดับผู้ผลิตที่มียอดขายมากที่สุดในช่วงปี 2000 - 2020
- Nintendo, Take Two Interactive, Sony Computer Entertainment ได้รับความนิยมมากที่สุด
![image](https://github.com/user-attachments/assets/1db15267-57ee-49db-8942-1954356759e6)

---

## In-Depth Analysis
- สมมติฐานที่ 1 : แนวโน้มยอดขายเปลี่ยนไปตามยุคของแพลตฟอร์ม 
- ผลลัพธ์ : จากกราฟแสดงให้เห็นว่า เมื่อยุคสมัยเปลี่ยนไป ยอดขายก็เพิ่มขึ้น และแพลตฟอร์มที่เป็นที่นิยมก็เปลี่ยนไปตามยุคสมัยด้วย (เป็นจริง)
![image](https://github.com/user-attachments/assets/d74149ce-d021-419e-a2ff-fdc7beb84f2c)
![image](https://github.com/user-attachments/assets/8a6992bd-9730-4adb-b1db-afd89fb82409)
![image](https://github.com/user-attachments/assets/a2885132-8a12-4e50-a75d-897f13ff622b)
![image](https://github.com/user-attachments/assets/f8ce141b-8e93-4997-9a8e-e8d1d3f3dd5f)
---
- สมมติฐานที่ 2 : Nintendo เป็นผู้นำในยอดขายทั่วโลก
- ผลลัพธ์ : จากกราฟยอดขายรวมทุกปี (1980-2020) Nintendo เป็นอันดับ 1 (เป็นจริง)
![image](https://github.com/user-attachments/assets/a2b1f725-1ff5-4adb-83ad-0881735e65a1)
---
มีการสร้าง Field ใหม่ชื่อ PlatformEra โดยใช้ Calculate Field เพื่อแยกช่วงของยุคสมัย
![image](https://github.com/user-attachments/assets/345c0624-180b-4212-93cb-e4285631f8f6)

---

## Visualization
1. Dashboard ยอดขายรวมทั่วโลกตามปี และตามภูมิภาค
![image](https://github.com/user-attachments/assets/dd39db57-6c6f-404f-960a-a220397c9b27)
---
2. Dashboard ความนิยมของ Platform และผู้ผลิต แบ่งตามยุคสมัย
![image](https://github.com/user-attachments/assets/c772081c-4816-447b-bc0a-23b3d789c668)
![image](https://github.com/user-attachments/assets/b2299f04-02b9-4656-bce2-6c60b8b05c42)
![image](https://github.com/user-attachments/assets/63df8136-26ed-4c46-b821-412eadefb563)
![image](https://github.com/user-attachments/assets/5eed8502-ecd8-4ed1-a23d-786c880353a7)

Public Dashboard Link
- Dashboard 1 : https://public.tableau.com/app/profile/nutnaree.suktad/viz/Project_109_415/Dashboard1?publish=yes
- Dashboard 2 : https://public.tableau.com/app/profile/nutnaree.suktad/viz/Project_109_415/Dashboard2?publish=yes

---

## Summary
จากการวิเคราะห์ข้อมูลยอดขายวิดีโอเกมทั่วโลก พบว่าอุตสาหกรรมวิดีโอเกมมีการเปลี่ยนแปลงและเติบโตอย่างต่อเนื่อง โดยมีปัจจัยสำคัญที่ส่งผลต่อยอดขาย ได้แก่ แนวเกม (Genre), แพลตฟอร์ม (Platform), ผู้จัดจำหน่าย (Publisher) และยุคสมัย (PlatformEra) ของเทคโนโลยี โดยสามารถสรุปสาระสำคัญจากโครงการนี้ได้ดังนี้
1. ประเภทเกมที่ขายดีที่สุด ได้แก่ Platform และ Shooter ซึ่งเข้าถึงผู้เล่นได้กว้าง โดยมีค่าเฉลี่ยยอดขายค่อนข้างสูงเมื่อเทียบกับประเภทเกมอื่น ๆ
2. แพลตฟอร์มที่ได้รับความนิยม จะแตกต่างกันไปตามยุคสมัย เช่น PS, Wii, และ DS เคยเป็นผู้นำในช่วงยุค 2000s ก่อนจะถูกแทนที่ด้วยแพลตฟอร์มใหม่ที่ทันสมัยกว่า
3. Nintendo เป็นผู้ผลิตที่ประสบความสำเร็จสูงสุดในยอดขายรวมทั่วโลก จากข้อมูลที่รวบรวมตั้งแต่ปี 1980-2020

มีการใช้เทคนิคการสร้าง Field ใหม่ เช่น PlatformEra ทำให้สามารถแบ่งข้อมูลตามยุคสมัยได้อย่างชัดเจน ช่วยให้เห็นภาพรวมของอุตสาหกรรมวิดีโอเกมในแต่ละช่วงเวลา

และสุดท้าย โครงการนี้แสดงให้เห็นถึงความสำคัญของ Data Analytics และ Business Intelligence ในการวิเคราะห์ข้อมูลเชิงลึก เพื่อนำไปสู่การตัดสินใจทางด้านธุรกิจที่มีประสิทธิภาพ และยังเป็นการฝึกฝนทักษะในการใช้เครื่องมือที่เกี่ยวข้อง เช่น Excel และ Tableau ซึ่งสามารถนำไปประยุกต์ใช้ในการทำงานจริงในอนาคต

---

Thank you for your time.
