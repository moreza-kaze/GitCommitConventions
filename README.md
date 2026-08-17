<div dir="rtl">

# 📝 راهنمای پیشوندهای پیام Commit در Git

استفاده از پیشوند در پیام‌های Commit کمک می‌کند فقط با دیدن عنوان Commit بفهمیم **چه تغییری در پروژه انجام شده است**.

این روش بر اساس استاندارد **Conventional Commits** است و باعث می‌شود تاریخچه Git مرتب‌تر، خواناتر و قابل‌فهم‌تر باشد.

---

## ⚡ مرجع سریع

| پیشوند     | چه زمانی استفاده کنیم؟                      |
| ---------- | ------------------------------------------- |
| `feat`     | وقتی قابلیت جدید اضافه کرده‌ایم             |
| `fix`      | وقتی یک باگ را برطرف کرده‌ایم               |
| `chore`    | برای کارهای جانبی و نگهداری پروژه           |
| `docs`     | وقتی فقط مستندات تغییر کرده‌اند             |
| `style`    | تغییر فرمت و ظاهر کد بدون تغییر منطق        |
| `refactor` | تغییر ساختار کد بدون تغییر رفتار            |
| `perf`     | برای بهتر کردن Performance                  |
| `test`     | اضافه یا اصلاح کردن تست‌ها                  |
| `build`    | تغییر Build، Dependencies یا ابزارهای Build |
| `ci`       | تغییر تنظیمات CI/CD                         |
| `revert`   | برگرداندن تغییرات یک Commit قبلی            |

---

# 📚 توضیحات و مثال‌ها

## ✨ `feat`

وقتی یک **قابلیت جدید** به پروژه اضافه می‌کنیم.

مثلاً:

* اضافه کردن Login
* اضافه کردن Dark Mode
* اضافه کردن صفحه کاربران
* اضافه کردن Search

**مثال:**

<div dir="ltr">

```text
feat: add dark mode support
```

</div>

اگر بخواهیم مشخص کنیم تغییر مربوط به کدام بخش است:

<div dir="ltr">

```text
feat(auth): add login with OTP
```

</div>

---

## 🐛 `fix`

وقتی یک **باگ یا مشکل موجود** را برطرف می‌کنیم.

مثلاً:

* رفع مشکل Login
* رفع Crash برنامه
* رفع نمایش اشتباه اطلاعات
* رفع مشکل Validation فرم

**مثال:**

<div dir="ltr">

```text
fix: prevent crash on application startup
```

</div>

مثال با Scope:

<div dir="ltr">

```text
fix(auth): resolve login redirect issue
```

</div>

---

## 🔧 `chore`

برای کارهای جانبی و نگهداری پروژه که معمولاً قابلیت جدیدی به برنامه اضافه نمی‌کنند.

مثلاً:

* آپدیت پکیج‌ها
* حذف فایل‌های اضافی
* تغییر تنظیمات ابزارها
* مرتب کردن تنظیمات پروژه

**مثال:**

<div dir="ltr">

```text
chore: update project dependencies
```

</div>

یا:

<div dir="ltr">

```text
chore: remove unused files
```

</div>

---

## 📖 `docs`

وقتی فقط **مستندات پروژه** تغییر می‌کنند.

مثلاً:

* تغییر `README`
* اضافه کردن توضیحات API
* اضافه کردن راهنمای نصب
* اصلاح Documentation

**مثال:**

<div dir="ltr">

```text
docs: add installation guide to README
```

</div>

یا:

<div dir="ltr">

```text
docs(api): add authentication examples
```

</div>

---

## 🎨 `style`

وقتی فقط فرمت و ظاهر کد تغییر می‌کند و **منطق برنامه هیچ تغییری نمی‌کند**.

مثلاً:

* اجرای Prettier
* اصلاح Indentation
* حذف فاصله‌های اضافی
* مرتب کردن فرمت کد

**مثال:**

<div dir="ltr">

```text
style: format code with Prettier
```

</div>

> `style` معمولاً برای تغییر UI یا CSS استفاده نمی‌شود؛ منظور اصلی تغییر Style خود کد بدون تغییر رفتار برنامه است.

---

## ♻️ `refactor`

وقتی ساختار کد را بهتر می‌کنیم ولی **رفتار برنامه تغییر نمی‌کند**.

مثلاً:

* ساده کردن یک Function
* جدا کردن Logic به Hook
* حذف کدهای تکراری
* تغییر ساختار Componentها

**مثال:**

<div dir="ltr">

```text
refactor: simplify authentication logic
```

</div>

یا:

<div dir="ltr">

```text
refactor(user): extract user logic into custom hook
```

</div>

---

## ⚡ `perf`

وقتی تغییری برای **بهبود سرعت یا Performance** برنامه انجام می‌دهیم.

مثلاً:

* کاهش درخواست‌های API
* بهینه کردن Query دیتابیس
* کاهش Re-render
* Lazy Load کردن بخش‌های برنامه

**مثال:**

<div dir="ltr">

```text
perf: reduce unnecessary component re-renders
```

