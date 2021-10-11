# Vaccine Passport 

### Group Members

Arnaud, Bonvin, ABonvin 
Bonvin, Max, MaxBonvin
Tharmakulasinkam, Vakisan, VakisanTharmakulasinkam
Tochon, Louis, Ltochon


<hr/>

### Project Description

The SOAR Vaccination Platform allows users to connect and check their vaccination pass or to add a new one and to display the current certificate status. The platform will also check if the certificate validity date is still valid or not.  

<hr/>

### Model

Class *User*
- Id
- Email
- Password
- Name
- First Name
- Adress
- Phone number
- Vaccine id

Methods :
- Login
- Delete certificate
- Create account
- Delete account
- Show certificate
- Add vaccine
- Logout

Class *Vaccine*
- Id
- Brand
- Lot number
- Injection date
- Injection site
- Dose number

<hr/>

### View

When the user opens the app, a logging screen appears with the following: 

- [q] = quit
    The user can quit the application.
- [1] = login
    A login menu appears with a two input fields for an email and a password. If the login is successful, the user then continue onto the main menu. 
- [3] = register
    A registration menu appears and asks the user for an email and a password to register a new account. If the registration is successful, the user is taken back to the login menu.

After logging in, the user us greeted with the main menu:

- [q] = quit
    The user can quit the application.
- [1] = AddCertificate
    The user can add a Vaccination Certificate to the app.
- [2] = DisplayCertificate
    The user can display the certificate stores in his account.
- [3] = DeleteAccount
    The user can either press [1] to go back to the main menu or press [2] to delete all the data about the user stored on the database of the application.
- [4] = Logout
    The user can log out and go back to the login menu.
    
<hr/>

### Controller

- LoginController
This controller holds username and password information of a user who wants 
to log in. If the user successfully logs in, the controller holds the currentUser. In addition, it manages log in and log out functions of the application. 

- UserController 
This controller holds username, first name, last name, email, password and  amount information. It also manages creation of a new user account with his own certificate.

- CertificateController
This controller holds all the datas related to a certificate and allows to add it to a specific user.


### Exceptions

AlreadyExistsException
- Error raised when the user tries to create an account with an email address that is already in use.

DoesNotExistsException
- Error raised when the user wants to use an email address that does not exist to create a new account.

CertificateAlreadyEnteredException
- Error raised when the certificate entered by the user has already been entered in the app.

CertificateNotValidException
- Error raised when the certificate entered by the user is not valid.


