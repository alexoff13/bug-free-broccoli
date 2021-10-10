# Протокол HTTP. Основы работы с консолью разработчика в браузере
---
## Сайт https://ulearn.me
Нажимаем "Войти с помощью ВКонтакте" и получаем:
```yaml
:authority: oauth.vk.com
:method: GET
:path: /authorize?client_id=4381546&redirect_uri=https%3A%2F%2Fulearn.me%2Fsignin-vkontakte&scope=%7B%7D&response_type=code&v=5.85
:scheme: https
accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
accept-encoding: gzip, deflate, br
accept-language: ru-RU,ru;q=0.9,en-US;q=0.8,en;q=0.7
cache-control: max-age=0
cookie: *******************
referer: https://ulearn.me/
sec-ch-ua: ";Not A Brand";v="99", "Chromium";v="94"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Linux"
sec-fetch-dest: document
sec-fetch-mode: navigate
sec-fetch-site: cross-site
sec-fetch-user: ?1
upgrade-insecure-requests: 1
user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/94.0.4606.61 Safari/537.36
```
Так же имеется поле `Form Data`, которое содержит `client_id`:
```yaml
client_id: 4381546
redirect_uri: https://ulearn.me/signin-vkontakte
scope: {}
response_type: code
v: 5.85
```
---
Одновременно посылается `POST` запрос:
```yaml
:authority: ulearn.me
:method: POST
:path: /Login/ExternalLogin?ReturnUrl=%2F
:scheme: https
accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
accept-encoding: gzip, deflate, br
accept-language: ru-RU,ru;q=0.9,en-US;q=0.8,en;q=0.7
cache-control: max-age=0
content-length: 183
content-type: application/x-www-form-urlencoded
cookie: *************************************
origin: https://ulearn.me
referer: https://ulearn.me/login?returnUrl=%2f
sec-ch-ua: ";Not A Brand";v="99", "Chromium";v="94"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Linux"
sec-fetch-dest: document
sec-fetch-mode: navigate
sec-fetch-site: same-origin
sec-fetch-user: ?1
upgrade-insecure-requests: 1
user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/94.0.4606.61 Safari/537.36
```
---

