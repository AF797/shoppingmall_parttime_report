# shoppingmall_parttime_report

<p align="center">
  <img src="https://img.shields.io/badge/anaconda-44A833?style=flat-for-the-badge&logo=anaconda&logoColor=white"/>
  <img src="https://img.shields.io/badge/Spyder-FF0000?style=flat-for-the-badge&logo=spyderide&logoColor=white"/>
  <img src="https://img.shields.io/badge/Visual Studio Code-3178C6?style=flat-for-the-badge&logo=visualstudio&logoColor=white"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-for-the-badge&logo=javascript&logoColor=white"/>
</p>

## Employment Period

2023.03.27 ~ 2023.09.15 (예정)

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

-------------

### 2-1 배너

![배너](https://github.com/AF797/shoppingmall_parttime_report/assets/86837707/108d2f4c-9295-48f4-bc65-812c7f375d7c)

기존에는 상단에서부터 최근 본 상품, 웹 최상단 이동, 최하단 이동으로 구성되어 있었다.

이를 최근 본 상품, 문의 및 견적, 공지사항으로 구성시켰다.

문의 및 견적을 누르면 해당 페이지로 이동하고, 모바일일 경우 전화로 연결되게 구현하였다.

-------------

### 2-2 상품 진열

![상품진열](https://github.com/AF797/shoppingmall_parttime_report/assets/86837707/652c2709-3889-4ec7-bc90-b6d5003b9ff3)

cafe24에 기본적으로 제공해 주는 템플릿에 한 가지 오류가 있었다.

사진을 보면 이전에는 5열 종대로 정렬할 경우 10개를 등록하면 5열 종대가 해제되고 1열횡대로 표현되는 오류가 있었다.

이를 커스텀 하여서 5열 종대로 정상 작동하도록 하였다.

사진에 이후 부분이 6열 종대인 이유는 회사 디자이너의 요청으로 6열 종대로 표현되게 수정하였다.

또한 최대 등록 개수가 10개였는데 이 또한 커스텀 하여 개수 제한을 제거하였다.

-------------

### 2-3 메일 서비스

![mailtest](https://github.com/AF797/shoppingmall_parttime_report/assets/86837707/4f632fd4-5e06-43f9-adfc-a73e36af3ea9)

[2-1 배너](#2-1-배너)에 언급되었던 견적문의를 이용할 때 고객이 글을 작성하면 일일이 홈페이지에 접속하여 작성 유무를 확인해야 하는 번거러움이 있었다.

이를 해결하기위하여 고객이 견적문의에서 게시글을 작성하면 작성 내용과 함께 담당자에게 메일을 보내는 시스템을 구현하였다.

위 사진을 보면 정상 작동하는 것을 확인할 수 있다.

-------------

### 2-4 상품 상세설명 수정

![상품상세](https://github.com/AF797/shoppingmall_parttime_report/assets/86837707/e7f138db-115d-4457-b1d9-4f06c12fd390)

위 사진처럼 필독사항(주의사항)을 필독사항으로 수정해 달라는 의뢰를 받았다

cafe24에서 수정하려 하니 기능지원을 하지 않는듯 하여 코딩을 이용해서 수정해야 겠다는 생각이 들어 코드를 작성해보았다.

원본 코드는 아래와 같다.

```
<table border="1">
  <caption>{$name} 기본 정보</caption>
    <tbody>
      <tr class="{$item_display|display}">
        <th scope="row">{$item_title}</th>
        <td>{$item_content}</td>
      </tr>
      <tr class="{$item_display|display}">
        <th scope="row">{$item_title}</th>
        <td>{$item_content}</td>
      </tr>
    </tbody>
</table>
```

수정한 코드는 아래와 같다.

```
<table border="1">
  <caption>{$name} 기본 정보</caption>
    <tbody>
      <tr class="{$item_display|display}">
        <th scope="row">{$item_title}</th>
        <td>{$item_content}</td>
      </tr>
      <tr class="{$item_display|display}">
        <th scope="row">{$item_title}</th>
        <script>
          window.onload = function() {
            var itemTitleElements = document.querySelectorAll('.section .infoArea table tbody tr');

            for (var i = 0; i < itemTitleElements.length; i++) {
              var itemTitleElement = itemTitleElements[i].querySelector('th');
              var itemTitle = itemTitleElement.textContent.trim();

              if (itemTitle === "필독사항(주의사항)") {
                itemTitleElement.textContent = "필독사항";
                itemTitleElement.classList.add("important");
              }
            }
          };
        </script>
        <style>
          .important {
            font-size: 14px;
            color: #555555;
          }
        </style>
        <td>{$item_content}</td>
      </tr>
    </tbody>
</table>
```

여기서 한가지 문제점은 window.onload를 사용하다보니 필독사항 부분이 버벅거리면서 수정되는 현상이 생겼다.

이에 대한 부분은 추후에 더 좋은 방법이 있으면 찾을 것이다.

P.S. 알고보니 cafe24에서 직접 세팅한 값들이라 수정할 수 있는 부분이 있다. 의미없는 행동이긴 하였지만 이번 기회에 재미있는 경험을 하였으니 만족한다.

[2-6 쇼핑몰 장바구니 가격표시](#2-6-쇼핑몰-장바구니-가격표시)에 작업을 해보니 onload를 안써도 되는듯 하다. onload를 사용하지 않고 하면 버벅거리는것은 없을것으로 사료된다. (2023-08-24)

-------------

### 2-5 견적서, 거래명세서 날인

cafe24에서 견적서와 거래명세서는 html방식으로 만들어서 출력을 한다.

날인 이미지를 단순 삽입을 하기에는 기본틀이 무너지고 깔끔해지지 않아서 이를 해결하기위해서는 다른 방법을 고민해야 했다.

고민을 하던 중 워터마크가 생각이나 날인을 워터마크 형식으로 삽입해야겠다고 생각했다.

```
// 이미지일 경우
<img src="이미지 링크" alt="Watermark Image" class="watermark">
<style>
.watermark {
  position: absolute;
  top: 50px;
  left: 50px;
  opacity: 0.5;
}
</style>

//cafe24는 {$seal_image} 이런 형식을 많이 사용한다.
<div class="watermark">{$seal_image}</div>
<style>
.watermark {
  position: absolute;
  top: 50px;
  left: 50px;
  opacity: 0.5;
}
</style>
```

이번 기회에 워터마크도 해보았고 재미있었다.

-------------

### 2-6 쇼핑몰 장바구니 가격표시
쇼핑몰에 건드릴 부분이 있는지 돌아다니던 중 장바구니의 가격표시가 이상하다는 것을 느꼈다.

다른 스킨은 어떤지 모르겠으나 근무하고 있는 회사는 아키테이블이라는 스킨을 사용하고 있다.

![11](https://github.com/AF797/shoppingmall_parttime_report/assets/86837707/d7158760-2b35-4c9a-8d01-4f99d87d7b44)

웹을 만진거라고는 HTML, CSS, JS만 간단히 건드려 보았던지라 아래 코드에 {$total_order_price_front}와 같은 형식을 보고 어떤식으로 손봐야할지 감이 안잡혔었다.
```
<div class="total">
    <h3 class="title">결제예정금액</h3>
    <div class="paymentPrice">
        {$total_order_price_front_head}<strong id="{$total_order_price_front_id}">{$total_order_price_front}</strong>{$total_order_price_front_tail}
        <span class="refer {$total_order_price_ref_display|display}">{$total_order_price_back_head}<span id="{$total_order_price_back_id}">{$total_order_price_back}</span>{$total_order_price_back_tail}</span>
    </div>
</div>
```
console.log로 일일이 다 찍어 본 후 형식을 파악해서 아래 사진과 같이 수정했다.

- 수정 전
  
![22](https://github.com/AF797/shoppingmall_parttime_report/assets/86837707/11cf52b3-523b-4fe3-b235-37813f16d2ec)

- 수정 후
  
![33](https://github.com/AF797/shoppingmall_parttime_report/assets/86837707/42f9ceee-e385-4c50-b629-509ae0ea5079)

상상치도 못한 부분에서 이런 황당한 오류를 발견해서 당황스러웠다. 고쳐야 할 다른 부분도 있는지 찾아보아야겠다고 느꼈다.

-------------

## 3. 고객 관리 시스템 제작
이사님께서 고객이 첫 주문인지 아닌지를 알 수 있는 프로그램을 원하셔서 관리할 수 있는 프로그램을 간단하게 만들어보았다.

Link : https://github.com/AF797/User_Management_System

### 구현 영상
![ppap](https://github.com/AF797/shoppingmall_parttime_report/assets/86837707/f3a0d9cb-a764-4ba9-936e-172080e0ca0d)

### Update
추후에 추가적으로 프로그램을 여러개 만들듯하여 종합 시스템을 만들었다. (23.08.04)

![ppap2](https://github.com/AF797/shoppingmall_parttime_report/assets/86837707/747c85bc-8058-4a62-814d-7c83225cbba2)

OCR을 이용하여 주문 양식 작성 기능을 추가하였다. [4. OCR을 이용한 주문 양식 작성](#4-ocr을-이용한-주문-양식-작성)에 내용이 있다. (23.08.07)

![11](https://github.com/AF797/shoppingmall_parttime_report/assets/86837707/69fe0c72-f3c7-4971-9877-2cd2517c37b9)

-------------

## 4. OCR을 이용한 주문 양식 작성
주문량이 꽤 많아져 어떻게 하면 간편하게 할 수 있을까 고민을 하던 중 OCR 기술이 생각나서 시스템을 만들어 보았다.

### 구현 사진

![22](https://github.com/AF797/shoppingmall_parttime_report/assets/86837707/34764225-da2d-4cc6-a461-28eb177dd316)

### Link

https://github.com/AF797/Shopping_mall_OCR

-------------

## 5. Coupang Wing API
이번에는 Coupang Wing API를 사용해서 발주 양식에 맞춰서 txt 파일로 볼 수 있는 시스템을 만들어 보았다.

엄청 간단했던 시스템이라 따로 Git하지 않고, 여기서만 다룰 예정이다.

### 구현 사진

![coupang](https://github.com/AF797/shoppingmall_parttime_report/assets/86837707/7bfeb46d-0757-40ac-b24e-3ea12cd605fc)

개인정보들은 캡쳐를 위해 수기로 블라인더 처리를 하였다.

-------------

## 6. 쇼핑몰 장바구니 가격표시
쇼핑몰에 건드릴 부분이 있는지 돌아다니던 중 장바구니의 가격표시가 이상하다는 것을 느꼈다.

다른 스킨은 어떤지 모르겠으나 근무하고 있는 회사는 아키테이블이라는 스킨을 사용하고 있다.

![11](https://github.com/AF797/shoppingmall_parttime_report/assets/86837707/d7158760-2b35-4c9a-8d01-4f99d87d7b44)

웹을 만진거라고는 HTML, CSS, JS만 간단히 건드려 보았던지라 아래 코드에 {$total_order_price_front}와 같은 형식을 보고 어떤식으로 손봐야할지 감이 안잡혔었다.
```
<div class="total">
    <h3 class="title">결제예정금액</h3>
    <div class="paymentPrice">
        {$total_order_price_front_head}<strong id="{$total_order_price_front_id}">{$total_order_price_front}</strong>{$total_order_price_front_tail}
        <span class="refer {$total_order_price_ref_display|display}">{$total_order_price_back_head}<span id="{$total_order_price_back_id}">{$total_order_price_back}</span>{$total_order_price_back_tail}</span>
    </div>
</div>
```
console.log로 일일이 다 찍어 본 후 형식을 파악해서 아래 사진과 같이 수정했다.

- 수정 전
  
![22](https://github.com/AF797/shoppingmall_parttime_report/assets/86837707/11cf52b3-523b-4fe3-b235-37813f16d2ec)

- 수정 후
  
![33](https://github.com/AF797/shoppingmall_parttime_report/assets/86837707/42f9ceee-e385-4c50-b629-509ae0ea5079)

상상치도 못한 부분에서 이런 황당한 오류를 발견해서 당황스러웠다. 고쳐야 할 다른 부분도 있는지 찾아보아야겠다고 느꼈다.
