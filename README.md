# FPGA-Breackout_Clone
Breakout game clone implemented in Verilog for FPGA

## 語言環境
* 語言 : Verilog
* 開發環境 : Quartus 13.1
## 照片
  ![game](https://user-images.githubusercontent.com/122383629/211610812-e33b9299-2bb5-463a-83ac-d4cdb30b7008.jpg)
## 功能說明
a. 七段顯示器顯示累計得分數 \
b. LED燈顯示血條 \
c. 黃色障礙物來阻擋球 \
d. 每打到磚塊得一分 \
e. 除原本的球之外，會偶爾出現特殊球(粉紅球)無視障礙物直接打到磚塊 \
f. 可手動調整球速 \
g. 勝利時會在8X8 RGB顯示WIN，輸了會顯示LOSE \
h. 打到磚塊會發出聲音 
## WIN
  ![win](https://user-images.githubusercontent.com/122383629/211617781-c5b47757-f7bc-4e7e-bce1-989e95473028.jpg)  
## LOSE
  ![lose](https://user-images.githubusercontent.com/122383629/211617843-0a6da537-8963-4b11-9c34-2dc9f0782a2d.jpg)
## 使用到的傳感器
* 按壓鍵* 3 : 左右移動,發射
* 8X8 RGB 顯示器 : 顯示遊戲畫面
* LED燈 : 血量條
* 七段顯示器 : 顯示累計得分數
* 蜂鳴器 : 發出聲音
* 指撥開關* 3 : 開始,重製,調整速度
## 程式 input/output 說明
* input
  * CLK       : 當作除頻器
  * reset     : 當死掉時,可以重製位置
  * start     : 用來啟動或暫停遊戲
  * left      : 使板子向左移
  * right     : 使板子向右移
  * throw     : 當球在板子上,丟出球
  * highSpeed : 選擇是否讓球快速地移動(on 為快速移動)
* output
  * led : 用來顯示8X8 RGB
  * life : LED燈顯示生命條
  * a,b,c,d,e,f,g : 操作七段顯示器
  * COM : 用來選擇要顯示哪個七段顯示器
  * beep : 蜂鳴器的聲音
