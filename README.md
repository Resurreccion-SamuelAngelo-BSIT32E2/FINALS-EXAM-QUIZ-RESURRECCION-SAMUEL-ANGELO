# FINALS-EXAM-QUIZ-RESURRECCION-SAMUEL-ANGELO
HR Application Architecture
1. Attendance Monitoring
Domain Objects:
Employee
EmployeeID (Primary Key)
Name
Department
Position
Attendance
AttendanceID (Primary Key)
Date
Status (Present, Absent, Excused)
EmployeeID (Foreign Key references Employee.EmployeeID)
Repository:
EmployeeRepository: Handles CRUD operations for Employee.
AttendanceRepository: Handles CRUD operations for Attendance.
Service:
AttendanceService:
addAttendance: Adds attendance record.
overrideAttendance: Overrides an existing attendance record.
readAttendanceOfEmployeeById: Reads attendance records of an employee by their ID.
ERD:

2. Onboarding and Offboarding
Domain Objects:
Employee
EmployeeID (Primary Key)
Name
Department
Position
HireDate
TerminationDate
Onboarding
OnboardingID (Primary Key)
EmployeeID (Foreign Key references Employee.EmployeeID)
StartDate
CompletionDate
Offboarding
OffboardingID (Primary Key)
EmployeeID (Foreign Key references Employee.EmployeeID)
StartDate
CompletionDate
Repository:
EmployeeRepository: Handles CRUD operations for Employee.
OnboardingRepository: Handles CRUD operations for Onboarding.
OffboardingRepository: Handles CRUD operations for Offboarding.
Service:
OnboardingService:
startOnboarding: Starts onboarding process.
completeOnboarding: Completes onboarding process.
readOnboardingStatus: Reads the status of onboarding.
OffboardingService:
startOffboarding: Starts offboarding process.
completeOffboarding: Completes offboarding process.
readOffboardingStatus: Reads the status of offboarding.
ERD:

3. Payroll
Domain Objects:
Employee
EmployeeID (Primary Key)
Name
Department
Position
Payroll
PayrollID (Primary Key)
EmployeeID (Foreign Key references Employee.EmployeeID)
Salary
PaymentDate
Deductions
Repository:
EmployeeRepository: Handles CRUD operations for Employee.
PayrollRepository: Handles CRUD operations for Payroll.
Service:
PayrollService:
processPayroll: Processes payroll for employees.
generatePayslip: Generates payslips.
readPayrollByEmployeeId: Reads payroll details of an employee by their ID.
ERD:

4. Compensation and Benefits
Domain Objects:
Employee
EmployeeID (Primary Key)
Name
Department
Position
Compensation
CompensationID (Primary Key)
EmployeeID (Foreign Key references Employee.EmployeeID)
BaseSalary
Bonus
Benefit
BenefitID (Primary Key)
EmployeeID (Foreign Key references Employee.EmployeeID)
BenefitType
Description
Repository:
EmployeeRepository: Handles CRUD operations for Employee.
CompensationRepository: Handles CRUD operations for Compensation.
BenefitRepository: Handles CRUD operations for Benefit.
Service:
CompensationService:
updateCompensation: Updates compensation details.
readCompensationByEmployeeId: Reads compensation details by employee ID.
BenefitService:
addBenefit: Adds a benefit.
removeBenefit: Removes a benefit.
readBenefitsByEmployeeId: Reads benefits by employee ID.
