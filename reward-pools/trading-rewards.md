---
description: Обзор программы вознаграждения пользователей за торговлю.

---

# Награды за торговлю

25% \(`250 000 000 DYDX`\) будет распределено между пользователями, которые торгуют в рамках протокола на основе сочетания уплаченных комиссий и суммы открытых позиций.

**Цели**

* Мотивируйте всех трейдеров на использование бессрочных контрактов dYdX уровня 2
* Стимулируйте рост рыночной ликвидности и общей степени использования продуктов

## **Обзор**

![](../.gitbook/assets/image%20%283%29.png)

Токены DYDX будут распределяться между трейдерами по формуле присуждения наград, основанной на сочетании уплаченных комиссий и суммы открытых позиций в протоколе dYdX уровня 2. Токены DYDX будут распределяться в течение 28-дневного периода на протяжении пяти лет и не подлежат передаче во владение или блокировке. В каждую эпоху будет распределяться 3 835 616 DYDX.

Для расчета количества DYDX, присуждаемых конкретному трейдеру в качестве награды за определенную эпоху, используется функция Кобба — Дугласа:

$$
 w\ =\ \left(\frac{f}{F}\right)^{\alpha } \times \ \left(\frac{d}{D}\right)^{1-\alpha }
 $$

$$
 r=R\times \frac{w}{\sum\limits _{n} w_{n}} \ \ ,n=1,2...k
 $$

| Параметр | Определение |
| :--- | :--- |
| r | Награда для конкретного трейдера. |
| R | Совокупный размер наград, подлежащих распределению между всеми трейдерами в пуле за эпоху. |
| f | Общая сумма комиссий, уплаченных трейдером в этой эпохе. |
| w | Личная оценка трейдера. |
| $${\sum\limits &lt;g id="1" ctype="italic" equiv-text="_"&gt;{n} w</g>{n}}$$ | Сумма всех оценок трейдера. |
| F | Общая сумма комиссий, уплаченных всеми трейдерами в этой эпохе. |
| d | Общая взвешенная сумма открытых позиций трейдера \(измеряемая ежечасно\) на всех рынках в этой эпохе. |
| D | Общая взвешенная сумма открытых позиций \(измеряемая ежечасно\) на всех рынках в этой эпохе. |
| k | Общее число трейдеров в этой эпохе. |
| α | Постоянная величина в диапазоне, которая определяет долю комиссий по отношению к открытым позициям. Изначально значение α равно 0,7. |

Следующий пример иллюстрирует размер наград за торговлю, полученных трейдерами А, Б и В на основании расчета по вышеуказанной формуле:

![](https://lh4.googleusercontent.com/LWYcMg6ImkQCV1aVsS2jVwjcFfTmBG4u7JZHrnf4l4MmHcxCZlu_af57UaSgHhr6TYi9thIyr8794SECk6_E8Vn4sR2QJFniUSbQGhIZZrkvTf0QRHmzzvt6awR9N8kxHhCooRp4)

## Часто задаваемые вопросы

### Кто имеет право на получение наград за торговлю?

Право на получение DYDX в качестве награды за торговлю имеют все трейдеры, торгующие бессрочными контрактами dYdX уровня 2.

Этот продукт недоступен трейдерам в Соединенных Штатах Америки и на Запрещенных территориях, как определено в [Условиях использования](https://dydx.exchange/terms) dYdX.

### Сколько DYDX мне удалось заработать по программе вознаграждения за торговлю?

В определенную эпоху пользователи могут просмотреть уплаченные комиссии, среднюю сумму открытых позиций и предполагаемый размер наград за торговлю здесь.

### Как получить награды за торговлю? Когда можно вывести и перевести DYDX, полученные в качестве награды?

Заработанные в качестве награды за торговлю токены DYDX станут доступны для перевода по окончании каждой эпохи. Владельцы токенов DYDX могут получить их примерно через `7 дней` \(**период ожидания**\) после окончания эпохи. После получения токены можно использовать или делегировать управлению dYdX.

Трейдеры могут получить награды за торговлю в конце каждой эпохи [здесь](https://dydx.community/dashboard).

Чтобы получить DYDX, пользователям необходимо нажать «Получить», заключить сделку и уплатить комиссию за газ.

![](../.gitbook/assets/image%20%284%29.png)

### Что такое сумма открытых позиций?

Сумма открытых позиций — это общее количество невыполненных бессрочных контрактов, обязательства в отношении какого-либо актива по которым продолжают действовать. Сумма открытых позиций равна общему количеству купленных или проданных контрактов, но не общей сумме таких контрактов. Увеличение суммы открытых позиций свидетельствует о притоке на рынок дополнительной денежной массы, тогда как ее уменьшение указывает на отток денежных средств с рынка.

Ниже представлена таблица данных торговой деятельности трейдеров A, Б, В, Г и Д на рынке опционов. Сумма открытых позиций рассчитывается в USDC каждый день по окончании торговой деятельности:

| Время | Торговая деятельность | Сумма открытых позиций \(USDC\) |
| :--- | :--- | :--- |
| 1 июля | **Трейдер A** покупает 1 BTC по цене 30 000 USD, а **трейдер Б** продает 1 BTC по цене 30 000 USD | 30 000 USD |
| 3 июля | **Трейдер В** покупает 5 BTC по цене 30 000 USD, а **трейдер Г** продает 5 BTC по цене 30 000 USD | 180 000 USD |
| 5 июля | **Трейдер А** продает 1 BTC по цене 30 000 USD, а трейде**р Г покуп**ает 1 BTC по цене 30 000 USD | 150 000 USD |
| 10 июля | **Трейдер Д** покупает 5 BTC по цене 30 000 USD, а **трейдер В** продает 5 BTC по цене 30 000 USD | 150 000 USD |

В контексте формулы расчета размера награды за торговлю сумма открытых позиций измеряется каждую минуту на всех рынках и усредняется по определенной эпохе для расчета размера наград.

### Какие комиссии взимает dYdX?

dYdX использует модель комиссионных сборов мейкера и тейкера для вычисления своих комиссионных сборов. На платформе dYdX существует два типа ордеров — мейкер-ордера и тейкер-ордера.

* Мейкер-ордера не исполняются моментально, а остаются в ордербуке, добавляя ему глубины и ликвидности.
* Тейкер-ордера, наоборот, моментально исполняют существующие мейкер-ордера. Они изымают ликвидность из ордербука.

Комиссии для мейкеров и тейкеров определяются на основе перечня комиссий, взвешенных по объему за 30-дневный период. Стандартный перечень комиссий размещен [здесь](https://help.dydx.exchange/en/articles/4798040-perpetual-trade-fees). Владельцы DYDX могут получить [скидку на торговую комиссию](trading-rewards.md) на основе количества DYDX, которым они владеют на текущий момент.
