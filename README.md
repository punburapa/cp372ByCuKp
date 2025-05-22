# cp372ByCuKp
 Data Analytic project about Human Resource

 Tableau Public: [Click Here](https://public.tableau.com/shared/NGX7YFFFF?:display_count=n&:origin=viz_share_link)

 Presentation Video: [Click Here]()

## Project Canvas
![Project Canvas](/assets/image/Project%20Canvas.jpg)

**Problem Statement:** เนื่องจากบริษัทมีปัญหาการขาดงาน ซึ่งมีผลมาจากหลายปัญจัยเช่น ค่าใช้จ่ายในการเดินทาง ระยะทาง หรือในด้านสุขภาพที่อาจส่งผล ทำให้จำเป็นต้อง
วิเคราะห์สาเหตุการขาดงาน และนำมาปรับใช้เพื่อแก้ไขปัญหานี้

**Business Objectives:** ปรับโครงสร้างองกรณ์ เพื่อให้ผลงานจากแรงงานมีประสิทธิภาพต่องบประมาณการว่าจ้างมากที่สุด เพื่อหาสาเหตุที่ทำให้มีการลาเกิดขึ้น 

**Key Stakeholders:** HR, Management Board

**Success metrics:** จำนวนการลาลดลง

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
