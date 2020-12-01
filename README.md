[![Work in Repl.it](https://classroom.github.com/assets/work-in-replit-14baed9a392b3a25080506f3b7b6d57f295ec2978f6f33ec97e36a161684cbe9.svg)](https://classroom.github.com/online_ide?assignment_repo_id=3642470&assignment_repo_type=AssignmentRepo)


<h1>報告要包括</h1>

>做法說明

>程式方塊圖與寫法

>畫圖做結果分析

>討論預測值誤差很大的，是怎麼回事？

>如何改進？

<h1>做法說明</h1>
  
    Step1:先帶入所需套件包含Pandas、seaborn、sklearn、xgboost等等
    Step2:使用Google雲端載入CSV檔
    Step3:觀察Data屬性，發現尾巴在右，為右偏態
    Step4:再劃一個分為圖觀察點是否在線上，分析結果有點偏離
    Step5:開始整理Data，將其取log(1+x)進行收斂，收斂之後發現更接近常態分布，分位圖也接近在線上
    Step6:觀察是否有Missing Ratio，經測試為0，並進行
    Step7:觀察skewness特徵並用BOX-COX進行轉換，最後在使用one-hot code
    Step8:使用XGBoost進行訓練，測試之後，並輸出預測的CSV檔
<h1>程式方塊圖與寫法</h1>
![image](https://github.com/MachineLearningNTUT/regression-109318083/blob/main/Diagram.jpg)

<h1>畫圖做結果分析</h1>

    常態分佈的調整，取對數log,特徵相關，
    於code中備註
<h1> 討論預測值誤差很大的，是怎麼回事？ 如何改進？</h1> 
    
    可能需要再疊加Gradient Boosting等其他Model做平均來提升，或是調整Xgboost的參數值
