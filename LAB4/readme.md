# P76081027 薛閔豪

# 檔案說明:
* GA的Flow為flows_GA
* NA的Flow為flows_NA
* App Inventor2分別為:
    * om2m_lab4.aia
    * om2m_lab4_2.aia

# LAB4_GA with Node-red
## 目標:
    使用 node-red 分別建立以下
	1. Create a "Location_Gateway_Application" Application on OM2M
	2. Create a "DESCRIPTOR" container on OM2M
	3. Create a "DESCRIPTOR contentInsances" on OM2M
	4. Create a "DATA" container on OM2M
	5. Create a "DATA contentInsances" (for testing) on OM2M
    6. Create a http node to forward data to GSCL

## 作法or步驟:  
![](https://i.imgur.com/XCele3h.png)

![](https://i.imgur.com/14C0d25.png)


    
# LAB4_App inventor Sender(om2m_lab4.aia)
## 目標:
    須完成兩個功能
      1.讀取手機(or 模擬器)的location sensor
      2.將其值交給 GA(node-red)
 
## 作法or步驟:  
**操作結果**

![](https://i.imgur.com/Je7edBM.png)
* 需注意框起來的地方要設定成自己電腦的IP，紫色Block為向Server發出訊息
![](https://i.imgur.com/zDEiSpE.png)

       
# LAB4_NA with Node-red
# 目標:
    使用 node-red 建立以下
    1. Create a "Location_Network_Application" Application on OM2M
    2. Subscribe new contentInsatnace in the   gscl/Location_Gateway_Application/DATA  on OM2M and save recive notify
    3. Create a http node to response previously save data
    
## 作法or步驟:  
![](https://i.imgur.com/9dwOUOT.png)
![](https://i.imgur.com/fDFxGay.png)
3.
![](https://i.imgur.com/uEnjXEn.png)

![](https://i.imgur.com/cJuOyfe.png)

    
    
# LAB4_APP Inventor reciver(om2m_lab4_2.aia)
## 目標:
    須完成兩個功能
      1. http get NA(node-red) 上儲存的 data
      2. 將該 data 用來啟動 google map 並顯示位子
      
## 作法or步驟:  
1. get NA Data回傳結果


![](https://i.imgur.com/vX9vjw9.png)

* 處理server回傳的DATA

![](https://i.imgur.com/y7YPG6Q.png)

* 將NA回傳的經緯度Set到GPS上
![](https://i.imgur.com/hNvVhMA.png)
