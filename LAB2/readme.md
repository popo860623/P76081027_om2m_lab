# LAB2_Get_Sensor_Value(GetSensorValues)
## 目標:
    按下按鈕時，抓取手機上的三種sensor，Accelerometer、OrientationSensor、LocationSensor
# 測試環境
打包成APK檔並在BlueStack上測試
## 作法or步驟:
1. UI介面設定

![](https://i.imgur.com/zYAwdwZ.png)


2. 按下即可得到Sensor Values，如下圖:

![](https://i.imgur.com/fOlyd1m.png)


    
    
# LAB2_Show_Location_on_Google.aia(檔案名稱)
## 目標:
    實現五個功能，1.抓取LocationSensor(GPS) 2.將1中的值傳到node-red顯示 3.讀取server存放的location資料 4(5).將1(3)中的資料用google map定位 

## 作法or步驟:
1. 可以依GetSensorValue得到的值如下，我們會用到經緯度，可先保存起來:

![](https://i.imgur.com/qYAISmR.png)


*  將此值送至node-red

![](https://i.imgur.com/vVvkMCI.png)


2. node-red顯示結果

![](https://i.imgur.com/kpdk5nw.png)


3. 讀取server存放的location資料

從Server端讀取latitude、longtitude，紅框為按鈕及回傳的結果
![](https://i.imgur.com/P1QrV5R.png)


4. 兩個紅框分別為開啟目前位置及根據Server回傳值來定位地圖

![](https://i.imgur.com/FziH0Tg.png)





    
    
    
# LAB2_flow.json(flows.json)
## 目標:
    1.接受來自app的訊息，並回復response，2.回傳在server儲存的location data
    
## 作法or步驟:

1. 接受來自app的訊息並回覆

![](https://i.imgur.com/ad9XzQR.png)

* response是一個function，程式碼如下:
```
msg.payload = "Latitude:"+msg.payload.latitude+",Longtitude:"+msg.payload.longtitude
return msg;
```
目的是為了讀取收到來自app的Payload，解析我們需要的資訊並加以處理成要回覆的Payload

2. 回傳儲存在server端的location

* Server端接收來自app的GET Request並回覆

![](https://i.imgur.com/h981WHf.png)


* Server端設定的location位置

![](https://i.imgur.com/VHfp2NW.png)

* 取得Server的location資訊
![](https://i.imgur.com/FtngkNv.png)
* 回傳結果
![](https://i.imgur.com/N1XMOEN.png)




