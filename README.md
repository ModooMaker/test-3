# ModooMaker/test-3 — Helium Jekyll 테마 Fork

Bootstrap 4 기반 Helium Jekyll 테마를 가져와 설정을 살펴본 과거 저장소입니다. 테마와 기본 UI·샘플의 구현은 원작 작업이며, 이 Fork의 독자적인 제품 기능으로 소개하지 않습니다.

## 목적과 현재 구현

사이트 테마를 검토한 실험 후보로 분류할 수 있습니다. 개인 계정의 `_config.yml` 수정 커밋은 확인되지만 구체적인 제품 개발 목표는 문서화되어 있지 않습니다.

현재 파일에는 랜딩 페이지·블로그·포스트·태그·UI 구성요소 샘플, Liquid 레이아웃, CSS/JavaScript 자산이 있습니다. 별도의 앱 API나 DB는 없습니다.

## 기술 스택과 구조

- Jekyll, Liquid, Markdown, Ruby Rake
- HTML/CSS/JavaScript, Bootstrap 4, Font Awesome
- `_config.yml`의 테마·URL 설정과 `_layouts/`의 화면 틀
- `_posts/`의 샘플 글과 `assets/`의 스타일·이미지·스크립트

화면 틀과 글을 정적 생성으로 연결하는 구조입니다. 루트의 `buttons.html`, `cards.html`, `tables.html` 등은 테마 구성요소를 확인하는 샘플입니다.

## 화면과 참고 데모

이 Fork는 GitHub Pages가 비활성화되어 있고 별도 배포 데모를 확인하지 못했습니다. [원작 저장소](https://github.com/heliumjk/heliumjk.github.io)의 안내와 이미지는 원작 참고 자료이며 이 저장소에서 검증한 배포 결과가 아닙니다.

## 설치와 실행 조건

원작 문서는 Jekyll 3.x 계열을 안내하지만 이 저장소에는 Gemfile과 의존성 잠금 파일이 없습니다. 재현 가능한 Ruby/Jekyll 버전 조합을 확정할 수 없으며 새 환경 설치·빌드를 이번 점검에서 실행하지 않았습니다.

Ruby와 필요한 Jekyll 환경이 이미 있다면 다음과 같이 로컬 제공을 시도할 수 있습니다.

```bash
git clone https://github.com/ModooMaker/test-3.git
cd test-3
jekyll serve --host 127.0.0.1 --baseurl ""
```

기본 확인 주소는 `http://127.0.0.1:4000/`입니다. [_config.yml](_config.yml)의 기존 `url`과 `baseurl`은 이 Fork의 이름과 다르므로 배포 경로·외부 연동을 별도 확인해야 합니다. [Rakefile](Rakefile)은 글 생성 등 보조 작업이며 자동 회귀 테스트 묶음이 아닙니다.

## 검증과 현재 한계

- 원작 README는 프로젝트가 더 이상 유지보수되지 않는다고 알립니다. 이 Fork가 그 상태를 해결했다고 확인할 근거는 없습니다.
- 원작 미완성 목록에는 홈 광고 블록, CSS·이미지 최적화, 404 스타일, 코드 하이라이트 스타일이 남아 있습니다. 이 Fork에서 완료한 기능으로 표현하지 않습니다.
- 저장소 내 자동 테스트와 CI workflow는 없습니다. 오래된 외부 스크립트·링크·선택 연동의 정상 동작도 확인하지 않았습니다.
- 2026-11-13 점검은 소스·설정·Fork 관계와 README 파일 링크 조사에 한정했습니다.

## 출처와 라이선스

[Helium 원작](https://github.com/heliumjk/heliumjk.github.io), [기존 변경 이력](changelog.md), [LICENSE](LICENSE)를 함께 확인하세요. 기존 Credits와 License 고지는 아래에 원문으로 보존합니다. 테마의 출처·저작권을 유지해야 합니다.

## Credits
### Resources used
- [Helium B4](https://uideck.com/products/helium-ui-kit/)
- [Font Awesome](http://fontawesome.io/)
- [Bootstrap 4](https://v4-alpha.getbootstrap.com/)

### Inspiration and thoughtful code-jacking
Inspiration and bits of things listed below are present inside dactl's code:
- [Daktilo](https://github.com/kronik3r/daktilo) - dactl is based on Daktilo and inherits it's one-column layout.
- [Hydejack](https://github.com/qwtel/hydejack/) - I've learned a lot about Jekyll when I took apart [@qwtel](https://github.com/qwtel/)'s excellent fork of [Hyde](https://github.com/poole/hyde) theme. I embraced his more partials = everything is easier to edit policy. Hydejack theme gave me an idea on how to create hero images liquid scripting, loading google fonts and using rem's/em's and more.
- [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes) - This guy makes awesome themes and writes a lot about Jekyll and it's more obscure use cases on his blog, [Made Mistakes](https://mademistakes.com). Looking through his theme's code - Minimal Mistakes in particular - gave me lot of information about how to build a robust theme and how to make it configurable within `_config.yml`
- [Trophy](https://github.com/thomasvaeth/trophy-jekyll) - Link border slide animation SASS mixin which I slightly modified to be able to easily change the direction of the animation.
- Various blog posts about Jekyll and [Stackoverflow](https://www.stackoverflow.com) posts with useful [Liquid](https://github.com/Shopify/liquid) snippets.

## License
All parts of helium Jekyll theme are free to use and abuse under the open-source [MIT license](http://opensource.org/licenses/mit-license.php).
