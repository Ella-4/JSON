# JSON 데이터 처리 및 Pandas DataFrame 활용

## 개요

이 프로젝트는 **JSON(JavaScript Object Notation) 데이터의 기본적인 이해부터 시작하여, Python의 `json` 라이브러리를 이용한 데이터 파싱, 그리고 `Pandas` 라이브러리를 활용한 DataFrame 기반의 데이터 분석 및 시각화, 다양한 형태의 JSON 저장 방법**까지 포괄적으로 다룹니다. 실제 센서 데이터를 예시로 사용하여 JSON 데이터의 중첩된 구조를 평면화하고, 필요한 정보를 추출하여 분석에 용이한 형태로 가공하는 실습을 포함합니다.

## 주요 기능

* **JSON 기본 개념 학습:** JSON의 구조, 데이터 타입, 그리고 Python 객체(딕셔너리, 리스트)와의 매핑 관계를 이해합니다.

* **`json` 라이브러리 활용:**

  * `json.load()`: JSON 파일에서 Python 객체로 데이터 로드

  * `json.dump()`: Python 객체를 JSON 파일로 저장

  * `json.loads()`: JSON 문자열을 Python 객체로 변환

  * `json.dumps()`: Python 객체를 JSON 문자열로 변환 (가독성 향상을 위한 `indent` 옵션 포함)

* **`Pandas` DataFrame 활용:**

  * `pd.read_json()`: JSON 파일을 직접 DataFrame으로 읽어오기

  * `pd.json_normalize()`: 중첩된 JSON 구조를 평면화하여 DataFrame으로 변환

  * `df.explode()`: 리스트 형태의 컬럼 데이터를 개별 행으로 분리하여 분석 용이성 증대

  * `df.value_counts()`: 특정 컬럼의 데이터 빈도수 계산

  * `df.to_json()`: DataFrame을 다양한 `orient` 옵션(records, split, index, columns, values, table)을 사용하여 JSON 파일로 저장

* **데이터 분석 및 시각화:** 추출된 데이터를 기반으로 간단한 통계 분석을 수행하고, `matplotlib`을 활용하여 결과를 시각화합니다.

* **실제 데이터 처리:** 자동차 주행 센서 데이터(`parsing_target.json`)에서 GPS 좌표 및 객체 `points` 데이터를 추출하고, 이를 `x`, `y` 좌표로 분리하여 `parsed_points.csv` 파일로 저장합니다.

## 🛠️ 설치 방법

프로젝트를 로컬 환경에서 실행하기 위한 단계별 지침입니다.

1. **리포지토리 클론:**

   ```bash
   git clone [https://github.com/당신의깃허브아이디/Your_JSON_Repo_Name.git](https://github.com/당신의깃허브아이디/Your_JSON_Repo_Name.git)
   cd Your_JSON_Repo_Name
   ```

2. **의존성 설치:**

   * Python 가상 환경 활성화 (권장):

     ```bash
     python -m venv venv
     source venv/bin/activate # macOS/Linux
     # venv\Scripts\activate # Windows
     ```

   * 필요한 Python 라이브러리 설치:

     ```bash
     pip install pandas matplotlib numpy
     ```

     (`json` 라이브러리는 Python 내장 라이브러리이므로 별도 설치가 필요 없습니다.)

## 사용 방법

1. **Jupyter Notebook 실행:**

   * 프로젝트 폴더에서 다음 명령어를 실행하여 Jupyter Notebook을 시작합니다.

     ```bash
     jupyter notebook
     ```

   * 웹 브라우저에서 Jupyter Notebook 인터페이스가 열리면 `JSON 데이터 다루기.ipynb` 및 `JSON 데이터, 데이터프레임.ipynb` 파일을 클릭하여 엽니다.

2. **코드 셀 실행:**

   * 각 노트북 파일 내의 코드 셀을 순서대로 실행하면서 JSON 데이터의 로드, 파싱, 변환, 분석, 시각화, 저장 과정을 직접 확인합니다.

   * 특히 각 노트북의 `[TODO]` 섹션에 있는 코드를 완성하고 실행하여 결과 파일을 생성하는 것을 목표로 합니다.

## 기술 스택

* **언어:** Python

* **라이브러리:** `json` (내장), `pandas`, `matplotlib`, `numpy`

* **환경:** Jupyter Notebook
