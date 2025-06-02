# 🚀 STUDIX 앱 배포 옵션

## ✅ 빌드 완료!
`frontend/dist` 폴더에 배포용 파일이 생성되었습니다.

## 🌐 즉시 배포 가능한 옵션들

### 1. 📎 Netlify Drop (2분 배포)
1. https://app.netlify.com/drop 접속
2. `frontend/dist` 폴더를 드래그앤드롭
3. 즉시 링크 생성: `https://dreamy-app-123456.netlify.app`

### 2. 🔗 Vercel (1분 배포)
```bash
# Vercel CLI 설치 (한번만)
npm install -g vercel

# 배포
cd frontend
vercel --prod
```
생성되는 링크: `https://studix-app.vercel.app`

### 3. 📄 GitHub Pages (5분 배포)
1. GitHub에 리포지토리 생성
2. 코드 업로드
3. Settings → Pages → Deploy from branch
4. 링크: `https://username.github.io/studix-app`

### 4. 🌍 Surge.sh (30초 배포)
```bash
# Surge 설치
npm install -g surge

# 배포
cd frontend/dist
surge
```

## 🔥 지금 당장 링크를 원한다면:

### 옵션 A: Netlify Drop (가장 쉬움)
1. https://app.netlify.com/drop 에 접속
2. 이 경로의 폴더를 드래그앤드롭: `/mnt/c/Users/User/studix-app/frontend/dist`
3. 2분 후 링크 생성!

### 옵션 B: 로컬 서버로 미리보기
```bash
cd frontend
npm run preview
```
로컬 링크: http://localhost:4173

## 📱 현재 상태
- ✅ 프론트엔드 빌드 완료
- ✅ UI/UX 확인 가능  
- ⚠️ 백엔드 없이 실행 (데모 모드)
- ⚠️ 실제 데이터 저장/불러오기는 백엔드 배포 후 가능

## 🎯 추천 순서
1. **Netlify Drop으로 프론트엔드 먼저 배포** (2분)
2. **UI/UX 확인 및 피드백**
3. **백엔드 배포** (필요시)
4. **실제 데이터 연동**

## 💡 참고사항
- 현재 빌드된 버전은 백엔드 없이도 UI를 확인할 수 있습니다
- AI 챗봇, 캘린더, 대시보드 모든 화면을 볼 수 있습니다
- 실제 데이터 저장은 백엔드 배포 후 가능합니다

어떤 옵션으로 배포하시겠습니까?