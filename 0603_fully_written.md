# Future Insights：Harnessing AI and Social Media for Advanced Event and Epidemic Forecasting

## 1. 日期與講者
- **日期**：2025年6月3日  
- **講者**：呂昌田教授

## 2. 主題題目
**利用AI與社群媒體進行時空事件預測**

### 目標：
- 探討如何透過結合監督式與非監督式學習模型，實現精準的事件預測與流行病監測。
- 提供動態關鍵字捕捉技術與多任務學習模型的應用。
- 分析數據稀疏性對模型準確性的影響，並提出解決方案。
- 探討如何應用AI技術於不同地區的異質性數據中。

## 3. 心得
本次演講深入剖析了AI在社群媒體數據中的應用，特別是在即時事件預測與流行病監測方面的突破。

### 重點：
1. **動態查詢擴展 (DQE)** 技術有效提升了新興關鍵字的捕捉能力，能夠即時應對社群媒體中快速變化的話題。
2. **多任務學習 (Multitask Learning)** 模型的設計，解決了數據稀疏性與區域異質性問題，特別是在小型社區數據中的應用效果顯著。
3. 結合監督與非監督模型的融合策略，顯示AI在低數據環境中的強大潛力，並能夠在多樣化的情境下進行事件預測。
4. 案例研究中展示了模型在抗議活動預測中的應用，特別是在小型城市的預測中，模型的準確性令人印象深刻。

## 4. 關鍵字
- **AI應用**：EMBERS模型、Spatiotemporal Events Forecasting  
- **技術**：動態查詢擴展 (Dynamic Query Expansion, DQE)、多任務學習 (Multitask Learning)  
- **數據來源**：社群媒體 (Twitter)、公開數據 (GDELT, W-ICEWS)  
- **挑戰**：數據稀疏性、地區異質性、關鍵字動態變化  
- **模型表現**：CMTFL-II, LASSO, rMTFL  

## 5. 報告重點
### (1) 監督式方法 (Supervised Methods)
- **優點**：
  - 充分利用歷史事件知識，適合大規模訓練集。
  - 能夠提供穩定且高效的預測結果，特別是在數據量充足的情況下。
- **缺點**：
  - 僅限於固定關鍵字，無法捕捉新興事件特徵。
  - 無法適應快速變化的事件或話題，對於動態數據的靈活性較低。

### (2) 非監督式方法 (Unsupervised Methods)
- **優點**：
  - 捕捉即時動態關鍵字，適應社群媒體的實時變化。
  - 能夠處理未知或新興事件，對於無標籤數據的應用效果良好。
- **缺點**：
  - 無法充分利用歷史數據，需結合其他模型提升準確性。
  - 在數據量較少的情況下，模型的穩定性可能受到影響。

### (3) 模型比較
#### One-for-all 模型：
- **優點**：足夠數據訓練單一模型，適合大範圍的事件預測。
- **缺點**：忽略地區特徵差異，可能導致預測結果不夠精確。

#### One-to-one 模型：
- **優點**：考慮每個地區的獨特性，能夠針對特定地區進行精準預測。
- **缺點**：小城市數據不足，忽略地區間的相關性，可能導致預測結果不穩定。

### (4) 模型融合與改進
- **挑戰**：
  - 如何結合監督與非監督模型以提升預測準確性？
  - 如何同時考慮地區特徵與足夠的訓練數據？
- **解決方案**：
  - 靜態與動態特徵結合，調整各地區特徵權重，實現模型的靈活性與準確性。
  - 多任務學習提升跨地區預測準確性，特別是在數據稀疏的地區能夠發揮作用。
  - 引入動態查詢擴展技術，實現對新興關鍵字的快速捕捉與分析。

### (5) 案例研究 (Case Study)
#### 成功案例：
- **小城市抗議活動預測**：該模型能夠成功預測小型社區中的抗議活動，並提供提前警告。
- **動態關鍵字『Misiones』的捕捉**：模型能夠快速識別新興話題，並結合歷史數據進行分析。

#### 模型表現：
- **CMTFL-II** 效果最佳，能夠在不同地區的數據中實現準確預測。
- **LASSO** 與 **rMTFL** 表現良好，特別是在數據量有限的情況下。

## 6. 參考文獻
1. L. Zhao*, F. Chen*, C.T. Lu, R. Ramakrishnan, "Dynamic Theme Tracking in Twitter," IEEE Big Data, 2015.  
2. L. Zhao*, J. Chen, F. Chen, W. Wang, C.T. Lu, R. Ramakrishnan, "SimNest: Social Media Nested Epidemic Simulation via Online Semi-supervised Deep Learning," IEEE ICDM, 2015.  
3. N. Ramakrishnan, P. Butler, S. Muthiah, et al., "Beating the News with EMBERS: Forecasting Civil Unrest using Open Source Indicators," ACM KDD, 2014.  
4. S. Muthiah, P. Butler, R. Khandpur, et al., "EMBERS at 4 years: Experiences operating an Open Source Indicators Forecasting System," ACM KDD, 2016.
