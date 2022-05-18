# telegramBOT--ACCOUNTANT
import sqlite3

try :
    conn = sqlite3.connect ("accountant.db")
    cursor = conn.cursor()

    # создаем пользователя с user_id = 1000
    cursor.execute ("INSERT OR IGNORE INTO `users` (`users_ID`) VALUES(?)",(100,))
except sqlite3.Error as error:
    #Считываем пользователей
    users = cursor.execute("SELECT * FROM `users`")
    print(users.fetchall())
    # подтверждаем изменения 
    conn.commit()

    print('Error', error)
finally:
    if (conn):
        conn.close()
