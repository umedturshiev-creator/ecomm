SMARTPAY CRM v3.5.1 — CHAT FIX

Почему чат мог не появиться:
Если в левом нижнем углу CRM указано «v3.3.2 Role Fix», сайт продолжает открывать старый index.html.
Это не ошибка чата — новый файл не заменил корневой index.html либо браузер/PWA показывает старую версию.

УСТАНОВКА
1. В Google Apps Script замените Code.gs и обновите действующее развертывание:
   Deploy → Manage deployments → Edit → New version → Deploy.
2. В КОРНЕ репозитория, где сейчас лежит рабочий index.html, замените:
   - index.html
   - sw.js
   - manifest.json
   Не загружайте папку SmartPay_CRM_E2EE_Chat_v3.5.1 внутрь репозитория как отдельную папку.
3. Дождитесь завершения GitHub Pages deployment.
4. Откройте адрес сайта с параметром ?v=351, например:
   https://ваш-сайт/index.html?v=351
5. Нажмите Ctrl+Shift+R или Ctrl+F5.
6. В инструментах браузера при необходимости:
   F12 → Application → Service Workers → Unregister,
   затем Application → Storage → Clear site data.
7. Войдите в CRM заново.

ПРОВЕРКА
В левом нижнем углу должно быть: v3.5.1 CHAT FIX.
После входа справа внизу должна отображаться кнопка чата 💬.

Личные сообщения шифруются в браузере; общий чат видят все сотрудники.
