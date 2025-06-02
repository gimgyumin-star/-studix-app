# 🚀 STUDIX 앱 - 간단한 배포 방법들

## 😤 Netlify Drop이 안 될 때 대안들

### 🎯 방법 1: GitHub Pages (추천!)

#### 단계:
1. **GitHub 계정으로 로그인**: https://github.com
2. **새 리포지토리 생성**: "studix-app" 이름으로
3. **파일 업로드**:
   - "Upload files" 클릭
   - `/mnt/c/Users/User/studix-app/frontend/dist/` 폴더 안의 모든 파일을 선택해서 드래그앤드롭
   - 커밋 메시지: "Deploy STUDIX app"
4. **Pages 설정**:
   - Settings → Pages
   - Source: "Deploy from a branch"
   - Branch: "main"
   - Folder: "/ (root)"
   - Save 클릭
5. **링크 생성**: https://username.github.io/studix-app

### 🎯 방법 2: Netlify 파일 업로드

#### Netlify Drop 대신:
1. **Netlify 회원가입**: https://netlify.com
2. **Sites 메뉴**: "Add new site" → "Deploy manually"
3. **파일 선택**: 
   - "index.html" 파일을 개별적으로 드래그
   - "assets" 폴더를 드래그
   - "_redirects" 파일을 드래그
4. **배포 완료**

### 🎯 방법 3: Firebase Hosting

#### 단계:
1. **Firebase 콘솔**: https://console.firebase.google.com
2. **프로젝트 생성**: "studix-app"
3. **Hosting 설정**:
   - "Get started" 클릭
   - Firebase CLI 설치 건너뛰기
   - "Continue to console"
4. **파일 업로드**:
   - "Deploy" → "Upload files"
   - dist 폴더 내용 업로드

### 🎯 방법 4: 로컬 테스트용 링크

```bash
# 로컬에서 서버 실행 (현재 터미널에서)
cd /mnt/c/Users/User/studix-app/frontend
npm run preview
```
→ http://localhost:4173 에서 확인 가능
→ 같은 네트워크의 다른 기기에서도 접속 가능

### 🎯 방법 5: 압축 파일 공유

생성된 파일: `/mnt/c/Users/User/studix-app/frontend/studix-app.tar.gz`

이 파일을:
1. 이메일로 전송
2. 클라우드 드라이브에 업로드
3. 웹 호스팅에 업로드

## 💡 가장 쉬운 방법: GitHub Pages

1. **GitHub에 가입** (무료)
2. **새 리포지토리 생성**
3. **dist 폴더의 모든 파일 업로드**:
   - index.html
   - _redirects
   - assets/ (폴더)
   - vite.svg
4. **Settings → Pages 설정**
5. **5분 후 링크 생성!**

## 🔧 문제 해결

### Netlify Drop이 안 되는 이유들:
- 브라우저 보안 설정
- 폴더 권한 문제
- 파일 크기 제한
- 네트워크 문제

### 해결책:
- **개별 파일 업로드** 시도
- **다른 브라우저** 사용
- **GitHub Pages** 사용 (가장 확실함)

## 🎉 추천 순서

1. **GitHub Pages** (가장 확실하고 무료)
2. **Netlify 개별 파일 업로드**
3. **Firebase Hosting**
4. **로컬 서버 + 네트워크 공유**

어떤 방법을 시도해보시겠습니까?