# 📘 React Documentation – المختصر المفيد

هذا الدليل مصمم ليجعلك **مبرمج React قوي** بدون الحاجة للبحث عن دورات خارجية. مرتب من الأساسيات حتى المستوى المتقدم، مع أمثلة مختصرة ومفاهيم عملية.

---

## 1️⃣ ما هي React؟
- مكتبة JavaScript لبناء واجهات المستخدم (UI)
- مبنية على **Component-Based Architecture**
- تعتمد على **Virtual DOM** لتحسين الأداء

> React ليست Framework، بل مكتبة

---

## 2️⃣ متطلبات قبل React
لازم تكون متمكن من:
- HTML
- CSS
- JavaScript (خصوصًا):
  - let / const
  - arrow functions
  - destructuring
  - map / filter
  - spread operator
  - promises

---

## 3️⃣ إنشاء مشروع React
### باستخدام Vite (الأفضل حاليًا)
```bash
npm create vite@latest my-app
cd my-app
npm install
npm run dev
```

---

## 4️⃣ Structure المشروع
```
src/
 ├─ components/
 ├─ pages/
 ├─ assets/
 ├─ App.jsx
 ├─ main.jsx
```

---

## 5️⃣ Component
### Functional Component
```jsx
function Header() {
  return <h1>Hello React</h1>;
}
export default Header;
```

### Rules
- اسم الكمبوننت يبدأ بحرف Capital
- يرجع JSX واحد فقط

---

## 6️⃣ JSX
- يشبه HTML لكنه JavaScript
- class ➜ className
- for ➜ htmlFor

```jsx
const name = "Mohammed";
<h1>Hello {name}</h1>
```

---

## 7️⃣ Props
تمرير بيانات بين الكمبوننتات

```jsx
function Card({ title }) {
  return <h2>{title}</h2>;
}

<Card title="React" />
```

---

## 8️⃣ State (useState)
تخزين البيانات المتغيرة

```jsx
import { useState } from "react";

const [count, setCount] = useState(0);
```

⚠️ لا تعدل الـ state مباشرة

---

## 9️⃣ Events
```jsx
<button onClick={() => setCount(count + 1)}>+</button>
```

---

## 🔟 Conditional Rendering
```jsx
{isLoggedIn ? <Dashboard /> : <Login />}
```

---

## 1️⃣1️⃣ Lists & Keys
```jsx
items.map(item => (
  <li key={item.id}>{item.name}</li>
))
```

---

## 1️⃣2️⃣ useEffect
تنفيذ أكواد عند:
- تحميل الصفحة
- تغير state

```jsx
useEffect(() => {
  console.log("Mounted");
}, []);
```

---

## 1️⃣3️⃣ Forms
### Controlled Input
```jsx
<input value={name} onChange={e => setName(e.target.value)} />
```

---

## 1️⃣4️⃣ React Router
### Installation
```bash
npm i react-router-dom
```

```jsx
<Route path="/login" element={<Login />} />
```

---

## 1️⃣5️⃣ Styling
### CSS
- CSS File
- CSS Modules
- Tailwind CSS ✅ (مفضل)

---

## 1️⃣6️⃣ Folder Organization (Best Practice)
```
components/
 ├─ Button/
 │   ├─ index.jsx
 │   ├─ style.css
```

---

## 1️⃣7️⃣ Refs (useRef)
```jsx
const inputRef = useRef();
inputRef.current.focus();
```

---

## 1️⃣8️⃣ Context API
مشاركة البيانات بدون props drilling

```jsx
const ThemeContext = createContext();
```

---

## 1️⃣9️⃣ Performance
- React.memo
- useCallback
- useMemo

---

## 2️⃣0️⃣ API & Fetching Data
```jsx
fetch(url)
  .then(res => res.json())
  .then(data => setData(data));
```

أو Axios

---

## 2️⃣1️⃣ Authentication
- Login / Register
- Token (JWT)
- Protected Routes

---

## 2️⃣2️⃣ Error Handling
- Try / Catch
- Error Boundary

---

## 2️⃣3️⃣ Deployment
- Vercel
- Netlify
- Firebase

---

## 2️⃣4️⃣ Important Libraries
- react-router-dom
- axios
- react-icons
- tailwindcss
- zustand / redux

---

## 2️⃣5️⃣ What makes you React Developer 💪
✔ Components reusable
✔ Clean structure
✔ State management
✔ API integration
✔ Responsive UI

---

## 🔥 Roadmap مختصر
1. JSX + Components
2. Props + State
3. Hooks
4. Router
5. API
6. Auth
7. Performance
8. Real Projects

---

## ✅ نصيحتي ليك
> أي فكرة تخطر في بالك ➜ نفذها بمشروع React صغير

لو داير:
- شرح أي جزء بالتفصيل
- مشاريع تدريبية
- تحويل HTML ➜ React

قولي 🔥

