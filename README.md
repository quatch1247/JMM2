## 🌐 소개
### '점뭐먹?'은 도렴빌딩을 중심으로, 빌딩 내 및 주변에서 점심 식사하기 좋은 식당들을 추천하는 웹 서비스입니다.
#### 1) 매일 같은 메뉴를 반복하거나 새로운 식당을 찾느라 시간을 낭비하는 일상적인 고민을 덜어줍니다.
#### 2) 도보로 15분 내에 있는 식당들만 추천해, 실질적이고 효율적인 점심식사가 가능합니다.
#### 3) 해당 식당에 대한 리뷰를 제공하여, 다른 사용자들의 의견을 확인할 수 있습니다.
<br/>

## 배포 주소
### link : [배포주소](http://www.myai.kro.kr:8080/gun-1.0.0-BUILD-SNAPSHOT/)

<br/>

## 🛠️ 주요 기능 설명

### 반응형 웹 디자인 적용
- 반응형 웹 디자인을 적용하여, 다양한 디바이스에서 최적의 사용자 경험을 제공합니다.
- 모바일과 데스크탑 환경에서 직관적이고 접근성 높은 UI를 제공합니다.

<table>
<tr>
<td style="padding: 5px;"><img style="height: 400px; width: auto;" alt="mobile_view" src="https://github.com/user-attachments/assets/6a42dcf4-58aa-48f4-881f-be518617ea1f"></td>
<td style="padding: 5px;"><img style="height: 400px; width: auto;" alt="desktop_view" src="https://github.com/user-attachments/assets/5f2f36c5-8ab0-40d8-b819-47536588a775"></td>
</tr>
</table>
<br/>

### 로그인, 회원가입 기능
- 회원가입 페이지에서 닉네임(익명)과 직위, 성별을 선택하여 사용자를 구분합니다.
<table>
<tr>
<td style="padding: 5px;"><img style="height: 400px; width: auto;" alt="login" src="https://github.com/user-attachments/assets/6e605fc8-34de-4368-b8e3-0626d40d79d4"></td>
<td style="padding: 5px;"><img style="height: 400px; width: auto;" alt="register" src="https://github.com/user-attachments/assets/715560f8-e517-4ed6-a505-345896b448a2"></td>
</tr>
</table>
<br/><br/>

### AI 검색
- 자연어 기반 데이터베이스 질의를 통해 사용자의 요구에 가장 적합한 식당이나 메뉴를 추천합니다.
- 사용자의 선택에 따라 메뉴만 추천하거나 메뉴와 식당을 모두 추천할 수 있습니다.

<table>
<tr>
<td style="padding: 5px;"><img style="height: 400px; width: auto;" alt="before_ai_search" src="https://github.com/user-attachments/assets/8789aa13-d95b-485e-9a2e-be04243812f1"></td>
<td style="padding: 5px;"><img style="height: 400px; width: auto;" alt="header_ai_search" src="https://github.com/user-attachments/assets/6257281f-7d82-4744-8d08-d22f3aec95f4"></td>
<td style="padding: 5px;"><img style="height: 400px; width: auto;" alt="loading_ai_search" src="https://github.com/user-attachments/assets/20619b19-b8cd-4f77-abc1-474d8b92702d"></td>
<td style="padding: 5px;"><img style="height: 400px; width: auto;" alt="after_ai_search" src="https://github.com/user-attachments/assets/04bdaec8-87b0-4819-99da-ac5cd437fd2a"></td>
</tr>
</table>
<br/><br/>

- **LangChain SQL 에이전트 기반 데이터베이스 검색**: 자연어를 사용하여 사용자가 원하는 메뉴나 식당을 효율적으로 추천합니다. 이 기술은 사용자가 입력한 자연어 쿼리를 SQL 쿼리로 변환해 데이터베이스에서 직접 데이터를 검색하고, 그 결과를 사용자 친화적인 형태로 제공하는 기능을 포함합니다.
- **복잡한 데이터 처리**: LangChain SQL 에이전트는 데이터베이스의 스키마를 동적으로 분석하여 관련 테이블과 필드를 식별하고, 복잡한 SQL 쿼리도 쉽게 실행할 수 있습니다. 이를 통해 사용자는 SQL을 직접 작성할 필요 없이 자연어로 원하는 정보를 얻을 수 있습니다.
- **응답 최적화**: 결과가 출력된 후, 추가적인 후처리 과정을 통해 데이터베이스 구조나 테이블 언급을 피하고, 사용자에게 더 친숙한 방식으로 정보가 제공되도록 합니다. 또한, 불필요한 데이터는 필터링하여 최종 결과를 다듬습니다.
<br/><br/>

<img width="1299" alt="sqlagent_screenshot2" src="https://github.com/user-attachments/assets/16a6d70a-fd38-4b17-b1a2-4c3a6435f89d">

