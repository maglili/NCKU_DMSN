# NCKU MNSN HW2

電機所 碩一 N26091194 鄧立昌

## 執行說明

使用 Jupyter notebook 或其他支援 IPython 的環境開啟 AprioriAll.ipynb 後，直接執行全部 cell 即可。

最後一個 cell 需要使用者輸入 minimal support，輸入的 minimal support 是佔整體資料的 % 數，若共有100筆資料， minimal support 設定為 2 (%)，則代表為 100 * 0.02 = 20。

**注意**: 若 minimal support 設定太小 < 0.6 (%)， 則本程式執行需要非常久的時間(可能為數小時)。

## 程式說明:

在本程式去除了重複購買的 pattern，也就是說若 sequence = <(12) (12) (12) (12) ... (12)> 這種重複的購買，都將被忽略，最後 sequence  只會被當成 < (12) >，多餘的 element 將被去除，以利於後面的計算。

若不提除，則程式將會找到如 <(12)>、<(12) (12) >、...、<(12) *n> 的 pattern，這將會減緩本程式的執行速度，且並沒提供真正有價值的 pattern。

 ## 輸出結果:

本程式除了在 cell 打印出結果之外，也會在當前的工作目錄輸出 "output.txt"，每個 elemet 使用 "|" 分隔開。

  