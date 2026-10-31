# DuDu Badminton support site

The public web pages for [DuDu Badminton](https://minhthang2811.github.io/dudu-support/),
the iPhone and iPad warm-up and stretching coach. The app's own code is in a
private repository; this one holds only what App Store Connect links to.

## Pages

| File | URL | App Store Connect field |
|---|---|---|
| `index.md` | https://minhthang2811.github.io/dudu-support/ | Marketing URL |
| `support.md` | https://minhthang2811.github.io/dudu-support/support | Support URL |
| `privacy-policy.md` | https://minhthang2811.github.io/dudu-support/privacy-policy | Privacy Policy URL |

Each page is in English with a Vietnamese section at the end, so the English
and Vietnamese localizations in App Store Connect point at the same three
addresses. The app links to the privacy policy and the support page too, from
Profile → Settings (App Review asks for the privacy policy to be reachable
inside the app, guideline 5.1.1).

## Publishing

GitHub Pages builds the root of `main` with Jekyll, using the theme set in
`_config.yml`. Push to `main` and the site rebuilds within a minute or two.
There is no build step of our own: every page is plain Markdown.

## Keeping the privacy policy true

The policy says DuDu makes no network requests of any kind. DuDu is a native
SwiftUI app with no networking code and no third-party SDKs, so that holds as
long as:

- the only way out is a link the user taps in Profile → Settings, which Safari
  opens;
- the voice coach keeps using Apple's on-device `AVSpeechSynthesizer`;
- nothing is added that phones home (analytics, crash reporting, ads).

If any of that changes, the privacy policy here, the App Review notes and the
App Privacy answers in App Store Connect have to change together.
