# email-verification-
import smtplib

# List of email addresses to send the email to
recipients = ['email1@example.com', 'email2@example.com', 'email3@example.com']

# Your email address and password
sender = 'your_email@example.com'
password = 'your_email_password'

# The email subject and message
subject = 'Bulk email test'
message = 'This is a test of the bulk email function.'

# Connect to the email server and send the email
server = smtplib.SMTP('smtp.example.com', 587)
server.starttls()
server.login(sender, password)
server.sendmail(sender, recipients, f'Subject: {subject}\n\n{message}')
server.quit()