위의 이미지는 AI 검색 기능이 작동하면서 SQL 에이전트를 통해 데이터베이스와 상호작용하는 과정을 보여줍니다. 자연어 쿼리가 SQL로 변환되어 실행된 결과를 확인할 수 있습니다. 이 기능을 통해 사용자는 복잡한 SQL 쿼리를 이해할 필요 없이, 단순히 질문만으로 필요한 정보를 신속하게 얻을 수 있습니다. 예를 들어, "주변에 괜찮은 라멘집이 있는지 찾아봐줘"와 같은 질문에 대해 특정 식당과 메뉴를 검색하여 찾아주는 방식으로 작동합니다.
<br/><br/>

### 랜덤 추천
- 새로고침 시 무작위로 식당을 추천하며, 음식 이미지, 네이버 지도, 주요 메뉴와 가격, AI 요약 정보 등을 제공합니다.
- 이미지 아래의 '좋아요', '몰라요', '별로예요' 버튼을 선택하면 해당 정보가 저장되며, 이후 동일한 식당이 추천될 때 상태가 유지됩니다.
- 상세보기 버튼을 클릭하면 네이버 지도 링크로 연결되어 더 자세한 메뉴나 위치를 확인할 수 있습니다.
- 랜덤 추천과 도렴빌딩 랜덤 추천에는 댓글 기능이 있으며, 로그인 시 입력한 닉네임과 직위가 표시됩니다. 댓글은 다른 사용자들이 확인할 수 있습니다.

<table>
<tr>
<td style="padding: 5px;"><img style="height: 400px; width: auto;" alt="before_random" src="https://github.com/user-attachments/assets/7a721d91-c728-4c3d-b5d2-826e93a6d180"></td>
<td style="padding: 5px;"><img style="height: 400px; width: auto;" src="https://github.com/user-attachments/assets/66172069-6d6c-4cb5-939f-e8c5ff23b65c"></td>
</tr>
</table>
<br/><br/>

### 도렴빌딩 추천
- 도렴빌딩 건물 지하의 식당들만 추천합니다. 랜덤 추천과 동일한 기능을 제공하나, 추천 식당이 도렴빌딩 내로 한정됩니다.

<table>
<tr>
<td style="padding: 5px;">
    <img style="height: 400px; width: auto;" alt="before_building" src="https://github.com/user-attachments/assets/3708c238-28e1-40d5-a4e5-226b17dc75f0">
</td>
<td style="padding: 5px;">
    <img style="height: 400px; width: auto;" alt="after_building" src="https://github.com/user-attachments/assets/c0aecb3a-8c2c-4de9-95cb-d4e4956a4731">
</td>
</tr>
</table>
<br/><br/>


### 날씨기반 추천
- 기상청의 단기예보 데이터를 API로 받아, 주변 식당 데이터와 종합하여 AI가 날씨에 맞는 음식을 추천합니다. 해당 날씨 정보와 추천 이유도 함께 제공합니다.

<table>
<tr>
<td style="padding: 5px;">
    <img style="height: 400px; width: auto;" alt="before_weather" src="https://github.com/user-attachments/assets/7a272e42-f7f8-428f-8ed7-3799d34006e6">
</td>
<td style="padding: 5px;">
    <img style="height: 400px; width: auto;" alt="after_weather" src="https://github.com/user-attachments/assets/a660d0eb-171b-412e-ab64-dd488ecf1741">
</td>
</tr>
</table>
<br/><br/>


### 좋아요 누른 식당
- 사용자가 랜덤 추천 또는 도렴빌딩 랜덤 추천 페이지에서 '좋아요'를 누른 식당의 리스트를 제공합니다. 식당 이름, 전체 '좋아요' 수, '취소' 버튼을 통해 관리할 수 있습니다.

<table>
<tr>
<td style="padding: 5px;">
    <img style="height: 400px; width: auto;" alt="like_count" src="https://github.com/user-attachments/assets/d33263a6-3b06-4d76-bad9-b4e6e39550c5">
</td>
</tr>
</table>
<br/><br/>

### 식당 선호도 순위
- 전체 사용자 기준으로 상위 10개의 식당을 막대 그래프로 순위별로 보여줍니다. 순위는 '좋아요'에서 '싫어요'를 뺀 숫자로 결정됩니다.
<table>
<tr>
<td style="padding: 5px;">
    <img style="height: 400px; width: auto;" alt="ranking_chart" src="https://github.com/user-attachments/assets/97436c5c-4d16-4691-8ad8-1a07519c6e51">
</td>
</tr>
</table>
<br/><br/>

### Q&A 페이지
- 프로젝트에 대한 자주 묻는 질문들을 정리하여 제공합니다.

<table>
<tr>
<td style="padding: 5px;">
    <img style="height: 400px; width: auto;" alt="qna" src="https://github.com/user-attachments/assets/0f56c0f7-b625-447d-8749-a76f9fd8a971">
</td>
</tr>
</table>
<br/><br/>


### 제보 페이지
- 추천에서 누락된 식당이나 서비스에 대한 피드백을 관리자가 받을 수 있도록 폼 형식을 제공합니다.
<table>
<tr>
<td style="padding: 5px;">
    <img style="height: 400px; width: auto;" alt="report" src="https://github.com/user-attachments/assets/97550eea-c4b5-4f71-9bf1-379b94a733ff">
</td>
</tr>
</table>
<br/><br/>
