compare base_model, residual_model, bottenlock_model
Resnet에 사용된 기법인 residual_block과 bottenlock_block의 효과를 확인하기 위함
mnist 데이터셋에 작은 규모의 모델들로 학습한 뒤 결과 확인

residual기법을 사용하지 않을 경우 모델의 학습이 원활히 이루어지지 않음을 확인함
총 파라미터가 1500개가 넘지 않는 작은 모델이기에, bottenlock_block의 경우 유의미한 효과를 보지 못함.
