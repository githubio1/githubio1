import random
import string
import time
import os
import subprocess

first_name = "esa"
last_name = "7sa"
password = "Aa123456$"
email_count = 100

email_domain = "@gmail.com"
email_list = []

for i in range(email_count):
    email = first_name + '.' + last_name + str(i+1) + email_domain
    email_list.append(email)

for email in email_list:
    email_username = email.split('@')[0]
    command = f"curl -u {email_username}:{password} --url 'smtps://smtp.gmail.com:465' --ssl-reqd --mail-from '{email}' --mail-rcpt '{email}' --upload-file /dev/null"
    subprocess.Popen(command, shell=True)
    time.sleep(0.1)

print(f"{email_count} emails created successfully.")
