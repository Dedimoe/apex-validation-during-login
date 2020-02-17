# apex-validation-during-login
apex-validation-during-login

purpose: during login, if sysdate between date of 10 and 21 every month --> normal login, if not will error occure: Aplikasi ini akan tersedia pada 11 s.d. 20 setiap bulannya. 
 
left panel: on processing --> add validation

right panel: property
type: rows returned
sql query:
 
paste this
```
select 1 as ada from dual 
where sysdate between to_date(to_char(sysdate,'yyyy-mm-')||'10', 'yyyy-mm-dd') 
and to_date(to_char(sysdate,'yyyy-mm-')||'21', 'yyyy-mm-dd')
```
