# Макети та клікабельний прототип Figma

**Поточна редакція макетів:** Mini Issue Tracker — Simplified Prototype (Figma, `J4cFxVfdTPvCdLarVS5BVs`).

- [Макети Figma — редагований файл](https://www.figma.com/design/J4cFxVfdTPvCdLarVS5BVs/Mini-Issue-Tracker)
- [Клікабельний прототип — відкрити зі списку All](https://www.figma.com/proto/J4cFxVfdTPvCdLarVS5BVs/Mini-Issue-Tracker?node-id=2-5493&page-id=0%3A1&starting-point-node-id=2%3A5493&scaling=scale-down)
- [Important — стан зі збереженим Resolved](https://www.figma.com/design/J4cFxVfdTPvCdLarVS5BVs/Mini-Issue-Tracker?node-id=2-5555)
- [Створення з порожнього списку](https://www.figma.com/design/J4cFxVfdTPvCdLarVS5BVs/Mini-Issue-Tracker?node-id=3032-1492)
- [Деталі заявки та статуси](https://www.figma.com/design/J4cFxVfdTPvCdLarVS5BVs/Mini-Issue-Tracker?node-id=2-5920)
- [Рольові обмеження](https://www.figma.com/design/J4cFxVfdTPvCdLarVS5BVs/Mini-Issue-Tracker?node-id=2-6380)

Посилання відкривають поточний файл. Клікабельні переходи відтворюються у Figma Present; підготовлені стани не є підключеним до бази даних застосунком.

---


## Завдання для макетування

### Mini Issue Tracker — Figma Brief v0.2

**Цільовий виконавець:** Figma AI Agent  
**Етап:** G5 — low-fidelity wireframes, Release MVP  
**Дата:** 14.10.2026  
**Очікуваний артефакт:** редагований набір із **15 основних демонстраційних frames** та повторно використовуваних компонентів у Figma; цей brief сам по собі не є макетом або звітом про виконану генерацію.  
**Статус основи:** D-01–D-10 APPROVED для навчального проєкту; G4 Plan Review — PASS / PLAN READY, reviewer approved. Screen Map і Screen Contracts документально перевірені, але це не тотожне підтвердженню кожного учасника чи викладача.

## 1. Джерела, пріоритет та словник

Використовуй **тільки** ці п’ять документів як нормативну основу цього завдання:

1. `01_Input_Pack_v0.1.md` — Release MVP US-01–US-08, BR, AC, обмеження, SOURCE / DERIVED / UNRESOLVED.
2. `Decision_Log.md` v1.2 — UX-рішення D-01–D-10 зі статусом APPROVED.
3. `02_Screen_Map_v0.3.2.md` — Screen ID, F-01–F-15, переходи T-01–T-18, заборонені дії N-01–N-06.
4. `03_Screen_Contracts_v0.1.2.md` — дані, права, інваріанти, validation, error/empty, матриця 33 AC і TC-00–TC-31.
5. `04_Plan_Review_FINAL.md` — незалежна документальна перевірка G4, зауваження й підтверджені межі.

**Правило пріоритету:** для складу релізу застосовуй §8 Input Pack (US-01–US-08); для UX-виборів — APPROVED D-01–D-10; для складу екранів — Screen Map v0.3.2; для умов конкретного контролу — Screen Contracts v0.1.2. Непідтверджені деталі **не перетворюй на вимоги**. `AC-03.1–AC-03.4` — **локальні alias** ненумерованих у первинному джерелі критеріїв US-03. Показуй їх як traceability IDs, не як дослівну нумерацію SD_Spec.

Маркування: **REQUIRED** — джерело або затверджене UX-рішення; **DERIVED** — логічний наслідок; **RECOMMENDED** — нейтральний дизайн-вибір для генерації; **TBD / UNRESOLVED** — немає погодженого рішення. `Frame` — одиниця демонстрації, **не нова продуктова сторінка**.

## 2. Загальні параметри візуального виконання

- **REQUIRED:** web application, desktop-first; grayscale (білий, чорний, нейтральні сірі), low-fidelity, без декоративних ілюстрацій, градієнтів, брендингу, кольорових семантичних бейджів і фотореалістичних assets. [KC-03; D-01]
- **REQUIRED:** створюй **нативні редаговані Figma Frames**, текстові шари, прості vector shapes і повторно використовувані компоненти/variants. Не об’єднуй цілий екран у зображення. Структура шарів і назви станів мають бути зрозумілими.
- **RECOMMENDED, не специфікація:** робоча ширина desktop frame **1440 px**, висота **900 px або за контентом**; максимальна ширина контенту 1120–1200 px; 8 px spacing scale; 16/24/32 px інтервали; шрифт Inter або системний sans-serif; заголовок 24 px, секції 18 px, текст/поля 14–16 px, метадані 12–13 px; border 1 px; радіуси 4–6 px. Якщо контент перевищує viewport, збільшуй висоту frame — не обрізай його.
- **RECOMMENDED:** білий фон, світло-сірі межі, темно-сірий основний текст; selected tab — підкреслення/темний текст, disabled — світлий сірий та слабший контраст; **без reliance on color** для status і priority: усі значення відображати текстом.
- **REQUIRED:** повторюй той самий top/header, tabs і layout у станах S-02; той самий header, інформаційні блоки, три незалежні контролі і Comments в усіх S-03. [D-01; D-05; D-06]
- **RECOMMENDED:** відображай різні стани шляхом окремих демонстраційних frames і variants, а не складними анімаціями. Інтеракції майбутнього прототипу описані в §9; **не заявляй**, що прототип уже з’єднано або протестовано. [D-08]

## 3. Продуктова інформаційна архітектура

**Продуктова сторінка 1:** `S-02 Issues List` — вкладки `All` / `Important`, включно з `Empty` станом.  
**Продуктова сторінка 2:** `S-03 Issue Details` — усі дані, керування assignee/priority/status і коментарі.  
**Overlay, не сторінка:** `M-01 Create Issue`, із `M-01-V` validation state.  
**Не продуктова сторінка:** `S-01 Authentication boundary` — placeholder; не проєктуй login UI.  
**Не продуктова сторінка:** `REF-01 Review Notes` — службові анотації **поза** продуктовими frames.

Release MVP: **US-01 Create Issue, US-02 View Issues, US-03 Assign Issue, US-04 Set Priority, US-05 Track Progress, US-06 Add Comment, US-07 Update Status, US-08 View Important Open Issues**. Фільтр Important означає **High або Critical та status ≠ Closed**; `Resolved` включати. [AC-08.1–08.4; BR-09/09.1]

### 3.1. Обов'язкові дані та точні значення

| Сутність/контроль | Погоджені значення або поля | Джерело |
|---|---|---|
| Issue на S-03 | `ID`, `Title`, `Description`, `Status`, `Priority`, `Assignee` якщо є, `Author`, `Created at` | US-01/02, AC-02.4 |
| Рядок списку | `ID`, `Title`, `Status`, `Priority`, `Assignee` якщо призначений | AC-02.2, AC-05.3 |
| Tabs | `All`, `Important` | D-01; US-08 |
| Основний CTA списку | `Create Issue` в **спільній шапці** у всіх станах, включно з Empty | D-01, D-10 |
| Modal | `Title`, `Description`, `Create`, `Cancel` | US-01; D-09 |
| Валідація порожнього Title | **`Title is required`** (точний текст) | BDD US-01; AC-01.2 |
| Priority display | `Not Set` для початкового незаданого; встановлювані **лише** `Low`, `Normal`, `High`, `Critical` | BR-04–06; D-03 |
| Status | `Open`, `In Progress`, `Resolved`, `Closed` | BR-03, BR-07/08.1 |
| Підтвердження змін | Окремий `Apply` біля **Assignee**, **Priority**, **Status** | D-06 |
| Comments | текст, author, date/time; input + submit; точний напис submit **TBD** | US-06, AC-06.1–06.5 |
| Повернення | `Back` (рекомендований короткий UI-label; сама дія погоджена) | D-07; Screen Map T-16/17 |

`Not Set` — **не** варіант вибору після встановлення priority і **не** `Low`. Відсутній assignee — валідні дані, не помилка. Для порожнього assignee нейтральний display `—` або `Unassigned` — **лише RECOMMENDED/TBD**, не погоджений точний copy. Дані ID, author, created-at після Create — системні, не поля modal. [AC-01.4/01.5; D-03/04]

## 4. Список рівно 15 основних frames — точні назви

У Figma встановлюй **наведений текст повністю як ім'я frame**; дужки `[...]` нижче не є частиною назви. Внутрішні frames для компонентів дозволені, але не зараховуються як нові основні screen frames.

| F-ID | Точне ім'я Figma frame | Screen / component state | Акцент |
|---|---|---|---|
| F-01 | `F-01 — S-01 — Authentication Boundary` | S-01 | Placeholder |
| F-02 | `F-02 — S-02-A — Issues List — All` | S-02-A | All, є рядки |
| F-03 | `F-03 — S-02-B — Issues List — Important` | S-02-B | Тільки відповідні issues |
| F-04 | `F-04 — S-02-C — Issues List — Empty` | S-02-C | Empty у вибраній вкладці |
| F-05 | `F-05 — M-01 — Create Issue Modal` | M-01 + S-02 background | Create/Cancel |
| F-06 | `F-06 — M-01-V — Create Validation Error` | M-01-V + S-02 background | Title required |
| F-07 | `F-07 — S-03 — Newly Created Issue` | S-03; CS-ASSIGNEE-NONE; CS-PRIORITY-NOTSET | Open / Not Set / no assignee |
| F-08 | `F-08 — S-03 — Assignee and Priority Applied` | S-03 після Apply | Обидві зміни підтверджено |
| F-09 | `F-09 — S-03-ST-OPEN — Issue Details` | S-03-ST-OPEN | Actor є assignee |
| F-10 | `F-10 — S-03-ST-INPROGRESS — Issue Details` | S-03-ST-INPROGRESS | Open → In Progress |
| F-11 | `F-11 — S-03-ST-RESOLVED — Issue Details` | S-03-ST-RESOLVED | Два allowed targets |
| F-12 | `F-12 — S-03-ST-CLOSED — Issue Details` | S-03-ST-CLOSED | Немає status transitions |
| F-13 | `F-13 — S-03 — Comment Success` | CS-COMMENT-SUCCESS | Новий comment із author/time |
| F-14 | `F-14 — S-03 — Comment Error` | CS-COMMENT-ERROR | Помилка, без нового comment |
| F-15 | `F-15 — S-03-R-DISABLED — Restricted Controls` | S-03-R-DISABLED | Видимі disabled-дії |

**REF-01** створи як окрему **непродуктову секцію/notes board**, не як 16-й основний продуктово-демонстраційний frame. Назва секції: `REF-01 — Review Notes (Non-product)`. За потреби створи додаткові **component variants**, а не нові продуктові сторінки. [Screen Map §2 F-01–F-15; D-05/08]

## 5. Детальні інструкції до кожного frame

### F-01 — S-01 Authentication Boundary

**REQUIRED:** порожня нейтральна поверхня з **єдиним змістовим підписом** `Authentication entry — mechanism TBD`. Не додавай input-ів, email, password, SSO, recovery, login-кнопки, logout або user switcher. Це boundary marker, не форма. Прототипна стартова точка — F-02 **для вже автентифікованого користувача**; F-01 не моделює шлях фактичної автентифікації. [BR-01; NFR-02; D-02/08; S-01; TC-00]

**RECOMMENDED:** розмісти короткий рядок по центру й поза frame службову note `Prototype assumes authenticated team member`. Не вставляй note в продуктовий екран.

### F-02 — S-02-A Issues List / All

**Компонування (RECOMMENDED):** спільна шапка `Issues` з праворуч розміщеною **enabled** кнопкою `Create Issue`; нижче — tabs `All` (selected) / `Important`; далі таблиця на всю доступну ширину: `ID | Title | Status | Priority | Assignee`. Текстові issue-рядки є клікабельними entry points у S-03. Список відображає **всі** тестові issues включно з `Closed`, `Not Set` та непризначеними. Не додавай search, sort, pagination, filter chips, create inline, delete, edit або керування статусом у рядках. [US-02/05; AC-02.1–02.3, AC-05.1/05.3; D-01/03/10]

**Поведінка:** `Important` → F-03 (або Empty Important variant F-04); `Create Issue` → F-05 поверх All; вибір відповідного рядка → відповідна S-03; `Back` із деталей із origin All → All з актуальними даними. [T-01/05/07/16; D-07/09]

### F-03 — S-02-B Issues List / Important

Копія shell F-02 з `Important` selected. Та сама таблиця і той самий `Create Issue` в header. Показати тільки issues з **priority High/Critical** і статусом **Open / In Progress / Resolved**. Серед рядків обов'язково має бути принаймні один `Resolved`; **жодного Closed**, Low, Normal, Not Set. `All` повертає до F-02; натиснення рядка відкриває S-03 із `originListState=Important`. [US-08; AC-08.1–08.4; BR-09/09.1; D-01/07/10; T-06/07/17]

### F-04 — S-02-C Empty

Зберігай **спільні header, кнопку `Create Issue`, обидві tabs та активну вкладку**. В області таблиці не має рядків; покажи стриманий текст, наприклад `No issues to display` — **RECOMMENDED copy, TBD**, не затверджена вимога. За замовчуванням демонструй `Important` selected за наявності в All тільки Low/Normal/Not Set або Closed; **створи component variant `Empty / All`** для повністю порожньої бази. Не називай Empty Important «no issues in system». Не додавай другу Create-кнопку всередині Empty. Кнопка в шапці **enabled для Team Member і Team Lead**. [AC-02.5, AC-08.1–08.4; D-10; TC-09/31; T-18]

**Поведінка:** `Create Issue` → M-01 із запам’ятованою вкладкою та Empty-контекстом; `Cancel` → той самий Empty; успішний Create → F-07; Back із нової issue в Empty All може вже показувати рядок у All, а в Empty Important нова Not Set issue залишається поза фільтром. [D-07/09/10; TC-06/31]

### F-05 — M-01 Create Issue Modal

Відобрази затемнену **grayscale** підкладку **поточного** S-02 (приклад — All), над нею centered modal. В modal: заголовок `Create Issue` (RECOMMENDED для назви modal), label `Title` з single-line text input, label `Description` із multiline textarea, унизу **дві** кнопки `Cancel` та `Create`. Явно познач поля як required без вигаданого формату/лімітів. У modal **не** додавай ID, assignee, priority, status, author, created-at, attachments. [US-01; AC-01.1–01.5; D-01/03/04/09; T-01/03/04]

**Поведінка:** `Cancel` → origin S-02 (All/Important/Empty) **без нової issue**; валідний `Create` → **F-07 S-03 нової issue**, modal закритий; не повертай одразу до списку. Для demo передбач component variants `Modal / From All`, `Modal / From Important`, `Modal / From Empty` (один основний F-05). Не вигадуй Esc/overlay-click закриття або autosave чернетки. [D-09; U-10]

### F-06 — M-01-V Create Validation Error

Той самий modal, поля й кнопки; Title порожнє, під ним точний текст **`Title is required`**. Важливо: `Create` з порожніми полями не створює issue; modal залишається відкритим. За порожнього `Description` познач поле як невалідне; **текст Description error не визначений** — можна поставити зовнішню note `Description required — exact error copy TBD`, а не видавати вигаданий текст за джерельний. Показуй виправлення Title/Description як компонентний сценарій; після обох валідних значень Create може вести до F-07. `Cancel` повертає до origin. [AC-01.2/01.3; BDD US-01; D-09; TC-02/03/04/05]

### F-07 — S-03 Newly Created Issue

**REQUIRED details content:** верхній `Back`; заголовок issue та ID; секція з незмінними для редагування `Title`, `Description`, `Author`, `Created at`; окремі row/section для `Assignee`, `Priority`, `Status`; `Comments` із наявними записами або порожньою секцією та полем додавання comment. Початкові значення **Status `Open`, Priority `Not Set`, Assignee відсутній**, новий фіктивний ID, author = actor, створено у фіктивний час. `Title` і `Description` лише читаються — **ніякого edit**. [US-01/02/05/06/07; AC-01.4/01.5, AC-02.4, AC-07.1; D-03/04/09]

**RECOMMENDED layout:** зліва основний блок Description і нижче Comments; справа компактна вертикальна колонка з метаданими/трьома контролями; повний текст `ID`, `Author`, `Created at` читається без прихованих меню. **Ролі:** для actor `TL-C` assignee і priority selectors + їхні Apply enabled; status disabled для **всіх** поки немає assignee. Якщо actor Team Member, disabled і assignee/priority. `Not Set` **display-only initial state**, не reset option. [D-04–06; AC-07.4; TC-01/21]

### F-08 — S-03 Assignee and Priority Applied

Та сама S-03, але **після двох окремих Apply** Team Lead: assignee показує **одного** конкретного team member (наприклад TM-A), priority — `High`; status лишається `Open`, доки його окремо не змінить поточний assignee. Не показуй одну спільну кнопку Save. Візуалізуй поточне підтверджене значення в одному місці, а поруч control із власним `Apply`. Додатково в компонентах покажи `Before Apply / Selection pending` так, щоб старе збережене значення **ще відображалось**; натискання потрібного Apply оновлює тільки відповідне поле. Team Lead не отримує status-права для issue, призначеної TM-A. [US-03/04; AC-03.1–03.4 (aliases), AC-04.1/04.2; D-04/05/06; TC-10/11/14/22]

### F-09 — S-03-ST-OPEN

Prepared issue **MIT-101** (`Priority Critical`, `Assignee Maya Chen`), actor **TM-A = current assignee**; `Status Open`. Status selector enabled і пропонує **лише** `In Progress`; поруч status-specific `Apply`. `Resolved` і `Closed` **не** пропонуються, не показуй прямого переходу. Для TM-A assignee і priority selectors/Apply visible disabled; Comments enabled. Звідси status Apply → F-10. [BR-08/08.1; US-07; AC-07.2–07.5; D-05/06; T-10; N-03]

### F-10 — S-03-ST-INPROGRESS

Та сама **MIT-101** / той самий actor-assignee, але наступний демонстраційний момент; `Status In Progress`. Наступний дозволений target лише `Resolved`, з власним Apply → F-11. `Open` і `Closed` заборонені, не пропонувати. Зміни assignee/priority залишаються role gated. [BR-08.1; AC-07.2–07.5; D-05/06; T-11; N-04]

### F-11 — S-03-ST-RESOLVED

Та сама **MIT-101** у наступний демонстраційний момент, `Status Resolved` (**не** Closed). Status selector для поточного assignee пропонує **рівно** два target-и: `In Progress` і `Closed`; Apply target `In Progress` → F-10; Apply target `Closed` → F-12. Для High/Critical issue її все ще включають в Important. [BR-08.1, BR-09.1; AC-08.1/08.2/08.4; D-06; T-12/13]

### F-12 — S-03-ST-CLOSED

Та сама **MIT-101** після переходу з Resolved: показуй `Status Closed`; selector **visible disabled** та відповідний `Apply` disabled, **навіть якщо actor — assignee**: вихідних переходів немає. Comments лишаються доступними обом ролям; assignee/priority controls підпорядковані своїм звичайним рольовим правам. `Back` із origin Important → Important, де цієї issue **немає** (можливо Empty). `Back` із origin All → All, де Closed issue залишається. [BR-08.1/09.1; AC-08.4; D-05/07; T-13/16/17; N-05]

### F-13 — S-03 Comment Success

У Comments покажи baseline comment(s) та **новий успішно доданий** comment з **текстом, author та date/time**; current actor може бути Team Member/Lead, assignee неважливий, навіть Closed issue допускає comments. Залишайся на S-03; status/priority/assignee не змінюються. Точний label кнопки submit у джерелі **не зафіксований**; для wireframe використовуй `Add Comment` (**RECOMMENDED, TBD**) і познач це в REF-01. Не роби обов'язковим toast. Не стверджуй real persistence. [US-06; AC-06.1–06.4; D-08; T-14; TC-23/25]

### F-14 — S-03 Comment Error

Та сама Comments section і baseline comments, але **невдалий новий comment не доданий**. Показуй видиме inline error message, наприклад `Could not save comment` (**RECOMMENDED placeholder; exact copy TBD**). Не показуй автора/часу для нібито збереженого невдалого comment; не змінюй інші дані issue. Не задавай непогоджену retry policy або обов'язкове очищення/збереження поля. [AC-06.5; D-08; T-15; TC-26]

### F-15 — S-03-R-DISABLED Restricted Controls

Демонстраційний actor **TM-B (Team Member, не поточний assignee)**, issue призначено TM-A. Усі три блоки `Assignee`, `Priority`, `Status` видимі з value/selector/`Apply`, але **кожен selector та його Apply disabled**. `Comments` input + submit залишаються enabled, `Back` enabled; дані можна читати. Заборонений клік **нічого не змінює і не викликає повідомлення про успіх**. Додай **зовнішню** note REF-01 з поясненням: Member не assign/priority; non-assignee не status, навіть Team Lead. В component variants окремо покажи `Team Lead / non-assignee`: assignee + priority enabled, status disabled; `Team Member / assignee`: тільки status enabled за наявності allowed transition. [US-03/04/07; AC-03.3 (alias), AC-04.2, AC-07.4; D-05/06; N-01/02; TC-13/17/29/30]

## 6. Повторно використовувані компоненти та variants

Створи на окремій **непродуктовій** component shelf / section (не додає продуктову сторінку) ці майстер-компоненти з Auto Layout, текстовими props, variants і зрозумілими layer names:

| Компонент (ім'я) | Основні variants / властивості | Де використовувати |
|---|---|---|
| `CMP / List Header` | CTA enabled (включно з Empty), `scope=All/Important` | F-02/03/04, підкладка F-05/06 |
| `CMP / Tab` | `All/Important`; `active/inactive` | S-02 |
| `CMP / Issue Row` | values: ID, Title, Status, Priority, Assignee; hover optional | F-02/03 |
| `CMP / Empty List` | `scope=All/Important`; neutral copy TBD | F-04 |
| `CMP / Button` | `primary/secondary`; `enabled/disabled`; назви Create Issue/Create/Cancel/Apply/Back | Усі потрібні frames |
| `CMP / Text Input` | `default/filled/error/disabled`; required label | M-01 |
| `CMP / Text Area` | `default/filled/error`; label | M-01, Comments |
| `CMP / Create Modal` | `default/title-error/description-invalid`; `origin=All/Important/Empty` | F-05/06 |
| `CMP / Issue Metadata` | ID, Author, Created at, Title/Description read-only | F-07–15 |
| `CMP / Assignment Field` | `none/assigned`, `enabled/disabled`, `pending/applied`; власний Apply | S-03 |
| `CMP / Priority Field` | `Not Set/Low/Normal/High/Critical`, `enabled/disabled`, `pending/applied`; без reset | S-03 |
| `CMP / Status Field` | `Open/In Progress/Resolved/Closed`, `assignee/non-assignee`, `enabled/disabled`, `allowedTargets`, власний Apply | S-03 |
| `CMP / Comment Entry` | baseline/success/error; author/time | F-07–15 |
| `CMP / Comment Composer` | empty/filled/submit-state (не вигадувати поведінку) | F-07–15 |

**Технічні вимоги до компонентів:** instances, не окремо намальовані дублікати; внутрішні назви на кшталт `Header / Create Issue`, `Details / Status / Apply`, `Comments / Entry / Timestamp`; roles/variants називай явно. `Apply` у кожному із **трьох** полів фізично окремий і прив’язаний тільки до відповідного selector. Не додавай fourth global Save. [D-05/06]

## 7. Roles, permissions і demonstrative data

### 7.1. Матриця доступів (REQUIRED)

| Дія | TM-A/TM-B, коли assignee | TM-A/TM-B, коли non-assignee | TL-C, коли assignee | TL-C, коли non-assignee |
|---|---|---|---|---|
| View list / details | enabled | enabled | enabled | enabled |
| Create / Cancel | enabled | enabled | enabled | enabled |
| Assign/Reassign + Apply | **disabled** | **disabled** | enabled | enabled |
| Change Priority + Apply | **disabled** | **disabled** | enabled | enabled |
| Change Status + Apply | enabled¹ | **disabled** | enabled¹ | **disabled** |
| Add/View Comments | enabled | enabled | enabled | enabled |
| Back, All/Important | enabled | enabled | enabled | enabled |

¹ Лише якщо є **дозволений вихідний перехід**; `Closed` → disabled. Без assignee status disabled для **всіх**. Team Lead **не може** змінювати status чужої issue. Після reassign право status переходить новому assignee. Самопризначення TL-C — **UNRESOLVED**; якщо потрібно показати TL-C-assignee, використовуй **підготовлену** issue, не демонструй self-assignment як погоджену дію. [Screen Contracts §3, §4.6; D-04–06; TC-21/30]

### 7.2. Підготовлені фіктивні акаунти

- `TM-A` — **Maya Chen**, Team Member.
- `TM-B` — **Alex Rivera**, Team Member.
- `TL-C` — **Jordan Lee**, Team Lead.

Ці імена — **RECOMMENDED fictional test data**, не реальні акаунти/користувачі та не нові ролі. Actor визначається анотацією біля frame, **не** новим role-switcher усередині продукту. [BR-01; D-08]

### 7.3. Підготовлений набір issues

Нижче приклади для screenshot-ready frames; ID і timestamp — **вигадані** з рекомендованим, а не нормативним форматом. Для F-02 використай кілька рядків, щоб покрити різні статуси та значення priority; для F-03 лише рядки з позначкою `Yes`.

| ID | Title | Status | Priority | Assignee | Important? |
|---|---|---|---|---|---|
| MIT-101 | Login page fails after redirect | Open | Critical | Maya Chen | Yes |
| MIT-102 | Search results show duplicate records | In Progress | High | Maya Chen | Yes |
| MIT-103 | Exported report misses totals | Resolved | High | Alex Rivera | Yes |
| MIT-104 | Incorrect spacing in settings | Open | Low | — | No |
| MIT-105 | Tooltip covers the save control | In Progress | Normal | Alex Rivera | No |
| MIT-106 | Session warning not shown | Closed | Critical | Maya Chen | No |
| MIT-107 | Intermittent loading message | Open | Not Set | — | No |

**Примітка до набору даних:** таблиця фіксує **початковий snapshot**. Подальші статуси MIT-101 у F-10–F-12 — наступні моменти демонстрації, а не паралельні дублікати MIT-101 в одному списку.

`MIT-108` (F-07): `Notifications do not update after refresh`; Description `The notifications list continues to show older items after a browser refresh.`; author `Alex Rivera` (якщо actor TM-B); created-at `14 Oct 2026, 10:20` (format RECOMMENDED); status `Open`, priority `Not Set`, assignee absent. **Не** додавати comment у нову issue автоматично. F-08 може показати MIT-108 з assignee Maya Chen та priority High **після двох окремих Apply** від TL-C. Для F-09–F-12 використовуй **MIT-101** (`Login page fails after redirect`; початкові `Status Open`, `Priority Critical`, `Assignee Maya Chen`; actor **TM-A / Maya Chen**). **F-09 → F-10 → F-11 → F-12 — послідовні демонстраційні стани тієї самої MIT-101 у різні моменти часу, а не чотири одночасні записи:** `Open` → `In Progress` → `Resolved` → `Closed`. У F-09, F-10 і F-11 MIT-101 входить до **Important**, оскільки priority `Critical` і status ≠ `Closed`; у F-12 вона **виключена з Important**, але залишається в **All**. **MIT-102** зберігає початковий статус `In Progress` і використовується лише як окремий рядок демонстраційного набору даних, не як початкова issue статусного ланцюжка. Comments samples: `I can reproduce this in the latest build.` — Maya Chen, `14 Oct 2026, 10:35`; новий успішний `I have attached the steps to our internal notes.` — Alex Rivera, `14 Oct 2026, 10:42` (**лише текст коментаря, жодних вкладень у продукті**). У F-14 цей другий текст **не** додавати до comments list.

**Важливо для test data:** F-04 `Important Empty` використовує інший prepared dataset (`MIT-104`, `MIT-105`, `MIT-106`, `MIT-107`), ніж F-03; не видавай суперечливі demo frames за одну live-сесію з реально синхронізованою БД. Для варіанта `All Empty` використай нуль issues. [D-08; AC-02.5; TC-09/27/31]

## 8. Стани й правила зміни даних

### 8.1. Status transition matrix

| Current | Дозволено запропонувати поточному assignee | Result after Status Apply | Інші варіанти |
|---|---|---|---|
| Open | In Progress | In Progress | Не пропонувати |
| In Progress | Resolved | Resolved | Не пропонувати |
| Resolved | In Progress; Closed | Вибрана ціль | Не пропонувати Open |
| Closed | — | Немає зміни | Selector + Apply disabled |

Проміжний вибір **не** змінює поточний status до Apply. Заборонені status targets не потрібно зображати disabled-опціями меню; їх **не пропонують**. Натомість коли actor не має прав, **весь selector і його Apply видимі й disabled**. [BR-08.1; D-05/06; Screen Contracts §2.1]

### 8.2. Important filtering

`Important = (Priority ∈ {High, Critical}) AND (Status ≠ Closed)`; лише `Open`, `In Progress`, `Resolved`. `Not Set`, `Low`, `Normal` не входять за будь-якого status; `Closed` не входить навіть з `Critical`. All завжди включає Closed. Після Apply priority/status Figma demo має представляти **оновлений** склад вкладки при поверненні; якщо останнє Important issue перестало відповідати — показати Empty Important, але вкладку не скидати. [BR-09/09.1; AC-08.1–08.4; D-07; TC-27/28]

### 8.3. Success, validation, error, empty, disabled

| Стан | Обов'язковий результат у wireframe | Не вигадувати |
|---|---|---|
| Create valid | Modal закрито; нова issue на S-03, Open / Not Set / no assignee | Toast, back-to-list, backend |
| Title empty | `Title is required`; M-01 відкрито; no issue | Інші точні validation messages |
| Description empty | Required validation, no issue, modal відкрито; error copy TBD | Уявний затверджений текст |
| Create Cancel | Modal закрито, той самий All/Important/Empty context, no issue | Збереження draft, додатковий confirm |
| Assignment/Priority Apply | Лише своє поле оновлено, лишається S-03 | Autosave/global Save/reset/clear |
| Status Apply | Лише дозволений перехід; лишається S-03 | Skip states, restart Closed |
| Comments empty submit | Comment не створюється; exact UI response TBD | Фіксований alert message |
| Comment success | Новий comment із текстом, author, timestamp | Обов'язковий toast, реальна persistence |
| Comment error | Видима помилка, нового comment немає | Автоматичний retry або вигадана error recovery |
| Empty All/Important | Нуль рядків, scope збережено, Create Issue enabled | Додаткова empty CTA, load-error підміна |
| Disabled controls | Видимі, неактивні; **не** тригерять змін | Tooltip/permission dialog як продуктову функцію |

[US-01–08; AC-01.1–01.5, AC-06.1–06.5; D-03–10; Screen Contracts §4]

## 9. Підготовка до clickable prototype — transition map

Нижченаведене — **специфікація майбутніх зв'язків**, не твердження про вже створений prototype. Для розгалужень All/Important/Empty і picker target використовуй interactive variants або окремі **демонстраційні** connections без додавання нових продуктових сторінок. Якщо один F-05 не може одночасно коректно пам'ятати три origin, створи overlay variant/instances в межах відповідного frame; не обіцяй реальної persistence чи умовної логіки.

| T-ID | From / trigger | To (показаний frame або state) | Головний контракт |
|---|---|---|---|
| T-01 | F-02/F-03/F-04 → `Create Issue` | F-05 / modal overlay з origin | Enabled навіть Empty; D-01/10 |
| T-02 | F-05 → invalid `Create` | F-06 | No issue, `Title is required`; AC-01.2/01.3 |
| T-03 | F-05/F-06 (corrected) → valid `Create` | F-07 | Новий S-03; Open, Not Set, no assignee; D-09 |
| T-04 | F-05/F-06 → `Cancel` | F-02 або F-03 або F-04 за origin | Без створення; D-09 |
| T-05 | F-02 → `Important` | F-03 або F-04 / Important variant | High/Critical not Closed; US-08 |
| T-06 | F-03 → `All` | F-02 або F-04 / All variant | All issues; US-02 |
| T-07 | F-02/F-03 → issue row | відповідний S-03 (F-07–15 за dataset) | Origin All/Important; AC-02.3/02.4 |
| T-08 | S-03 Team Lead → Assignee `Apply` | S-03 variant / F-08 | Призначити/перепризначити одного; D-04/06 |
| T-09 | S-03 Team Lead → Priority `Apply` | S-03 variant / F-08 | Встановити Low/Normal/High/Critical; D-03/06 |
| T-10 | F-09 Open → `In Progress` + `Apply` | F-10 | Лише current assignee |
| T-11 | F-10 In Progress → `Resolved` + `Apply` | F-11 | Лише current assignee |
| T-12 | F-11 Resolved → `In Progress` + `Apply` | F-10 | Reopen work |
| T-13 | F-11 Resolved → `Closed` + `Apply` | F-12 | Після Back виключити з Important |
| T-14 | S-03 comment submit / prepared success | F-13 | Comment додано з author/time |
| T-15 | S-03 comment submit / prepared failure | F-14 | Помилка, comment не додано |
| T-16 | S-03 → `Back`, origin All | F-02 або F-04 / All | All з актуальними даними; D-07 |
| T-17 | S-03 → `Back`, origin Important | F-03 або F-04 / Important | Important з актуальними даними; D-07 |
| T-18 | S-02 scope з 0 результатів | F-04 / відповідний scope | Valid Empty, не load error |

**Не створювати prototype links для:** Team Member assign/priority (N-01); non-assignee status (N-02); Open → Resolved/Closed (N-03); In Progress → Closed (N-04); виходів із Closed (N-05); empty comment як success (N-06). [Screen Map §4–5]

## 10. Figma canvas: структура, розташування й найменування

**RECOMMENDED canvas layout**, одна Figma page `Mini Issue Tracker / MVP Wireframes`:

- **Section 01 — Entry & Lists:** F-01, F-02, F-03, F-04 в один горизонтальний ряд, порядок зліва направо.
- **Section 02 — Create Flow:** F-05, F-06, F-07 зліва направо; покажи modal на автентичній підкладці S-02.
- **Section 03 — Assignment/Priority & Status:** F-08, F-09, F-10, F-11, F-12 — послідовно, за потреби перенеси F-11/F-12 на наступний canvas ряд без зміни ID.
- **Section 04 — Comments & Permissions:** F-13, F-14, F-15.
- **Section 05 — Components:** component shelf з master components і variants, **не** продуктова сторінка.
- **Section REF-01 — Review Notes (Non-product):** нижче/праворуч із чіткою позначкою `NOT PRODUCT UI`; annotations не мають потрапляти до screen frames.

**RECOMMENDED:** відступ між основними frames 160–240 px, між секціями 280–400 px; section headers поза frames; малі технічні labels `actor=TM-A`, `origin=Important`, `prepared data` — поза продуктом. Ієрархія шарів усередині кожного screen: `Screen / Header`, `Screen / Navigation`, `Screen / Main`, `Screen / Sidebar` (за наявності), `Screen / Comments`, `Screen / Overlay` (тільки M-01), а для контролів — `Field / Label`, `Field / Value`, `Field / Selector`, `Field / Apply`, `Field / State`. Ім'я кожного **основного** frame строго як у §4.

## 11. REF-01 — обов'язкові review notes поза UI

У `REF-01 — Review Notes (Non-product)` явно зазнач:

1. **D-05:** disabled controls показано навмисно; це не підтвердження серверної авторизації. Пояснення не реалізовані tooltip у продукті.
2. **D-08:** усі issues, users, comments, ID та timestamps — fake prepared data; показані success/error transitions не підтверджують працюючий backend, auth, DB, save або persistence.
3. **D-02:** authentication method TBD; немає login form.
4. **U-01/U-04:** whitespace-only, максимальна довжина, format, Description validation copy, comment input після success/failure і retry — unresolved.
5. **U-02/U-05/U-07:** empty/error copy, дата/час/локаль, ID presentation і порожній assignee placeholder — нейтральні UI-рекомендації, не requirements.
6. **U-06:** self-assignment Team Lead unresolved; prepared TL-C-assignee допустимий лише як заздалегідь змодельований стан.
7. **U-09/U-10/U-11:** Apply без зміни, pending selection при Back, технічні save conflicts/failures, double-submit, Esc, draft handling, синхронізація між сесіями — не моделювати як затверджене UX.
8. **Scope:** Attachments US-09 Deferred; AI SR-10/SR-11 Future; search, sort, pagination, delete, edit issue, change history, custom filters та окремі pages для керування не включати.

## 12. Обмеження і явно заборонені доповнення

**DO NOT GENERATE:** file upload або paperclip CTA; AI suggestions/auto-priority/category; реальну форму login/SSO/password, role picker/logout; Assignment/Priority/Status/Comments pages; dashboard, profile, settings, notifications center, reporting; search/sorting/filter widgets, pagination; delete issue; edit Title/Description; clear assignee, reset priority до Not Set; workflow status targets поза таблицею; global Save; toast/tooltip/confirmation dialog як нібито погоджені функції; API/backend/DB/persistence або production-ready UI. [Input Pack §2; Screen Contracts §1/7; D-01–10]

**Не плутай:** `Resolved` не означає `Closed`; у S-02-B `Resolved High/Critical` видимий. В Issue Details лишається Comments і для Closed. Дія status залежить **від current assignee**, не від авторства або посади Team Lead. [BR-08/09.1; AC-07.4]

## 13. Критерії оцінювання створених макетів

Це вимоги до результату етапу F1, а не протокол фактичного тестування. Підсумкові результати наведено у P1 Test Record, прогоні 07.11.2026 та звіті G6.

### 13.1. Кількість і структура

- Рівно **15 основних frames F-01–F-15**, з точними назвами §4; додаткові instances/variants не видаються за нові продуктові screens.
- S-02 — одна сторінка з All/Important/Empty; S-03 — одна сторінка з усіма керуваннями; M-01 — overlay; F-01 — boundary only; REF-01 поза продуктом.
- Desktop-first, grayscale, low-fi; editable frames/components; читабельний, послідовний layout і names.

### 13.2. UI і дані

- F-02/F-03 показують `ID, Title, Status, Priority, Assignee`; F-03 включає Resolved High/Critical та виключає Closed.
- F-04 зберігає активну вкладку; `Create Issue` у спільній шапці enabled; немає другого empty CTA.
- F-05/F-06 містять тільки required `Title`, `Description`, `Create`, `Cancel`; Title error **`Title is required`**.
- F-07: нова issue `Open`, `Not Set`, без assignee, із ID/Author/Created at; modal закритий.
- F-08: тільки Team Lead встановлює/reassign assignee і priority, через **два окремі** Apply; немає reset/clear.
- F-09–12 точно відображають чотири дозволені status transitions і відсутність виходів із Closed; status тільки current assignee.
- F-13: saved comment + author + timestamp; F-14: error без доданого comment.
- F-15: forbidden controls **visible/disabled**, Comments лишаються доступні; пояснення в REF-01.

### 13.3. Навігація і coverage

- Map T-01–T-18 описано та можна під'єднати без вигаданих сторінок; Cancel повертає origin; Create → S-03; Back зберігає All/Important і оновлений вміст.
- Відсутні переходи N-01–N-06; статусні target-и не порушують BR-08.1.
- Усі 8 US та **33 AC** мають місце перевірки: US-01 5; US-02 5; US-03 4 локальні alias; US-04 2; US-05 3; US-06 5; US-07 5; US-08 4. Зіставляти з Screen Contracts §5 і G4 Plan Review §3, не стверджувати, що TC-00–TC-31 виконано.
- Unresolved copy, technical behavior і recommendation явно марковані; немає deferred/future та додаткового issue tracker functionality.

**Очікуваний результат F1:** набір редагованих low-fidelity wireframes, компоненти та REF-01 для наступного створення клікабельного прототипу. Критерії виконання й межі перевірки визначені окремими журналами P1 та G6.

---


## Фінальні посилання Figma

### Figma — макети та клікабельний прототип

**Фінальний файл:** `Mini Issue Tracker — Simplified Prototype` (`J4cFxVfdTPvCdLarVS5BVs`).

- [Редагований проєкт Figma](https://www.figma.com/design/J4cFxVfdTPvCdLarVS5BVs/Mini-Issue-Tracker)
- [Прототип: початковий список All](https://www.figma.com/proto/J4cFxVfdTPvCdLarVS5BVs/Mini-Issue-Tracker?node-id=2-5493&page-id=0%3A1&starting-point-node-id=2%3A5493&scaling=scale-down)

Прототип демонструє підготовлені стани навчальної системи. Доступ за посиланням визначається правами Figma; ZIP-архів не замінює спільний доступ до файлу.
