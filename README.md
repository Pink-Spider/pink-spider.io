# pink-spider.io

PinkSpider 회사 사이트입니다. 주소는 <https://pink-spider.io> 입니다.

- 한 장짜리 정적 페이지입니다. 빌드 과정이 없습니다.
- 영어(`/`)와 한국어(`/ko/`) 두 가지입니다.
- 외부 요청이 없습니다. 글꼴 파일, 스크립트, 분석 도구를 쓰지 않습니다.

## 파일

| 파일 | 내용 |
|------|------|
| `index.html` | 영어 페이지 |
| `ko/index.html` | 한국어 페이지 |
| `assets/site.css` | 스타일 |
| `assets/level-up-together.svg` | 제품 로고 (제품 사이트의 `public/images/lut_logo.svg` 와 같은 파일) |
| `assets/og.png` | 링크 미리보기 이미지 (1200×630) |
| `assets/favicon.svg` | 파비콘 |
| `404.html` | 없는 주소 안내 |
| `robots.txt`, `sitemap.xml` | 검색엔진용 |
| `CNAME` | GitHub Pages 에 연결한 도메인 (`pink-spider.io`) |
| `.nojekyll` | GitHub Pages 가 파일을 그대로 내보내게 한다 |

## 고칠 때

- 문구를 고치면 두 언어 파일을 함께 고칩니다.
- 회사 정보(이름, 대표자, 연락처)는 본문과 `<script type="application/ld+json">` 두 곳에 있습니다.
- 워드마크의 분홍 점(`.spider`)은 "Spider" 의 i 위에 겹쳐 그립니다. 글꼴이나 글자 크기 규칙을 바꾸면 점 위치를 다시 확인합니다.
- 색을 바꾸면 글자와 바탕의 명암비가 4.5 이상인지 확인합니다.

## 미리 보기

```bash
python3 -m http.server 3795 --bind 127.0.0.1
# http://127.0.0.1:3795/  (영어)
# http://127.0.0.1:3795/ko/  (한국어)
```

## 배포

`main` 브랜치에 push 하면 GitHub Pages 가 그대로 내보냅니다.
설정 위치는 저장소 Settings ▸ Pages 입니다(브랜치 `main`, 폴더 `/`, 도메인 `pink-spider.io`).

## DNS (후이즈)

네임서버는 바꾸지 않습니다. 이 도메인은 회사 메일에도 쓰이므로, 통째로 옮기다 기록을 빠뜨리면 메일이 끊깁니다.
아래 기록만 추가합니다.

| 종류 | 호스트 | 값 |
|------|--------|----|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `level-up-together.github.io` |

- 기록이 퍼지는 데 최대 24시간이 걸릴 수 있습니다.
- 인증서가 발급되면 Settings ▸ Pages 에서 "Enforce HTTPS" 를 켭니다.
