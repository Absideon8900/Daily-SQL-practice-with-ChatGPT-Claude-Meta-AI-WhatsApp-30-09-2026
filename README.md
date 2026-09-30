# Daily SQL practice with ChatGPT, Claude, Meta AI (WhatsApp)<br> 
<b>30th September 2026</b></br>
```SQL
Windows PowerShell
Copyright (C) Microsoft Corporation. All rights reserved.

Install the latest PowerShell for new features and improvements! https://aka.ms/PSWindows

PS C:\Users\hp> cd\
PS C:\> cd "C:\Users\hp\downloads\sql_practice(0)"
PS C:\Users\hp\downloads\sql_practice(0)> & "C:\Users\public\sqlite\sqlite3.exe" practice.db
SQLite version 3.53.4 2026-07-24 19:02:57
Enter ".help" for usage hints.
sqlite> CREATE TABLE orders (
(x1...> order_id INTEGER,
(x1...> customer_id TEXT,
(x1...> order_date TEXT,
(x1...> category TEXT,
(x1...> product_name TEXT,
(x1...> quantity INTEGER,
(x1...> unit_price INTEGER,
(x1...> discount_pct INTEGER,
(x1...> payment_method TEXT,
(x1...> order_status TEXT);
sqlite> .mode csv
sqlite> .import --skip 1 sql_practice_small.csv orders
sqlite> .header on
sqlite> .mode column
sqlite> SELECT * FROM orders;
order_id  customer_id  order_date   category    product_name  quantity  unit_price  discount_pct  payment_method  order_status
--------  -----------  ----------  -----------  ------------  --------  ----------  ------------  --------------  ------------
    1001  C01          2026-09-01  Electronics  Mouse                2         800            10  UPI             Completed
    1002  C02          2026-09-02  Books        Novel                3         450             5  Card            Completed
    1003  C01          2026-09-03  Sports       Football             1        1200             0  Cash            Pending
    1004  C03          2026-09-04  Clothing     T-Shirt              4         900            15  UPI             Completed
    1005  C04          2026-09-05  Books        Atlas                2         600            10  Card            Cancelled
    1006  C02          2026-09-06  Electronics  Keyboard             5        1500             5  UPI             Completed
    1007  C05          2026-09-07  Home         Lamp                 1         700             0  Cash            Pending
    1008  C03          2026-09-08  Sports       Cricket Bat          2        1800            10  Card            Completed
    1009  C04          2026-09-09  Clothing     Jeans                3        1300            20  UPI             Completed
    1010  C01          2026-09-10  Books        Guidebook            4         500             5  Cash            Pending
sqlite>
```
