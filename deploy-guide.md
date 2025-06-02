# STUDIX 앱 배포 가이드

## 🌐 온라인 배포 옵션

### 1. Vercel + MongoDB Atlas (추천)

#### Frontend 배포 (Vercel)
```bash
# 1. Vercel CLI 설치
npm i -g vercel

# 2. 프론트엔드 배포
cd frontend
vercel

# 3. 도메인 설정 후 배포 완료
```

#### Backend 배포 옵션
**Option A: Render.com**
- 무료 호스팅 가능
- GitHub 연동 자동 배포

**Option B: Railway.app**
- MongoDB 내장 지원
- 간단한 설정

#### Database (MongoDB Atlas)
```bash
# 1. MongoDB Atlas 계정 생성 (무료)
# 2. 클러스터 생성
# 3. 연결 문자열 복사
# 4. 환경변수에 추가
```

### 2. 전체 스택 배포 (Railway)

#### 단계별 가이드
1. **GitHub 리포지토리 생성**
2. **Railway 계정 연결**
3. **환경변수 설정**
4. **자동 배포 완료**

### 3. Docker + Cloud 배포

#### Dockerfile 생성 필요
- 컨테이너화된 배포
- AWS/Google Cloud/Azure 사용 가능

## 🚀 빠른 배포 솔루션

가장 빠르고 무료로 배포할 수 있는 방법을 선택해주세요:

### A. Netlify + Render (무료)
- **Frontend**: Netlify
- **Backend**: Render.com
- **Database**: MongoDB Atlas

### B. Vercel + Railway (무료)
- **Frontend**: Vercel
- **Backend**: Railway
- **Database**: Railway PostgreSQL 또는 MongoDB Atlas

### C. GitHub Pages + Heroku (무료)
- **Frontend**: GitHub Pages
- **Backend**: Heroku
- **Database**: MongoDB Atlas

## 📋 배포 전 준비사항

1. **환경변수 설정**
   ```env
   MONGODB_URI=mongodb+srv://...
   JWT_SECRET=your_secret_key
   NODE_ENV=production
   FRONTEND_URL=https://your-frontend-url.com
   ```

2. **CORS 설정 업데이트**
   ```javascript
   // backend/server.js
   app.use(cors({
     origin: ['http://localhost:5173', 'https://your-frontend-url.com'],
     credentials: true
   }));
   ```

3. **API URL 업데이트**
   ```javascript
   // frontend/src/utils/api.js
   const API_BASE_URL = process.env.NODE_ENV === 'production' 
     ? 'https://your-backend-url.com/api'
     : 'http://localhost:3000/api'
   ```

## 🎯 원하는 배포 방법을 알려주세요!

어떤 방식으로 배포하시겠습니까?
1. **간단한 무료 배포** (Netlify + Render)
2. **고성능 배포** (Vercel + Railway)
3. **커스텀 도메인** (AWS/GCP)
4. **로컬에서만 사용** (현재 상태 유지)

선택해주시면 해당 방법에 맞는 상세한 배포 가이드를 제공해드리겠습니다!