# Udemy Course - Deep-Learning-with-TensorFlow

### 檔案內容
---
Section 4與5的樣本寫法同(初始皆為亂數產生資料)，可視為同樣本不同寫法完成ML訓練。

1. Section_2內的Excel檔案是用來直觀呈現「學習率」變化對資料的影響。 <br>
2. Section_4內的exercise練習有自己註記的中文解釋，該檔案整體是使用numpy來執行的。  <br>
3. Section_5內的exercise練習"TensorFlow_Minimal_example_All_exercises"有自己註記的中文解釋，該檔案是使用TensorFlow來執行的。  <br>
4. Section_12內的exercise練習"TensorFlow_MNIST_All_Exercises"有自己註記的中文解釋。 <br>
5. Section_13內的exercise練習"TensorFlow_Audiobooks_Preprocessing_with_comments"有自己註記的中文解釋，該檔案是將csv做預處理的步驟。 "TensorFlow_Audiobooks_Machine_Learning_with_comments"則是預處理完後，讀取處理過後的資料內容和訓練測試模型的部分。 <br>
<br>
<br>

### 課程與程式小筆記
---
Ch05說明TensorFlow 1 時便內含keras的使用，而在TensorFlow 2 大幅改善套件的內容，像是刪減掉不常使用的函式、設有簡潔的API等等，且相比scikit-learn更適合使用於類神經網路的處理，scikit-learn則在k-means與隨機森林的表現較佳。而一般機器學習可用numpy套件然後以數學公式的方法實作，TensorFlow就像是將這些數學公式整理寫成新的套件和函式供人呼叫使用。<br>
exercise內kernel_initializer是關於權值初始化的設定，其未來章節與類神經網路的正反項運作有相當的重要性。

Ch06講了一些類神經網路包含active function和正反向傳遞的概念，數學推導可以看bp的pdf或網路查。

Ch08說明overfitting和underfitting，並介紹data set使用上一般會被分為training, validation, test三個部分。validation驗證多是由underfitting逐漸往overfitting邁進，因此當發現validation的loss高於training的loss時(又或者validation下降中的loss突然升高)，應該暫停看看，因為極有可能出現overfitting的情況。若data set太小，可以採cross-validation方式將資料切為[training, validation], [test]兩個部分。

Ch09介紹權重初始化的重要性和xavier初始化，其是希望每一層outputs的標準差都能盡量相等。

Ch10 ①最初說明Stochastic gradient descent是以批次(batch)為單位進行參數的更新，而訓練所抽取的批次樣本是隨機的，其優點在於它相較於GF能更快速的找到最佳解，但可能因為學習率太大使得參數更新幅度過多，反而會遠離最佳解(有點像車開太快開過頭要繞遠路的意思)。再SGD後，課程提到了local與global minimum的狀況，並以Momentum方式尋找global minimum，其原理如同物理上動量的慣性。 ②學習率從大至小，原因與SGD有點類似，加快速度並避免oscillation，超過最佳解。最後簡單說明了AdaGrad和RMSprop兩者能動態改善學習率。最後，③將上述針對weight的Momentum與針對學習率的AdaGrad或RMSprop結合在一起，便是Adam Optimizer。

Ch11 介紹了幾個常見的規一化方式和將資料做編碼轉換的方法：One-hot Encoding與Binary Encoding。前者在在資料類型少時理解上較為直覺，但容易隨著計算造成維度增加，而此時後者反而能以較少的維度進行表示。(https://bigdatafinance.tw/index.php/tech/data-processing/987-2019-08-24-12-55-29)

Ch12 做數字辨識，區分validation和test的不同，validation與test的accuracy相互比較可確保是否有overfitting。

Ch13 做有聲書購買預測。預處理時盡量將預測的target data數量均分，因為數量不對等容易使學習效果不佳，尤其在像是0.9 : 0.1這種情況下均猜某種結果都能有九成準確率了。

Ch14 提供矩陣運算的課程供為學習過的人。

Ch15 總結課程內容並概述CNN與RNN的運作，另外有稍微提及學校課程學到的幾種演算法。

<br>
<br>

#### 語法參考文件
---
keras的基本語法介紹
https://cloud.tencent.com/developer/article/1010815
