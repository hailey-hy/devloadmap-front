# 🪴개발 정원
<img width="500" alt="dev-garden" src="https://user-images.githubusercontent.com/93465128/202973018-d0b7871d-4d14-414a-b80e-2480f6fb7555.png">

- 개발 정원은 예비 개발자들이 개발 공부를 더 재미있게 할 수 있도록 돕는 공부 기록 다이어리입니다.
- 처음 이용 시 사용자는 텅 빈 정원을 받게 되며, 주어진 개발 공부 로드맵을 완료할수록 정원이 채워집니다.
- 🔗 팀 노션페이지: [https://www.notion.so/33c2efa3bb3c4805857ba7d663959c9d](https://www.notion.so/33c2efa3bb3c4805857ba7d663959c9d)
- 🔗 서비스 URL : https://devroadmap.netlify.app



## ****🔧****사용 기술

<img src="https://img.shields.io/badge/React-61DAFB?style=flat&logo=React&logoColor=white"/> <img src="https://img.shields.io/badge/Redux-764ABC?style=flat&logo=Redux&logoColor=white"/> <img src="https://img.shields.io/badge/ES6 JS-F7DF1E?style=flat&logo=JavaScript&logoColor=black"/> <img src="https://img.shields.io/badge/React Bootstrap-7952B3?style=flat&logo=Bootstrap&logoColor=white"/> <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=CSS3&logoColor=white"/>


## ****👊핵심 기능****

- 회원가입, 로그인 기능
- 백엔드/프론트엔드 분야로 구분된 공부 로드맵 선택 및 성취도 입력 기능
- 입력된 성취도에 따라 정원 오브젝트 표시 및 진도율 표시 기능
- 친구 추가 및 친구의 정원 방문 기능
- 친구에게 방명록 남기기 및 내가 받은 방명록 확인 기능

## ****👥**** 팀원 구성
| 전해연 | 양정민 |
| --- | --- |
| 프론트엔드 개발 | 백엔드 개발 |

## ♟트러블 슈팅 및 리팩토링

### 1. **setState()의 상태값 업데이트 오작동**

- 문제 상황
    - POST 요청과 함께 사용된 setState가 제대로 작동하지 않아 상태값 업데이트가 목표 시점보다 늦게 이뤄지는 현상
- 원인 진단
    - setState()는 비동기로 작동하여 처리가 늦어지면 코드가 작성된 순서와 다르게 완료될 수 있음
    - POST 요청도 비동기로 작동되며, setState보다 처리 우선순위가 높으므로 업데이트 시점이 목표 시점과 다를 수 있음
- 해결
    - POST 요청 후 해당 페이지에서 사용자가 더이상 머물지 않으므로, useState로 업데이트된 상태를 가지고 있을 필요가 없다고 판단
    - 따라서 useState를 굳이 사용하지 않고 일반 객체로 만들어 해결

## 🗓 ****개발 기간****

- 2022/7 ~ 2022/10
