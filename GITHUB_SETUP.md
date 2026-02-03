# 🚀 GitHub 저장소 만들기 가이드

## Step 1: GitHub에서 저장소 생성

1. **GitHub 접속**
   - https://github.com/new 로 이동
   - (로그인 필요: yunjunchoi 계정)

2. **저장소 설정**
   - **Repository name**: `voice-timer-for-kids`
   - **Description**: `Voice Stopwatch Timer For Kids - PWA 앱`
   - **Public** 선택 (GitHub Pages 무료 사용)
   - ❌ "Initialize this repository..." 체크 **하지 마세요**
   - **Create repository** 클릭

## Step 2: 로컬 파일 업로드

GitHub가 보여주는 명령어 대신, 아래 명령어를 사용하세요:

```bash
cd /home/yjmoltbot/clawd/pwa
git remote add origin https://github.com/yunjunchoi/voice-timer-for-kids.git
git push -u origin main
```

**인증 필요 시:**
- Username: `yunjunchoi`
- Password: Personal Access Token (PAT) 사용
  - https://github.com/settings/tokens 에서 생성
  - 또는 SSH 키 사용

## Step 3: GitHub Pages 활성화

1. 저장소 페이지에서 **Settings** 클릭
2. 왼쪽 메뉴에서 **Pages** 클릭
3. **Source**: Deploy from a branch
4. **Branch**: main / (root)
5. **Save** 클릭

**5분 후 앱이 라이브됩니다!** 🎉

**URL**: https://yunjunchoi.github.io/voice-timer-for-kids

## 📱 완료 후

웹사이트가 활성화되면:
- 핸드폰에서 URL 접속
- 홈화면에 추가
- 앱처럼 사용!

---

## 🔒 인증 간편하게 하기

### 방법 1: Personal Access Token (PAT)

1. https://github.com/settings/tokens 접속
2. **Generate new token (classic)** 클릭
3. Note: `Voice Timer Upload`
4. Expiration: 선택 (예: 90 days)
5. Scopes: `repo` 체크
6. **Generate token**
7. 토큰 복사 (다시 안 보여줌!)
8. git push 시 Password로 사용

### 방법 2: SSH (더 안전)

```bash
# SSH 키 생성 (이미 있으면 스킵)
ssh-keygen -t ed25519 -C "yunjunchoi@github.com"

# 공개 키 복사
cat ~/.ssh/id_ed25519.pub
```

1. https://github.com/settings/keys 접속
2. **New SSH key** 클릭
3. 복사한 공개 키 붙여넣기
4. **Add SSH key**

그 다음:
```bash
cd /home/yjmoltbot/clawd/pwa
git remote set-url origin git@github.com:yunjunchoi/voice-timer-for-kids.git
git push -u origin main
```

---

**준비 완료!** 명령어만 실행하시면 됩니다! 🚀
