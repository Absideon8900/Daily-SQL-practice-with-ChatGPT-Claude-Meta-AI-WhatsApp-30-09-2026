# Daily SQL practice with ChatGPT, Claude, Meta AI (WhatsApp)<br> 
<b>30th September 2026</b></br>
```SQL
Windows PowerShell
Copyright (C) Microsoft Corporation. All rights reserved.

Install the latest PowerShell for new features and improvements! https://aka.ms/PSWindows

PS C:\Users\hp> cd downloads
PS C:\Users\hp\downloads> cd "sql_practice(0)"
PS C:\Users\hp\downloads\sql_practice(0)> & "C:\Users\Public\Sqlite\Sqlite3.exe" practice_00.db
SQLite version 3.53.4 2026-07-24 19:02:57
Enter ".help" for usage hints.
sqlite> CREATE TABLE orders (
(x1...> order_id INTEGER,
(x1...> customer_id TEXT,
(x1...> order_date TEXT,
(x1...> category TEXT,
(x1...> product_name TEXT,
(x1...> quantity INTEGER,
(x1...> unit_price DECIMAL,
(x1...> discount_pct DECIMAL,
(x1...> payment_method TEXT,
(x1...> order_status TEXT);
sqlite> .mode csv
sqlite> .import --skip 1 orders.csv orders
sqlite> .header on
sqlite> .mode column
sqlite> SELECT * FROM orders;
order_id  customer_id      order_date          category         product_name      quantity  unit_price  discount_pct  payment_method  order_status
--------  -----------  -------------------  --------------  --------------------  --------  ----------  ------------  --------------  ------------
    1001  CUST-121     2025-02-22 21:00:00  Electronics     Wireless Mouse               3       81.02          0.05                  Completed
    1002  CUST-119     2025-09-16 19:00:00  Books           SQL Essentials               1       37.17          0.05  Credit Card     Shipped
    1003  CUST-107     2025-01-04 05:00:00  Sports          Tennis Racket                2      140.27           0.1  Apple Pay       Completed
    1004  CUST-109     2025-02-19 11:00:00  Clothing        Denim Jeans                  3       39.64          0.15  Debit Card      Shipped
    1005  CUST-109     2025-02-10 17:00:00  Electronics     USB-C Cable                  5        46.2          0.15  Debit Card      Refunded
    1006  CUST-121     2025-01-24 21:00:00  Sports          Water Bottle                 5       65.76             0  PayPal          Refunded
    1007  CUST-110     2025-11-22 11:00:00  Electronics     Mechanical Keyboard          1      120.24          0.15  PayPal          Completed
    1008  CUST-112     2025-10-01 23:00:00  Clothing        Hoodie                       1      186.65          0.05  PayPal          Completed
    1009  CUST-115     2025-01-29 07:00:00  Books           Algorithms Unlocked          5       73.69           0.1  Credit Card     Refunded
    1010  CUST-111     2025-06-11 06:00:00  Books           Algorithms Unlocked          1       71.19           0.2  Apple Pay       Pending
    1011  CUST-129     2025-10-03 08:00:00  Books           Python Data Analysis         3       50.49           0.2                  Pending
    1012  CUST-129     2025-09-18 15:00:00  Sports          Tennis Racket                3        73.6          0.05  Credit Card     Refunded
    1013  CUST-102     2025-11-02 02:00:00  Electronics     Mechanical Keyboard          2       239.7          0.15  Apple Pay       Pending
    1014  CUST-120     2025-12-15 23:00:00  Books           Sci-Fi Novel                 3      291.61             0  Credit Card     Cancelled
    1015  CUST-129     2025-03-22 14:00:00  Sports          Water Bottle                 3       42.35          0.15  Credit Card     Cancelled
    1016  CUST-129     2025-11-17 09:00:00  Home & Kitchen  Desk Lamp                    2      157.23             0                  Shipped
    1017  CUST-107     2025-01-01 19:00:00  Clothing        Hoodie                       2      166.42           0.2  Debit Card      Pending
    1018  CUST-101     2025-10-18 02:00:00  Electronics     HD Monitor                   3       79.44          0.05  Credit Card     Cancelled
    1019  CUST-116     2025-10-09 05:00:00  Electronics     Bluetooth Speaker            2       47.23          0.15  Debit Card      Shipped
    1020  CUST-128     2025-06-09 12:00:00  Sports          Tennis Racket                2      279.38          0.05  Debit Card      Pending
    1021  CUST-129     2025-06-23 00:00:00  Sports          Tennis Racket                1       81.89             0                  Shipped
    1022  CUST-108     2025-04-28 02:00:00  Sports          Dumbbell Set                 1       30.59             0  Credit Card     Refunded
    1023  CUST-111     2025-04-20 17:00:00  Electronics     Bluetooth Speaker            2       90.76          0.15  PayPal          Cancelled
    1024  CUST-130     2025-07-28 06:00:00  Sports          Resistance Bands             4       80.47          0.15  Credit Card     Completed
    1025  CUST-122     2025-12-11 20:00:00  Books           Algorithms Unlocked          4      129.22             0  Credit Card     Completed
    1026  CUST-113     2025-08-18 04:00:00  Home & Kitchen  Coffee Maker                 2       65.56           0.2  Apple Pay       Completed
    1027  CUST-109     2025-02-20 01:00:00  Books           Python Data Analysis         1      138.51           0.2                  Refunded
    1028  CUST-101     2025-04-20 12:00:00  Electronics     Mechanical Keyboard          2      127.86          0.15  Credit Card     Completed
    1029  CUST-113     2025-05-27 13:00:00  Electronics     USB-C Cable                  3      278.69          0.15                  Cancelled
    1030  CUST-123     2025-10-24 23:00:00  Books           Python Data Analysis         2       96.05             0                  Completed
    1031  CUST-124     2025-09-29 05:00:00  Home & Kitchen  Coffee Maker                 1      179.41           0.2  Credit Card     Shipped
    1032  CUST-103     2025-07-26 03:00:00  Clothing        Cotton T-Shirt               5       29.71          0.05                  Completed
    1033  CUST-119     2025-10-17 16:00:00  Sports          Yoga Mat                     5       33.78           0.2  Debit Card      Completed
    1034  CUST-107     2025-08-23 10:00:00  Home & Kitchen  Air Fryer                    3      124.78           0.1  Credit Card     Completed
    1035  CUST-115     2025-09-17 08:00:00  Sports          Resistance Bands             1       31.25          0.05  PayPal          Completed
    1036  CUST-129     2025-10-06 22:00:00  Electronics     Mechanical Keyboard          3       92.65          0.15  Debit Card      Shipped
    1037  CUST-126     2025-03-10 08:00:00  Sports          Yoga Mat                     5       96.82             0  Credit Card     Completed
    1038  CUST-124     2025-06-25 06:00:00  Sports          Dumbbell Set                 3       91.71          0.05  Debit Card      Shipped
    1039  CUST-116     2025-01-23 00:00:00  Home & Kitchen  Coffee Maker                 1      193.94           0.1  Debit Card      Refunded
    1040  CUST-105     2025-10-15 00:00:00  Home & Kitchen  Air Fryer                    4      169.99          0.15  Credit Card     Completed
    1041  CUST-129     2025-10-10 04:00:00  Clothing        Winter Jacket                1      252.03           0.2  Apple Pay       Completed
    1042  CUST-102     2025-12-16 07:00:00  Home & Kitchen  Stainless Steel Pan          1      270.69          0.05  Credit Card     Completed
    1043  CUST-125     2025-03-25 05:00:00  Sports          Tennis Racket                5      227.35          0.05  Apple Pay       Completed
    1044  CUST-106     2025-07-15 01:00:00  Home & Kitchen  Blender                      2       87.37             0  Apple Pay       Completed
    1045  CUST-107     2025-04-25 00:00:00  Books           Algorithms Unlocked          3      247.96          0.05  PayPal          Pending
    1046  CUST-111     2025-07-24 21:00:00  Home & Kitchen  Coffee Maker                 3      111.83           0.2                  Completed
    1047  CUST-101     2025-01-20 03:00:00  Electronics     HD Monitor                   2      178.37           0.1                  Pending
    1048  CUST-112     2025-07-17 18:00:00  Home & Kitchen  Blender                      5      295.43             0  PayPal          Completed
    1049  CUST-102     2025-12-18 23:00:00  Books           SQL Essentials               5      278.42           0.2  PayPal          Completed
    1050  CUST-114     2025-06-03 16:00:00  Electronics     HD Monitor                   5      101.04             0  Debit Card      Cancelled
    1051  CUST-114     2025-08-04 21:00:00  Home & Kitchen  Blender                      3      170.78          0.05  Apple Pay       Cancelled
    1052  CUST-124     2025-01-01 09:00:00  Clothing        Winter Jacket                5       97.28           0.2  Debit Card      Completed
    1053  CUST-114     2025-12-12 06:00:00  Sports          Resistance Bands             3      144.85          0.15                  Pending
    1054  CUST-126     2025-06-21 02:00:00  Clothing        Cotton T-Shirt               3      159.48           0.2  PayPal          Cancelled
    1055  CUST-110     2025-09-01 19:00:00  Clothing        Denim Jeans                  2       17.08          0.05  Credit Card     Pending
    1056  CUST-114     2025-03-17 20:00:00  Sports          Dumbbell Set                 4      153.37          0.05  Credit Card     Refunded
    1057  CUST-128     2025-08-26 01:00:00  Electronics     USB-C Cable                  2       61.01           0.2                  Completed
    1058  CUST-130     2025-10-14 19:00:00  Electronics     USB-C Cable                  2      242.41           0.2  Debit Card      Refunded
    1059  CUST-129     2025-08-17 05:00:00  Books           Sci-Fi Novel                 5      133.75           0.2  Apple Pay       Pending
    1060  CUST-109     2025-05-21 14:00:00  Clothing        Hoodie                       5      150.53          0.05  Credit Card     Cancelled
    1061  CUST-110     2025-02-11 04:00:00  Clothing        Hoodie                       3      102.72           0.2  PayPal          Completed
    1062  CUST-113     2025-10-05 14:00:00  Clothing        Denim Jeans                  1      130.31           0.1  Apple Pay       Completed
    1063  CUST-107     2025-10-22 12:00:00  Books           System Design                5      284.36             0  Apple Pay       Completed
    1064  CUST-112     2025-11-05 07:00:00  Home & Kitchen  Blender                      4      166.08           0.2  Apple Pay       Completed
    1065  CUST-109     2025-03-26 14:00:00  Books           System Design                1      122.77          0.15  PayPal          Shipped
    1066  CUST-118     2025-02-12 20:00:00  Electronics     USB-C Cable                  5      173.67             0  Apple Pay       Completed
    1067  CUST-128     2025-04-19 14:00:00  Books           Python Data Analysis         1       85.45           0.1  Debit Card      Completed
    1068  CUST-125     2025-08-29 00:00:00  Books           Algorithms Unlocked          4       83.16             0                  Completed
    1069  CUST-112     2025-04-13 00:00:00  Clothing        Cotton T-Shirt               1      228.73          0.05                  Completed
    1070  CUST-108     2025-08-27 22:00:00  Clothing        Running Shoes                1      173.55          0.05  Debit Card      Refunded
    1071  CUST-112     2025-03-25 09:00:00  Clothing        Winter Jacket                5      289.48             0  Credit Card     Shipped
    1072  CUST-101     2025-02-08 18:00:00  Home & Kitchen  Desk Lamp                    4      125.03          0.05  PayPal          Completed
    1073  CUST-123     2025-01-22 11:00:00  Home & Kitchen  Desk Lamp                    1      240.91           0.2                  Pending
    1074  CUST-122     2025-08-04 15:00:00  Home & Kitchen  Coffee Maker                 5      197.79             0  Credit Card     Pending
    1075  CUST-112     2025-11-30 08:00:00  Books           Python Data Analysis         4       61.08           0.2                  Refunded
    1076  CUST-130     2025-05-18 10:00:00  Sports          Tennis Racket                4      136.32           0.2  PayPal          Refunded
    1077  CUST-130     2025-10-19 19:00:00  Electronics     HD Monitor                   4       80.72          0.15  Apple Pay       Completed
    1078  CUST-101     2025-05-13 10:00:00  Books           Algorithms Unlocked          2      151.39           0.1  Debit Card      Shipped
    1079  CUST-123     2025-02-13 07:00:00  Home & Kitchen  Desk Lamp                    1      159.82          0.05  Apple Pay       Pending
    1080  CUST-118     2025-02-17 09:00:00  Clothing        Running Shoes                4      139.97             0  PayPal          Pending
    1081  CUST-123     2025-09-29 11:00:00  Clothing        Hoodie                       5      117.02           0.2  Apple Pay       Cancelled
    1082  CUST-118     2025-04-29 03:00:00  Home & Kitchen  Stainless Steel Pan          4       88.57           0.1  PayPal          Completed
    1083  CUST-104     2025-05-22 23:00:00  Sports          Dumbbell Set                 2       72.75          0.15                  Refunded
    1084  CUST-117     2025-04-27 11:00:00  Sports          Water Bottle                 1      251.46           0.1  PayPal          Completed
    1085  CUST-101     2025-10-11 09:00:00  Sports          Dumbbell Set                 3        23.2             0  PayPal          Cancelled
    1086  CUST-128     2025-09-03 14:00:00  Books           SQL Essentials               1      176.48          0.15  Debit Card      Completed
    1087  CUST-102     2025-09-09 02:00:00  Home & Kitchen  Blender                      1      248.41          0.15                  Cancelled
    1088  CUST-122     2025-02-13 07:00:00  Electronics     Mechanical Keyboard          2      245.23           0.1  Credit Card     Shipped
    1089  CUST-125     2025-09-25 12:00:00  Books           Sci-Fi Novel                 5      239.31          0.05  Apple Pay       Pending
    1090  CUST-110     2025-11-09 23:00:00  Sports          Tennis Racket                3       174.9             0  Credit Card     Refunded
    1091  CUST-107     2025-10-10 02:00:00  Clothing        Hoodie                       1       55.55          0.05  PayPal          Completed
    1092  CUST-114     2025-05-28 22:00:00  Books           Sci-Fi Novel                 4       94.47          0.05  Debit Card      Cancelled
    1093  CUST-128     2025-12-05 06:00:00  Books           SQL Essentials               2      277.93           0.2  Apple Pay       Completed
    1094  CUST-118     2025-01-31 05:00:00  Clothing        Denim Jeans                  3      249.72             0  Debit Card      Shipped
    1095  CUST-124     2025-12-25 12:00:00  Sports          Water Bottle                 4       46.06           0.1  Debit Card      Shipped
    1096  CUST-118     2025-06-15 19:00:00  Books           System Design                1      183.43          0.15  Debit Card      Completed
    1097  CUST-103     2025-10-23 01:00:00  Clothing        Winter Jacket                5      285.73           0.1  PayPal          Pending
    1098  CUST-117     2025-11-22 15:00:00  Books           Algorithms Unlocked          2      299.11          0.15  Credit Card     Pending
    1099  CUST-112     2025-06-18 13:00:00  Books           Algorithms Unlocked          3      204.34          0.05  Apple Pay       Completed
    1100  CUST-122     2025-05-10 10:00:00  Books           Sci-Fi Novel                 1       141.9           0.1  Credit Card     Refunded
    1101  CUST-113     2025-04-07 16:00:00  Sports          Yoga Mat                     5      143.97             0  Debit Card      Shipped
    1102  CUST-125     2025-03-09 09:00:00  Books           System Design                1       69.03           0.2  Apple Pay       Cancelled
    1103  CUST-116     2025-06-09 17:00:00  Electronics     Wireless Mouse               5       241.8          0.05  Credit Card     Shipped
    1104  CUST-114     2025-11-28 04:00:00  Electronics     Mechanical Keyboard          1      143.82             0  Apple Pay       Cancelled
    1105  CUST-110     2025-05-05 14:00:00  Sports          Water Bottle                 4      252.07          0.15                  Completed
    1106  CUST-113     2025-02-05 08:00:00  Clothing        Winter Jacket                5      226.42          0.05  Apple Pay       Completed
    1107  CUST-130     2025-10-28 18:00:00  Sports          Water Bottle                 1       92.02           0.1  Apple Pay       Refunded
    1108  CUST-105     2025-10-06 12:00:00  Books           Sci-Fi Novel                 4      110.09           0.2  Apple Pay       Completed
    1109  CUST-128     2025-01-23 10:00:00  Clothing        Denim Jeans                  5      121.06          0.15  Apple Pay       Cancelled
    1110  CUST-130     2025-03-06 16:00:00  Books           System Design                2      153.65             0                  Completed
    1111  CUST-128     2025-01-08 23:00:00  Electronics     USB-C Cable                  1      162.53          0.15  PayPal          Pending
    1112  CUST-128     2025-06-23 19:00:00  Clothing        Cotton T-Shirt               4      236.64           0.1  Apple Pay       Cancelled
    1113  CUST-103     2025-10-05 01:00:00  Home & Kitchen  Desk Lamp                    4       286.7          0.15                  Completed
    1114  CUST-108     2025-11-21 22:00:00  Home & Kitchen  Air Fryer                    1      135.85             0  Credit Card     Pending
    1115  CUST-106     2025-05-31 11:00:00  Home & Kitchen  Coffee Maker                 1      104.07             0  Debit Card      Pending
    1116  CUST-105     2025-03-29 05:00:00  Clothing        Winter Jacket                4      174.12          0.05  Credit Card     Shipped
    1117  CUST-128     2025-03-15 07:00:00  Books           Sci-Fi Novel                 2      154.32           0.2  Apple Pay       Cancelled
    1118  CUST-109     2025-05-28 21:00:00  Books           Algorithms Unlocked          1      270.68          0.15                  Completed
    1119  CUST-103     2025-12-20 08:00:00  Books           Algorithms Unlocked          5       96.75          0.15  Apple Pay       Refunded
    1120  CUST-110     2025-10-20 11:00:00  Clothing        Running Shoes                4       40.93          0.15                  Completed
    1121  CUST-123     2025-12-18 23:00:00  Home & Kitchen  Coffee Maker                 4        89.6           0.2  Credit Card     Shipped
    1122  CUST-124     2025-04-23 20:00:00  Books           Algorithms Unlocked          2      186.05           0.1  PayPal          Shipped
    1123  CUST-109     2025-01-18 18:00:00  Clothing        Cotton T-Shirt               1       99.59          0.15  Debit Card      Cancelled
    1124  CUST-105     2025-04-13 04:00:00  Electronics     HD Monitor                   3      226.77          0.05                  Completed
    1125  CUST-117     2025-06-01 23:00:00  Sports          Water Bottle                 2       84.52          0.15  Debit Card      Refunded
    1126  CUST-104     2025-12-13 23:00:00  Books           SQL Essentials               2       228.7          0.05  Apple Pay       Refunded
    1127  CUST-126     2025-05-16 17:00:00  Sports          Water Bottle                 1       239.3             0  Credit Card     Pending
    1128  CUST-112     2025-02-25 21:00:00  Home & Kitchen  Desk Lamp                    4       248.5           0.1  PayPal          Pending
    1129  CUST-101     2025-11-28 02:00:00  Sports          Resistance Bands             3      275.42          0.05  Apple Pay       Cancelled
    1130  CUST-110     2025-06-05 15:00:00  Books           SQL Essentials               2       23.15             0  Credit Card     Completed
    1131  CUST-108     2025-08-03 18:00:00  Sports          Dumbbell Set                 4      141.56           0.2  PayPal          Pending
    1132  CUST-121     2025-01-17 22:00:00  Electronics     USB-C Cable                  5      128.35           0.1  Debit Card      Completed
    1133  CUST-115     2025-10-06 20:00:00  Books           Python Data Analysis         3       38.81           0.1  Debit Card      Completed
    1134  CUST-113     2025-02-16 21:00:00  Home & Kitchen  Air Fryer                    1      285.21          0.15  PayPal          Cancelled
    1135  CUST-121     2025-03-06 18:00:00  Sports          Yoga Mat                     1      238.17          0.05  PayPal          Completed
    1136  CUST-127     2025-06-18 04:00:00  Sports          Dumbbell Set                 5       72.63          0.05                  Completed
    1137  CUST-109     2025-02-26 21:00:00  Clothing        Denim Jeans                  5       82.69          0.05  Credit Card     Completed
    1138  CUST-101     2025-05-16 01:00:00  Home & Kitchen  Air Fryer                    5      103.89          0.05  PayPal          Cancelled
    1139  CUST-114     2025-09-20 18:00:00  Sports          Yoga Mat                     1      148.11           0.1  Credit Card     Pending
    1140  CUST-117     2025-06-04 14:00:00  Clothing        Winter Jacket                1       220.9           0.2  Credit Card     Completed
    1141  CUST-116     2025-02-07 02:00:00  Books           System Design                1      152.18          0.15  Debit Card      Shipped
    1142  CUST-105     2025-10-08 22:00:00  Electronics     Mechanical Keyboard          3      191.05           0.2  Debit Card      Pending
    1143  CUST-120     2025-02-20 22:00:00  Sports          Water Bottle                 4      156.61          0.15  Credit Card     Refunded
    1144  CUST-121     2025-07-31 10:00:00  Sports          Dumbbell Set                 4      140.95          0.05  Apple Pay       Pending
    1145  CUST-114     2025-07-11 04:00:00  Electronics     HD Monitor                   4      100.63           0.1  Apple Pay       Completed
    1146  CUST-103     2025-03-08 17:00:00  Electronics     Wireless Mouse               4          38           0.1  Credit Card     Shipped
    1147  CUST-118     2025-01-27 09:00:00  Sports          Water Bottle                 1      129.13          0.15                  Completed
    1148  CUST-112     2025-04-25 03:00:00  Electronics     Bluetooth Speaker            5       71.69          0.15  Debit Card      Refunded
    1149  CUST-118     2025-10-15 19:00:00  Home & Kitchen  Coffee Maker                 3      176.49          0.15                  Cancelled
    1150  CUST-121     2025-01-15 05:00:00  Sports          Yoga Mat                     5      279.43           0.1  Debit Card      Cancelled
sqlite>
```
