// Queries //

select d.name, avg(e.age) as average_age from employees e join departments d on e.department_id=d.id group by d.name;


select d.name, count(*) as employee_count from employees e join departments d on e.department_id=d.id where e.age >40 group by d.name order by employee_count desc limit 1;


select count(*) as recent_joiners from employees where joining_date >=current_date -INTERVAL 100 DAY;

update employees e join departments d on e.department_id=d.id 
SET e.joining_date = current_date - INTERVAL 1 DAY where d.name ="HR";


select count(*) as recent_joiners from employees where joining_date>= current_date - INTERVAL 100 DAY;
