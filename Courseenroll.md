# University Enrollment DDD Model

## Aggregate Root
CourseEnrollment

The CourseEnrollment aggregate represents a student's enrollment in a university course.

## Invariants
- Credit hours must be greater than 0.
- A course cannot have more than 6 credit hours.
- A course cannot be dropped twice.
- Enrollment changes must be controlled by the CourseEnrollment aggregate.

## Domain Events

### CourseEnrollmentCreated
This event occurs when a student successfully enrolls in a course.

### CourseEnrollmentDropped
This event occurs when a student drops a course.

## DDD Model

University Enrollment
        |
        v
CourseEnrollment
(Aggregate Root)
        |
        +-- Student ID
        +-- Course ID
        +-- Credit Hours
        +-- Enrollment Status
        |
        +-- CourseEnrollmentCreated
        |
        +-- CourseEnrollmentDropped
        
