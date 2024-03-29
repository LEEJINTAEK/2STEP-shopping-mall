# 2STEP 👟

**신발 쇼핑물🛒**

<br />

## 목차

1. [**개발**](#개발)
2. [**컨벤션**](#컨벤션)
3. [**기능 구현 계획**](#기능-구현-계획)
4. [**참조문서**](#참조-문서)

## 개발

<br />

| 이름   | 역할          | 이미지 |
| ------ | ------------- | ------ |
| 임예림 | 기획 팀장, FE | 🐰     |
| 이진택 | FE 팀장, FE   | 🐷     |
| 홍경진 | FE            | 🐶     |

**기술 Stack 💻**

![HTML5](https://img.shields.io/badge/-HTML5-E34F26?&style=flat-square&logo=html5&logoColor=white) <br />
![CSS](https://img.shields.io/badge/-CSS3-1572B6?&style=flat-square&logo=css3&logoColor=white) <br />
![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?&style=flat-square&logo=javascript&logoColor=white)

<br />
<br />

## 컨벤션

### 커밋 컨벤션

<br />

```plaintext
Feat: "로그인 페이지의 로그인 기능 구현"
```

<br />

`'태그:(space)제목'의 형태`

| 태그 이름        | 설명                                                                      |
| :--------------- | :------------------------------------------------------------------------ |
| Feat             | 새로운 기능을 추가할 경우                                                 |
| Fix              | 버그를 고친 경우                                                          |
| Design           | CSS 등 사용자 UI 디자인 변경                                              |
| !BREAKING CHANGE | 커다란 API 변경의 경우                                                    |
| !HOTFIX          | 급하게 치명적인 버그를 고쳐야하는 경우                                    |
| Style            | 코드 포맷 변경, 세미 콜론 누락, 코드 수정이 없는 경우                     |
| Refactor         | 프로덕션 코드 리팩토링                                                    |
| Comment          | 필요한 주석 추가 및 변경                                                  |
| Docs             | 문서를 수정한 경우                                                        |
| Test             | 테스트 추가, 테스트 리팩토링(프로덕션 코드 변경 X)                        |
| Chore            | 빌드 테스트 업데이트, 패키지 매니저를 설정하는 경우(프로덕션 코드 변경 X) |
| Rename           | 파일 혹은 폴더명을 수정하거나 옮기는 작업만인 경우                        |
| Remove           | 파일을 삭제하는 작업만 수행한 경우                                        |

<br />
<br />

## 기능 구현 계획

<br />

**사용자 관련 기능**

1. 회원가입

- 회원가입 폼의 입력 값이 조건에 안 맞을 시 (이메일 형식, 비밀번호와 비밀번호확인의 일치 여부 등) 이를 사용자에게 알려준다.<br />
- 조건에 맞게 입력 후 제출 버튼을 누를 시, 백엔드 서버와 연결되어 회원가입 정보가 db에 저장된다.

2. 로그인

- 로그인 폼의 입력 값이 조건에 안 맞을 시 (이메일 형식이 안 맞거나, 비밀번호가 틀리거나 등) 이를 사용자에게 알려준다.
- 로그인 db에 저장된 정보로 로그인 성공 시, JWT 토큰이 프론트 단(sessionStorage, localStorage 등)에 저장되고,
  다른 페이지(랜딩페이지, 상품페이지 등)로 이동한다.

3. 로그아웃

- 로그아웃 시, 프론트 단에 저장되어 있던 JWT토큰이 제거된다.

4. 사용자 정보 조회 - 사용자는 개인 페이지에서 자신의 회원 정보를 조회할 수 있다.

5. 사용자 정보 수정 - 사용자는 개인 페이지에서 자신의 회원 정보를 수정할 수 있다.

6. 사용자 정보 삭제 - 사용자는 개인 페이지에서 자신의 회원 정보를 삭제(탈퇴)할 수 있다.

7. 관리자 기능 - 관리자 계정이 존재하며, 일반 사용자 계정과 구분된다.

8. 사용자 정보 - db에 사용자의 이메일, 이름, 비밀번호(해쉬화된 문자열), 주소를 저장할 수 있다.

<br />
<br />

**상품(제품) 관련 기능**

1. 카테고리 조회 - 사용자가 카테고리 목록을 화면에서 확인할 수 있다.

2. 카테고리 추가 - 관리자는 관리자 페이지에서, 상품이 속할 카테고리를 추가할 수 있다.

3. 카테고리 수정 - 관리자는 관리자 페이지에서, 상품이 속할 카테고리 관련 데이터 (카테고리 이름 등)를 수정할 수 있다.

4. 카테고리 삭제 - 관리자는 관리자 페이지에서, 상품이 속할 카테고리 관련 데이터를 삭제할 수 있다.

5. 상품 추가 - 관리자는 관리자 페이지에서 상품을 추가할 수 있다.

6. 상품 수정 - 관리자는 관리자 페이지에서 상품 관련 데이터를 수정할 수 있다.

7. 상품 삭제 - 관리자는 관리자 페이지에서 상품 관련 데이터를 삭제할 수 있다.

8. 상품 정보 - 상품은 특정 카테고리에 속해 있다.

9. 상품 목록 - 사용자가 특정 카테고리를 선택할 시, 해당 카테고리에 속한 상품 목록이 화면에 나타난다.

10. 상품 상세 - 사용자가 특정 상품을 선택할 시, 해당 상품의 상세 정보가 화면에 나타난다.

11. 상품 정보 - db에 상품의 이름, 가격, 설명, 제조사를 저장할 수 있다.

<br />
<br />

**장바구니 관련 기능**

1. 장바구니 관련 데이터는 백엔드 데이터베이스가 아닌, 프론트단(localStorage, sessionStorage, indexedDB 등)에서 관리된다.

2. 프론트 단에, 장바구니에 속한 상품 관련 데이터가 저장되어서, 페이지를 새로고침해도 장바구니에 상품들이 그대로 남아 있다.

3. 장바구니 추가 - 사용자는 상품을 장바구니에 추가할 수 있다.

4. 장바구니 수정 - 사용자는 장바구니에 속한 상품의 수량을 수정할 수 있다.

5. 장바구니 전체 삭제 - 사용자는 장바구니에서, 버튼 1번의 클릭으로, 장바구니 상의 전체 상품을 제거할 수 있다.

6. 장바구니 부분 삭제 - 사용자는 장바구니에서, 일부 상품을 골라서 제거할 수 있다.

7. 장바구니 조회 - 사용자는 장바구니에 담긴 상품 목록을 확인할 수 있다.

8. 장바구니 가격 조회 - 사용자는 장바구니에 담긴 상품들의 총 가격을 확인할 수 있다.

<br />
<br />

**주문 관련 기능**

1. 주문 추가 - 사용자는 장바구니에 속한 상품의 수량을 변경할 수 있다.

2. 주문 수정 - 관리자는 사용자의 주문 내역에서 배송 상태를 수정할 수 있다.

3. 주문 수정 - 사용자는 주문 완료 후 배송이 시작되기 전까지 주문 정보를 수정할 수 있다.

4. 주문 완료 - 주문 완료 시, 주문 완료 페이지로 이동한다.

5. 주문 조회

- 사용자는 개인 페이지에서 자신의 주문 내역을 조회할 수 있다.
- 관리자는 관리 페이지에서 사용자들의 주문 내역을 조회할 수 있다.

6. 주문 취소 - 사용자는 개인 페이지에서 자신의 주문 내역을 취소할 수 있다.

7. 주문 삭제 - 관리자는 관리 페이지에서 사용자들의 주문 내역을 삭제할 수 있다.

8. 주문 정보

- db에 배송 상태가 저장된다.
- db에 배송지 정보, 주문 총액, 수령자 이름 및 연락처가 저장된다.

<br />
<br />

## 참조 문서

**bulmaCSS**

> https://bulma.io/documentation/overview/start/#starter-template

<br />

**ICONS Fontawesome**

> https://fontawesome.com/

**JS_References MDN**

> https://developer.mozilla.org/ko/
