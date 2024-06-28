## Features:
 
- FastAPI project structure tree
 
- user module
- 
  **User**
        - **id**, **name**, **email**, **password**, **phone_number**,**created_at**,**otp**, **expires_at**, **is_active** ,**roles**, **refresh_token**(roles Relation to the **UserRole** table)
  
   **Role**
        - **id**, **name**, **email**,**user**(user Relation to the **UserRole** table)
 
   **UserRole**
    - **user_id**, **role_id**, **user**,**role**(user and Relation to the **User** table and **Role** table)
 
- database => sqlite
 
- authentication => JWT Autentication
 
 
## Structured Tree
 
```
 
├── fastapi
 
│   ├── project
 
│   │   ├── core
 
│   │   │    ├──__init__.py
 
│   │   │    ├──auth.py
 
│   │   │    └──config.py   # Contains core functionality like database management,
 
│   │   ├── routers   # Contains modules for each feature (user, product, payments).
 
│   │   │    ├── __init__.py
 
│   │   │    ├──Role.py
 
│   │   │    └──User.py
 
│   │   ├── crud.py
 
│   │   ├── database.py
 
│   │   ├── dependency.py
 
│   │   ├── main.py     # Initializes the FastAPI app and brings together various components.
 
│   │   ├── models      # Contains modules defining database models for Users,Role UserRole.
 
│   │   ├── __init__.py
 
│   │   ├── schemas.py   # Pydantic model for data validation
 
│   │    ├── requirements.txt # Lists project dependencies.
 
```
 
**/user/create-otp**: Api used to Create User by Signin
 
**/user/verify-otp**:Api used to Verify the User to  Signin once the otp verfied tahen the user created
 
**/user/login**: Api used to Login once otp is valid then user login and get token (put)
 
**/user/login**: Api used to Login and get Tokens(post)
 
**/user/request_otp**: Api used to  request get otp to login
 
**/user/refresh_token/**: Api used to create a Access Token
 
**/user/change_password/**: Api used to Change The Password after Login
 
**/user/logout/**:Api used to logout
 
**/user/single/user/{user_id}**:Api used to Get the Single user Data
 
**/user/all/**:Api used to Get the all the User
 
**/user/user/{user_id}**:Api used to delete the Single user Data
 
**/user/email_To_Forget_Password**:Api used to Change passwords if the user Forget the Password user Verification by the Email
 
**/user/otp_verify**: Api used to verify the otp Allow user Change Password in Forget Password
 
**/user/change_froget_password**: Api perform , once the user verify the otp  user Allowed to  Change Password  in fileds for new_password
 
**/user/create/User_Role**:Api used to create a User with Role Manually by  Anotheruser
 
**/user/user/{user_id}**:Api used to update the created a User and Role Manually by  Anotheruser
 
**/Role/create/role**:Api used to Create the Role
 
# Setup
Creat folder by the Structured Tree
 
 
Create a virtual environment to install dependencies in and activate it:
 
```sh
 
$ python -m venv venv
 
$ source venv/bin/activate
 
```
 
Then install the dependencies:
 
```sh
 
# for this to Install all library at once
 
(venv)$ pip install -r requirements.txt
 
#other wise install all the packages manually
 
(venv)$ pip install fastapi
(venv)$ pip install bycrpt
(venv)$ pip install uvicorn
(venv)$ pip install PyJWT python-jose
(venv)$ pip install pydantic
(venv)$ pip install passlib
(venv)$ pip install SQLAlchemy
(venv)$ pip install alembic
 
 
```
 
Once `pip` has finished downloaded you installed all the requirement:
 
To Run the Api **uvicorn project.main:app --reload**
 
 
# Tools
 
### Back-end
 
#### Language:
 
    Python above(3.7)
 
#### Frameworks:
 
    FastAPI
 
    pydantic
 
#### Other libraries / tools:
 
    SQLAlchemy
 
    starlette
 
    uvicorn
 
    python-jose
 
    bycrpt
 
    pyJWT
 
    passlib
 
### Thank You
 
