# Talix.kr → SearchRight.net 리다이렉트

기존 `http(s)://(www.)talix.kr` 조합의 모든 도메인을 `searchright.net`으로 리다이렉트하는 GitHub Pages

### 1. DNS 설정 (가비아)

```
# A 레코드 (루트 도메인)
타입: A
호스트: @
값: 185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153

# CNAME 레코드 (www)
타입: CNAME
호스트: www
값: your-username.github.io
```

### 2. 파일 구조

```
├── index.html    # 리다이렉트 페이지
├── CNAME         # 도메인 설정 파일
└── README.md
```

## 테스트

```bash
# DNS 확인
dig talix.kr
dig www.talix.kr

# 리다이렉트 테스트
curl -I https://talix.kr
```
