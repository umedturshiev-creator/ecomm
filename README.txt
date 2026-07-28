SmartPay CRM v3.10.42 — синхронизация прочитанных уведомлений

Нужно заменить ОБА файла:
1) index.html — на GitHub Pages / в веб-версии
2) Code.gs — в Google Apps Script

После замены Code.gs нужно сохранить проект Apps Script и сделать Deploy / Manage deployments / Edit / New version / Deploy.
После замены index.html нужно обновить CRM через Ctrl + F5.

Новый лист NotificationReads создастся автоматически при первом запросе к backend.
