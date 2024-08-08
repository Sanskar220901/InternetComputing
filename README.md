# InternetComputing

What the Database looks like:
mysql> show tables;
+------------------------+
| Tables_in_inventory_db |
+------------------------+
| product                |
| supplier               |
| users                  |
+------------------------+
mysql> describe product;
+-------------+---------------+------+-----+---------+-------+
| Field       | Type          | Null | Key | Default | Extra |
+-------------+---------------+------+-----+---------+-------+
| ProductID   | int           | NO   | PRI | NULL    |       |
| ProductName | varchar(100)  | YES  |     | NULL    |       |
| Description | varchar(255)  | NO   | PRI | NULL    |       |
| Price       | decimal(10,2) | YES  |     | NULL    |       |
| Quantity    | int           | YES  |     | NULL    |       |
| Status      | char(1)       | YES  |     | NULL    |       |
| SupplierID  | int           | NO   | PRI | NULL    |       |
+-------------+---------------+------+-----+---------+-------+

mysql> select * from product;
+-----------+-------------+--------------------+---------+----------+--------+------------+
| ProductID | ProductName | Description        | Price   | Quantity | Status | SupplierID |
+-----------+-------------+--------------------+---------+----------+--------+------------+
|      1234 | TV          | Plate TV           | 1499.99 |        5 | A      |       7671 |
|      1234 | TV          | Plate TV           |  599.30 |        5 | B      |       8672 |
|      1234 | TV          | Plate TV           |  799.90 |       20 | C      |       9144 |
|      1516 | Mouse       | Wireless Mouse     |   69.90 |       25 | C      |       2345 |
|      1516 | Mouse       | Wireless Mouse     |   99.50 |       30 | A      |       3579 |
|      1516 | Mouse       | Wireless Mouse     |   69.50 |       20 | A      |       7807 |
|      1516 | Mouse       | Wireless Mouse     |   49.40 |       50 | B      |       9794 |
|      2591 | Camera      | Camera             |  799.90 |       50 | B      |       7890 |
|      2591 | Camera      | Digital Camera     |  449.40 |       50 | A      |       3592 |
|      2591 | Camera      | Digital Camera     |  499.90 |
 10 | B      |       9512 |
|      2591 | Camera      | Instant Camera     |  179.50 |       30 | C      |       8642 |
|      3034 | Telephone   | Cordless Phone     |  299.99 |
 40 | A      |       3456 |
|      3034 | Telephone   | Home Telephone     |   59.50 |       20 | A      |       8655 |
|      3034 | Telephone   | Home Telephone     |  169.99 |       15 | A      |       8692 |
|      3034 | Telephone   | Home telephone     |   99.90 |       25 | A      |       8765 |
|      3374 | Laptop      | Laptop             | 1399.20 |       10 | B      |       1357 |
|      3374 | Laptop      | Laptop             | 1369.90 |       15 | A      |       4567 |
|      3374 | Laptop      | MacBook Pro        | 1799.90 |
 30 | A      |       9876 |
|      3374 | Laptop      | Refurbished Laptop | 1099.10 |       20 | A      |       6954 |
+-----------+-------------+--------------------+---------+----------+--------+------------+

mysql> describe supplier;
+--------------+--------------+------+-----+---------+-------+
| Field        | Type         | Null | Key | Default | Extra |
+--------------+--------------+------+-----+---------+-------+
| SupplierID   | int          | NO   | PRI | NULL    |       |
| SupplierName | varchar(100) | YES  |     | NULL    |       |
| Address      | varchar(255) | YES  |     | NULL    |       |
| Phone        | varchar(20)  | YES  |     | NULL    |       |
| Email        | varchar(100) | YES  |     | NULL    |       |
+--------------+--------------+------+-----+---------+-------+
5 rows in set (0.01 sec)

mysql> select * from supplier;
+------------+------------------+---------------------------+----------------+-------------------------+
| SupplierID | SupplierName     | Address                   | Phone          | Email                   |
+------------+------------------+---------------------------+----------------+-------------------------+
|       1357 | Sharp            | 123 Tokyo St              | 80-4745-3107   | support@sharp.co.jp     |
|       2345 | MSI              | 789 Mofan St              | 943-299-465    | support@msi.tw          |
|       3456 | Panasonic        | 246 Osaka St              | 443-887-9967   | support@panasonic.co.jp |
|       3579 | RedPark Ltd.     | 789 Park Ave              | 604-683-2555   | info@redpark.ca         |
|       3592 | IBM              | 456 New York St           | 201-335-9423   | support@ibm.com         |
|       4567 | Qualcomm         | 456 San Diego St          | 44-7700-087231 | info@qualcomm.co.uk     |
|       6954 | Apple            | 246 Cupertino St          | 202-918-2132   | support@apple.com       |
|       7084 | Acer             | 135 Taipei St             | 905-926-031    | support@acer.tw         |
|       7671 | LG Electronics   | 789 Busan St              | 668-286-5378   | support@lge.kr          |
|       7807 | Intel            | 2200 Mission College Blvd | 408-646-7611   | support@intel.com       |
|       7890 | Samsung          | 456 Seoul St              | 909-763-4442   | support@samsung.com     |
|       8642 | Xerox Inc.       | 456 High St               | 505-398-8414   | info@xrx.com            |
|       8655 | Dell             | 246 Austin St             | 505-351-3181   | support@dell.com        |
|       8672 | AMD              | 246 Santa Clara St        | 312-866-2043   | support@amd.com         |
|       8692 | Microsoft        | 123 Redmond St            | 505-549-0420   | support@microsoft.com   |
|       8765 | Philips          | 789 Amsterdam St          | 61-483-898-670 | support@philips.au      |
|       9144 | Fujitsu          | 456 Tokyo St              | 03-3556-7890   | support@fujitsu.co.jp   |
|       9512 | Acme Corporation | 123 Main St               | 205-288-8591   | info@acme-corp.com      |
|       9794 | Amazon           | 246 Seattle St            | 555-343-8950   | support@amazon.com      |
|       9876 | Toshiba          | 246 Osaka St              | 90-6378-0835   | support@toshiba.co.jp   |
+------------+------------------+---------------------------+----------------+-------------------------+

![image](https://github.com/user-attachments/assets/d0b528e4-180f-4da1-9ce7-864b9c490e98)
