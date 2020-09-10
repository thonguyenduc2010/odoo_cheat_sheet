-- Nhóm giá trị lại 
```
update purchase_order 
set product_code = (select string_agg(code, ', ') 
from purchase_order_line 
where order_id = purchase_order.id) where product_code is null

SELECT "Movie",
array_to_string(array_agg(distinct "Actor"),',') AS Actor
FROM Table1
GROUP BY "Movie";
```

-- Xóa ký tự
```
SELECT trim(code)

SELECT substring('w3resource' from 4 for 5);
```
