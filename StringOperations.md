# String Operations

- __Like__
  - select * from instructor where name like 'a%'; _to select starting from a_
  - select * from instructor where name like 'a%r';
  - select * from instructor where name like '%a%'; _selects a whereever it is_
  - select * from instructor where name like 'r_%_'; _custom_

- __Not__
  - select * from instructor where not department_name='computer science';
  
- __Or__
  - select * from instructor where department_name='electrical' or department_name='electronics'; _shows either one of them is present if 
  both are present it shows both_ 
  
- __And__
  - select * from instructor where department_name='electrical' and department_name='mechanical'; _shows both if both are not there shows
  empty set
  
- __Between/Not Between__
  - select * from instructor where salary between 50000 and 60000;
  - select * from instructor where salary not between 50000 and 60000;
  
- __IN/Not in__
  - select * from instructor where department_name in('electrical','electorincs'); _like OR_
  - select * from instructor where department_name not in('electrical','electorincs');
