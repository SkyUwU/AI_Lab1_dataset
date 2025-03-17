# AI_Lab1_dataset
### 資料型態
- .jpg
### 外部來源
- Google圖片搜尋以及圖片對應網站
### 資料數量與組成
共587張，分為三類
  - 亞洲人: 214張
  - 非洲人: 210張
  - 歐美人: 163張
### 資料收集的條件
1. 屬於img
2. class = YQ4gaf (Google搜尋中的圖片大部分的class)
3. src是http開頭，避免收集到Base64編碼的預覽圖
### 資料收集過程
主要是找到python相關爬蟲函式的用法及部分程式，利用電腦執行python程式達到爬蟲的功能，最後收集完成再手動篩選掉部分不適合的圖片，以下是大致的執行步驟。
1. 利用selenium函式庫，到Google圖片搜尋需要的關鍵詞
2. 模擬滾輪操作並將各張圖片的src的url經過篩選後存到設定的list中
3. 利用requests函式庫，到list中的各張圖片的url下載圖片
4. 等到下載三類圖片都結束後，手動將大小過小或是明顯不符合該分類的圖片刪除
### 資料範例
以下是三類照片的範例，手動篩選標準主要是臉的部分不能太小，然後盡量是正臉且沒有太多其他無關的資訊。
- 亞洲人  
  <img src="https://media.licdn.com/dms/image/v2/C4D03AQFvSQfWJqXisw/profile-displayphoto-shrink_200_200/profile-displayphoto-shrink_200_200/0/1656120359929?e=2147483647&v=beta&t=YAUYrDBu_jMijx1vGvyno6bJYO5ZpARwlJzBZW15U4s" width="150">  
- 非洲人  
  <img src="https://encrypted-tbn1.gstatic.com/images?q=tbn:ANd9GcT4pVGwC_-gr6ZBZ3qoDLz28-qREpr-uSQEkGiiwzezSih_JS2c" width="170">  
- 歐美人  
  <img src="https://i1.kknews.cc/ouX896xHpEazZekk6lO3yGSK3fGkTmupjkSUHAg/0.jpg" width="170">  
