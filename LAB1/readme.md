# LAB1_Guess_number(GuessNumber)

## 目標:
	隨機生成一個1~100之間的整數，讓使用者透過textbox輸入要猜測的數字，並且提示遊戲進度。
## 作法or步驟
1. 進入APP中畫面如下

![](https://i.imgur.com/BkHo9w2.png)

2. 可在Textbox中輸入要猜的數字，然後按下**Guess**，若猜錯Label2會顯示Guess wrong，猜對則顯示**Congratulations! You found the number**

![](https://i.imgur.com/FazswCg.png)

3. 按下**Restart**可重新開始







# LAB1_Post_text(檔案名稱)
## 目標:
    將textbox中的文字，經由HTTP POST的方式傳到自己定義的node-red server，並將回傳的response放置到畫面上。

## 作法or步驟:

# LAB1_flow(HttpPostApp)

## 目標:
    接收來自LAB1_POST_text的http request，回傳"Hello"加上收到訊息name
    
## 作法or步驟:
1. UI介面設定

![](https://i.imgur.com/2TpOGYR.png)

2. Web Property設定，需將URL設定成本身電腦IP的位置，不能設定成本機端，因為模擬器算是Remote端，所以需透過IP找到Server的位置

![](https://i.imgur.com/ocgROGk.png)

3. Server端用Node-red實作，檔名為**HttPostAppFlow.txt**

需將此txt檔import進node-red，步驟如下

* 先按右上角的三條橫線會出現這個列表，點選import->Clipboard
![](https://i.imgur.com/Y8Wmp6q.png)

* 將**HttPostAppFlow.txt**的內容貼上格子內即可import成功
![](https://i.imgur.com/PhqfvHH.png)



