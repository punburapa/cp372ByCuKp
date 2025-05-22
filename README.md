# cp372ByCuKp
 Data Analytic project about Human Resource

 Tableau Public Link : [Click Here](https://public.tableau.com/shared/NGX7YFFFF?:display_count=n&:origin=viz_share_link)

**Problem Statement:** เนื่องจากบริษัทมีปัญหาการขาดงาน ซึ่งมีผลมาจากหลายปัญจัยเช่น ค่าใช้จ่ายในการเดินทาง ระยะทาง หรือในด้านสุขภาพที่อาจส่งผล ทำให้จำเป็นต้อง
วิเคราะห์สาเหตุการขาดงาน และนำมาปรับใช้เพื่อแก้ไขปัญหานี้

**Business Objectives:** ปรับโครงสร้างองกรณ์ เพื่อให้ผลงานจากแรงงานมีประสิทธิภาพต่องบประมาณการว่าจ้างมากที่สุด เพื่อหาสาเหตุที่ทำให้มีการลาเกิดขึ้น 

**Key Stakeholders:** HR, Management Board

**Success metrics:** จำนวนการลาลดลง

## Data Dictionary

- **Day of the week:** 
  - Sunday(1)
  - Monday (2)
  - Tuesday (3)
  - Wednesday (4)
  - Thursday (5)
  - Friday (6)
  - saturday(7)
- **Seasons :** 
  - summer (1)
  - autumn (2)
  - winter (3)
  - spring (4)
- **Transportation expense:** ค่าใช้จ่ายในการเดินทางต่อเดือน
- **Distance from Residence to Work:** ระยะทางจากที่พักถึงที่ทำงาน (Km)
- **Service time:** จำนวนปีที่ทำงานกับบริษัทมา
- **Hit target:** เป้าหมายที่ทำได้
- **Disciplinary failure:** มีความผิดทางวินัยหรือไม่
- **Education:** 
  - high school (1)
  - graduate (2)
  - postgraduate (3)
  - master and doctor (4)
- **Social drinker:** พนักงานคนนั้นเป็นคนดื่มเข้าสังคมหรือไม่
- **Social smoker:** พนักงานคนนั้นเป็นคนสูบบุหรี่เข้าสังคมหรือไม่
- **Pet:** จำนวนสัตว์เลี้ยงที่พนักงานนั้นมี

## Data Preparation
### Data Cleaning

![Missing Data in DataCleaning](/assets//image/Data%20Cleaning1.png)

มี Missing data ที่ Column "Reason.Reason for absence_name" ที่เกิดจาก ไม่ได้ระบุ Reason of Absence ไว้ จึงไม่มี Absence name
ไม่ส่งผลต่อการวิเคราะห์ข้อมูล จึงไม่จำเป็นต้องลงมือใดๆ


