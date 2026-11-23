# NEXUS HOST Mobile 0.1.0

Android-приложение на Kotlin + Jetpack Compose. В этой версии доступны экраны Dashboard, Console и Settings с нижней навигацией и тёмным оформлением.

**Важно:** это пока UI-preview. Кнопки управления сервером и показатели демонстрационные; подключения к NEXUS HOST и удалённого управления ещё нет.

## Как получить APK без Android Studio

В архив уже добавлен GitHub Actions workflow `.github/workflows/build-apk.yml`. Он автоматически собирает APK при загрузке проекта в репозиторий GitHub.

1. На компьютере открой [github.com](https://github.com) и войди в аккаунт (если аккаунта нет — создай).
2. Создай новый репозиторий: **New repository**. Назови его `nexus-host-mobile`. Для простоты можно выбрать **Public**.
3. Распакуй этот ZIP на компьютере. Загрузи **содержимое папки `nexus-host-mobile`**, а не сам ZIP, в созданный репозиторий. В GitHub нажми **Add file → Upload files**, перетащи файлы и папки проекта в окно загрузки и нажми **Commit changes**.
4. Открой в репозитории вкладку **Actions**. Выбери workflow **Build NEXUS HOST APK**. Если сборка не стартовала автоматически, нажми **Run workflow → Run workflow**.
5. Дождись завершения сборки со статусом зелёной галочки. Открой завершённый запуск workflow.
6. Внизу страницы найди **Artifacts** и скачай `nexus-host-mobile-debug-apk`.
7. На телефоне распакуй скачанный ZIP-архив артефакта. Внутри будет `app-debug.apk`. Открой его и подтверди установку. Android может попросить разрешить установку приложений из используемого файлового менеджера или браузера.

## Сборка в Android Studio

Открой папку проекта в Android Studio, дождись синхронизации Gradle и выбери **Build → Build APK(s)**. APK будет в `app/build/outputs/apk/debug/app-debug.apk`.

## Технические сведения

- Package: `com.nexushost.mobile`
- Minimum Android: 8.0 (API 26)
- Compile/Target SDK: 35
- Java: 17
- Gradle: 8.9
