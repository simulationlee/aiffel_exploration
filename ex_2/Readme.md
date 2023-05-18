## 아이펠캠퍼스 온라인4기 피어코드리뷰

- 코더 : 이승한
- 리뷰어 : 최지호

----------------------------------------------

## PRT(PeerReviewTemplate)

- [△] 코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
  - 프로젝트
    - 네. 정상적으로 작동합니다.
    - 주어진 문제(mse 3000 이하, 결과 시각화)를 전부 해결했습니다.
  - 프로젝트2: 아니오.
  
- [O] 주석을 보고 작성자의 코드가 이해되었나요?
  - 네. step별로 나누어져 있어서 문제 해결 과정이 어떤 순서대로 해결되는지 확인하기 쉬웠습니다.
  - 예)  
    ```Python
        # Step 1

        X = diabetes_dataset['data']
        df_X = pd.DataFrame(X, columns = diabetes_dataset['feature_names'] )
        y = diabetes_dataset['target']
        df_y = pd.DataFrame(y)
    ```
  - 코드에 이해가 필요한 부분엔 주석이 있어서 이해할 수 있었습니다.
  - 예)
    ```Python
        # Step 5

        W = np.random.rand(10)
        W = W.reshape(-1,1) #노드와 다른 점
        b = np.random.rand()

        def model(X, W, b):
            predictions = 0
            for i in range(10):
                predictions += X[:, i] * W[i]
            predictions += b
            predictions = predictions.reshape(-1,1)
            return predictions
     ```
        
- [X] 코드가 에러를 유발할 가능성이 있나요?
  - 아니오.
  - 차원이 맞지않아 계산에 오류가 발생할 수 있는 부분을 전부 수정 해주셨습니다.
  - 예)
    ```Python
        # Step 5

        W = np.random.rand(10)
        W = W.reshape(-1,1) #노드와 다른 점
        b = np.random.rand()

        def model(X, W, b):
            predictions = 0
            for i in range(10):
                predictions += X[:, i] * W[i]
            predictions += b
            predictions = predictions.reshape(-1,1)
            return predictions
     ```
  - 예시와 같이 reshape를 통해서 차원의 크기를 전부 맞춰주셨습니다.
  
- [O] 코드 작성자가 코드를 제대로 이해하고 작성했나요? (직접 인터뷰해보기)
  - 네. scatterplot의 결과가 나오는 이유를 설명해주셨습니다.
  - reshape를 사용하는 이유를 자세히 설명해주셨습니다.
    
- [O] 코드가 간결한가요?
  - 네. 이유 없이 선언된 변수나 코드의 중복 등이 없습니다.

----------------------------------------------

## 참고 링크 및 코드 개선
- 코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
- 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.