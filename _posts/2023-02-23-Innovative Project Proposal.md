---
layout: post
title: Innovative Project Proposal
author: [Shih-Cheng Chang]
category: [Lecture]
tags: [home, ai, auto]

---

## ESP32居家中央自動化控制器

---
### 應用與功能說明
* **主要功能描述**

  這次主要是想打造一個利用ESP32作為中央控制器，使其能自動操控家中所建置的設備，以及監測家中的狀況。本此將著重在以溫度、濕度為主，控制居家相關的設備，並且延伸出自動替植物澆水的功能。也額外增設了播放音樂，可依照天氣來挑選音樂的風格。

  雖然目前的功能不多，但整合了抓取、判斷、操控溫濕度，藉由調整參數，達到自動化的效果。加入遠端控制，除了可以監視家中設備的狀況，也可以依據使用者的喜好、想法，調整設備狀態。

![](https://raw.githubusercontent.com/PinLe1920/MCU-project/c84fba9f09621836e5a78e70c8da1e13084d171c/images/截圖%202023-03-23%20下午6.18.49.png)

* **適用的家居空間**

  依據目前的功能

  1. 智能風扇控制：可以運用在臥室、書房、客廳等。

  2. 自動澆水系統：可以運用在盆栽、花圃、居家小菜園等。

---
### 設計考量與所需相關技術
* **設計注意事項**

  若要能推廣到給予一般大眾能使用。

  首先：手機平台介面要夠簡潔，具有直覺性的操控、視窗畫的介面、圖形化的顯示。

  其次：溫濕度監測設備及自動化設備應具有擴增的能力，需要可以輕易的增加或減少設備。

  最後：穩定性，作為居家中央自動化控制器，需要滿足能長久使用、低故障率的要求。除了硬體之外，軟體建置的穩定性也很重要。

* **所需技術**

  1. 藍牙(Bluetooth)

  2. 無線網路(Wi-Fi)

  3. MAX98357 I2S 音訊放大器模組

  4. 土壤濕度感測模組

  5. 風扇控制驅動模組

  6. DHT11溫濕度模組

  7. App Inventor（手機平台建置）
  
---
### 系統方塊圖
![](https://raw.githubusercontent.com/PinLe1920/MCU-project/59219c268588db5e3df99360f4a28cc20940cc80/images/減肥小妙招-2.jpg)

---

## <補充>
### 設備說明

* **藍牙無線音樂播放器**

  建立ESP32的藍牙無線音樂播放器。假若使用ESP32自帶的DAC腳位輸出音頻訊號，聲音會有明顯失真的，所以我們必須要外掛一個MAX98357 I2S 音訊放大器模組，將音頻數據轉碼為立體聲     並輸出。通過藍牙立體聲音訊傳輸規範（A2DP）通訊協定，即可經由手機、平板、電腦等完成播放指定的音樂與調節音量，以及如何播放音樂等功能。

* **自動澆水澆花系統**

  透過土壤濕度感測器測量土壤濕度，如果太乾燥，就經由繼電器啟動抽水泵，抽水給盆栽，若濕度夠了，就停止供水。隨著時代的進步，自動化已逐漸在社會中廣泛的被使用，然而在現代的社會中人們常常因為工作忙碌，忘了幫植物澆水而導致植物枯萎，疏漏了對植物的照顧。為了能夠讓植物能夠健康的成長，則自動化偵測土壤濕度的澆水系統就是居家的好助手！

* **智能風扇控制**

  風扇模組可通過馬達驅動模組對扇葉的轉速進行調節，也可以透過PWM的輸出訊號來控制調節馬達轉速。

* **氣象站**

  通過無線網絡從openweathermap.org網站上獲取本地的天氣資料，像是天氣、溫度、濕度（甚至是風向、風速、氣壓、月相、日出與日落時間等），作為家中設備狀態調整的參考。也可以透過無線網路傳送天氣資料到手機，呈現在手機的居家中央平台APP上，使操作起來更為直覺。
![](https://raw.githubusercontent.com/PinLe1920/MCU-project/c84fba9f09621836e5a78e70c8da1e13084d171c/images/截圖%202023-03-23%20下午6.18.28.png)
![](https://raw.githubusercontent.com/PinLe1920/MCU-project/c84fba9f09621836e5a78e70c8da1e13084d171c/images/截圖%202023-03-23%20下午6.15.42.png)

* **溫度與溼度感測器**

  連接「DHT11溫溼度模組」讀取DHT11溫溼度模組所測到的溫度、溼度。DHT11是一個結合濕度計和測溫元件量測週遭空氣環境，並與一個高性能八位元單晶片相連接，將所量測到的溫、濕度資料拆解成為數位訊號，再由感測器接腳將資料送出。

---
### 相關知識
* **訊號轉換**

藍牙設備從移動設備接收音樂數據時，是無法通過耳機和揚聲器直接播放。需要輸出DAC訊號，藍牙設備需要通過I2S解碼晶片對這些數據進行解碼。這些音頻訊號的功率非常小，只能驅動耳機等小功率音樂收聽設備。必須使用功放晶片放大這些DAC訊號的功率，才能夠驅動功率相對較大的音樂播放設備，如揚聲器。

![](https://raw.githubusercontent.com/PinLe1920/MCU-project/bc25a87b30b5b982bb993b3686b105094dd4ba68/images/ESP32_10033-2.png)

---
## <參考資料>
[ESP32|米羅科技文創學院]([https://www.runoob.com](https://shop.mirotek.com.tw/category/iot/esp32/))

---
<br>
<br>

*This site was last updated {{ site.time | date: "%B %d, %Y" }}.*
