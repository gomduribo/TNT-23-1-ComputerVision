compare base_model, residual_model, bottenlock_model

Resnet에 사용된 기법인 residual_block과 bottenlock_block의 효과를 확인하기 위함

mnist 데이터셋에 작은 규모의 모델들로 학습한 뒤 결과 확인

residual기법을 사용하지 않을 경우 모델의 학습이 원활히 이루어지지 않음을 확인함

총 파라미터가 1500개가 넘지 않는 작은 모델이기에, bottenlock_block의 경우 유의미한 효과를 보지 못함.


이후 'Residual Networks Behave Like Ensembles of Relatively Shallow Networks'

resnet의 residual block들이 앙상블처럼 활동한다는 논문이 있어 직접 실험해봄. 가장 처음 layer1을 제외한, layer2,3,4들을 하나씩 빼보면서 val_score을 구해보았다.

base_model에서 layer를 뺄 때와 달리, residual model은 layer를 skip하였을 때에도 어느 정도의 accuracy를 보여주었다.
