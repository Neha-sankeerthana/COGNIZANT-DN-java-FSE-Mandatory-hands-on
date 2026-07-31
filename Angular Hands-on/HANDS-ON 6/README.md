# Hands-On 6: Services & Dependency Injection in Angular

This repository contains the implementation of **Hands-On 6 – Services & Dependency Injection** from the **Digital Nurture 5.0 Angular Hands-On Exercise Book**. The project demonstrates how Angular services are used to centralize business logic, share data between components, implement Dependency Injection (DI), and understand the difference between root-level and component-level service providers.

---

## 📌 Objectives

- Create reusable Angular Services
- Inject services into components
- Share data across multiple components using a singleton service
- Understand `providedIn: 'root'`
- Implement Hierarchical Dependency Injection
- Demonstrate component-level providers
- Perform service-to-service injection

---

## 🛠️ Technologies Used

- Angular 20
- TypeScript
- HTML5
- CSS3
- Angular Dependency Injection

---

## 📂 Project Structure

```text
src/
│
├── app/
│   ├── components/
│   │   ├── home/
│   │   ├── course-list/
│   │   ├── course-card/
│   │   ├── student-profile/
│   │   ├── course-summary-widget/
│   │   └── notification/
│   │
│   ├── models/
│   │   └── course.model.ts
│   │
│   ├── services/
│   │   ├── course.service.ts
│   │   ├── enrollment.service.ts
│   │   └── notification.service.ts
│   │
│   └── app.component.*
│
└── ...
```

---

# Task 1 – Create and Use a Course Service

## Goal

Build a `CourseService` that provides course data to multiple components.

### Features Implemented

- Generated `CourseService`
- Registered the service using:

```typescript
@Injectable({
  providedIn: 'root'
})
```

- Maintains a private array of courses
- Implemented the following methods:

```typescript
getCourses(): Course[]

getCourseById(id: number): Course | undefined

addCourse(course: Course): void
```

---

## Course Model

```typescript
export interface Course {
    id: number;
    name: string;
    code: string;
    credits: number;
    gradeStatus: 'passed' | 'failed' | 'pending';
}
```

---

## Components Using CourseService

### HomeComponent

- Displays the total number of available courses.
- Reads live data from `CourseService`.

### CourseListComponent

- Retrieves and displays all courses.
- Uses `getCourses()` instead of hardcoded data.

### CourseSummaryWidget

- Injects the same service instance.
- Demonstrates shared application state.
- Automatically reflects updates when a course is added.

---

# Task 2 – Enrollment Service and Hierarchical Dependency Injection

## Goal

Create an `EnrollmentService` and demonstrate Angular's Hierarchical Dependency Injection.

### Features Implemented

Created `EnrollmentService` with the following methods:

```typescript
enroll(courseId: number): void

unenroll(courseId: number): void

isEnrolled(courseId: number): boolean

getEnrolledCourses(): Course[]
```

The service internally injects `CourseService` to retrieve complete course information.

---

## Components Using EnrollmentService

### CourseCardComponent

- Enroll button
- Unenroll button
- Button label changes dynamically using `isEnrolled()`.

### StudentProfileComponent

Displays all enrolled courses using:

```typescript
getEnrolledCourses()
```

---

# Hierarchical Dependency Injection

A dedicated `NotificationService` is provided at the component level.

Example:

```typescript
@Component({
  selector: 'app-notification',
  providers: [NotificationService]
})
```

Providing the service in the component creates a **new service instance** that is available only to that component and its child components, demonstrating Angular's Hierarchical Dependency Injection.

---

# Key Concepts Covered

- Angular Services
- Dependency Injection (DI)
- Singleton Service Pattern
- `providedIn: 'root'`
- Root-level Providers
- Component-level Providers
- Shared State Management
- Service-to-Service Injection
- Hierarchical Dependency Injection

---

# Expected Output

- Course list is loaded from `CourseService`.
- Home component displays the live course count.
- Multiple components share the same singleton service instance.
- Adding a course updates all dependent components.
- Enrollment and unenrollment work correctly.
- Student Profile displays enrolled courses.
- Notification component uses an independent service instance.

---

# How to Run the Project

### Clone the Repository

```bash
git clone https://github.com/your-username/your-repository.git
```

### Navigate to the Project

```bash
cd your-repository
```

### Install Dependencies

```bash
npm install
```

### Start the Development Server

```bash
ng serve
```

Open your browser and navigate to:

```text
http://localhost:4200
```

---

# Learning Outcomes

After completing this hands-on exercise, you will be able to:

- Create reusable Angular services.
- Use `@Injectable()` for dependency injection.
- Inject services into components.
- Share data across multiple components.
- Understand the Singleton Service Pattern.
- Differentiate between root-level and component-level providers.
- Implement Hierarchical Dependency Injection.
- Perform service-to-service injection.
- Build maintainable and modular Angular applications.

---

# Conclusion

This project demonstrates the practical implementation of Angular Services and Dependency Injection by creating reusable services, sharing application state across components, implementing enrollment functionality, and understanding Angular's DI hierarchy. It provides a strong foundation for building scalable, maintainable, and modular Angular applications using best practices.

---

## Author

**NEHA SANKEERTHANA**

**Digital Nurture 5.0 – Angular Hands-On 6**
