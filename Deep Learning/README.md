# Deep-Learning
#下載 flowers 資料集，並用深度學習的方法進行「分類」
===
一開始以os.path.join的方式來讀取資料夾中的圖片並分成五類，顏色的部分一開始使用黑白但最後訓練結果不佳(準確率50%左右)因此改為RGB(提升至72.5%)<br>
固定所以圖片的大小為64X64，因所有圖片大小都不盡相同<br>
讀取固定大小後的圖片<br>
打亂所有圖片的排序<br>
將圖片資料以及分類標籤分別存進X,y陣列中<br>
使用pickle模組進行資料的儲存與讀取<br>
將圖片資料標準化<br>
分割訓練集和驗證集，分別為80%訓練20%驗證<br>
建立CNN卷積層，主要參考網路上找到的方法<br>
建立好後開始訓練模型，batch_size跟epochs的數量經過不斷的測試以準確率最高的來使用，由於每次訓練時都會佔CPU100%，所以這邊花了蠻多時間去測試出準確率最高的結果。<br>
畫圖後看出誤差的確有因為訓練次數的增加而減少。<br>
訓練完後進行分類預測<br>
接著以混淆矩陣以及Machine Learning有用到的性能指標進行衡量<br>
題目說印出測試集隨機十筆預測後的結果和正解進行比較，我的想法是我在分割訓練集和驗證集時沒有固定random_state，因此每次重新執行整個程式時都會是隨機的，
然後印出預測結果與正解的前十筆資料進行對比。<br>
最後我試著將訓練模型儲存<br>