## Сайт https://github.com/
Нажимаем "Sign in" 
Получаем:
```yaml:authority: github.com
:method: GET
:path: /login
:scheme: https
accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
accept-encoding: gzip, deflate, br
accept-language: ru-RU,ru;q=0.9,en-US;q=0.8,en;q=0.7
cache-control: max-age=0
cookie: _octo=GH1.1.2029694454.1622937951; tz=Asia%2FVladivostok; _device_id=882c8d49e60cc79fef7f82eed9d17cf2; tz=Asia%2FVladivostok; color_mode=%7B%22color_mode%22%3A%22dark%22%2C%22light_theme%22%3A%7B%22name%22%3A%22light%22%2C%22color_mode%22%3A%22light%22%7D%2C%22dark_theme%22%3A%7B%22name%22%3A%22dark_dimmed%22%2C%22color_mode%22%3A%22dark%22%7D%7D; has_recent_activity=1; user_session=Ap5-G29EyZq5yHcn-zntM6hRBOwXRo7UMTIwf4xWQy39hiuF; __Host-user_session_same_site=Ap5-G29EyZq5yHcn-zntM6hRBOwXRo7UMTIwf4xWQy39hiuF; logged_in=yes; dotcom_user=alexoff13; _gh_sess=%2FL9LeJ3Lg3oBlESQuMBElYzCHP%2B9zl%2BbSvdC09TTntFnCMqHRMxJKDoH%2FF2cA4k6D6co5xHeqLxcKRbPc%2FGDkXRGgTu9SRD3DBcrIDND0XPpYOiHSgfvpUC7moi%2FhF4h80YsvAW1mfpr9k1hWYDjPBJgQESE%2F5GBofbSm5CH5arteWK0vuRso1iHfZgBWfHAKtQaGpx4tQFqRA4LfYGoLJfrrUwywwnHTK5GKgxPKMsDdYcA2wJugHzxmmoqOohuvyTF0hTG7YqAqJbW8jtEonw1tncd2tqG7xm8L8bd2jJejJnFbgfh4HmShpVceC6VnMxYIgk5%2ByzQ2vIPkhUDR4ZlHXXLN8EaIjgrTrBOGyRzWmWIy89KOR5EcSMfGVahRVTFfr3Xbs24XzIROMcEdydhb8sEwnO1vJKbgul50PkbiElkJaeCjLCppjK0co7U6MUjqPGtTcXYuZLPfNBLVhg1FsQIfZTutDE%2FM3xGAS66EZjlIsFzSeZcK3GqNlChwyS1ENCOIjHxLfUiywA%2BP9qDxHUvokWAmUXCT0ZW4ggynBKA6LJVdsEkYlywM5M%2FHtLCmlaa%2Bd6%2FGkHBPcbrzsSIiriysCFex21oYXb5tELsWTKJWeN%2FYMd07Q31WtD%2FRkh8hPagrTm0WNEC%2BE2GpO%2F9U%2Bpu2jma2dOPakj01OLwmmBkZQSWjdZ8EL9qQKV8%2F%2Fs4UHKhUA7huI2LesPAc%2FDQeLu48Yk9KFZdqMAyG6N4Jt9zI5My8H2G7Mi77fXTAXJENqNCabcxtqdzQlxPge9G5cZWi9%2Beu%2BalhzvhXmf7R%2B9gOshB%2FWDHm%2BEowMKeh0bewrf8paGCODdWiLOH79M4rBziLssVKgUWvjvMwNU%2FVqiOBSGTLVTxJB%2BnA0DH7%2Fu6Iosw%2FBHPiiuFp5zq5crCs%2FYtx0Ix6jFkZ5pqMnbxFHXxMMJSQ7fUsd9wh%2ByhsIYT7Phm24Ge0C02HmUQ2kYpC00O2GX67nLh%2Bnw3YFGLDE1mINIK5X%2BNJF%2FDMjcuVB0YNn23Zzru%2Ff6vsH3%2BaeJ3Lj3%2Bg0L7fb5kP28kstiPcpAFImh%2BNYpvtgF2r1BXYt04lCONoy%2Fpvahpwsk3VY0CxaVzzwsH4zPg7Y0TaSyTwWrF--J6PJagC9y5tGNxqz--N89CjUL%2FYW9uCeEMJhqWYA%3D%3D
referer: https://github.com/login
sec-ch-ua: ";Not A Brand";v="99", "Chromium";v="94"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Linux"
sec-fetch-dest: document
sec-fetch-mode: navigate
sec-fetch-site: same-origin
sec-fetch-user: ?1
upgrade-insecure-requests: 1
user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/94.0.4606.61 Safari/537.36
```
После того как водим данные, посылается `post` запрос:
```yaml
:authority: github.com
:method: POST
:path: /session
:scheme: https
accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
accept-encoding: gzip, deflate, br
accept-language: ru-RU,ru;q=0.9,en-US;q=0.8,en;q=0.7
cache-control: max-age=0
content-length: 461
content-type: application/x-www-form-urlencoded
cookie: **********************
origin: https://github.com
referer: https://github.com/login
sec-ch-ua: ";Not A Brand";v="99", "Chromium";v="94"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Linux"
sec-fetch-dest: document
sec-fetch-mode: navigate
sec-fetch-site: same-origin
sec-fetch-user: ?1
upgrade-insecure-requests: 1
user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/94.0.4606.61 Safari/537.36
```
Так же имеется поле `Form Data`, которое содержит `client_id`:
```yaml
commit: Sign in
authenticity_token: ******************************
login: alexoff13
password: 12345678
trusted_device: 
webauthn-support: supported
webauthn-iuvpaa-support: unsupported
return_to: https://github.com/login
allow_signup: 
client_id: 
integration: 
required_field_787e: 
timestamp: *************
timestamp_secret: *****************
```
---
## Вывод
Мы рассмотрели процесс аутентификации на двух сайтах.






