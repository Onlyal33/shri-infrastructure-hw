При push и pull-request в master запускается cкрипт из ci.yml: проверка коммита, сборка, линтер, тесты

При появлении тега вида v10 запускается скрипт из release.yml: ci и создание issue с инфо о релизе, issue устанавливается тег RC

При установке релизному issue тега RELEASE запускается скрипт из deploy.yml: деплой, создание комментария в issue и закрытие issue
--------------
В этом репозитории находится пример приложения с тестами:

- [e2e тесты](e2e/example.spec.ts)
- [unit тесты](src/example.test.tsx)

Для запуска примеров необходимо установить [NodeJS](https://nodejs.org/en/download/) 16 или выше.

Как запустить:

```sh
# установить зависимости
npm ci

# запустить приложение
npm start
```

Как запустить e2e тесты:

```sh
# скачать браузеры
npx playwright install

# запустить тесты
npm run e2e
```

Как запустить модульные тесты:

```sh
npm test
```
