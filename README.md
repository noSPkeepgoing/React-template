# React Template 🚀

**React + TypeScript + Vite** 기반의 프로젝트 스타터입니다.  
실전 프로젝트에서 바로 사용할 수 있는 기본 구조와 주요 라이브러리를 포함합니다.

## 주요 패키지 📦

- **React**: ^19.1.0
- **React DOM**: ^19.1.0
- **TypeScript**: ~5.8.3
- **Vite**: ^6.3.5
- **React Router DOM**: ^7.6.2
- **SCSS**: ^1.89.1
- **Axios**: ^1.9.0
- **React Query**: ^5.80.3
- **Zustand**: ^5.0.5
- **ESLint**: ^9.25.0
- **Prettier**: ^3.5.3

## 설치 방법 📦

1. 저장소를 클론.

   ```bash
   git clone <repository-url>
   cd react-template
   ```

2. 의존성을 설치.

   ```bash
   npm install
   ```

3. 개발 서버를 실행.
   ```bash
   npm run dev
   ```

## 폴더 구조 📁

```
src/
├── assets/      # 이미지, 폰트 등 정적 파일
├── components/  # 재사용 가능한 컴포넌트
├── hooks/       # 커스텀 훅
├── pages/       # 페이지 컴포넌트
├── apis/        # API 통신 관련 로직
├── styles/      # 전역 스타일
├── types/       # 타입 정의
└── utils/       # 유틸리티 함수
```

## 라우팅 예시 🛣️

`react-router-dom`을 사용하여 라우팅을 구성.  
_예시로 `Home` 컴포넌트가 `/` 경로에 연결되어 있습니다._

```tsx
// src/App.tsx
import { BrowserRouter, Routes, Route } from 'react-router-dom';
import Home from './pages/home/Home';

function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path='/' element={<Home />} />
      </Routes>
    </BrowserRouter>
  );
}
```

## 스타일링 🎨

SCSS를 사용하여 모듈화된 스타일링을 지원.  
_전역 스타일은 `src/styles` 폴더에서 관리할 수 있습니다._

## API 통신 🌐

Axios를 사용하여 API 통신을 처리.  
_API 관련 로직은 `src/apis` 폴더에서 관리합니다._

## 상태 관리 🔄

- **서버 상태**: React Query를 사용하여 서버 상태를 관리.
- **클라이언트 상태**: Zustand를 사용하여 클라이언트 상태를 관리.

## 개발 가이드 📝

- **파일명**: 컴포넌트는 PascalCase (예: `Home.tsx`), 유틸리티/훅은 camelCase (예: `useAuth.ts`)로 작성.
- **폴더명**: kebab-case를 이용하여 작성 (예: `user-profile`, `api-services`).
- **컴포넌트**: 함수형 컴포넌트를 사용하며, Props는 인터페이스로 정의합니다.
- **변수/함수**: camelCase로 작성.
- **타입**: 인터페이스는 I 접두사 없이 사용, 목적을 명확히 표현 (예: `UserDto`, `ApiResponse`), enum은 단수형으로 작성 (예: `UserRole`)
