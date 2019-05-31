# JOIN

## From W3 Schools

```sql
create table customers(customerID integer not null, customerName varchar, contactName varchar, country varchar, constraint customers_customerID_pk primary key (customerID));

create table orders (orderID integer not null, customerID integer not null, orderDate timestamp, constraint orders_orderid_pk primary key (orderID), constraint orders_customers_customerID_id_fk foreign key (customerID) references public.customers (customerID));
```

```sql
\COPY public.orders from 'orders.txt' with DELIMITER E'\t'
\COPY public.customers from 'customers.txt' with DELIMITER E'\t'
```

```sql
SELECT Orders.OrderID, Customers.CustomerName, Orders.OrderDate
FROM Orders
INNER JOIN Customers ON Orders.CustomerID=Customers.CustomerID;
```