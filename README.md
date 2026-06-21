# fakeapiplatzi-qa-api

##

```bash
git init
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/letztersommer/fakeapiplatzi-qa-api
git push -u origin main

```

Цей репозиторій містить тестовий проект для запуску API-тестів за допомогою Newman.

## Про репозиторій

Репозиторій призначений для зберігання JSON-файлу з колекцією Postman та запуску автотестів через Newman. Тут також є приклад виконання звіту для перевірки API-поведінки.

## Встановлення

1. Відкрийте термінал у корені репозиторію.
2. Виконайте команду:

```bash
npm install
```

Це встановить залежність `newman`, яка потрібна для виконання тестів.

## Запуск тестів Newman

Щоб запустити тести з колекції Postman, використайте команду:

```bash
npx newman run tests/fakeapi.platzi.postman.json
```

Якщо потрібно зберегти звіт про виконання, додайте опцію `--reporters` та `--reporter-html-export`:

```bash
npx newman run tests/fakeapi.platzi.postman.json --reporters cli,html --reporter-html-export newman/newman-report.html
```

## Додаткові поради

- Переконайтесь, що `npm install` було виконано перед запуском.
- Якщо потрібно оновити колекцію, редагуйте `tests/fakeapi.platzi.postman.json` в Postman або іншому редакторі Postman JSON.

---

Цей README допоможе вам швидко запустити тестування API та зберегти результати в `newman/`.
