# Homework #1 - A/B Testing in the Wild

1. Which of the following use cases can you reliably conduct an A/B test? (True/False)

* [x] Frontend person wants to change color of the 'Go' button on a search bar. Will it increase conversion rate?
        
* [ ] The data team created four versions of machine learning model for product recommendations to new users of an app. Which one is the best?

* [ ] Two managers from different factions have Layout A and Layout B for a physical convenience store. Which one should we use?

* [ ] Mr. Rabbito thinks offline stores are the best channel to distribute our products, whereas Ms. Rakko thinks online websites are the way to go. Who is right?
      
* [ ] Your boss wants to add a premium version to your freemium service. Is it a good idea?

* [x] The backend team came up with a new setup that they think will speed up the website load time. Should we implement this change?

* [ ] Kuruma Inc., a car dealer, wants to change the banner on their homepage to see if it will attract more repeated customers. Average time between purchase of the car company is 5 years. How do you know if the banner change has an effect? 

* [ ] Your company undergoes a total revamp of its corporate identity. Is it the right call?

* [X] Elastic ninja at your company wants to show 15 products on the first page of search results instead of 20 products. Should you allow them?

* [ ] Marketing person wants to know who respond better to our ads campaigns between iOS users and Android users. How to tell?

2. What are the metrics you should use for the following A/B tests? Assume that the granularities are: page views and unique visitors.

* Which button colors will make customers find it more easily? clicks / sessions

* Which sets of products on a landing page will make customers more likely to buy? purchases / cookies

* Which types of promotion coupons will be more effective? purchases / cookies

* Which website layouts will attract more customers to click on sign up button? clicks / user-ids (non-logins count as 1 user id)

3. Based on the transaction table below, what are the event-based conversion rate and cohort-based conversion rate of 2020-11? Assume 7-day attribution period. Conversion rate is calculated by purchases / unique users.

| date       | user | event    |
|------------|------|----------|
| 2020-11-01 | A    | visit    |
| 2020-11-01 | A    | purchase |
| 2020-11-05 | B    | visit    |
| 2020-11-13 | B    | visit    |
| 2020-11-30 | C    | visit    |
| 2020-12-05 | C    | purchase |

   event-based แบ่ง journey เป็น  
     ของ A มี 1 journey และ 1 success  
     ของ B มี 2 journey และ 0 success  
     ของ C มี 1 journey และ 0 success  
     event-based conversion rate = 1/3  
   
   cohoet-based แบ่ง journey เป็น  
     ของ A มี 1 journey และ 1 success  
     ของ B มี 2 journey และ 0 success  
     ของ C มี 1 journey และ 1 success  
     cohort-based conversion rate = 2/3  

4. Give 3 examples of values that are usually distributed in the following manner (do not use examples from class):

* Bernoulli/Binomial distributions: เป็นคนถนัดซ้าย, เป็นเพศชาย, นอนน้อยกว่า 6 ชม ในคืนที่ผ่านมา

* Normal/Student t's distribution: แต้มรวมจากทอยลูกเต๋า 3 ลูก, IQ, ไซส์รองเท้า

* Exponential distribution: มูลค่าทรัพย์สินส่วนตัว(สำรวจทุกคนบนโลก), ระยะเวลารอรถเมล์คันต่อไป, ระยะทางที่รถยนต์วิ่งได้ก่อนน้ำมันหมด

* Poisson distribution: จำนวน email ที่ได้รับในช่วง 0:00-6:00, จำนวนอุบัติเหตุทางรถยนต์ใน 1 วันในกรุงเทพ, จำนวนเด็กเกิดใหม่ใน 1 วันในกรุงเทพ

5. Which variables should you control for in an A/B test of the following cases?

* We want to test if SMOKING -> CANCER (Smoking causes cancer) and we know that AGE -> SMOKING and AGE -> CANCER. We should control for AGE.

* We want to test if GUN OWNERSHIP -> CRIMES and we know that GUN OWNERSHIP -> GUN SALES and CRIMES -> GUN SALES. We should control nothing.

* We want to test if CROP BURNING -> LUNG DISEASES and we know that CROP BURNING -> PM2.5 and PM2.5 -> LUNG DISEASES. We should control PM2.5.
