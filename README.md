# scala-web-sbt-spring-thyme-remeber-me-insecure

## Description
A springboot secure web app with thymeleaf support.
Three roles are defined; USER, ADMIN, and SUPER. All roles
can access pages `/home`, `/login`, and `/about`. Only USER
can access `/user` and ADMIN only `/admin` whereas SUPER can
navigate to either and have its own `/super`. Each role
has an action USER=VIEW ONLY, ADMIN=READ/WRITE, SUPER=CREATE.
All password are encoded with bcrypt.

Uses the rememberMe cookie for a 2 min window
this as well as other setting can be found in
`config/Security.scala`. One way to test is the following:
- Set rememberMe checkbox
- login
- set a bookmark to the secured page
- open a new window
- use the bookmark

rememberMe cookie does not redirect it only authenticates.

## Tech stack
- scala
- sbt
  - springboot
  - thymeleaf
  - bootstrap
  - jquery
  - datatable

## Docker stack
- hseeberger/scala-sbt:11.0.2-oraclelinux7_1.3.5_2.12.10

## To run
`sudo ./install.sh -u`
Available at http://localhost
- Login with id: user and password: pass
- Login with id: admin and password: pass
- Login with id: super and password: pass

## To stop (optional)
`sudo ./install.sh -d`

## For help
`sudo ./install.sh -h`
