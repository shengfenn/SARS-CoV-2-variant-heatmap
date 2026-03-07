# SARS-CoV-2-variant-heatmap

## 製作動機

剛進實驗室時，老師請我們練習用Adobe Illustrator整理當時出現過的SARS-CoV-2變異株之spike protein突變位點，做出統整的圖。記得當時花不少時間從0開始製作(成果如下圖)，而用來作為reference的WHO突變位點資料也沒有被保存下來。
![圖片替代文字](變異株比較.png)
因此，我好奇是否能利用我較為熟悉的python，從序列比對開始到為比對結果賦予意義，最終製作成比較表。這樣除了能確保資料的可靠性，還能處理較大型、複雜的序列資料。

## 製作流程
- 抓取NCBI中SARS-CoV-2各變異株的spike protein資料
(因NCBI資料龐大，參考瑞士生物資訊研究院所維護的ViralZone提供的[序列編號](https://viralzone.expasy.org/9556))
- 以原始病毒株作為基準，和各序列進行比對
- 為比對結果賦予意義，如deletion、insertion、substitution
- 將結果儲存成dataframe，最後繪製heatmap

## 製作結果
1. 比較圖(此結果僅以5個序列做測試)
![圖片替代文字](mutation_heatmap.png)
2. [程式碼](SARS-CoV-2.ipynb)