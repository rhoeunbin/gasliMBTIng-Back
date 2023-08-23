# gasliMBTIng

>  'MBTI는 gaslighting가 아닐까?' 라는 생각에 이름을 gaslighting과 MBTI를 합쳐 `gasliMBTIng`으로 정함
> 
>  gasliMBTIng의 초성을 따 GL을 가운데 로고로 넣고, 16개의 MBTI를 작은 불씨로 표현하여 가스등 주변에 배치

![gaslimbtinglogo](https://github.com/rhoeunbin/gasliMBTIng-Back/assets/108652504/d7047fc7-2cf3-4f7c-89c1-01f904f5e7b5)


## 기획 의도

> 주변 사람들의 MBTI 정보를 손쉽게 저장하고 간편하게 확인할 수 있는 사전과 같은 앱
>
> 

## 기간

- 2022.11.24 ~ 2022.12.15
- 사이트 주소 : https://www.gasliMBTIng.xyz
- 사이트 바로가기

![2  QR](https://user-images.githubusercontent.com/108647524/215270686-87b24f40-b6b0-4eec-a136-900b1ecccf52.png)



## 팀 구성👩🧑

<a href="https://github.com/w00ye0l/gasliMBTIng-Front/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=w00ye0l/gasliMBTIng-Front" />
</a>

| 이름   | 역할 |
| ------ | ---- |
| 이우열 | FE, 팀장 |
| 김현정 | BE      |
| 최준우 | BE      |
| 이상욱 | BE      |
| 노은빈 | BE, PPT |



## 💻기술 스택

  <img src="https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white"> <img src="https://img.shields.io/badge/html5-E34F26?style=for-the-badge&logo=html5&logoColor=white"> <img src="https://img.shields.io/badge/css-1572B6?style=for-the-badge&logo=css3&logoColor=white"> <img src="https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"> 

  <img src="https://img.shields.io/badge/vue.js-4FC08D?style=for-the-badge&logo=vue.js&logoColor=white"> <img src="https://img.shields.io/badge/django-092E20?style=for-the-badge&logo=django&logoColor=white">  <img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white"> <img src="https://img.shields.io/badge/git-F05032?style=for-the-badge&logo=git&logoColor=white">



## ✏DB설계

![1  gas_erd](https://user-images.githubusercontent.com/108647524/215270685-258f8807-16b4-40a6-9f5c-b1d920538b96.png)





## ✨서비스 소개

### 메인페이지

![gasliMBTIng_main](https://github.com/rhoeunbin/gasliMBTIng-Back/assets/108652504/762b65a1-6855-4d22-a2f1-989e5cf631f7)



- 로고의 16개 별은 MBTI의 16가지 성격 유형을 표현했습니다.
- 별 중앙에 있는 가스등은 gaslighting의 유래인, 1944년 영화 <가스등>에서 착안하여 심볼 마크로 지정하였습니다.
- `[MBTI?]`버튼을 누르면 Modal 팝업창이 출력됩니다.
- Modal 팝업창에서는 gasliMBTIng에 대한 설명과 앱 사용에 대해 간단히 설명하고 있습니다.



### 로그인, 회원가입 페이지

![gasliMBTIng_login](https://github.com/rhoeunbin/gasliMBTIng-Back/assets/108652504/0892be4c-ab86-4cf9-aa60-f9edb9d9b142)


- 이메일, 비밀번호로 로그인합니다. 또한 카카오 로그인을 통해 소셜 로그인이 가능합니다.
- 계정이 없다면 `[회원 가입]`을 통해 회원가입이 가능합니다.
- 회원가입은 이메일, 닉네임, 비밀번호, 프로필 사진, 나이, 성별, MBTI 정보를 입력받습니다.
- 계정 인증은 DRF(Django REST work)의 Token 인증을 기반으로 하고 있습니다.
- 회원가입이 이루어지면 사용자에 대해 Token을 발급합니다.
- 이 Token을 발급받은 사용자가 이메일, 비밀번호를 입력하여 로그인하게 되면 서버에게 발급받은 Toekn을 전달함으로써 정당한 사용자임을 인정받습니다.



### MBTI 저장 페이지

![gasliMBTIng_guest](https://github.com/rhoeunbin/gasliMBTIng-Back/assets/108652504/f38a494f-5e4d-48f3-a53d-096b6d53bc57)


- 친구, 가족 등 지인들의 MBTI 정보를 저장할 수 있는 페이지 입니다. 이름, MBTI, 그룹태그를 넣어 저장하고 목록을 생성할 수 있습니다.
- 그룹태크는 기본적으로 주어진 `[추천 인기 그룹 태그]`중 선택하거나, 직접 새로운 그룹태그를 입력하여 생성하고 분류할 수 있습니다.
- 상단의 그룹 태그별 필터 기능을 통해 해당 그룹의 지인들만 조회할 수도 있습니다. 이를 통해 지인들의 MBTI 정보를 관리할 수 있습니다.



### MBTI 정보 페이지

![gasliMBTIng_info](https://github.com/rhoeunbin/gasliMBTIng-Back/assets/108652504/2be885c2-3fd2-4d4a-ae99-adc0751a7640)

- MBTI 정보에서는 MBTI 성격 유형 별 다양한 글을 열람할 수 있도록 한 조회 페이지 입니다.
- MBTI 별 성격 특징을 알려주기도 하며, 다른 MBTI의 사람을 만날 때 주의할 점이나 상대하는 유용한 방법을 안내합니다.
- 정보 게시글을 읽고 나면 하단에 관련 글 링크를 제공하여 열람한 페이지의 MBTI 관련 다른 글에 쉽게 접근할 수 있도록 합니다.
- 게시글을 편리하게 열람할 수 있도록 상단에 분류 버튼을 제공하여 유형별 게시글을 필터하여 필요한 정보만을 볼 수 있도록 합니다.



### 커뮤니티 페이지

![gasliMBTIng_commu](https://github.com/rhoeunbin/gasliMBTIng-Back/assets/108652504/b345db47-22c4-4bb0-8095-290aa880592b)

- 커뮤니티는 사용자 간에 자유롭게 글을 쓰고 의견을 주고 받는 페이지입니다.
- 커뮤니티 글을 작성할 때 글의 유형이 무엇인지 카테고리를 선택하고 본인의 MBTI 정보를 입력하여, 글을 읽는 사람들이 이 글이 어떤 MBTI 사람의 글인지를 쉽게 파악하게 합니다.
- 이미지를 업로드할 수 있어 글을 더욱 재밌게 열람할 수 있고, 글 작성 시점으로부터 시간이 얼마나 경과하였는지 알려줍니다.
- 글을 읽은 사람이 이에 대한 공감으로 댓글을 작성하고 필요할 경우 삭제할 수 있도록 하였습니다.
- 이 때 접속한 사용자가 댓글 쓴 작성자일 경우 `(작성자)`로 표시하여 본인이 작성한 댓글임을 쉽게 알아볼 수 있도록 하였습니다.



### 회원정보, 방명록 페이지

![gasliMBTIng_profile](https://github.com/rhoeunbin/gasliMBTIng-Back/assets/108652504/678d7971-1351-4ede-bc51-6d27a7a50f66)

- 회원정보 페이지에서는 사용자 본인의 정보를 확인하고 편집할 수 있습니다. 또한 로그아웃, 회원탈퇴 버튼을 통해 계정 사용을 중지하거나 계정 삭제를 할 수 있습니다.
- 다른 사용자의 회원정보 페이지에 접근하여 방명록을 쓸 수 있도록 하였습니다.
- 방명록 작성자명은 접속한 계정이 아닌, 사용자가 직접 설정하여 익명으로 작성할 수 있습니다. 또한 본인의 회원정보 페이지에서 다른 사용자가 남긴 방명록을 열람할 수 있습니다.
- MBTI 저장 페이지에서 저장한 친구의 MBTI를 분석하여, 내가 등록한 사람들의 MBTI 분포도를 쉽게 열람할 수 있도록 가로 막대 그래프로 가시화 하였습니다.
