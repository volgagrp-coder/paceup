# Скриншоты PaceUp — продвинутый шагомер

Снимки работы приложения: слева — ход разработки, справа — экран «Сегодня» PWA-шагомера
в демо-режиме (имитация сигнала акселерометра, каденс 108 шаг/мин).

| Файл | Сессия | Шагов | Каденс |
|---|---|---|---|
| `paceup-01.png` (копия `ш1.png`) | 03:56 | 425 | 108 шаг/мин |
| `paceup-02.png` (копия `ш2.png`) | 04:56 | 534 | 108 шаг/мин |
| `paceup-03.png` (копия `ш3.png`) | 05:40 | 613 | 108 шаг/мин |

Предусмотрены два набора имен: `ш1…ш3.png` — исходники (кириллица),
`paceup-0N.png` — копии с латинскими именами. В Markdown-ссылках надёжнее использовать
латинские имена: кириллица в URL кодируется `%D1%881.png` и ломается в некоторых рендерах.

Размер файлов 145–220 КБ (лимит GitHub — 100 МБ на файл, так что проблем не будет).

---

## Как загрузить в репозиторий

### Вариант 1. Через веб-интерфейс GitHub (самый простой, git не нужен)

1. Открыть свой репозиторий → вкладка **Add file → Upload files**.
2. Перетащить в окно загрузки файлы (лучше три латинских: `paceup-01…03.png`),
   в поле путь указать `screenshots`.
3. Внизу нажать **Commit changes**.

### Вариант 2. Через git

```bash
cd <папка_репозитория>
mkdir -p screenshots
cp "<путь>\PaceUp\screenshots\"*.png screenshots/
git add screenshots/
git commit -m "Add PaceUp pedometer screenshots"
git push
```

### Вариант 3. Через GitHub CLI

```bash
gh repo clone owner/repo
cd repo
mkdir -p screenshots
cp "<путь>\PaceUp\screenshots\"*.png screenshots/
git add screenshots/ && git commit -m "Add PaceUp screenshots" && git push
```

---

## Как показать скриншоты в README репозитория

Добавьте в корневой `README.md` репозитория:

```markdown
## Экраны

![PaceUp — экран «Сегодня», 425 шагов](screenshots/paceup-01.png)

![PaceUp — экран «Сегодня», 534 шага](screenshots/paceup-02.png)

![PaceUp — экран «Сегодня», 613 шагов](screenshots/paceup-03.png)
```

Или одной строкой-галереей:

```markdown
| | | |
|:---:|:---:|:---:|
| ![](screenshots/paceup-01.png) | ![](screenshots/paceup-02.png) | ![](screenshots/paceup-03.png) |
```
