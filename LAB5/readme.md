# P76081027 薛閔豪

# 檔案說明:
* Lab5.aia
* flows.json

# LAB5
## 目標:
    使用任意方法完成以下:
    1. 分別控制 LAMP_0 的開/關、LAMP_1 的開/關、ALL_ON、ALL_OFF 共六個動作
    2. 在 APP 上，顯示當前燈泡的狀態 (主動 or 被動皆可)

## 作法or步驟:  
### 燈泡ON/OFF控制
1. 透過Switch來判斷從手機端發出Post的內容
2. 將欲執行之動作的URL發出Post的Request
    ![](https://i.imgur.com/ZPNijdh.png)
### 從APP取得燈泡目前狀態
1. 在APP端對/LAB5_sub_phone發出POST的Request
2. 分別對OM2M取得LAMP STATUS的URL發出POST
3. 對回傳的XML解析取得燈泡STATUS(True/False)
![](https://i.imgur.com/LXGRitB.png)

4. APP解析從/LAB5_sub_phone的Response並將結果顯示
![](https://i.imgur.com/BTH7nPP.png)

5. 取得結果

![](https://i.imgur.com/qlVLjnF.png)


