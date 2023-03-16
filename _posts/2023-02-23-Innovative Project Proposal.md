---
layout: post
title: Innovative Project Proposal
author: [Shih-Cheng Chang]
category: [Lecture]
tags: [jekyll, ai]
---

### ESP32 MP3 藍牙無線音樂播放器 MAX98357音訊放大器

---
## 實驗說明：

在這篇將示範打造一個ESP32 MP3 Player 藍牙無線音樂播放器。假若使用ESP32自帶的DAC腳位輸出音頻訊號，你會發現聲音明顯失真，所以我們必須要外掛一個MAX98357 I2S 音訊放大器模組，將音頻數據轉碼為立體聲並輸出。

ESP32藍牙無線音樂播放器，通過藍牙立體聲音訊傳輸規範（A2DP）通訊協定，即可經由手機、平板、電腦等完成播放指定的音樂與調節音量，以及如何播放音樂等功能，無需繁瑣的底層作業，使用簡單方便，穩定可靠。

---
### 系統方塊圖
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Future_Home_companion_robot.png?raw=true)

---
## Design Methodology (設計方法)
* Top-Down Design  ：由上層應用分析再區分出下層個別功能及所需軟硬體設計
* Bottom-Up Design ：由底層軟硬體元件往上組合出上層所需應用功能

---
## Market Analysis (市場分析)
![](https://blog.hubspot.com/hs-fs/hubfs/tam-sam-som.png?width=1200&name=tam-sam-som.png)

---
### TAM of Future Home Products
The Target Market size (TAM) of Future Home Products is the number of household.<br>

---
### Taiwan Households = 8.93M (台灣 9百萬戶）
* [Total number of households in Taiwan from 2010 to 2020(in 1,000s)](https://www.statista.com/statistics/330804/taiwan-national-total-number-of-households/#:~:text=By%20the%20end%20of%202020,households%20in%20the%20previous%20year.)

### Japan Households = 57.2M (日本 5千7百萬戶)
* [Number of Households in Japan](https://www.helgilibrary.com/indicators/number-of-households/japan/) 

### South Korea Households = 19.9M (南韓 2千萬戶)
* [Number of Households in South Korea](https://www.helgilibrary.com/indicators/number-of-households/south-korea/)

---
### American Households = 129.93M (美國 1.3億戶)
* [Number of households in the U.S. from 1960 to 2021(in millions)](https://www.statista.com/statistics/183635/number-of-households-in-the-us/)<br>
* [The average American household consisted of 2.51 people in 2021.](https://www.statista.com/statistics/183648/average-size-of-households-in-the-us/)<br>



<br>
<br>

*This site was last updated {{ site.time | date: "%B %d, %Y" }}.*


