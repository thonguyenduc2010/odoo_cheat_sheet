-- Nhóm giá trị lại 
```
update purchase_order set product_code = (select string_agg(code, ', ') from purchase_order_line where order_id = purchase_order.id) where product_code is null

```
