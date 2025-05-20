# Re:catch FE Assignment

## Project Setup

```bash
yarn install
yarn dev
```

## 요구사항

1. **내용:** 회원 목록을 관리할 수 있는 테이블을 만드는 것이 목표입니다.
   1. 회원 하나 하나의 데이터를 **레코드(Record)**라고 부릅니다.
   2. 레코드를 이루고 있는 속성들을 **필드(Field)**라고 부릅니다.
   3. **필드**
      1. 필드는 `type`, `label`, `required` 로 이루어집니다.
      2. `type` 은 `text`, `textarea`, `date`, `select`, `checkbox` 의 다섯 가지 값으로 이루어집니다.
         1. text type 은 20글자 초과 할 수 없습니다.
         2. textarea type 은 50글자 초과 할 수 없습니다.
         3. 위 정책은 커스텀 필드가 추가되어도 유지될 정책입니다.
      3. 회원 레코드에는 총 6개의 `기본 필드`가 존재합니다. type, label, required 순으로 보면 아래와 같습니다.
         1. text, ‘이름‘, true
         2. text, ‘주소‘, false
         3. textarea, ‘메모‘, false
         4. date, ‘가입일‘, true
         5. select, ‘직업‘, false
            1. 개발자
            2. PO
            3. 디자이너
         6. checkbox, ‘이메일 수신 동의’, false
      4. 이후 위 정책들이 적용된 상태로, 사용자가 직접 type, label, required를 설정하여 생성, 수정, 삭제할 수 있는 `커스텀 필드` 기능이 추가될 예정이라고 생각하고, 확장성 있게 코드를 작성해주세요.
   4. **레코드**
      1. 레코드는 필드들의 조합입니다.
      2. 레코드 목록을 테이블 형태로 볼 수 있어야 합니다.
         1. 각 필드가 column으로 제공되어야 합니다.
         2. 필드별로 filtering 할 수 있어야 합니다.
      3. 레코드를 추가할 수 있어야 합니다.
      4. 레코드를 삭제할 수 있어야 합니다.
      5. 레코드를 수정할 수 있어야 합니다.
         1. 레코드를 수정할 때, 필드 타입별로 다른 input이 떠야 합니다.
      6. 초기 레코드는 `이름`, `주소`, `메모`, `가입일`, `직업`, `이메일 수신 동의` 순으로 보면 아래와 같습니다.
         1. John Doe, 서울 강남구, 외국인, 2024-10-02, 개발자, true
         2. Foo Bar, 서울 서초구, 한국인, 2024-10-01, PO, false
   5. **저장 기능**
      1. 개발 서버를 켤 때, `env`로 `STORAGE`를 `in-memory` 또는 `local-storage`로 설정 가능해야 합니다.
      2. `STORAGE`를 `local-storage`로 설정한다면 레코드들이 로컬 스토리지에 저장되어야 합니다. 즉, 개발 서버를 껐다 켜거나 브라우저를 새로고침 해도 데이터가 보존되어야 합니다.

## Project Structure

```bash
src/
├── App.tsx
├── main.tsx
├── index.css
``

## packages

- vite
- react
- antd
- styled-components

##
```