</div>

یا:

<div dir="ltr">

```text
perf(api): cache user requests
```

</div>

---

## 🧪 `test`

وقتی تست جدید اضافه می‌کنیم یا تست‌های قبلی را تغییر می‌دهیم.

مثلاً:

* Unit Test
* Integration Test
* Browser Test
* اصلاح تست خراب

**مثال:**

<div dir="ltr">

```text
test: add login form validation tests
```

</div>

یا:

<div dir="ltr">

```text
test(auth): add tests for login flow
```

</div>

---

## 📦 `build`

برای تغییراتی که مربوط به **Build پروژه یا Dependencies** هستند.

مثلاً:

* تغییر Vite
* تغییر Webpack
* اضافه یا حذف Dependency
* تغییر Dockerfile مربوط به Build

**مثال:**

<div dir="ltr">

```text
build: upgrade Vite to version 8
```

</div>

یا:

<div dir="ltr">

```text
build: add react-query dependency
```

</div>

---

## 🚀 `ci`

برای تغییرات مربوط به **CI/CD** استفاده می‌شود.

مثلاً:

* تغییر GitHub Actions
* تغییر GitLab CI
* تغییر Pipeline
* تغییر مراحل Build و Deploy

**مثال:**

<div dir="ltr">

```text
ci: add automated test stage
```

</div>

یا:

<div dir="ltr">

```text
ci: update GitLab deployment pipeline
```

</div>

---

## ⏪ `revert`

وقتی می‌خواهیم تغییرات یک Commit قبلی را برگردانیم.

**مثال:**

<div dir="ltr">

```text
revert: revert "feat: add dark mode support"
```

</div>

یعنی تغییر مربوط به اضافه شدن Dark Mode برگردانده شده است.

---

# 🎯 ساختار پیشنهادی Commit

بهتر است پیام Commit تا جای ممکن **کوتاه، واضح و مشخص** باشد.

### ساختار ساده

<div dir="ltr">

```text
<type>: <description>
```

</div>

مثال:

<div dir="ltr">

```text
feat: add user profile page
```

</div>

### ساختار با Scope

اگر بخواهیم مشخص کنیم تغییر مربوط به کدام بخش پروژه است:

<div dir="ltr">

```text
<type>(<scope>): <description>
```

</div>

مثال:

<div dir="ltr">

```text
feat(auth): add OTP login
fix(user): resolve profile image upload issue
refactor(api): simplify request handler
test(login): add validation tests
```

</div>

---

# ✅ چند نمونه واقعی

## Frontend

فرض کنیم روی یک پروژه Frontend کار می‌کنیم:

<div dir="ltr">

```text
feat(auth): add login page

fix(auth): resolve invalid token redirect

feat(user): add profile page

refactor(user): extract profile form logic into hook

test(auth): add login validation tests

style: format project with Prettier

chore: update dependencies

build: upgrade Vite

ci: add test stage to GitLab pipeline

docs: update project setup instructions
```

</div>

---

## Backend

فرض کنیم روی یک پروژه Backend کار می‌کنیم:

<div dir="ltr">

```text
feat(auth): add user login API

fix(auth): resolve token expiration issue

feat(user): add user profile endpoint

feat(user): add update profile API

refactor(auth): simplify authentication service

refactor(user): move user validation into service

test(auth): add login API tests

test(user): add user profile endpoint tests

perf(database): optimize user queries

fix(database): resolve duplicate user creation issue

build: update backend dependencies

chore: remove unused packages

ci: add backend test stage to GitLab pipeline

docs(api): add authentication endpoints documentation
```

</div>

---

## 🧩 نمونه Scope در Backend

در پروژه‌های Backend معمولاً `scope` می‌تواند نام بخش یا ماژول پروژه باشد.

مثلاً:

<div dir="ltr">

```text
auth
user
product
order
payment
database
api
notification
```

</div>

### اضافه کردن API ساخت محصول

<div dir="ltr">

```text
feat(product): add create product API
```

</div>

### رفع باگ پرداخت

<div dir="ltr">

```text
fix(payment): resolve failed transaction status
```

</div>

### بهینه‌سازی Queryهای سفارش

<div dir="ltr">

```text
perf(order): optimize order queries
```

</div>

---

## ✅ جمع‌بندی

با رعایت این ساختار، Git History پروژه خیلی مرتب‌تر می‌شود و فقط با دیدن پیام هر Commit می‌توان فهمید:

* چه نوع تغییری انجام شده
* تغییر مربوط به کدام بخش پروژه بوده
* آیا قابلیت جدید اضافه شده یا باگی رفع شده
* آیا تغییر مربوط به تست، Build، CI/CD یا مستندات بوده

در نتیجه بررسی Commitها، Code Review و پیدا کردن تغییرات پروژه بسیار راحت‌تر می‌شود.

</div>


## 📄 License

Copyright © 2026 moreza-kaze. All Rights Reserved.

این محتوا بدون اجازه کتبی صاحب اثر قابل کپی وتغییر در پروژه‌های دیگر نیست.
