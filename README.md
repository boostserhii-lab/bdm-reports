# BDM Reports — Sergey (Stylized PC/Console)

Архів місячної звітності Outbound BDM, напрямок **Stylized PC/Console**, RetroStyle Games.

Джерело правди — спільний BDM Dashboard (`retrostylegames-boost/rsg-leadgen`,
`bdm-dashboard/strategy_plans.json`). Це репо тримає автономну копію: сторінки
відкриваються локально, без доступу до дашборду й без авторизації.

## Звіти

| Період | Тип | Файл |
|---|---|---|
| Червень 2026 | results | [Reports/june-2026.html](Reports/june-2026.html) |
| Липень 2026 | results | [Reports/july-2026.html](Reports/july-2026.html) |
| Серпень 2026 | results | [Reports/august-2026.html](Reports/august-2026.html) |
| Вересень 2026 | plan | [Reports/september-2026.html](Reports/september-2026.html) |
| Жовтень 2026 | results | [Reports/october-2026.html](Reports/october-2026.html) |
| Листопад 2026 | plan | [Reports/november-2026.html](Reports/november-2026.html) |

`results` — ретроспектива місяця: факт vs ціль, підписані клієнти, ставки зі
статусами, блокери й висновки.
`plan` — тезис місяця, цілі, капасіті, ініціативи, гіпотези, asks.

## Дані

| Файл | Що всередині |
|---|---|
| [data/sergey-strategy.json](data/sergey-strategy.json) | Блок `Сергей` зі `strategy_plans.json` — текстова частина всіх місяців |
| [data/totals.json](data/totals.json) | Живі Totals із дашборду: $Won, підписані угоди, воронка, AM unlock, pipeline |

Жовтень і листопад зібрані напряму з метрик дашборда (знімок 2026-11-02): стратегія на жовтень у `strategy_plans.json` не заповнена, тож у `sergey-strategy.json` їх немає.
Текстова частина (тезиси, ставки, ініціативи) ведеться вручну у
`strategy_plans.json`. Totals рахуються дашбордом із Pipedrive і потрапляють сюди
знімком на дату генерації — тож можуть розходитися з поточним станом, якщо угоду
пізніше перекваліфікували за каналом.

## Статуси ставок

| Статус | Значення |
|---|---|
| 🟢 `win` | Спрацювало — отримали результат |
| 🟡 `partial` | Частково — рух є, але не добили |
| 🔵 `pending` | В процесі — ще крутиться або запуститься пізніше |
| 🔴 `miss` | Не зайшло — не спрацювало або не дійшли руки |

## Як оновити

Сторінки згенеровані зі `strategy_plans.json` + знімка Totals. Після закриття
нового місяця на дашборді — перегенерувати сторінки й закомітити оновлені файли.
