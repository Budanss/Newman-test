# 🧪 Newman Test Automation

Репозиторий предназначен для автоматизации тестирования API с помощью [Postman] и [Newman]
Запуск тестов осуществляется через GitHub Actions, с последующей генерацией и публикацией HTML-отчётов.

---

## 🚀 Что делает этот проект

- ✅ Запускает Postman-коллекцию (`collections/newOrder.json`)
- ✅ Использует окружение (`environment/Dev-environment.json`)
- ✅ Автоматически запускает тесты:
  - при коммитах в `main`
  - вручную через GitHub UI
  - по расписанию (ежедневно в 03:00 UTC)
- ✅ Сохраняет HTML-отчёты с датой
- ✅ Публикует отчёт на GitHub Pages

---

## 🌐 HTML-отчёт (GitHub Pages)

Последний опубликованный отчёт доступен по ссылке:  
🔗 [`https://budanss.github.io/Newman-test/report.html`](https://budanss.github.io/Newman-test/report.html)

---

## 📁 Структура проекта

Newman-test/
├── collections/               # Коллекции Postman
│   └── newOrder.json
├── environment/               # Файл окружения
│   └── Dev-environment.json
├── docs/                      # Папка для GitHub Pages (отчёты)
│   ├── report.html            # Последний опубликованный отчёт
│   └── .nojekyll
└── .github/
└── workflows/                 # GitHub Actions workflows
├── runNewman.yml              # Запускает тесты и сохраняет отчёт как артефакт
└── newman.yml                 # Публикует отчёт в docs/ для GitHub Pages

---

## ⚙️ Технологии и инструменты

- **Postman** — создание и управление API-тестами
- **Newman** — запуск коллекций Postman через CLI
- **newman-reporter-htmlextra** — генерация HTML-отчётов
- **GitHub Actions** — CI/CD для автоматизации
- **GitHub Pages** — хостинг отчётов

---
