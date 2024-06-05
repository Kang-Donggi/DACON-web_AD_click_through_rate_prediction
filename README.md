# DACON-web_AD_click_through_rate_prediction
### 개요: 
웹 광고 클릭률 예측 AI 경진대회
### 결과: 
-Tabuler 데이터에서 특정 유저가 광고를 클릭 할 확률 예측<br/> 
-777명 참가자 중 15등으로 대회 마무리


### -실험 주요사항
1. 결측치 대체에 Knn, Datawig를 통한 딥러닝 기반 대체 등 다수 방법 실험하였으나 0으로 대체 했을 때 가장 높은 성능
2. scaling, 다중공선성 등 다수 전처리 방법 사용하였으나 Standard scaler에서만 약간의 효과 확인
3. optuna를 통해 최적의 하이퍼파라미터 탐색에서 높은 성능 향상 확인하였음
4. 모델은 Catboost, XGboost, lightgbm을 사용하여 최적의 파라미터 탐색 후 Stratified K-fold 사용
5. 앙상블 수행 시 일반화 성능에 효과가 있을 것으로 예상하였으나 public에서는 AUC score가 하락하여 단일 모델 XGboost로 최종 제출

