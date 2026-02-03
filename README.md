# Voice Stopwatch Timer For Kids - PWA 설치 가이드

## 📱 무료 PWA 버전 (지금 바로 시작!)

### 🍎 iOS (iPhone/iPad) 설치 방법

1. **Safari로 열기**
   - `pwa/index.html` 파일을 Safari로 엽니다
   - 또는 다운로드 후 파일 앱에서 Safari로 열기

2. **홈화면에 추가**
   - 하단 공유 버튼 탭 (박스에서 화살표 나가는 아이콘)
   - 스크롤해서 "홈 화면에 추가" 선택
   - 이름 확인/수정 → "추가" 탭

3. **앱처럼 사용!**
   - 홈화면에 아이콘 생성됨
   - 탭하면 전체화면으로 실행 (브라우저 UI 없음)
   - 오프라인에서도 작동!

### 🤖 Android 설치 방법

1. **Chrome으로 열기**
   - `pwa/index.html` 파일을 Chrome으로 엽니다

2. **자동 설치 프롬프트**
   - 화면 하단에 "홈화면에 추가" 버튼 표시됨
   - 버튼 탭 → "설치" 선택

3. **수동 설치 (프롬프트 안 뜨면)**
   - 우측 상단 ⋮ 메뉴
   - "홈 화면에 추가" 또는 "앱 설치" 선택

4. **앱처럼 사용!**
   - 앱 서랍에 아이콘 추가됨
   - 독립 앱으로 실행
   - 오프라인 작동!

---

## 🌐 웹 서버로 배포 (선택사항)

### 로컬 테스트 (같은 WiFi)

```bash
cd pwa
python3 -m http.server 8080
```

핸드폰에서 접속: `http://[PC_IP]:8080`

### 무료 호스팅 옵션

1. **GitHub Pages** (무료, 추천!)
   - GitHub 저장소 생성
   - `pwa/` 폴더 업로드
   - Settings → Pages → 활성화
   - URL: `https://[username].github.io/[repo-name]`

2. **Netlify** (무료)
   - netlify.com 가입
   - `pwa/` 폴더 드래그 앤 드롭
   - 자동 배포 완료!

3. **Vercel** (무료)
   - vercel.com 가입
   - GitHub 연동 또는 폴더 업로드

---

## 🚀 앱스토어 출시 (나중에)

PWA가 잘 작동하고 사용자가 있으면 앱스토어 출시를 고려하세요.

### 필요한 것

**Apple App Store:**
- Apple Developer 계정: $99/년
- Mac 컴퓨터 (Xcode 필요)
- 심사 기간: 1-3일

**Google Play Store:**
- Google Play Developer 계정: $25 (평생)
- 심사 기간: 몇 시간 ~ 1일

### 변환 도구

**PWA → 네이티브 앱 (자동 변환)**

1. **PWABuilder** (추천, 무료)
   - https://www.pwabuilder.com
   - URL 입력 → Android/iOS 패키지 생성
   - 앱스토어 제출용 파일 다운로드

2. **Capacitor** (더 많은 제어)
   ```bash
   npm install @capacitor/core @capacitor/cli
   npx cap init
   npx cap add ios
   npx cap add android
   ```

---

## ✅ 체크리스트

### PWA 완성 상태
- [x] 오프라인 작동 (Service Worker)
- [x] 설치 가능 (Manifest)
- [x] 반응형 디자인
- [x] 아이콘 (SVG)
- [x] iOS/Android 호환
- [x] 화면 꺼짐 방지
- [x] 음성 지원

### 다음 단계 (선택)
- [ ] 웹 서버 배포 (GitHub Pages 등)
- [ ] 도메인 연결 (선택)
- [ ] 앱스토어 출시 결정

---

## 💡 팁

**무료로 시작:**
1. 파일 직접 공유 (지금 가능!)
2. GitHub Pages 배포 (링크로 공유)
3. 사용자 피드백 수집
4. 인기 있으면 앱스토어 출시 고려

**비용 없이 수백 명이 사용 가능합니다!** 🎉

앱스토어는 "검색되게 하려면" 필요하지만, PWA만으로도 충분히 훌륭한 앱 경험을 제공합니다.

---

## 🆘 문제 해결

**설치 버튼이 안 보여요**
- iOS: Safari의 공유 버튼 사용
- Android: Chrome 메뉴에서 수동 설치

**오프라인이 안 돼요**
- 첫 방문 시 한 번은 인터넷 필요
- 이후 완전 오프라인 작동

**음성이 안 나와요**
- 음량 확인
- 목소리 선택에서 📱 로컬 음성 선택
- 무음 모드 해제

---

**만든 날:** 2026-02-04
**버전:** 1.0.0
**제작:** YJ봇 🤖
