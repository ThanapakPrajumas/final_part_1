# final_part_1
1.ผมคิดว่าทั้งสองแบบนี้ต่างก็มีทั้งข้อดีและข้อเสียที่แตกต่างกัน อย่าง Agile ก็มีข้อดีในเรื่องของความยืดหยุ่นต่อการเปลี่ยนแปลง เน้นความเรียบง่ายและรวดเร็ว เหมาะกับลูกค้าที่มีความเข้าใจยากๆและมีแนวโน้มที่จะเปลี่ยนแปลงอยู่ตลอดเวลา ซึ่งจะต่างกับแบบ Waterfall ที่มีลำดับการทำงานที่ตายตัวด้วยการเริ่มตั้งแต่รวบรวมข้อมูล กำหนดความต้องการของผู้ใช้ วิเคราะห์ทางเลือก ออกแบบ เขียนโปรแกรม ทดสอบระบบและสุดท้ายทำการติดตั้งระบบ ปัญหาสำคัญของ Waterfall ก็คือขั้นตอนของการพัฒนาที่ไม่ยืดหยุ่น เพราะตัวงานจะแบ่งเป็นช่วงๆแบบตายตัว ทำให้มีข้อผูกมัดตั้งแต่เริ่มโครงงานและไม่สามารถเปลี่ยนความต้องการของผู้ใช้ได้ ดังนั้นแล้ว ไม่ว่าเราจะเลือกแบบ Agile หรือ Waterfall แล้ว สิ่งสำคัญที่สุดเลยก็คือลูกค้าที่เราติดต่อด้วยเป็นคนแบบไหนต้องการอะไร เราถึงเลือกทำในแบบที่เหมาะสมที่สุด

2.ผมคิดว่ายังคงมีคนที่ใช้งานพวก centralized version control อยู่เป็นส่วนน้อย ขึ้นอยู่กับปัจจัยต่างๆ เช่น วิธีการนำไปใช้ จำนวนคนในทีม ปริมาณงานที่ต้องแก้ไขร่วมกัน เป็นต้น ซึ่ง centralized version control นี้จะมีข้อเสียคือ มีเซิร์ฟเวอร์เป็นศูนย์กลาง1ตัวเป็นคลังข้อมูล เมื่อไฟล์เกิดพังขึ้นมาก็จะทำให้ไม่สามารถดึงไฟล์มาได้ แต่ Git นั้นเป็น distributed version control ซึ่งในแต่ละคนจะมี copy ของไฟล์ตั้งแต่เริ่มแรกจนท้ายสุด ดังนั้นจึงสามารถ maintain code ได้โดยที่ทุกมี copy ของไฟล์ทั้งหมดอยู่ที่ local computer ไม่จำเป็นต้องรอ changes copy จาก central repo อีกต่อไป ดังนั้น ผมคิดว่า Git และ Github นั้นเป็น version control ที่ใช้งานได้ดีที่สุดในตอนนี้

3.git branch feature1
 git commit –m “branch commit”
 git remote add origin https://github.com/ThanapakPrajumas/final_part_1.git
 git push –u origin master

4.อะไรคือสิ่งที่ทำให้เกิด conflict เวลา merge เพราะว่าในการพัฒนา Software ส่วนใหญ่ต้องทำงานเป็นทีม ต้องทำงานบน source code ชุดเดียวกัน พร้อมๆกัน ส่งผลให้เกิดปัญหา merge conflict  โดยวิธีการป้องกันไม่ให้เกิดปัญหาเหล่านี้คือ
4.1 ทำการ Merge บ่อยๆ ซึ่งปัญหาใหญ่ๆของ Merge conflict เกิดจากจำนวน source code ที่ชนหรือขัดแย้งกัน ดังนั้นถ้าต้องการหลีกเลี่ยงปัญหาเหล่านี้ ให้ทำการ merge บ่อยๆไปเลย นั่นคือ ทุกครั้งเมื่อทำการเปลี่ยนแปลง หรือ commit source code นั่นเอง จะช่วยลดข้อขัดแย้งต่างๆลงไปได้มาก ถึงจะเกิดข้อขัดแย้ง ก็เป็นเพียงปัญหาเล็กๆ ซึ่งสามาถแก้ไขได้อย่างงายดาย
4.2 การพูดคุย การสื่อสารกัน มันสำคัญมาก แต่ละคนในทีมได้พูดคุยกันหรือไม่ รู้หรือป่าวว่าเพื่อนๆแต่ละคนทำงานอะไร รู้หรือไม่ว่าแต่ละคนแก้ไข class อะไรกันอยู่ สิ่งที่แก้ไขไปนั้นกระทบใครบ้าง ดังนั้น ถ้าไม่รู้ ก็ควรพูดคุยกันเพื่อให้รู้ หรือบางครั้งต้องแก้ไข class เดียวกันอยู่ตลอดเวลา ก็มานั่งทำงานด้วยกันเลย

5.abcde


6.ในการทำ web application นั้นมีข้อดีตรง เหมาะกับองค์กรขนาดเล็กเพราะมีค่าใช้จ่ายต่ำกว่าและคิดค่าใช้จ่ายตามจำนวนการใช้งานจริง การใช้งานทำได้ง่าย เพียงแค่มีเว็บบราวเซอร์เป็นพื้นฐานในคอมพิวเตอร์ปัจจุบันแทบทุกเครื่องใช้งานได้ มีข้อมูลการจัดเก็บที่เดียว ง่ายต่อการจัดการและไม่เกิดความซ้ำซ้อน อยู่ที่ไหนก็สามารถทำงานได้เพราะสามารถล็อคอินเข้าใช้งานได้เลยโดยไม่ต้องติดตั้งโปรแกรม

7.เริ่มจาก Client ส่ง Request ไปที่ Web App ซึ่งจะถูกส่งต่อให้ Controllerทำการตรวจสอบข้อมูลที่มาให้ (Request Method, Request Parameters) 
แล้ว Controller จะเรียก Method ให้ทำงานเพื่อจัดการ Request นั้น 
Model จะทำการคำนวณและอาจติดต่อกับ Database เพื่อจัดการกับ Requestนั้น แล้วส่งผลลัพธ์กลับไปที่ Controller 
มื่อ Controller ได้ผลลัพธ์จาก Model แล้วก็ใช้ผลลัพธ์นั้นส่งต่อให้ View ทำงาน 
View จะสร้าง Page สำหรับแสดงผลลัพธ์นั้น แล้วส่ง page กลับไปที่ Controller  
Controller ส่ง Page นั้น (เป็น Response) กลับไปยัง Client 

8.ฺBootstrap ใช้ในการสร้างเทมเพลทให้กับเว็บ

9.Heroku คือผู้ให้บริการ Platform as a Service(PaaS)เช่น แอพพลิเคชั่นเซิร์ฟเวอร์,ดาต้าเบสเซิร์ฟเวอร์หรือมิดเดิลแวร์อื่นๆ ไม่ต้องเสียเวลาหา software ไม่ต้องหา server และลดความยุ่งยากในกร configuration เพราะเพียงแค่คลิกเลือกภาษาที่ต้องการสร้าง app ไม่ถึง นาทีเราก็มี environment พร้อมใช้งาน

10.ผมคิดว่าทางสาขาอยากให้นิสิตได้นำการเรียนรู้การใช้ประโยชน์ในการพัฒนาซอฟต์แวร์ต่างๆนี้ไปใช้งานจริง ไม่ว่าจะเป็นการเขียนภาษา Ruby การใช้ Version control อย่าง Git,Github 
