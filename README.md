# PROJECT_Tutorial_Angularjs
Angular-Tutorial-the tutorial for AngularJS
This project is an application skeleton for a typical AngularJS web app. You can use it to quickly bootstrap your angular webapp projects and dev environment for these projects.

The tutorial contains a sample AngularJS application and is preconfigured to install the AngularJS framework and a bunch of development and testing tools for instant web development gratification.

## Getting Started
ในการเริ่มต้น คุณสามารถโคลนที่ ```PROJECT_Tutorial_Angularjs``` เก็บและติดตั้งการขึ้นต่อกัน:

### Prerequisites ``` PROJECT_Tutorial_Angularjs  ```
คุณต้องใช้ git เพื่อโคลนที่ ``` PROJECT_Tutorial_Angularjs repository```. คุณสามารถรับ git ได้จากที่[นี่](https://git-scm.com/).

เรายังใช้เครื่องมือ Node.js จำนวนมากเพื่อเริ่มต้นและ ```PROJECT_Tutorial_Angularjs```. ทดสอบ คุณต้องมี Node.js และตัวจัดการแพ็คเกจ (npm) ติดตั้งอยู่ คุณสามารถรับได้จากที่[นี่](https://nodejs.org/en/).

### Clone ```PROJECT_Tutorial_Angularjs  ```
โคลนที่ ```PROJECT_Tutorial_Angularjs  ``` เก็บโดยใช้ git:
```
git clone https://github.com/San5box/PROJECT_Tutorial_Angularjs.git
cd PROJECT_Tutorial_Angularjs
```
หากคุณต้องการเริ่มโครงการใหม่โดยไม่มี ```PROJECT_Tutorial_Angularjs``` ประวัติการคอมมิต คุณสามารถทำได้จาก:
```
git clone --depth=1 https://github.com/San5box/PROJECT_Tutorial_Angularjs.git <your-project-name>

```
คำสั่ง ```depth=1``` บอกให้ git ดึงข้อมูลประวัติที่มีค่าคอมมิชชั่นหนึ่งรายการเท่านั้น

### Install Dependencies
เรามี dependencies 2 ประเภท เครื่องมือและโค้ดเฟรมเวิร์ก AngularJS เครื่องมือช่วยเราจัดการและทดสอบแอปพลิเคชัน
* เราได้รับเครื่องมือที่เราพึ่งพาและรหัส AngularJS ผ่านทาง [Node package manager](https://www.npmjs.com/)
* ในการรันการทดสอบแบบ end-to-end คุณจะต้อง ติดตั้ง [Java Development Kit (JDK)](https://en.wikipedia.org/wiki/Java_Development_Kit) บนเครื่องของคุณ ตรวจสอบส่วน end-to-end testing  สำหรับข้อมูลเพิ่มเติม

เราได้กำหนดค่าล่วงหน้า ```npm```ให้คัดลอกไฟล์ AngularJS ที่ดาวน์โหลดมาโดยอัตโนมัติเพื่อ ```app/lib``` ให้เราทำได้ง่ายๆ ดังนี้:

>npm install 

เบื้องหลังนี้จะเรียก ```npm run copy-libs```, ซึ่งคัดลอกไฟล์ AngularJS และการพึ่งพาส่วนหน้าอื่น ๆ หลังจากนั้น คุณควรพบว่าคุณมีไดเร็กทอรีใหม่สองไดเร็กทอรีในโครงการของคุณ
* ```node_modules ```- มีแพ็คเกจ npm สำหรับเครื่องมือที่เราต้องการ
* ```app/libs ``` - มีไฟล์เฟรมเวิร์ก AngularJS และการพึ่งพาส่วนหน้าอื่น ๆ
_หมายเหตุ การคัดลอกไฟล์ AngularJS จาก ```node_modules``` ทำให้ ```app/lib```ทำให้ง่ายต่อการให้บริการไฟล์โดยเว็บเซิร์ฟเวอร์ _

## Run the Application
เราได้กำหนดค่าโครงการล่วงหน้าด้วยเว็บเซิร์ฟเวอร์การพัฒนาอย่างง่าย วิธีที่ง่ายที่สุดในการเริ่มต้นเซิร์ฟเวอร์นี้คือ:

>npm start

ตอนนี้เรียกดูเว็ปแอพได้ที่ (http://localhost:4200/)

## Directory Layout
 ```app/                  --> all of the source files for the application
  app.css               --> default stylesheet
  core/                 --> all app specific modules
    version/              --> version related components
      version.js                 --> version module declaration and basic "version" value service
      version_test.js            --> "version" value service tests
      version-directive.js       --> custom directive that returns the current app version
      version-directive_test.js  --> version directive tests
      interpolate-filter.js      --> custom interpolation filter
      interpolate-filter_test.js --> interpolate filter tests
  view1/                --> the view1 view template and logic
    view1.html            --> the partial template
    view1.js              --> the controller logic
    view1_test.js         --> tests of the controller
  view2/                --> the view2 view template and logic
    view2.html            --> the partial template
    view2.js              --> the controller logic
    view2_test.js         --> tests of the controller
  app.js                --> main application module
  index.html            --> app layout file (the main html template file of the app)
  index-async.html      --> just like index.html, but loads js files asynchronously
e2e-tests/            --> end-to-end tests
  protractor-conf.js    --> Protractor config file
  scenarios.js          --> end-to-end scenarios to be run by Protractor
karma.conf.js         --> config file for running unit tests with Karma
package.json          --> Node.js specific metadata, including development tools dependencies
package-lock.json     --> Npm specific metadata, including versions of installed development tools dependencies
 ```

## Testing
การทดสอบในแอปพลิเคชันมี2 ประเภท PROJECT_Tutorial_Angularjs: การทดสอบหน่วยและการทดสอบแบบ end-to-end

### Running Unit Tests
เว็ปแอพ```PROJECT_Tutorial_Angularjs  ```นี้มีการกำหนดค่าล่วงหน้าพร้อมทดสอบหน่วย สิ่งเหล่านี้เขียนด้วย [Jasmine](https://jasmine.github.io/) อีกครั้ง การทดสอบเหล่านี้ดำเนินการด้วยตัววิ่งทดสอบ [Protractor](https://www.protractortest.org/#/)End-to-End test ใช้เหตุการณ์ดั้งเดิมและมีคุณสมบัติพิเศษสำหรับแอปพลิเคชัน AngularJS
* การกำหนดค่าพบได้ที่ ```karma.conf.js```
* การทดสอบหน่วยจะพบถัดจากรหัสที่กำลังทดสอบและมี```.spec.js```ส่วนต่อท้าย (เช่น ```view1.spec.js```)
วิธีที่ง่ายที่สุดในการรันการทดสอบหน่วยคือการใช้สคริปต์ npm ที่ให้มา:

>npm test

สคริปต์นี้จะเริ่มตัวดำเนินการทดสอบ Karma เพื่อดำเนินการทดสอบหน่วย นอกจากนี้ Karma จะเริ่มดูซอร์สและไฟล์ทดสอบสำหรับการเปลี่ยนแปลง จากนั้นทำการทดสอบใหม่ทุกครั้งที่มีการเปลี่ยนแปลง นี่คือกลยุทธ์ที่แนะนำ หากการทดสอบหน่วยของคุณถูกเรียกใช้ทุกครั้งที่คุณบันทึกไฟล์ คุณจะได้รับคำติชมทันทีเกี่ยวกับการเปลี่ยนแปลงใดๆ ที่ขัดขวางการทำงานของโค้ดที่คาดไว้ 

คุณยังสามารถขอให้ Karma ทำการทดสอบครั้งเดียวแล้วออก สิ่งนี้มีประโยชน์หากคุณต้องการตรวจสอบว่ารหัสรุ่นใดรุ่นหนึ่งทำงานตามที่คาดไว้ โครงการมีสคริปต์ที่กำหนดไว้ล่วงหน้าเพื่อทำสิ่งนี้:

>npm run test-single-run

### Running End-to-End Tests
เว็ปแอพ```PROJECT_Tutorial_Angularjs  ```นี้มาพร้อมกับการทดสอบแบบ end-to-end ซึ่งเขียนด้วย [Jasmine](https://jasmine.github.io/)
อีก ครั้ง การทดสอบเหล่านี้ดำเนินการด้วยตัววิ่งทดสอบ[Protractor](https://www.protractortest.org/#/)End-to-End test มันใช้เหตุการณ์ดั้งเดิมและมีคุณสมบัติพิเศษสำหรับแอปพลิเคชัน AngularJS
* การกำหนดค่าพบได้ที่ ```e2e-tests/protractor-conf.js ```
* การทดสอบแบบ end-to-end มีอยู่ใน ```e2e-tests/scenarios.js ```
ไม้โปรแทรกเตอร์จำลองการโต้ตอบกับเว็บแอปของเราและตรวจสอบว่าแอปพลิเคชันตอบสนองอย่างถูกต้อง ดังนั้น เว็บเซิร์ฟเวอร์ของเราต้องให้บริการแอปพลิเคชัน เพื่อให้ Protractor สามารถโต้ตอบกับมันได้

ก่อนเริ่ม Protractor ให้เปิดหน้าต่างเทอร์มินัลแยกต่างหากแล้วเรียกใช้:

>npm start

นอกจากนี้ เนื่องจาก Protractor สร้างขึ้นบน WebDriver เราจึงต้องตรวจสอบให้แน่ใจว่ามีการติดตั้งและเป็นปัจจุบัน โปรเจ็กต์ ```PROJECT_Tutorial_Angularjs  ```ได้รับการกำหนดค่าให้ทำสิ่งนี้โดยอัตโนมัติก่อนเรียกใช้การทดสอบแบบ end-to-end ดังนั้นคุณจึงไม่ต้องกังวลเกี่ยวกับเรื่องนี้ หากคุณต้องการอัปเดต WebDriver ด้วยตนเอง คุณสามารถเรียกใช้:

>npm run update-webdriver

เมื่อคุณแน่ใจว่าเว็บเซิร์ฟเวอร์การพัฒนาที่โฮสต์แอปพลิเคชันของเราเปิดใช้งานแล้ว คุณสามารถเรียกใช้การทดสอบแบบ end-to-end โดยใช้สคริปต์ npm ที่ให้มา:

>npm run protractor

สคริปต์นี้จะดำเนินการทดสอบแบบ end-to-end กับแอปพลิเคชันที่โฮสต์บนเซิร์ฟเวอร์การพัฒนา
หมายเหตุ: ภายใต้ประทุน Protractor ใช้ [Selenium Standalone Server](https://www.selenium.dev/)ซึ่งจะต้อง ติดตั้ง[Java Development Kit (JDK)](https://en.wikipedia.org/wiki/Java_Development_Kit)บนเครื่องของคุณ ตรวจสอบสิ่งนี้โดยเรียกใช้จากบรรทัดคำสั่ง```java -version```
หากยังไม่ได้ติดตั้ง JDK คุณสามารถดาวน์โหลดได้ที่[นี่](https://www.oracle.com/java/technologies/downloads/)

## Updating AngularJS and other dependencies
เนื่องจากโค้ดและเครื่องมือไลบรารีเฟรมเวิร์ก AngularJS ได้มาผ่านตัวจัดการแพ็คเกจ (เช่น npm) คุณจึงสามารถใช้เครื่องมือเหล่านี้เพื่ออัปเดตการขึ้นต่อกันได้อย่างง่ายดาย เพียงเรียกใช้สคริปต์ที่กำหนดค่าไว้ล่วงหน้า:

>npm run update-deps

การดำเนินการนี้จะเรียก```npm update```และ```npm run copy-libs```ซึ่งจะค้นหาและติดตั้งเวอร์ชันล่าสุดที่ตรงกับช่วงเวอร์ชันที่ระบุในไฟล์```package.json```

หากคุณต้องการอัปเดตการขึ้นต่อกันเป็นเวอร์ชันที่ใหม่กว่าที่ช่วงที่ระบุจะอนุญาต คุณสามารถเปลี่ยนช่วงเวอร์ชันใน```package.json```นั้นแล้วเรียกใช้ได้```npm run update-deps```ตามปกติ

## Loading AngularJS Asynchronously
โปรเจ็กต์ ```PROJECT_Tutorial_Angularjs  ```รองรับการโหลดเฟรมเวิร์กและสคริปต์แอปพลิเคชันแบบอะซิงโครนัส แบบพิเศษ```index-async.html```ได้รับการออกแบบเพื่อรองรับการโหลดรูปแบบนี้ เพื่อให้ใช้งานได้ คุณต้องฉีดชิ้นส่วนของ AngularJS JavaScript ลงในหน้า HTML โครงการมีสคริปต์ที่กำหนดไว้ล่วงหน้าเพื่อช่วยในการดำเนินการนี้:

>npm run update-index-async

การดำเนินการนี้จะคัดลอกเนื้อหาของ```angular-loader.js```ไฟล์ไลบรารีลงในหน้า```index-async.html```  คุณสามารถเรียกใช้ได้ทุกครั้งที่อัปเดตเวอร์ชันของ AngularJS ที่คุณใช้

## Serving the Application Files
แม้ว่า AngularJS จะเป็นเทคโนโลยีฝั่งไคลเอ็นต์เท่านั้น และสามารถสร้างเว็บแอป AngularJS ที่ไม่ต้องใช้เซิร์ฟเวอร์ส่วนหลังได้เลย เราขอแนะนำให้ให้บริการไฟล์โครงการโดยใช้เว็บเซิร์ฟเวอร์ภายในระหว่างการพัฒนาเพื่อหลีกเลี่ยงปัญหาข้อจำกัดด้านความปลอดภัย (แซนด์บ็อกซ์) ในเบราว์เซอร์ การใช้งานแซนด์บ็อกซ์จะแตกต่างกันไปในแต่ละเบราว์เซอร์ แต่มักจะป้องกันไม่ให้สิ่งต่างๆ เช่น คุกกี้, XHR ฯลฯ ทำงานอย่างถูกต้องเมื่อเปิดหน้า HTML ผ่านสคีม ```file://```แทน ```http://```

### Running the App during Development
โปรเจ็กต์นี้ได้รับการ  ```PROJECT_Tutorial_Angularjs  ```กำหนดค่าล่วงหน้าด้วยเว็บเซิร์ฟเวอร์การพัฒนาในพื้นที่ มันเป็นเครื่องมือ Node.js ที่เรียกว่าhttp [-server](https://github.com/http-party/http-server) คุณสามารถเริ่มเว็บเซิร์ฟเวอร์นี้ด้วย```npm start```แต่คุณสามารถเลือกติดตั้งเครื่องมือได้ทั่วโลก

>sudo npm install -g http-server

จากนั้นคุณสามารถเริ่มเว็บเซิร์ฟเวอร์การพัฒนาของคุณเองเพื่อให้บริการไฟล์สแตติกจากโฟลเดอร์ใดก็ได้โดยเรียกใช้:

>http-server -a localhost -p 8000

หรือคุณสามารถเลือกกำหนดค่าเว็บเซิร์ฟเวอร์ของคุณเอง เช่น Apache หรือ Nginx เพียงกำหนดค่าเซิร์ฟเวอร์ของคุณเพื่อให้บริการไฟล์ภายใต้```app/```ไดเร็กทอรี

### Running the App in Production
ขึ้นอยู่กับความซับซ้อนของแอปและโครงสร้างพื้นฐานโดยรวมของระบบ แต่กฎทั่วไปคือสิ่งที่คุณต้องมีในการผลิตคือไฟล์ภายใต้``app/``ไดเร็กทอรี ทุกอย่างอื่นควรละเว้น

แอป AngularJS เป็นเพียงกลุ่มของไฟล์ HTML, CSS และ JavaScript แบบคงที่ซึ่งจำเป็นต้องโฮสต์ไว้ที่ใดที่เบราว์เซอร์สามารถเข้าถึงได้

หากแอป AngularJS ของคุณกำลังพูดคุยกับเซิร์ฟเวอร์แบ็กเอนด์ผ่าน XHR หรือวิธีการอื่นๆ คุณต้องคิดหาวิธีที่ดีที่สุดในการโฮสต์ไฟล์แบบคงที่เพื่อให้สอดคล้องกับนโยบายต้นกำเนิดเดียวกัน หากมี โดยปกติจะทำโดยการโฮสต์ไฟล์โดยเซิร์ฟเวอร์ส่วนหลังหรือผ่านพร็อกซีย้อนกลับเซิร์ฟเวอร์ส่วนหลังและเว็บเซิร์ฟเวอร์

## Continuous Integration
### Travis CI
[Travis CI](https://www.travis-ci.com/)เป็นบริการการรวมอย่างต่อเนื่อง ซึ่งสามารถตรวจสอบ GitHub สำหรับการคอมมิตใหม่กับที่เก็บของคุณและรันสคริปต์ เช่น การสร้างแอปหรือการทดสอบรัน โปรเจ็กต์```PROJECT_Tutorial_Angularjs ```นี้มีไฟล์การกำหนดค่า Travis ```.travis.yml```ซึ่งจะทำให้ Travis ทำการทดสอบของคุณเมื่อคุณกดไปที่ GitHub

คุณจะต้องเปิดใช้งานการผสานรวมระหว่าง Travis และ GitHub ดู เว็บไซต์ [Travis](https://docs.travis-ci.com/user/tutorial/)สำหรับคำแนะนำเกี่ยวกับวิธีการทำเช่นนี้

## Contact
For more information on AngularJS please check out [angularjs.org](https://angularjs.org/). 
>Natkamon Meejaipranee
>Sirirat Mijit
