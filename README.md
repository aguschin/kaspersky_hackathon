Winning solution for Hackathon on Data Analysis from "Kaspersky lab"
https://events.kaspersky.com/hackathon/

Team DMIA [Data Mining In Action]

check out our elective course on Data Mining in MIPT - https://github.com/vkantor/MIPT_Data_Mining_In_Action_2016

Task - multivariate time series classification ("normal" TS vs TS with anomalies) based on Tennessee Eastman Problem http://users.abo.fi/khaggblo/RS/McAvoy.pdf

Detailed task description can be found in README.pdf

Data can be downloaded from https://yadi.sk/d/LzWCsMmo3GvWrt

Brief solution description:

0) Train LSTM to predict timeseries on 10 ticks ahead using "normal" TS as training data. lstm_baseline_nextstep.ipynb
1) Use LSTM to predict all TS from Train and Test and calculate new features based on error amount statistics.
2) Train Xgboost in xgboost_baseline.ipynb (producing xgb_best_4_knn.csv).
3) Train ExtraTrees in extratrees_baseline-window-lstm.ipynb (producing et_window_250_lstm.csv)
4) Train KNN in KNN_baseline.ipynb (producing knn_best.csv and final mixed submission  knn_xgb_et_RANKS_FINAL_002.csv)