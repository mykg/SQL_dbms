#LAB_NOTES 31-jan-2020

- refers to primary key attribute
- datatype should be same 
- Let Database customer_order
- mostly exists in child table
//below table is parent table
- create table customer(cust_id int primary key auto_increment, F_name char(15),L_name char(15), Mob_no bigint, email_id varchar(15));
//below table is child
- create table order (order_id primary key auto_increment, cust_id int, item_name char(20), order_time time, order_date date, amount int, 
  constraint order_fk1 foreign key (cust_id) references customer (cust_id) ON UPDATE CASCADE ON DELETE CASCADE);
//ON UPDATE/DELETE CASDADE it reflects the changes to child table
//if column name in child same as parent it automatically assign it as foreign key 
- alter table table_name add foreign key (attribute_name) references table_name (attribute_name);
- alter table table_name drop foreign key constraint_name; //constraint_name automatically genearted if not given by user
- show create table table_name; #to check details and constraints
