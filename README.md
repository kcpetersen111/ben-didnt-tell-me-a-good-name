"Requirments":

Admin account - Creates other professor accounts. This goes to Dr. Dave

Professor accounts can assign students to printers

Scheduler modes:
  - Assign mode: Printer is open for assignment (professor assigns)
  - Open mode: Printer is open for anyone to sign up, regardless of class status (desperate times call for desperate measures)

Name and desc for each printer

Students are assigned to classes - 1 printer per clsas

# API Spec

## Endpoints

CreateUser:
```
{
  "name": String,
  "access_level": Int(enum),
  "email": String,
  "classes": String[]
}
```
GetUser

UpdateUser

DeleteUser

Login: 
```
{
  "email": String,
  "password": String
}
```
## Models
User:
```
{
    name: string,
    access_level: AccessLevel,
    email: string,
    classes: string[],
    printers: string[],
    printers_can_assign: number
}
```

## Enums
AccessLevel:
```
{
    Unknown = 0,
    Admin = 1,
    Professor = 2,
    Student = 3
}
```
