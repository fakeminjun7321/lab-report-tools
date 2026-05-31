# 보고서 도구 모음 (Lab Report Tools)

실험 보고서를 쓸 때 자주 필요한 작업을 빠르게 끝내는 **브라우저 전용** 도구 모음입니다.
모든 처리는 브라우저 안에서만 이루어지며, 입력한 텍스트·데이터·파일은 **서버로 전송되지 않습니다.**

메인 서비스(화학·물리 보고서 초안 생성): https://chem-pre-lab-web.onrender.com

## 포함된 도구

| 도구 | 설명 |
|------|------|
| 글자수 세기 | 공백 포함/미포함 글자수, 단어수, 줄수, 바이트(UTF-8) |
| 평균·표준편차 계산기 | 개수·평균·표준편차·표준오차·범위 (Excel/CSV 업로드 지원) |
| 유효숫자·오차 계산기 | 백분율 오차, 유효숫자 반올림, 기본 오차 전파 |
| 텍스트 정리 | 여러 공백·빈 줄·줄바꿈을 깔끔한 평문으로 |
| 이미지 변환·압축 | 사진을 JPG·PNG·WebP로 변환·축소 |
| 선형회귀·추세선 | (x, y) 데이터로 기울기·절편·R²과 추세선 그래프 PNG (Excel/CSV 업로드 지원) |
| 그래프 생성기 | 산점도·꺾은선·막대 그래프 PNG (Excel/CSV 업로드 지원) |
| PDF 병합 | 여러 PDF를 원하는 순서로 한 파일로 |
| 파일 변환기 | 표(Excel↔CSV↔TSV), 이미지→PDF, PDF→이미지, 이미지 형식 변환 |
| LaTeX → 한글 수식 변환기 | LaTeX 수식을 한글(HWP) 수식 개체로 (텍스트 + HWP/HWPX 파일) |

## 배포

빌드 단계가 없는 순수 정적 사이트입니다. 모든 내부 링크가 **상대경로**라 어디서든 동작합니다.

- **GitHub Pages**: 저장소 Settings → Pages → Source를 `main` 브랜치 `/ (root)`로 지정.
  프로젝트 사이트(`아이디.github.io/저장소/`)와 유저 사이트(`아이디.github.io`) 모두 동작.
- **Vercel**: 저장소를 import 후 Framework Preset = "Other", Output Directory = 루트(`.`) 그대로 배포.

## 라이선스

- 이 저장소의 1차 저작물(도구 UI·로직)은 [MIT License](LICENSE)를 따릅니다.
- 단, [`equation/`](equation/) 폴더는 Shin Mingyu의 [latex-to-hwp](https://github.com/minigu5/latex-to-hwp)를
  기반으로 한 2차적 저작물로, **별도의 비영리·출처표시 라이선스**([`equation/LICENSE`](equation/LICENSE),
  [`equation/NOTICE`](equation/NOTICE))를 따릅니다. 이 사이트는 무료로 제공되며 광고·결제·유료 서비스에 사용되지 않습니다.
