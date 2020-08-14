# divinerites-cookies

## About

Small gohugo.io component for RGPD cookies consent management

## Usage

### config.toml

Include this `params.global.cookies` section in your `config.toml` ONLY if you want cookie consent.

File : `config.toml`

```toml
[params.global.cookies]
   enable = true
   # Layout de cookieconsent
   ck_enable = true
   ck_cdn = true
   ck_popup_bg = "#000"
   ck_button_bg = "transparent"
   ck_button_text = "#f1d600"
   ck_button_border = "#f1d600"
```

- `ck_enable` : Choose type of cookie management
  - true  = cookieconsent.osano
  - false = cookiechoice simple

- `ck_cdn` = local or CDN online osano script
  - true = CDN online version
  - false = local (not updated) version

### header & footer

1 - Call `header_cookies.html` partial in your `<head>` section

```go-html-template
<head>
...
{{ partial "header_cookies.html" . }}
...
</head>
```

2 - Call `footer_cookie.html` partial in your `<footer>` section

```go-html-template
<footer>
...
{{ partial "footer_cookie.html" . }}
...
</footer>
```

### Credits

- Cookie Consent : https://docs.osano.com/category/10-consent-management
- Copyright © 2020 onwards, Didier Divinerites
