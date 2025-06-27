# 🎯 정보보안 Wargame 제작 및 공격·방어 실습

## 📌 프로젝트 개요

![Wargame-정보시스템구축엔지니어](https://github.com/user-attachments/assets/69ac6398-e01e-457c-9f38-ed8bd1c57720)

- **프로젝트명:** 정보보안 Wargame 대회 – Wargame 제작 및 공격, 방어 실습
- **수행기간:** 2025.04.22 ~ 2025.06.03
- **목표:**
  - 웹 기반 Wargame 구축 및 다양한 취약점 진단·공격 실습
  - 사용자 입력 기반 플래그 제출 시스템 구현
  - WAF 설정 및 공격 탐지 로그 수집/분석

## 🧩 프로젝트 상세 내용

### 🛠 진행 과정 및 설계

- Wargame 대회의 목적 및 시스템 구조 설계
- **PHP + HTML** 기반의 문제 제작 및 통합 사이트 구현
- **1인당 10문제 출제**, 실시간 flag 판별 기능 포함
- 문제별 walkthrough(풀이 과정, 공격 흐름, 코드 포함) 문서 작성
- **공격 로그 탐지 기능 및 Web Application Firewall(WAF)** 설정

### 💡 주요 구현 기능

- Wargame 문제 페이지 UI 및 서버 사이드 로직
- flag 제출 기능 (입력 → 정답 여부 판별)
- 각 문제별 공격 흐름 및 취약점 설명 문서화
- WAF 기반 공격 탐지 및 로그 파일 생성/저장

---

## 🧑‍💻 담당 역할 및 기술 스택

### 🔧 직접 구현한 문제 유형

| 문제 유형 | 설명 |
|-----------|------|
| 🔸 XSS | URL 인코딩 포함 Reflected XSS 취약점 |
| 🔸 인증 우회 | `strcmp()` 함수의 취약점을 활용한 로그인 우회 |
| 🔸 명령 실행 | Command Injection 취약점을 통한 시스템 명령 실행 |
| 🔸 권한 상승 | Cookie 조작 기반의 인증 우회 |
| 🔸 이진 연산 | 2진수 NOT 연산을 이용한 숨겨진 데이터 복호화 |
| 🔸 암호화/복호화 | 간단한 인코딩/디코딩 및 해시 복원 문제 |
| 🔸 코드 분석 | 소스코드를 기반으로 플래그를 유추하는 문제 |

### 🛠 기타 담당 작업

- 문제 제작 및 통합 테스트
- walkthrough 문서 작성 (공격 흐름 및 코드 포함)
- WAF 설정 및 공격 로그 기록 기능 구현

---

## 🧠 프로젝트를 통해 얻은 성장

- 다양한 취약점을 실제 서비스에 구현해보며 **실전 보안 역량 강화**
- WAF와 공격 탐지 로직을 설계하며 **공격 로그 기반 위협 분석 능력 향상**
- 기술 문서를 체계적으로 정리하며 **문서화 및 사고력 향상**
- 팀과 함께 기획·운영·문제 공유를 반복하며 **보안 프로젝트 협업 역량 체득**

---

## 📁 프로젝트 디렉토리 구조 예시

```bash
wargame/
├── index.php               # 메인 페이지
├── submit_flag.php         # flag 제출 및 판별
├── challenge/
│   ├── xss_01.php
│   ├── strcmp_bypass.php
│   ├── cmd_injection.php
│   ├── cookie_bypass.php
│   ├── binary_not.php
│   ├── simple_crypto.php
│   ├── code_review.php
├── flag/
│   ├── flag1.txt
│   ├── flag2.txt
├── logs/
│   └── attack_log.txt      # 공격 탐지 로그
├── walkthrough/
│   ├── xss.md
│   ├── strcmp_bypass.md
│   └── ...
├── waf/
│   └── waf.php             # 간단한 WAF 구현
