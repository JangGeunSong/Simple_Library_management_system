# Simple_Library_management_system
This project made by on the winter semester course of the java programming use the network programming and database programming.
That using MVC design pattern to improve our OOP technique. and prevent to make object twice, we choose singleton pattern that you can check the AppManager.java file 


table book
create table book(bookID char(100) not null,bname char(100) not null,author char(100),publish char(100), primary key(bookID));
--> 책 정보 테이블

table rent_info
create table rent_info(bookID char(100) not null, rentID char(100), startdate date, enddate date, foreign key(bookID) references book(bookID));
-->대여 정보 테이블

table reservation_info
create table reservation_info(bookID char(100) not null, reservationID char(100), foreign key(bookID) references book(bookID));
-->예약정보 테이블

table user
create table user(userID char(100) not null, password char(100) not null, uname char(100), flag bool, primary key (userID), unique key (userID));
-->사용자 정보 테이블

we use the mysql database.
