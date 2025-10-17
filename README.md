# SNOVAHA Benefits

> 육아 혜택 서비스 - 임산부·유아 가족을 위한 정부 지원금, 할인 혜택, 육아 정보

## 📋 서비스 소개

SNOVAHA 육아 혜택 페이지는 임산부와 유아 가족을 위한 다양한 지원 정보를 제공합니다.

### 주요 기능

- 💰 **정부 지원금**: 첫만남 이용권, 부모급여, 아동수당 등
- 🎫 **할인 혜택**: 다둥이 행복카드, 임산부 배려석, 백화점 라운지 등
- 🍼 **육아 용품 정보**: 신생아 필수품, 카시트, 이유식 가이드
- 📢 **광고 영역**: 구글 애드센스 통합 (수익화)

## 🚀 배포

### AWS S3 + CloudFront

```bash
# S3 버킷: 1st-birthday-invitation-20251011
# 경로: /benefits/

# 배포
aws s3 cp index.html s3://BUCKET_NAME/benefits/
aws s3 cp home.css s3://BUCKET_NAME/benefits/

# CloudFront 캐시 무효화
aws cloudfront create-invalidation --distribution-id DIST_ID --paths "/benefits/*"
```

## 📝 구글 애드센스 설정

1. [Google AdSense](https://www.google.com/adsense/) 가입
2. 사이트 등록: `www.snovaha.com`
3. 승인 대기 (1-2주)
4. 승인 후 광고 코드를 `.ad-container` 영역에 삽입

### 광고 코드 예시

```html
<div class="ad-container">
    <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-XXXXXXXXXXXXXXXX"
         crossorigin="anonymous"></script>
    <ins class="adsbygoogle"
         style="display:block"
         data-ad-format="auto"
         data-full-width-responsive="true"></ins>
    <script>
         (adsbygoogle = window.adsbygoogle || []).push({});
    </script>
</div>
```

## 🔗 링크

- **메인**: https://www.snovaha.com
- **육아 혜택**: https://www.snovaha.com/benefits/
- **GitHub**: https://github.com/snovaha/snovaha-benefits

## 📦 파일 구조

```
snovaha-benefits/
├── index.html          # 메인 페이지
├── home.css           # 스타일시트
└── README.md          # 문서
```

## 🎨 디자인

- **컬러**: 옐로우 그라데이션 (#fef3c7 → #fde68a)
- **폰트**: Pretendard
- **스타일**: Toss-inspired 모던 디자인

## 📄 라이선스

MIT License

---

**SNOVAHA** - Super Nova + Han & Ahn

