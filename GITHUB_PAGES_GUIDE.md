# 🚀 STUDIX GitHub Pages 배포 가이드

## 📋 단계별 진행

### 1단계: GitHub 계정 준비
1. https://github.com 접속
2. 계정이 없다면 "Sign up" 클릭해서 가입
3. 계정이 있다면 로그인

### 2단계: 새 리포지토리 생성
1. 로그인 후 우상단 "+" 버튼 클릭
2. "New repository" 선택
3. 리포지토리 설정:
   - **Repository name**: `studix-app`
   - **Description**: `STUDIX - Smart Schedule Management App`
   - **Public** 선택 (무료 Pages를 위해 필요)
   - **Add a README file** 체크 해제
   - "Create repository" 클릭

### 3단계: 파일 업로드
1. 생성된 리포지토리에서 "uploading an existing file" 링크 클릭
2. 아래 경로의 파일들을 모두 선택:
   ```
   /mnt/c/Users/User/studix-app/frontend/dist/
   ```
   
   **업로드할 파일들**:
   - `index.html` ✅
   - `_redirects` ✅
   - `vite.svg` ✅
   - `assets` 폴더 (전체) ✅

3. 선택한 파일들을 GitHub 페이지로 드래그앤드롭
4. 커밋 메시지: `Deploy STUDIX app`
5. "Commit changes" 클릭

### 4단계: GitHub Pages 설정
1. 리포지토리에서 "Settings" 탭 클릭
2. 좌측 메뉴에서 "Pages" 클릭
3. Source 설정:
   - **Source**: "Deploy from a branch" 선택
   - **Branch**: "main" 선택
   - **Folder**: "/ (root)" 선택
4. "Save" 버튼 클릭

### 5단계: 배포 완료 대기
- 페이지 상단에 배포 상태가 표시됩니다
- 보통 2-5분 정도 소요
- 완료되면 링크가 표시됩니다: `https://username.github.io/studix-app`

## 🎯 예상 결과

배포가 완료되면:
- ✅ STUDIX 로고와 헤더 표시
- ✅ 대시보드 페이지 로드
- ✅ 사이드바 네비게이션 작동
- ✅ 다크모드 토글 작동
- ✅ 캘린더 및 AI 채팅 페이지 접근 가능

## 🐛 문제 해결

### 파일 업로드가 안 될 때:
1. 파일들을 개별적으로 업로드
2. assets 폴더는 먼저 폴더를 만들고 내부 파일들 업로드

### 페이지가 로드되지 않을 때:
1. Settings → Pages에서 링크 확인
2. 몇 분 더 기다리기
3. 브라우저 캐시 삭제 후 재접속

## 📱 완료 후 확인사항

링크가 생성되면:
1. 📊 대시보드 통계 확인
2. 📅 캘린더 네비게이션 테스트
3. 🤖 AI 채팅 "내일 수학 숙제" 입력 테스트
4. 🌙 다크모드 토글 테스트
5. 📱 모바일에서 반응형 디자인 확인

진행하시면서 문제가 있으면 언제든 말씀해주세요!