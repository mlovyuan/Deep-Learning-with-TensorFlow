# Udemy Course - Deep-Learning-with-TensorFlow

### 檔案內容
---
Section 4與5的樣本寫法同(初始皆為亂數產生資料)，可視為同樣本不同寫法完成ML訓練。

1. Section_2內的Excel檔案是用來直觀呈現「學習率」變化對資料的影響。 <br>
2. Section_4內的exercise練習有自己註記的中文解釋，該檔案整體是使用numpy來執行的。  <br>
3. Section_5內的exercise練習"TensorFlow_Minimal_example_All_exercises"有自己註記的中文解釋，該檔案是使用TensorFlow來執行的。  <br>
<br>
<br>

### 課程與程式小筆記
---
Ch05說明TensorFlow 1 時便內含keras的使用，而在TensorFlow 2 大幅改善套件的內容，像是刪減掉不常使用的函式、設有簡潔的API等等，且相比scikit-learn更適合使用於類神經網路的處理，scikit-learn則在k-means與隨機森林的表現較佳。而一般機器學習可用numpy套件然後以數學公式的方法實作，TensorFlow就像是將這些數學公式整理寫成新的套件和函式供人呼叫使用。<br>
exercise內kernel_initializer是關於權值初始化的設定，其未來章節與類神經網路的正反項運作有相當的重要性。

Ch06講了一些類神經網路包含active function和正反向傳遞的概念，數學推導可以看bp的pdf或網路查。

Ch07說明overfitting和underfitting，並介紹data set使用上一般會被分為training, validation, test三個部分。validation驗證多是由underfitting逐漸往overfitting邁進，當發現validation的loss高於training的loss時，應該暫停看看，因為極有可能出現overfitting的情況。若data set太小，可以採cross-validation方式將資料切為[training, validation], [test]兩個部分。