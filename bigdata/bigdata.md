# Hadoop(BigData)
1. **[Hive](#Hive)**<br>
2. 



# Hive
2. Connect to hive cli
    1. type ```hive```
    2. type ```show databases;```
    3. type ```create database rritecdb```
    4. desc rritecdb;
        
        ![image](https://user-images.githubusercontent.com/20516321/214228819-f9f120ef-2280-4dd5-9318-8d2f797e7cae.png)

    5. How system knows to create folder in ```/user/hive/warehouse/```
    6. type ```SET;``` observe warehouse location property. using this set property system knows the location of warehouse
3. can we run hive commands from terminal
    1. Yes
    2. In normal terminal type ```hive -e "show databases;"```
    3. also observe ```"hive -e set;" | grep warehouse
        
        ![image](https://user-images.githubusercontent.com/20516321/214229607-49d7673b-0eef-4818-ab04-001ab46455de.png)

4. hive-site.xml configuration file has metastore database information
    1. open terminal ```cd /etc/hive/conf/```
    2. type ```cat hive-site.xml | grep metastore```
    3. observe metastore database as mysql
5. Connect to mysql(Metastore)
    1. open terminal > type ```mysql -uroot -pcloudera```

        ![image](https://user-images.githubusercontent.com/20516321/214223593-bffe40ce-a79c-41e7-8baa-414e8cef7c36.png)

    2. type ```show databases;```

        ![image](https://user-images.githubusercontent.com/20516321/214224728-8d6d2333-0f35-49f1-aebd-b038fc02f822.png)

    3. type ```use metastore;```
    6. type ```select * from DBS;```   