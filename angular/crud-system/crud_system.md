# Angular CRUD System with ApiService

هذا المثال يوضح كيفية عمل **CRUD System** في Angular باستخدام **ApiService** للتواصل مع API.

---

## 1️⃣ ApiService

```ts
import { HttpClient } from '@angular/common/http';
import { Injectable } from '@angular/core';

@Injectable({ providedIn: 'root' })
export class ApiService {
  constructor(private http: HttpClient) {}
  url: string = 'http://localhost:3000/posts/';

  // Create / Apply leave
  applyleave(data: any) {
    return this.http.post<any>(this.url, data);
  }

  // Read / View leave
  viewleave() {
    return this.http.get<any[]>(this.url);
  }

  // Delete leave
  delete(id: number) {
    return this.http.delete<any>(this.url + id);
  }

  // Fetch data by id
  fetchdata(id: number) {
    return this.http.get<any>(this.url + id);
  }

  // Update data
  update(data: any, id: number) {
    return this.http.put<any>(this.url + id, data);
  }
}
```

---

## 2️⃣ Read / View Data

```ts
allData: any[] = []; // نسخة أصلية لحفظ جميع البيانات

constructor(private api: ApiService, private router: Router) {}

ngOnInit() {
  this.getdata();
}

getdata() {
  this.api.viewleave().subscribe((res: any[]) => {
    this.allData = res;
  });
}

// Delete
deletedata(id: number) {
  this.api.delete(id).subscribe((res: any) => {
    this.getdata();
  });
}
```

---

## 3️⃣ Create / Add Data

```ts
public leave: any = {};

constructor(private api: ApiService, private route: Router) {}

ngOnInit() {}

postdata() {
  this.api.applyleave(this.leave).subscribe((res: any) => {
    this.route.navigateByUrl('viewleave');
  });
}
```

---

## 4️⃣ Update Data

```ts
public data_id: any;
public leave: any = {};

constructor(private api: ApiService, private router: Router, private activatedroute: ActivatedRoute) {}

ngOnInit() {
  this.activatedroute.paramMap.subscribe((res: any) => {
    this.data_id = res.get('id') || '';
  });

  // Fetch data
  this.api.fetchdata(this.data_id).subscribe((data: any) => {
    this.leave = data;
  });
}

// Update
updatedata() {
  this.api.update(this.leave, this.data_id).subscribe((res: any) => {
    alert('Data updated successfully');
    this.router.navigateByUrl('/viewleave');
  });
}
```

