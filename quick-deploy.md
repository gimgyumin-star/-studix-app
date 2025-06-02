# 🚀 STUDIX 앱 즉시 배포하기

## 방법 1: Netlify (Frontend) + Render (Backend) - 5분 배포

### 1단계: Frontend 배포 (Netlify)
```bash
cd frontend
npm run build
# build 폴더가 생성됩니다
```

**Netlify 배포:**
1. https://netlify.com 접속
2. "Sites" → "Deploy manually" 
3. `frontend/dist` 폴더를 드래그앤드롭
4. 즉시 링크 생성! (예: https://amazing-app-123.netlify.app)

### 2단계: Backend 배포 (Render)
1. https://render.com 가입
2. "New Web Service" 클릭
3. GitHub 연동 또는 코드 업로드
4. 환경변수 설정:
   ```
   MONGODB_URI=mongodb+srv://your-connection-string
   NODE_ENV=production
   ```

### 3단계: Database (MongoDB Atlas)
1. https://mongodb.com/cloud/atlas 가입
2. 무료 클러스터 생성
3. 연결 문자열 복사
4. Render 환경변수에 추가

## 방법 2: GitHub Pages (무료, 더 빠름)

### GitHub에 업로드 후 Pages 활성화
```bash
# 1. GitHub 리포지토리 생성
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/username/studix-app.git
git push -u origin main

# 2. GitHub Pages에서 배포
# Settings → Pages → Source: GitHub Actions
```

## 방법 3: Vercel (1분 배포)

```bash
# 1. Vercel CLI 설치
npm i -g vercel

# 2. Frontend 배포
cd frontend
vercel --prod

# 즉시 링크 생성: https://studix-app.vercel.app
```

## 🔥 가장 빠른 방법: 데모 버전

프론트엔드만 먼저 배포하여 UI를 보여줄 수 있습니다:

### Static 버전 배포 (2분)
1. **Mock 데이터로 프론트엔드만 배포**
2. **UI/UX 확인 가능**
3. **나중에 백엔드 연결**

어떤 방법을 선택하시겠습니까?

## 📞 지금 바로 도움이 필요하시면:

1. **GitHub 리포지토리 URL**을 알려주시면 제가 직접 배포 설정을 도와드릴 수 있습니다.

2. **원하는 도메인 이름**이 있으시면 커스텀 도메인으로 설정해드릴 수 있습니다.

3. **무료 vs 유료** 옵션 중 어떤 것을 선호하시는지 알려주세요.

어떤 방법으로 진행하시겠습니까?