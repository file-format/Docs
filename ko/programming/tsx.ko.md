{
  "date" : "2023-12-28",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "TSX 파일 - React TypeScript 파일 - .tsx 파일이란 무엇이며 어떻게 여나요?",
  "description":"TSX React TypeScript 파일 및 해당 파일을 여는 방법에 대해 알아보세요.",
  "linktitle" : "TSX",
  "menu" : {
    "docs" : {
      "identifier": "programming-ko-tsx",
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-12-28"
}

## TSX 파일이란 무엇입니까?

".tsx" 파일 확장자는 일반적으로 **React** 코드가 포함된 TypeScript 파일과 연결됩니다. **TypeScript는 언어에 정적 타이핑을 추가하는 JavaScript의 상위 집합이며**React는 사용자 인터페이스 구축을 위한 JavaScript 라이브러리입니다**. React와 TypeScript를 함께 작업할 때 개발자는 파일에 TypeScript와 JSX(React의 JavaScript용 구문 확장)가 모두 포함되어 있음을 나타내기 위해 파일에 ".tsx" 확장자를 사용하는 경우가 많습니다.

## TSX 파일 예시

TypeScript를 사용하면 변수, 함수 매개변수 등에 대한 유형을 정의할 수 있습니다. React 구성 요소에 사용되는 소품, 상태 및 기타 변수의 유형을 지정하는 ".tsx" 파일에서 TypeScript 코드를 자주 볼 수 있습니다.

````
// 예: React 구성 요소의 TypeScript 코드
인터페이스 MyComponentProps {
   이름: 문자열;
   나이: 숫자;
}
const MyComponent: React.FC<MyComponentProps> = ({ 이름, 나이 }) => {
   // 여기에 컴포넌트 로직이 있습니다.
   return <div>{name}은(는) {age}세입니다.</div>;
};
````

## JSX(React 구문 확장)

JSX는 React에서 권장하는 JavaScript용 구문 확장입니다. 이는 XML/HTML과 유사하며 UI의 모양을 설명하는 데 사용됩니다.

````
// 예: React 구성 요소의 JSX
const MyComponent: React.FC<MyComponentProps> = ({ 이름, 나이 }) => {
   return <div>{name}은(는) {age}세입니다.</div>;
};
````

".tsx" 파일에는 일반적으로 기능 구성 요소 또는 클래스 구성 요소를 사용하는 React 구성 요소의 정의가 포함됩니다.

````
// 예: ".tsx" 파일의 React 구성요소 정의
const MyComponent: React.FC = () => {
   return <div>안녕하세요, 반응하세요!</div>;
};
````

파일 시작 부분에서 필요한 종속성과 모듈을 가져오는 import 문을 자주 볼 수 있습니다.

````
// 예: ".tsx" 파일의 Import 문
'반응'에서 반응을 가져옵니다;
````

## TSX 파일을 여는 방법은 무엇입니까?

TSX 파일은 일반 텍스트 파일이므로 텍스트 편집기에서 열 수 있습니다. 메모장. 그러나 이는 코딩 파일이며 IDE에서 열 수 있도록 되어 있습니다. 비주얼 스튜디오 코드.