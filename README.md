# 💰 알바로그 (AlbaLog)
> **정기 알바 & 일일·단기 알바 급여 계산 + 정산일 추적 + 애플 캘린더(.ics) 원클릭 연동 PWA**

정기 알바와 일일·단기 알바를 한 화면에서 관리하는 개인용 급여·정산 플래너입니다.
앱으로 설치하면 홈 화면에서 전체화면으로 실행되고, 근무 데이터는 기기 안(로컬스토리지)에만 저장됩니다.

---

## ✨ 기능

1. **일일 / 단기 알바 전용 탭**
   - 행사명, 행사 위치(근무지), 시급/일당, 근무 시간, 메모(복장·담당자 연락처 등) 맞춤 관리
2. **정산 추적**
   - 근무별 정산 방식(당일 / 익일 / 지정일) 선택
   - 미입금 ↔ 입금완료 원터치 체크, 입금 대기/완료 요약 보드
   - 달력에 입금 예정일 마커 표시
3. **애플 캘린더(iOS Calendar) 연동**
   - 근무를 등록하면 시간·장소·예상 일당이 담긴 일정을 .ics로 내보내 아이폰 기본 캘린더에 등록
   - 이번 달 전체 근무 일정과 입금일을 한 번에 내보내는 일괄 동기화 지원
4. **달력 맞춤 4단 보기 모드**
   - `시간+일당` / `위치+일당` / `일당만` / `근무시간` 전환
5. **PWA (Progressive Web App)**
   - 홈 화면에 추가하면 주소창 없이 전체화면 실행, 오프라인에서도 데이터 유지
   - 데이터는 localStorage에 저장되며 서버로 전송되지 않습니다

---

## 🚀 GitHub Pages 배포

1. GitHub에서 새 Repository를 만듭니다 (Public 설정 시 Pages 무료).
2. 파일을 모두 푸시합니다:
   ```bash
   git init
   git add .
   git commit -m "feat: 알바로그 v2.0"
   git branch -M main
   git remote add origin https://github.com/사용자아이디/my-alba.git
   git push -u origin main
   ```
3. 저장소 **Settings > Pages** 에서 **Build and deployment > Branch** 를 `main` / `/(root)` 로 설정하고 **Save**.
4. 약 1분 후 `https://사용자아이디.github.io/my-alba/` 주소로 접속됩니다.

---

## 📲 아이폰(iOS) 홈 화면에 앱으로 설치하기

1. 아이폰 **사파리(Safari)** 로 배포된 주소에 접속합니다.
2. 하단 **[공유] (네모에 위로 향한 화살표)** 를 탭합니다.
3. 메뉴에서 **[홈 화면에 추가]** 를 탭합니다.
4. 이름을 확인하고 **[추가]** 를 누르면 바탕화면에 '알바로그' 아이콘이 생깁니다.
5. 아이콘을 누르면 사파리 주소창 없이 앱처럼 전체화면으로 실행됩니다.

---

## 🍎 앱스토어 출시 가이드 (Capacitor)

표준 웹 기술(HTML5, CSS3, JS)로만 작성되어 있어 **Capacitor**로 iOS 네이티브 프로젝트 변환이 가능합니다:

```
# 1. Capacitor 초기화
npm init -y
npm install @capacitor/core @capacitor/cli @capacitor/ios
npx cap init "AlbaLog" "com.example.albalog" --web-dir .

# 2. iOS 프로젝트 생성
npx cap add ios
npx cap copy
npx cap open ios
```

`com.example.albalog` 부분은 출시 전에 본인이 소유한 번들 ID(예: 역도메인 형태)로 바꿔 주세요.
Xcode에서 개발자 계정으로 아카이브한 뒤 App Store Connect에 업로드하면 출시까지 이어집니다.
