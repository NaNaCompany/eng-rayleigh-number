# 레이리수 계산기

자연대류에서 부력과 확산의 상대 크기를 나타내는 레이리수 계산

- Plan ID: E071
- App: https://nanalab.kr/eng-rayleigh-number/
- Repository: https://github.com/NaNaCompany/eng-rayleigh-number
- Formula: `Ra = gβΔT L³/(να)`
- Output: 레이리수 Ra

## Model

모든 입력>0. 같은 기준 상태의 물성과 구성에 맞는 L·ΔT를 사용한다. βΔT가 작은 Boussinesq 근사 범위의 값이다. 형상별 임계값·열전달 상관식·대류 발생 판정은 출력하지 않는다. 이 앱은 βΔT≤0.1로 제한한다.

Inputs are normalized to SI. Only one scalar is returned. Model conditions, finite numbers, physical boundaries, overflow and underflow are checked. External solver APIs and property databases are not used.

## Verification

Run `node --test tests/*.test.mjs` with Node.js 22 or later. Independent 70-digit Decimal example result: `1500000`. Source and license notices are in [SOURCES.md](SOURCES.md) and [LICENSE](LICENSE).

## Hosting

GitHub Pages uses `main` and `/`, with the NaNaCompany domain inherited. Google GTM, GA4, AdSense, Cloudflare analytics and the gray More Apps link are included. All code, descriptions and graphics are original.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
