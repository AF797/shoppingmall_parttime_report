# shoppingmall_parttime_report

## Employment Period

2023.03.27 ~

--------

## notice

대학교 2학년 수료 후 휴학하여 쇼핑몰 회사에 Parttime을 하였다.

본 글은 Parttime 기간 동안의 업무내용이다.

언어들을 조금만 알아도 구현 가능한 수준이지만 기록용이기에 작성하게 되었다.

--------

## 1. 제품 포장 계산기 시스템 제작

제품을 고객에게 발송하기 위해 제품을 포장하는데 제품별 박스 당 개수가 달라 전부 외우지 않으면 포장에 어려움이 있었다.

제품별로 개수를 정리해둔 엑셀 파일이 있는데 이를 매번 확인하는데 있어 가독성도 떨어지고 번거로움이 있어 프로그램을 제작하게 되었다.

Link : https://github.com/AF797/product_box_calculator

--------

## 2. cafe24 쇼핑몰 커스텀

회사에 코딩을 할 줄 아는 사람이 없어 cafe24에서 기본적으로 제공하여 주는 템플릿을 이용하여 사용하고 있었다.

원하는 방식으로 커스텀을 하고 싶어 하였는데 어려움을 가지고 있는 상태였다.

그러하여 필자가 회사에서 원하는 기능들을 사용할 수 있도록 커스텀을 하여주었다.

아래 사진은 필자가 커스텀 한 사진들이다. 회사의 보안과 필자의 지적재산권으로 인해 코드는 공개하지 않겠다.

Shoppingmall Link : https://kyurimtech.co.kr/

### 2-1 배너

![배너](https://github.com/AF797/shoppingmall_parttime_report/assets/86837707/108d2f4c-9295-48f4-bc65-812c7f375d7c)

기존에는 상단에서부터 최근 본 상품, 웹 최상단 이동, 최하단 이동으로 구성되어 있었다.

이를 최근 본 상품, 문의 및 견적, 공지사항으로 구성시켰다.

문의 및 견적을 누르면 해당 페이지로 이동하고, 모바일일 경우 전화로 연결되게 구현하였다.

### 2-2 상품 진열

![상품진열](https://github.com/AF797/shoppingmall_parttime_report/assets/86837707/652c2709-3889-4ec7-bc90-b6d5003b9ff3)

cafe24에 기본적으로 제공해 주는 템플릿에 한 가지 오류가 있었다.

사진을 보면 이전에는 5열 종대로 정렬할 경우 10개를 등록하면 5열 종대가 해제되고 1열횡대로 표현되는 오류가 있었다.

이를 커스텀 하여서 5열 종대로 정상 작동하도록 하였다.

사진에 이후 부분이 6열 종대인 이유는 회사 디자이너의 요청으로 6열 종대로 표현되게 수정하였다.

또한 최대 등록 개수가 10개였는데 이 또한 커스텀 하여 개수 제한을 제거하였다.

### 2-3 메일 서비스

![mailtest](https://github.com/AF797/shoppingmall_parttime_report/assets/86837707/4f632fd4-5e06-43f9-adfc-a73e36af3ea9)

[2-1](#2-1-배너)에 언급되었던 견적문의를 이용할 때 고객이 글을 작성하면 일일이 홈페이지에 접속하여 작성 유무를 확인해야 하는 번거러움이 있었다.

이를 해결하기위하여 고객이 견적문의에서 게시글을 작성하면 작성 내용과 함께 담당자에게 메일을 보내는 시스템을 구현하였다.

위 사진을 보면 정상 작동하는 것을 확인할 수 있다.
