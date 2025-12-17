# 🅰️ Angular Toolkit – أساسيات وأوامر مهمة

دليل عملي مختصر لأساسيات Angular والأوامر الشائعة، جاهز للرفع على GitHub كملف **README.md**.

---

## 1️⃣ تثبيت Angular CLI

```bash
npm install -g @angular/cli
ng version
```

---

## 2️⃣ إنشاء مشروع Angular

```bash
ng new my-angular-app
cd my-angular-app
ng serve -o
```

أثناء الإنشاء:
- ✔️ Routing: Yes
- ✔️ CSS / SCSS (اختار اللي تفضله)

---

## 3️⃣ هيكلة المشروع الأساسية

```text
src/
 ├─ app/
 │   ├─ components/
 │   ├─ pages/
 │   ├─ services/
 │   ├─ app.component.ts
 │   ├─ app.module.ts
 │   └─ app-routing.module.ts
 ├─ assets/
 └─ environments/
```

---

## 4️⃣ أساسيات Angular

### Component
```ts
@Component({
  selector: 'app-home',
  templateUrl: './home.component.html',
  styleUrls: ['./home.component.css']
})
export class HomeComponent {}
```

---

## 5️⃣ Data Binding

### One Way Binding
```html
<h1>{{ title }}</h1>
```

### Two Way Binding
```html
<input [(ngModel)]="name" />
```

> لا تنسَ استيراد `FormsModule`

---

## 6️⃣ Directives

```html
<div *ngIf="isLoggedIn">Welcome</div>
<li *ngFor="let item of items">{{ item }}</li>
```

---

## 7️⃣ Services & Dependency Injection

```bash
ng generate service services/auth
```

```ts
@Injectable({ providedIn: 'root' })
export class AuthService {}
```

---

## 8️⃣ Routing

```ts
const routes: Routes = [
  { path: '', component: HomeComponent },
  { path: 'login', component: LoginComponent }
];
```

```html
<router-outlet></router-outlet>
```

---

## 9️⃣ Forms

### Template Driven Forms
```html
<form #f="ngForm" (ngSubmit)="onSubmit(f)">
  <input name="email" ngModel />
</form>
```

### Reactive Forms
```ts
this.form = new FormGroup({
  email: new FormControl('')
});
```

---

## 🔟 HTTP & API

```ts
constructor(private http: HttpClient) {}

this.http.get('https://api.example.com').subscribe();
```

> لا تنسَ `HttpClientModule`

---

## 1️⃣1️⃣ Styling

### Bootstrap
```bash
npm install bootstrap
```

```json
"styles": ["node_modules/bootstrap/dist/css/bootstrap.min.css"]
```

### Tailwind مع Angular
```bash
ng add @ngneat/tailwind
```

---

## 1️⃣2️⃣ أوامر Angular CLI المهمة

```bash
ng serve           # تشغيل المشروع
ng build           # build للإنتاج
ng generate component name
ng generate service name
ng generate module name
```

---

## 📌 Best Practices

- Component مسؤول عن العرض فقط
- Logic في Services
- استخدم Modules للتنظيم
- استعمل Lazy Loading

---

## 📂 جاهز للرفع على GitHub

- اسم الملف: `README.md`
- أضف وصف للمشروع
- Screenshots
- Tech Stack

---

✨ **Angular قوي جدًا للمشاريع الكبيرة – استثمر فيه صح** 🚀

