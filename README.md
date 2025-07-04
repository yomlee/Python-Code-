# Python Codes
[Python Basic Notes](Python Basic.md) 
 
# 1. Pandas 자료 구조 

Pandas

    * Pandas: Python 기반 데이터 분석 라이브러리 
    ```
    import pandas as pd 
    ```

자료구조

    * Series: 1차원 자료구조
        ```
        arr = np.arrange(100, 105, 1)
        s = pd.Series(arr, dtype='int32', index=list('가나다라마'))
        ```
    

    * DataFrame: 2차원 자료구조 
        ```
        pd.DataFrame([[1, 2, 3], 
              [4, 5, 6], 
              [7, 8, 9]], 
              columns=['가','나','다'])
        pd.DataFrame({
            'name': ['Kim', 'Lee', 'Park'], 
            'age': [24, 27, 34], 
            'children': [2, 1, 3]
            })
        ```

# 2. 파일 입출력
    
Excel
    * 파일 읽기 
    ```   
    excel = pd.read_excel('data/seoul_transportation.xlsx', sheet_name=None)
    ```
    * 시트 조회
    ```
    excel.keys()
    ```
    * 파일 저장 
    ```
    excel.to_excel('sample1.xlsx', index=False, sheet_name='샘플')
    ```

CSV
    * 파일 읽기
    ```
    df = pd.read_csv('data/seoul_population.csv') 
    ```
    * 파일 저장 
    ```
    df.to_csv('sample.csv', index=False)
    excel.to_csv('sample1.csv', index=False)
    ```

JSON
    * 파일 읽기 
    ```
    df = pd.read_json(url) 
    ```
    * 파일 저장 
    ```
    df.to_json('currency.json')
    ```



