# LAB3_OM2M with Postman
## 目標:
    使用Postman分別建立以下Entities
	1. Create a "MY_SENSOR" Application
	2. Create a "DESCRIPTOR" container
	3. Create a "DESCRIPTOR contentInsances"
	4. Create a "DATA" container
	5. Create a "DATA contentInsances"
	6. Create a "Subscription" contact to localhost:1400/monitor

## 作法or步驟:
* Step 1~6
![](https://i.imgur.com/Rdy2X0d.png)
* DATA ContentInstances
![](https://i.imgur.com/1doaK3n.png)
* DESCRIPTOR ContentInstances
![](https://i.imgur.com/J5g2meI.png)
* 6. Subsription contact to localhost:1440/monitor
![](https://i.imgur.com/thnnW6Z.png)


# LAB3_OM2M  GA with Node-red
## 目標:
    使用 node-red 在GSCL分別建立以下 Entities
	1. Create a "MY_SENSOR" Application
	2. Create a "DESCRIPTOR" container
	3. Create a "DESCRIPTOR contentInsances"
	4. Create a "DATA" container
	5. Create a "DATA contentInsances"
	6. 在 GA(node-red) 開啟 /sensorData Server 負責轉傳 data 到 OM2M
	

## 作法or步驟:
![](https://i.imgur.com/tJCf2n5.png)
6. 此處會將Step5的Data包裝成javascript的格式並送到/sensorData

* 此為DATA Container收到來自GA的ContenInstance
![](https://i.imgur.com/8KVAhSZ.png)


# LAB3_OM2M  NA with Node-red
## 目標:
    	

    使用 node-red 在 NSCL 分別建立以下 Entities
	1. Create a "MY_NETWORK_APPLICATION"
	2. Subscribe new contentInsatnace in the   gscl/MYSENSOR/DATA 並儲存
	3. 開啟 /getxmlfile Server 負責讀取先前儲存的資料
    
## 作法or步驟:
![](https://i.imgur.com/YimY42r.png)

2. Subscribe new contentInsatnace in the   gscl/MYSENSOR/DATA 並儲存

![](https://i.imgur.com/biirNv3.png)

* 當有新的ContentInstance，通知localhost:1880/notification

![](https://i.imgur.com/BAQcCM0.png)

* 儲存ContentInstance至notification.xml的結果圖

![](https://i.imgur.com/Wuj2piS.png)



