# FPGA-Breakout_Clone
使用 Verilog 實作打磚塊遊戲，並在 FPGA 開發板上執行。

## 語言環境
- 語言 : Verilog
- 開發環境 : Quartus 13.1
  
## 照片
<img src="./images/game.jpg" width="300">
  
## 功能說明
a. 七段顯示器顯示累計得分數  
b. LED燈顯示血條  
c. 黃色障礙物來阻擋球  
d. 每打到磚塊得一分  
e. 偶爾出現特殊球（粉紅球），無視障礙物直接打到磚塊  
f. 可手動調整球速  
g. 勝利時顯示 WIN，失敗時顯示 LOSE  
h. 打到磚塊時發出聲音  

## WIN
<img src="./images/win.jpg" width="300">
  
## LOSE
<img src="./images/lose.jpg" width="300">
  
## 使用到的硬體裝置
- 按壓鍵 × 3：左右移動、發射
- 8x8 RGB 顯示器：顯示遊戲畫面
- LED 燈：顯示血量條
- 七段顯示器：顯示累計得分數
- 蜂鳴器：發出碰撞音效
- 指撥開關 × 3：開始、重置、調整速度

## 程式 input/output 說明
- **input**
  - `CLK`：系統時脈，作為除頻器輸入
  - `reset`：重置遊戲狀態（死亡後可重來）
  - `start`：啟動或暫停遊戲
  - `left`：控制板子向左移動
  - `right`：控制板子向右移動
  - `throw`：球在板子上時，發射球
  - `highSpeed`：選擇是否讓球快速移動（ON 為快速移動）

- **output**
  - `led`：用來控制 8x8 RGB LED 顯示器（遊戲畫面輸出）
  - `life`：LED 燈顯示生命條
  - `a, b, c, d, e, f, g`：七段顯示器段選控制
  - `COM`：七段顯示器位選（選擇要顯示的位數）
  - `beep`：蜂鳴器輸出音效
