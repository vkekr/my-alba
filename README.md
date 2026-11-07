# 💰 하우머치+ (HowMuch Plus)
> **정기 알바 & 일일·단기 알바 급여 계산기 + 애플 캘린더(.ics) 원클릭 연동 PWA 앱**

기존 '하우머치' 앱의 편리하고 직관적인 카드형 UI를 계승하면서, 하우머치에 없던 **단기·일일알바 전용 관리**와 **iOS 애플 캘린더 자동 동기화 기능**을 완벽하게 탑재한 맞춤형 웹앱입니다.

---

## ✨ 핵심 차별화 기능

1. **일일 / 단기 알바 전용 탭**
   - 행사명, 행사 위치(근무지 장소), 시급/일당, 근무 시간, 메모(복장·담당자 연락처 등) 맞춤 관리
2. **애플 캘린더(iOS Calendar) 원클릭 연동**
   - 근무를 등록하자마자 아이폰 기본 캘린더에 시간, 장소, 예상 일당이 담긴 일정 자동 등록
   - 이번 달 전체 근무 일정을 한 번에 애플 캘린더로 내보내는 일괄 동기화(.ics) 지원
3. **달력(캘린더) 맞춤 4단 보기 모드**
   - `시간+일당`: 기본형 (근무 시간 뱃지 + 하단 예상 일당)
   - `위치+일당`: 근무 장소명과 일당을 한눈에 표시
   - `일당만`: 오늘 번 돈만 깔끔하게 축약 표시
   - `근무시간`: 총 근무 시간 위주 표시
4. **PWA (Progressive Web App)**
   - 아이폰 홈 화면에 추가하면 앱스토어 앱처럼 전체화면으로 매끄럽게 구동
   - 로컬스토리지(LocalStorage) 기반으로 오프라인에서도 데이터 영구 보관

---

## 🚀 1분 깃허브 배포 가이드 (GitHub Pages)

1. GitHub에서 새 Repository를 만듭니다 (예: `howmuch-plus`, Public 설정).
2. 이 폴더의 파일들을 모두 푸시합니다:
   ```bash
   git init
   git add .
   git commit -m "feat: 하우머치+ v1.0.0 출시"
   git branch -M main
   git remote add origin https://github.com/사용자아이디/howmuch-plus.git
   git push -u origin main
   ```
3. GitHub 저장소의 **Settings > Pages** 메뉴로 들어갑니다.
4. **Build and deployment > Branch**를 `main` 브랜치 / `/(root)`로 선택하고 **Save**를 누릅니다.
5. 약 1분 후 `https://사용자아이디.github.io/howmuch-plus` 주소로 전 세계 어디서든 열리는 무료 웹앱이 즉시 배포됩니다!

---

## 📲 아이폰(iOS) 홈 화면에 진짜 앱으로 설치하는 법

1. 아이폰의 **사파리(Safari)** 브라우저로 배포된 웹사이트 주소에 접속합니다.
2. 화면 하단 중앙의 **[공유 버튼] (네모에 위로 향한 화살표 아이콘)**을 탭합니다.
3. 메뉴를 아래로 내려 **[홈 화면에 추가]**를 탭합니다.
4. 이름을 확인하고 우측 상단 **[추가]**를 누르면, 아이폰 바탕화면에 파란색 '하우머치+' 앱 아이콘이 생성됩니다!
5. 이제 앱 아이콘을 터치하면 사파리 주소창 없이 **진짜 앱스토어 앱처럼 전체화면으로 실행**됩니다.

---

## 🍎 추후 애플 앱스토어 정식 출시 가이드 (Capacitor)

이 코드는 표준 웹 기술(HTML5, CSS3, JS)로만 작성되어 있어, **Capacitor**를 사용하면 5분 만에 Xcode iOS 네이티브 앱 프로젝트로 변환할 수 있습니다:

```bash
# 1. Capacitor 초기화
npm init -y
npm install @capacitor/core @capacitor/cli @capacitor/ios
npx cap init "HowMuchPlus" "com.jiwon.howmuchplus" --web-dir .

# 2. iOS 프로젝트 생성
npx cap add ios
npx cap copy

# 3. Xcode에서 열고 앱스토어 빌드
npx cap open ios
```
Xcode에서 개발자 계정으로 아카이브 후 App Store Connect에 업로드하면 정식 앱스토어 출시까지 바로 이어집니다!
