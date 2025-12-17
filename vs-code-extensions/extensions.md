# 💻 My VS Code Setup

هذا الريبو يحتوي على **إعدادات وإضافات VS Code** التي أستخدمها لتطوير مشاريع **Front-End (Angular, React) وBack-End (Laravel, PHP)** بكفاءة عالية.

---

## 🔹 1. Extensions

قائمة الإضافات المثبتة (يمكن تثبيتها مرة واحدة باستخدام `extensions.txt`):

### أساسية (General)
- Bracket Pair Colorizer
- Colorizer / Colorize
- Better Comments
- Snippets
- CSS Peek
- Icons / Icon Fonts
- GitLens
- Live Server
- Auto Rename Tag
- Code Spell Checker
- Todo Highlight

### مزامنة وخطوط
- Settings Sync
- Font Awesome Auto-complete

### Angular & Front-End
- Angular Language Service
- HTML Snippets
- CSS IntelliSense
- Angular UI Bootstrap Snippets
- Live Reload

### PHP / Laravel
- PHP Intelephense
- PHP Live Server

### AI Extensions
- AI Angular Auto Complete Code
- IntelliCode
- IntelliCode Completions
- GitHub Copilot

---

## 🔹 2. تثبيت الإضافات دفعة واحدة

```bash
cat extensions.txt | xargs -n 1 code --install-extension
```

> هذا الأمر يثبت جميع الإضافات المذكورة في `extensions.txt` تلقائيًا.

---

## 🔹 3. Settings

يمكنك تضمين ملف `settings.json` مع هذا الريبو ليحوي:
- إعدادات Prettier و ESLint
- إعدادات Live Server و Auto Save
- Theme و Font و Icon Theme المفضلة

---

## 🔹 4. Repo Structure مقترح

```text
vscode-setup/
 ├─ README.md          # هذا الملف
 ├─ extensions.txt     # قائمة الإضافات
 └─ settings.json      # إعدادات VS Code
```

---

✨ هذه الإعدادات تجعل بيئة التطوير جاهزة لأي مشروع Front-End أو Back-End بسرعة وكفاءة 🚀

