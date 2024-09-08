# INFORMATION SYSTEMS ADMINISTRATION AND DEVELOPMENT
## OPEN SOURCE TECHNOLOGIES IN WEB DEVELOPMENT
## Django and MySQL Connection Setup
![ttt](https://github.com/user-attachments/assets/783511ca-2644-4447-8646-ad41344f29a7)
---
## 1. Install MySQL and PHP engine
Make sure MySQL is installed on your server. You can install it using:
```python
sudo apt install apache2 mysql-server php php-mysql php-imap php-mbstring php-xml php-zip php-json libapache2-mod-php
```

## 2. Install Django MySQL Client make sure you are within virtual enviroment
After creating your MySQL database, you need to install the MySQL client for Django. Run:
```python
pip install mysqlclient
```

## 3. creating MYSQL user and database
```python
sudo mysql -u root
```

## 4. Set the root password and grant permissions:

```sql
USE mysql;
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'your_password';
FLUSH PRIVILEGES;
```
```sql
GRANT ALL PRIVILEGES ON *.* TO 'root'@'10.0.2.15' IDENTIFIED BY 'your_password' WITH GRANT OPTION;
FLUSH PRIVILEGES;
```
```sql
GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY 'your_password' WITH GRANT OPTION;
FLUSH PRIVILEGES;
```
- creating database
```sql
create database inventory_mis
```
## 5. Exit MySQL:

```sql
exit;
```

## 6. Restart MySQL to apply changes:

```python
sudo systemctl restart mysql
```

## 7. Update settings.py for Database Connection
- Modify your settings.py file in your Django project to configure the database connection. Update the DATABASES setting as follows:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'inventory_mis',
        'USER': 'root',
        'PASSWORD': 'your_password',
        'HOST': '10.0.2.15',
        'PORT': '3306',
    }
}
```
 
## 8. Run Migrations
- Apply migrations to set up your database schema:

```python
python manage.py migrate
```
## 9. Create Superuser
- Create a superuser for accessing the Django admin interface:

```python
python manage.py createsuperuser
```

**My Contacts**

**WhatsApp**  
+255675839840  
+255656848274

**YouTube**  
[Visit my YouTube Channel](https://www.youtube.com/channel/UCjepDdFYKzVHFiOhsiVVffQ)

**Telegram**  
+255656848274  
+255738144353

**PlayStore**  
[Visit my PlayStore Developer Page](https://play.google.com/store/apps/dev?id=7334720987169992827&hl=en_US&pli=1)

**GitHub**  
[Visit my GitHub](https://github.com/shamiraty/)

