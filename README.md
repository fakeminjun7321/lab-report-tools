# Quilo 도구 모음 (Lab Report Tools)

실험 보고서를 쓸 때 자주 필요한 작업을 빠르게 끝내는 **브라우저 전용** 도구 모음입니다.
모든 처리는 브라우저 안에서만 이루어지며, 입력한 텍스트·데이터·파일은 **서버로 전송되지 않습니다.**

메인 서비스 **Quilo**(AI 화학·물리 보고서 초안 생성): https://chem-pre-lab-web.onrender.com

## 포함된 도구

| 도구 | 설명 |
|------|------|
| 글자수 세기 | 공백 포함/미포함 글자수, 단어수, 줄수, 바이트(UTF-8) |
| 선형회귀·추세선 | (x, y) 데이터로 기울기·절편·R²과 추세선 그래프 PNG (Excel/CSV 업로드 지원) |
| 그래프 생성기 | 산점도·꺾은선·막대 그래프 PNG (Excel/CSV 업로드 지원) |
| **파일 변환기** | 아래 변환 기능을 한 곳에 통합 |

### 파일 변환기에 포함된 기능

- **표 변환** — Excel ↔ CSV ↔ TSV
- **이미지 변환·압축** — JPG · PNG · WebP, 이미지 ↔ PDF
- **PDF 도구 10종** — 병합 · 분할 · 페이지 추출 · 페이지 삭제 · 페이지 정렬 · 회전 · 페이지 번호 · 워터마크 · 여백 자르기 · 압축
- **LaTeX → 한글 수식 변환** — LaTeX 수식을 한글(HWP) 수식 개체로 (텍스트 + HWP/HWPX 파일)

> PDF·이미지 처리는 `pdf-lib` / `pdf.js` / `JSZip`을, 표 변환은 `SheetJS`를 브라우저에서 직접 사용합니다.

## 배포

빌드 단계가 없는 순수 정적 사이트입니다. 모든 내부 링크가 **상대경로**라 어디서든 동작합니다.

- **GitHub Pages**: 저장소 Settings → Pages → Source를 `main` 브랜치 `/ (root)`로 지정.
  프로젝트 사이트(`아이디.github.io/저장소/`)와 유저 사이트(`아이디.github.io`) 모두 동작.
- **Vercel**: 저장소를 import 후 Framework Preset = "Other", Output Directory = 루트(`.`) 그대로 배포.

이 사이트는 메인 앱(`public/tools` · `public/equation`)에서 상대경로로 변환해 만들어집니다. 메인 앱의 도구가 바뀌면 이 저장소도 함께 갱신합니다.

## 라이선스

- 이 저장소의 1차 저작물(도구 UI·로직)은 [MIT License](LICENSE)를 따릅니다.
- 단, [`equation/`](equation/) 폴더는 Shin Mingyu의 [latex-to-hwp](https://github.com/minigu5/latex-to-hwp)를
  기반으로 한 2차적 저작물로, **별도의 비영리·출처표시 라이선스**([`equation/LICENSE`](equation/LICENSE),
  [`equation/NOTICE`](equation/NOTICE))를 따릅니다. 이 사이트는 무료로 제공되며 광고·결제·유료 서비스에 사용되지 않습니다.
