# YOLOv4、YOLOv7及YOLOv9的發展過程

## 日期
2025年4月1日

## 講者
廖弘源博士

## 題目
YOLOv4、YOLOv7及YOLOv9的發展過程

---

## 心得報告
這次演講主要介紹了YOLO（You Only Look Once）系列模型的發展歷史，從YOLOv4到最新的YOLOv9，展示了物件偵測技術的進步與應用。演講中提到，物件偵測是計算機視覺中至關重要的第一步，並以ImageNet作為例子說明其在2010年成為一個視覺字典的概念。

此外，講者分析了YOLO系列模型的技術細節，包括模型結構的演進、可程式化梯度資訊（Programmable Gradient Information, PGI）以及E-ELAN（Extended Efficient Layer Aggregation Network）技術。這些技術不僅減少了計算量與參數，還提升了學習效率與收斂速度。

在PGI技術中，模型透過減少計算量來維持連結並增加梯度組合，這使得模型在不同的任務中能夠更有效地進行學習。而E-ELAN技術則是透過控制最短與最長梯度路徑來提升學習效率，這對於需要快速收斂的應用場景尤其重要。

講者還討論了YOLO模型的縮放因子（scaling factors），如解析度、深度與寬度，這些因子在設計物件偵測系統時需要仔細考量。

除此之外，講者還強調了設計物件偵測系統時需要考量的基本議題，包括網路架構、特徵整合方法、偵測方法、損失函數、標籤分配方法與訓練方法。這些因素共同決定了模型的最終性能。

---

## YOLO模型的技術背景
YOLO（You Only Look Once）系列模型自其首次推出以來，便因其高效的物件偵測能力而備受矚目。YOLO的核心理念是將整張圖片作為輸入，並通過單一的神經網路一次性完成所有的物件偵測任務。這與傳統的兩階段方法（如R-CNN系列）形成鮮明對比，後者需要先生成候選框再進行分類。

YOLO的技術突破在於其速度與準確度的平衡。從YOLOv1到YOLOv9，每一個版本的更新都在嘗試解決以下幾個核心問題：
1. **準確度的提升**：通過改進網路結構與損失函數，使模型能夠更精確地識別小物件與密集場景中的物件。
2. **速度的優化**：減少計算量與參數，確保模型能夠在低延遲的情況下進行實時偵測。
3. **適應性**：針對不同的應用場景（如醫療影像分析、自動駕駛等），提供靈活的模型縮放與調整方法。

---

## YOLOv4、YOLOv7與YOLOv9的技術比較

### YOLOv4
YOLOv4是YOLO家族中一個重要的里程碑，它引入了多種新技術以提升性能：
- **CSPDarknet53**：作為主幹網路，通過Cross Stage Partial Networks（CSPNet）減少計算冗餘。
- **Mosaic Data Augmentation**：通過拼接多張圖片來增強數據多樣性，提升模型的泛化能力。
- **CIoU損失函數**：改進了邊界框迴歸的準確性，特別是在目標物件重疊較多的情況下。

### YOLOv7
YOLOv7進一步優化了模型的效率與準確度：
- **E-ELAN技術**：改進了特徵聚合方式，允許更深層的網路結構在不增加計算複雜度的情況下提升性能。
- **Dynamic Label Assignment**：在訓練過程中動態分配標籤，解決了正負樣本不平衡的問題。
- **模型壓縮與加速**：通過蒸餾與剪枝技術，實現了輕量化部署。

### YOLOv9
作為最新一代模型，YOLOv9在以下方面進行了重大改進：
- **Programmable Gradient Information（PGI）**：提升了梯度的利用效率，使模型能夠在更少的計算資源下達到更高的準確度。
- **多尺度特徵融合**：改進了特徵金字塔的設計，提高了對不同大小物件的偵測能力。
- **自適應訓練策略**：根據數據集的特性自動調整超參數，減少了手動調參的工作量。

---

## YOLO的應用案例

### 1. 自動駕駛
YOLO模型在自動駕駛中被廣泛應用於偵測行人、車輛、交通標誌等。其實時性使得車輛能夠快速做出反應，避免交通事故。

### 2. 智慧城市
在智慧城市建設中，YOLO模型被用於監控系統，例如車流量統計、違規停車偵測等。這些應用需要高效且準確的物件偵測能力。

### 3. 醫療影像分析
YOLO模型在醫療領域的應用包括腫瘤偵測、細胞計數等。這些應用需要模型具備高準確度，且能夠處理高分辨率的影像。

### 4. 無人機監控
無人機搭載YOLO模型可以用於農業監控（如病蟲害檢測）、災害搜救等場景。其輕量化特性使其適合在資源有限的無人機平台上運行。

---

## YOLO模型的挑戰與未來發展

### 挑戰
1. **小物件偵測**：在高解析度影像中，小物件的偵測仍然是一個挑戰。
2. **多物件場景**：當影像中存在大量物件時，模型的準確性可能下降。
3. **計算資源限制**：在邊緣設備上的部署需要進一步的模型壓縮與優化。

### 未來發展方向
1. **多任務學習**：將物件偵測與其他任務（如語義分割、姿態估計）結合，提升模型的多功能性。
2. **自適應模型架構**：開發能夠根據硬體資源自動調整的模型架構。
3. **強化學習的應用**：利用強化學習技術進一步優化模型的訓練過程與性能。

---

## 參考文獻
1. 'YOLOv9: A Leap Forward in Object Detection Technology' from Ultralytics documentation. Available at: https://docs.ultralytics.com/models/yolov9/  
2. 'YOLO Explained: From v1 to Present' by Viso.ai. Available at: https://viso.ai/computer-vision/yolo-explained/  
3. 'YOLO Object Detection Explained: A Beginner's Guide' by Encord. Available at: https://encord.com/blog/yolo-object-detection-guide/  
4. 'Real-time Object Detection with YOLO: A Comprehensive Guide' by Towards Data Science. Available at: https://towardsdatascience.com/real-time-object-detection-with-yolo-a-comprehensive-guide-7b6a6a5f6c4d  
5. 'Understanding YOLO: From Basics to Advanced' by Analytics Vidhya. Available at: https://www.analyticsvidhya.com/blog/2021/06/understanding-yolo-from-basics-to-advanced/  
6. 'YOLOv4: Optimal Speed and Accuracy of Object Detection' by Alexey Bochkovskiy et al. Available at: https://arxiv.org/abs/2004.10934  
7. 'YOLOv7: Trainable Bag-of-Freebies Sets New State-of-the-Art for Real-Time Object Detectors' by Wong Kin-Yiu et al. Available at: https://arxiv.org/abs/2207.02696  
