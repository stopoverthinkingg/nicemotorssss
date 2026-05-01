# 나이스모터스 프로젝트 (Nice Motors)

## 프로젝트 개요
청주 엑스포매매단지 **손영준 실장**의 중고차 개인 딜러 웹사이트.
유튜버 스타일 랜딩페이지 + 실시간 매물 앱 구조.

## 담당자 정보
- **이름**: 손영준 실장
- **상호**: 나이스모터스 (Nice Motors)
- **전화**: 010-4561-9599
- **카카오 비즈니스 채널**: http://pf.kakao.com/_YtXCX/chat
- **위치**: 청주 엑스포매매단지

## 기술 스택
- **프론트엔드**: 순수 HTML/CSS/JS (단일 파일)
- **백엔드**: Supabase (DB + Auth)
- **배포**: Vercel (GitHub 연동 자동 배포)
- **GitHub**: https://github.com/stopoverthinkingg/nicemotorssss
- **Vercel 사이트**: https://nicemotors.vercel.app
- **GitHub Pages**: https://stopoverthinkingg.github.io/nicemotorssss/

## Supabase 설정
- **Project URL**: https://ormjkxizgqyusdfkzibb.supabase.co
- **테이블**: `cars` (매물 데이터)
- **컬럼**: id, cartype, name, year, yearnum, km, kmnum, color, price, pricenum, phone, notes, dealer, extra, photos, regdate, regts

## 파일 구조
```
index.html          # 메인 파일 (랜딩페이지 + 매물앱 통합)
CLAUDE.md           # 이 파일 (Claude Code 참고용)
```

## 사이트 구조

### 랜딩페이지 (8섹션 풀페이지 스크롤)
1. 히어로 - "세상에 싸고 좋은 차는 없습니다."
2. 저의 이야기 - 가성비만 좇던 이야기
3. 뼈아픈 경험 - 싸게 샀다가 두 배로 썼습니다
4. 중고차 시장의 진실 - "가격은 절대 거짓말을 하지 않습니다."
5. 새 차도 예외 아님 - GV80 신차 터널 경험
6. 최선은? - 리스크 최소화
7. 솔직하게 - 아직 먼저 찾아주시는 분이 많지 않습니다
8. CTA - 4개 카카오 상담 버튼

### 매물 앱
- Supabase에서 실시간 매물 로드
- 매물 카드 리스트 (사진, 가격, 연식, 주행거리)
- 필터링 (차종별)
- 매물 상세 모달
- 관리자 로그인 (Supabase Auth)
- 관리자 기능: 매물 등록/수정/삭제, 사진 업로드

## 디자인 시스템
- **메인 컬러**: #1D9E75 (초록)
- **강조 컬러**: #4ade80 (밝은 초록), #FEE500 (카카오 노랑)
- **배경**: #0a0a0a (어두운) / #f4f4f2 (밝은) 교차
- **폰트**: Noto Sans KR
- **우측 도트 네비게이션** 고정

## 개선 이력
- photos 분리 로드로 매물 목록 로딩 속도 개선
- Supabase 라이브러리 중복 로드 제거
- 타임아웃 12초 → 6초 단축
- 캐시 우선 표시로 깜빡임 제거
- 보안 헤더 추가 (X-Content-Type-Options, Referrer-Policy)
- OG 태그 추가 (SNS 공유 미리보기)
- 이미지 압축 품질 0.72 → 0.78

## 현재 이슈
- [ ] 관리자 로그인 안 됨 (Supabase Auth 비밀번호 확인 필요)
- [ ] Vercel에 최신 개선된 파일 배포 필요

## 배포 방법
1. `index.html` 수정
2. GitHub `nicemotorssss` 저장소에 푸시
3. Vercel 자동 배포 (1~2분 소요)

## 주의사항
- 코드 수정 시 섹션 누락 주의 (랜딩페이지 8섹션 전부 유지)
- Supabase anon key는 코드에 노출되어 있음 → RLS 정책으로 보완 필요
- 단일 HTML 파일 구조 유지 (외부 JS/CSS 파일 분리 금지)
