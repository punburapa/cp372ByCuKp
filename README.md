# cp372ByCuKp
 Data Analytic project about Human Resource

 สมาชิกกลุ่ม

1. กฤตภัค พิมพ์จุฬา 65102010012
2. ชินาวี อุดมสมบูรณ์ 65102010111
3. บูรพา ยืนยง 65102010418

 Tableau Public: [Click Here](https://public.tableau.com/shared/NGX7YFFFF?:display_count=n&:origin=viz_share_link)

 Presentation Video: [Click Here](https://youtu.be/u4NVEeT8qcE?si=g9vCKkS_aKGM6vHp)



## Project Canvas
![Project Canvas](/assets/image/Project%20Canvas.jpg)

**Problem Statement:** เนื่องจากบริษัทมีปัญหาการขาดงาน ซึ่งมีผลมาจากหลายปัญจัยเช่น ค่าใช้จ่ายในการเดินทาง ระยะทาง หรือในด้านสุขภาพที่อาจส่งผล ทำให้จำเป็นต้อง
วิเคราะห์สาเหตุการขาดงาน และนำมาปรับใช้เพื่อแก้ไขปัญหานี้

**Business Objectives:** ปรับโครงสร้างองกรณ์ เพื่อให้ผลงานจากแรงงานมีประสิทธิภาพต่องบประมาณการว่าจ้างมากที่สุด เพื่อหาสาเหตุที่ทำให้มีการลาเกิดขึ้น 

**Key Stakeholders:** Human Resource, Management Board

**Success metrics:** จำนวนการลาลดลง

**Timeline**

วันที่ 1 ทำความเข้าใจข้อมูล ตรวจสอบ missing data ที่จำเป็นต้องแก้ไข\
วันที่ 2-3 ทำ EDA สร้างกราฟเพื่อดูข้อมูลเชิงลึกหาสาเหตุของการลา\
วันที่ 4 วิเคราะห์ผลและตั้งสมมติฐานของสาเหตุการลาเบื้องต้น\
วันที่ 5 สรุป Insight เสนอแนะวิธีการแก้ปัญหาการลาแล้วจึงจัดทำรายงาน

## Data Dictionary

- **Reason for Absence**
  - Certain infectious and parasitic diseases (1)  
  - Neoplasms (2)  
  - Diseases of the blood and blood-forming organs and certain disorders involving the immune mechanism (3)  
  - Endocrine, nutritional and metabolic diseases (4)  
  - Mental and behavioural disorders (5)  
  - Diseases of the nervous system (6)  
  - Diseases of the eye and adnexa (7)  
  - Diseases of the ear and mastoid process (8)  
  - Diseases of the circulatory system (9)  
  - Diseases of the respiratory system (10)  
  - Diseases of the digestive system (11)  
  - Diseases of the skin and subcutaneous tissue (12)  
  - Diseases of the musculoskeletal system and connective tissue (13)  
  - Diseases of the genitourinary system (14)  
  - Pregnancy, childbirth and the puerperium (15)  
  - Certain conditions originating in the perinatal period (16)  
  - Congenital malformations, deformations and chromosomal abnormalities (17)  
  - Symptoms, signs and abnormal clinical and laboratory findings, not elsewhere classified (18)  
  - Injury, poisoning and certain other consequences of external causes (19)  
  - External causes of morbidity and mortality (20)  
  - Factors influencing health status and contact with health services (21)  
  - Patient follow-up (22)  
  - Medical consultation (23)  
  - Blood donation (24)  
  - Laboratory examination (25)  
  - Unjustified absence (26)  
  - Physiotherapy (27)  
  - Dental consultation (28)


- **Day of the week:** 
  - Sunday (1)
  - Monday (2)
  - Tuesday (3)
  - Wednesday (4)
  - Thursday (5)
  - Friday (6)
  - Saturday(7)
- **Seasons :** 
  - Summer (1)
  - Autumn (2)
  - Winter (3)
  - Spring (4)
- **Transportation expense:** ค่าใช้จ่ายในการเดินทางต่อเดือน
- **Distance from Residence to Work:** ระยะทางจากที่พักถึงที่ทำงาน (Km)
- **Service time:** จำนวนปีที่ทำงานกับบริษัทมา
- **Hit target:** เป้าหมายที่ทำได้
- **Disciplinary failure:** มีความผิดทางวินัยหรือไม่
- **Education:** 
  - High school (1)
  - Graduate (2)
  - Postgraduate (3)
  - Master and Doctor (4)
- **Social drinker:** พนักงานคนนั้นเป็นคนดื่มเข้าสังคมหรือไม่
- **Social smoker:** พนักงานคนนั้นเป็นคนสูบบุหรี่เข้าสังคมหรือไม่
- **Pet:** จำนวนสัตว์เลี้ยงที่พนักงานนั้นมี

## Data Preparation
### Data Cleaning

![Missing Data in DataCleaning](/assets//image/Data%20Cleaning1.png)

มี Missing data ที่ Column "Reason.Reason for absence_name" ที่เกิดจาก ไม่ได้ระบุ Reason of Absence ไว้ จึงไม่มี Absence name
ไม่ส่งผลต่อการวิเคราะห์ข้อมูล จึงไม่จำเป็นต้องลงมือใดๆ


### Feature Engineering

Level of drug addiction : คือ Social drinker + Social Smoker 

![Level of drug addiction Formula](/assets/image/Level%20of%20drug%20addiction%20Formula.png)

Age Enter Company : อายุที่เข้าทำงานกับบริษัท

![Age Enter Company Formula](/assets/image/Level%20of%20drug%20addiction%20Formula.png)

### Tableau Preparation
เปลี่ยนประเภทของข้อมูลใน Column เหล่านี้ให้เป็น String
- Social Drinker
- Social Smoker
- Level of drug addiction

![Tableau Preparation](/assets/image/Tableau%20Preparation.png)

## Exploratory Data Analysis (EDA)
### Distribution

>Distribution จะสามารถ bias ได้ เนื่องจากเป็นข้อมูลการลา ซึ่งไม่ใช่ข้อมูลของพนักงานทั้งหมด

Workload Distribution

![Workload Distribution](/assets/image/Workload%20Distribution.png)


Age Distribution

![Age Distribution](/assets/image/Age%20Distribution.png)


BMI Distribution

![BMI Distribution](/assets/image/BMI%20Distribution.png)


Distance from Residence to Work Distribution

![Distance from Residence to Work Distribution](/assets/image/Distance%20from%20Residence%20to%20Work%20Distribution.png)


### Bar Chart

Absence time for each employee

![Absence time for each employee](/assets/image/Absence%20time%20for%20each%20employee.png)


Percent of Absence from each employee
![Percent of Absence from each employee](/assets/image/Percent%20of%20Absence%20from%20each%20employee.png)


Percent of Absence from each Reason
![Percent of Absence from each Reason](/assets/image/Percent%20of%20Absence%20from%20each%20Reason.png)

Percent of Absence from each Day in a Week
![Percent of Absence from each Day in a Week](/assets/image/Percent%20of%20Absence%20from%20each%20Day%20in%20a%20Week.png)


## In-Depth Analysis
### เหตุผลการลาในแต่ละวันมันลักษณะต่างกันอย่างไร

Monday
![Monday](/assets/image/Monday.png)


Tuesday
![Tuesday](/assets/image/Tuesday.png)


Wednesday
![Wednesday](/assets/image/Wednesday.png)


Thursday
![Thursday](/assets/image/Thursday.png)

Friday
![Friday](/assets/image/Friday.png)

- วันจันทร์และวันศุกร์มีการลาแบบ unjustified ที่เด่น
- สาเหตุการลาหลักส่วนใหญ่คือการปรึกษาแพทย์
- มักลาไปกายภาพบำบัดในวัน พุธ พฤหัสบดี ศุกร์

### คนที่ลาไปกายภาพบำบัดหรือมีปัญหาสุขภาพทางกล้ามเนื้อมีลักษระเด่นของอายุหรือไม่

![Muscle age](/assets//image/Muscle%20age.png)


### จำนวนครั้งที่ลา และชั่วโมงรวมที่ลาไป ส่งผลกับประสิทธิภาพการทำงานหรือเปล่า


พบว่าไม่มีการส่งผลกันอย่างเห็นได้ชัด

![Worker Efficiency by Hit Target](/assets/image/Worker%20Efficiency%20by%20Hit%20Target.png)

ระดับการศึกษานั้นมีข้อมูลไม่เพียงพอที่จะสรุปได้ว่าส่งผลกับการทำงาน

![Worker Efficiency by Hit Target with Education](/assets/image/Worker%20Efficiency%20by%20Hit%20Target%20with%20Education.png)


เช่นเดียวกันกับการดื่มสุราหรือสูบบุหรี่


![10](/assets/image/10.jpg)

ี่
การเลี้ยงสัตว์

![11](/assets/image/11.jpg)


และการเลี้ยงลูก

![12](/assets/image/12.jpg)


เราจึงสนใจสาเหตุการลาหลักๆที่มาจากเรื่องสุขภาพ

![13](/assets/image/13.jpg)

ตัวอย่างเช่น พนักงานหมายเลข 3 ลาไปกายภาพบำบัดถึง 38 ครั้ง คิดรวมกันเป็น 97 ชั่วโมง

![14](/assets/image/14.jpg)

## Insight

การลาไปปรึกษาแพทย์ หรือกายภาพบำบัดมีมาก แต่ใช้เวลาน้อย เฉลี่ยแล้วเพียง 3 ชั่วโมง โดยสามารถจบได้ภายในครึ่งวัน

![15](/assets/image/15.jpg)

## Recommendations

14.81% ของชั่วโมงที่ลาไปทั้งหมดสามารถลดได้ด้วยการจัดสวัสดิการ ปรึกษาแพทย์ และทันตแพทย์ ที่ Office

![16](/assets/image/16.jpg)


19.49% ของชั่วโมงที่ลาจากสาเหตุสุขภาพกล้ามเนื้อสามารถลดได้ด้วยการเพิ่มสวัสดิการด้านสุขภาพ เช่น กายภาพบำบัดฟรีในทุกๆเดือน

![17](/assets/image/17.jpg)

