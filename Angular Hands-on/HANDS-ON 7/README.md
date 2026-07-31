# Angular Routing — Guards, Lazy Loading & Route Data

This project demonstrates Angular routing concepts including route configuration, route parameters, nested routes, lazy loading, route guards, and route data handling. It is based on the **Hands-On 7** exercise from the Digital Nurture Java FSE Angular module.

---

## Project Objective

Build a simple Angular portal application that:

* Configures application routes using `RouterModule`
* Uses route parameters and query parameters
* Implements nested routes
* Implements lazy loading for a feature module
* Protects routes using `CanActivate`
* Prevents accidental navigation using `CanDeactivate`
* Displays a 404 page for unknown routes

---

## Topics Covered

* Routing with `RouterModule`
* Route Parameters (`:id`)
* Query Parameters
* Nested / Child Routes
* Lazy Loading Feature Modules
* `CanActivate` Guard
* `CanDeactivate` Guard
* Route Data / Resolver concepts
* Wildcard Route (`**`)

---

## Project Structure

```text
src/
└── app/
    ├── pages/
    │   ├── home/
    │   ├── course-list/
    │   ├── course-detail/
    │   ├── profile/
    │   └── not-found/
    ├── layouts/
    │   └── courses-layout/
    ├── features/
    │   └── enrollment/
    │       ├── enrollment.module.ts
    │       ├── enrollment-routing.module.ts
    │       ├── enrollment-form/
    │       └── reactive-enrollment-form/
    ├── guards/
    │   ├── auth.guard.ts
    │   └── unsaved-changes.guard.ts
    ├── services/
    │   ├── auth.service.ts
    │   └── course.service.ts
    └── app-routing.module.ts
```

---

## Routing Configuration

### Main Routes

| Route          | Component               | Description            |
| -------------- | ----------------------- | ---------------------- |
| `/`            | HomeComponent           | Home page              |
| `/courses`     | CourseListComponent     | Course list            |
| `/courses/:id` | CourseDetailComponent   | Course details         |
| `/profile`     | StudentProfileComponent | Protected profile page |
| `/enroll`      | EnrollmentModule        | Lazy-loaded feature    |
| `**`           | NotFoundComponent       | 404 page               |

### Nested Routes

```ts
{
  path: 'courses',
  component: CoursesLayoutComponent,
  children: [
    { path: '', component: CourseListComponent },
    { path: ':id', component: CourseDetailComponent }
  ]
}
```

---

## Route Parameter Example

```ts
const id = this.route.snapshot.paramMap.get('id');
```

Example URL:

```text
/courses/2
```

---

## Query Parameter Example

Update URL:

```ts
this.router.navigate(['/courses'], {
  queryParams: { search: this.searchTerm }
});
```

Read query parameter:

```ts
const search = this.route.snapshot.queryParamMap.get('search');
```

Example URL:

```text
/courses?search=angular
```

---

## Lazy Loading

### Route Configuration

```ts
{
  path: 'enroll',
  loadChildren: () =>
    import('./features/enrollment/enrollment.module')
      .then(m => m.EnrollmentModule)
}
```

### Verification

Open **Chrome DevTools → Network**, navigate to `/enroll`, and observe that a separate JavaScript chunk is downloaded only when the route is visited.

---

## CanActivate Guard

### auth.guard.ts

```ts
canActivate(): boolean {
  if (this.authService.isLoggedIn) {
    return true;
  }

  this.router.navigate(['/']);
  return false;
}
```

### Apply Guard

```ts
{
  path: 'profile',
  canActivate: [AuthGuard],
  component: StudentProfileComponent
}
```

---

## CanDeactivate Guard

### unsaved-changes.guard.ts

```ts
canDeactivate(component: ReactiveEnrollmentFormComponent): boolean {
  if (component.enrollForm.dirty) {
    return window.confirm('You have unsaved changes. Leave?');
  }
  return true;
}
```

---

## Installation

### Prerequisites

* Node.js (v18+ recommended)
* npm
* Angular CLI

### Install Dependencies

```bash
npm install
```

---

## Run the Application

```bash
ng serve
```

Open:

```text
http://localhost:4200
```

---

## Generate Components / Guards

```bash
ng generate component pages/course-detail
ng generate guard guards/auth
ng generate guard guards/unsaved-changes
ng generate module features/enrollment --routing
```

---

## Expected Output

* Home page loads at `/`
* Course list loads at `/courses`
* Course details load correctly at `/courses/2`
* Search updates the URL query parameter
* `/profile` is accessible only when logged in
* `/enroll` loads lazily
* Navigation away from a dirty enrollment form shows a confirmation dialog
* Unknown routes display the 404 page

---

## Testing Checklist

* [ ] Route navigation works
* [ ] Dynamic route parameter works
* [ ] Query parameter updates correctly
* [ ] Nested routes render inside `router-outlet`
* [ ] Lazy-loaded module creates a separate chunk
* [ ] Auth guard blocks unauthorized access
* [ ] Unsaved changes guard prompts before leaving
* [ ] Wildcard route displays 404 page

---

## Technologies Used

* Angular 20
* TypeScript
* Angular Router
* RxJS
* HTML5
* CSS3

---

## Learning Outcomes

After completing this exercise, you will be able to:

* Configure Angular routes effectively
* Use route and query parameters
* Build nested routing structures
* Improve performance with lazy loading
* Secure routes with guards
* Handle unsaved form navigation safely
* Structure Angular applications using feature modules

---

## Author
**NEHA SANKEERTHANA**

**Digital Nurture 5.0 — Java FSE Angular Hands-On Exercise**

For educational and training purposes.

