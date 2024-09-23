尋找無障礙設施 Accessible Facilities Finder
===

> Project for **Microsoft Greater China Engage-Training Program for University Students with Disability**  
> Project Developing Time: Jul 2023 – Aug 2023  
> Developing TooL: Object-detection custom model/TFLite/Android Studio/Google Colab/LabelImg  
> **You can watch the demo video to see our result!**

### Demo Video
[link](https://youtu.be/RyL52ZXPWaQ)

### Group Information
* Team Name: TechnoTinkerers
* Team Members: 傅莉妮 & 郭沛蓉 & 廖安豪

### Project Description
* **Project Introducion**  
    尋找無障礙設施是一個協助使用者更快速辨認無障礙標誌的系統，同時解決使用者以肉眼搜尋時容易遺漏目標的缺點。  
    這個專案將利用圖片（如地圖或樓層圖）上的資訊，找出無障礙設施並標示在相應的位置，以提供更方便和準確的導引。  
    這個專案將有助於提升使用者在尋找無障礙設施時的便利性和效率，同時提供更好的導引功能，讓無障礙設施更易被發現和使用。

* **Project Design**  
    1. 應用程式 (APP)：專案內容為一個 APP 應用，讓使用者使用並進行操作。
    2. 圖片分析：利用系統已預先載入的圖片或使用者透過拍照立即辨識，系統將進行圖片分析，辨識並找出無障礙設施的位置。
    3. 圖片資料處理：系統接受傳入圖片檔案，並進行處理，找出地圖上的無障礙設施並標記在合適的位置上。

* **System Design**
    * Phase 1 —— 使用者選取應用程式內固定的圖片，並進行物件偵測 
        * 圖片庫：在應用程式內儲存固定圖片，並且可以選取圖片進行偵測
        * 機器學習模型：trained object detection model for wheelchair label
        * 介面呈現：在圖片上框選偵測結果，並標示可信度
    
    * Phase 2 —— 使用者拍攝實際畫面，即時處理並偵測照片上的標誌 
        * 相機模式：應用程式開啟裝置鏡頭，捕捉畫面
        * 機器學習模型：trained object detection model for wheelchair label
        * 介面呈現：即時處理拍攝好的照片，框選偵測結果並標示可信度

* **Project Result**  
    雖然從專案主題決定開始到產出最後的成果只有短短不到三周的時間，  
    我們最終仍完成了 app 的初步原型，並可實現 Phase 1 之功能。

    <img alt="image" src="https://imgur.com/eHGXYie.png">

* **Future Goal**
    * 完善 APP 功能
        * “儲存” 功能：將辨識好的結果儲存在相簿裡，因目前辨識完的圖片無法放大，若辨識的圖片解析度太低可能造成使用者觀看困難
        * “上傳圖片” 功能：使用者可從裝置的相簿中直接挑選圖片進行辨識分類
        * “即時偵測” 功能：使用者開啟攝影模式，即可在畫面中看見實時偵測的框選結果
        * “辨識其他無障礙設施” 功能：除了輪椅圖示的無障礙標誌以外，可以新增辨識電梯位置等功能
    * 提高模型辨識準確率
        * 增加訓練集的素材：尋找更多具有無障礙標誌的圖片作為訓練資料
        * 對圖片預先進行處理：包括縮放、旋轉、裁剪等處理，以確保在後續的標示過程中能夠得到適當處理
    * 滿足更多使用者的需求
        * 撰寫可適用於其他系統平台版本：例如 ios 系統等，讓沒有 Android 裝置的使用者也能方便使用
    
    