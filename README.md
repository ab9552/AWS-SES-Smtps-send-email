# AWS-SES-Smtps-send-email
send email using mailx and aws ses smtp

#Installing mailx
  yum -y update
  yum install -y mailx
#We can now start sending e-mails using
#create a symbolic link
  ln -s /bin/mailx /bin/email
###Set an External SMTP Server to Relay E-Mails

Open the file and add below containe in --->  vi /etc/mail.rc
  edit
  set smtp=smtps://email-smtp.us-east-1.amazonaws.com:465
  set smtp-auth=login
  set smtp-auth-user=AKIASIWQ4VCX5QKES/smtp creds access key
  set smtp-auth-password=BJyEJ3fQXm64DaKeAi2UBwt2B5QV8j2fS+x/ smtps secretee key
  set ssl-verify=ignore
  set nss-config-dir=/etc/pki/nssdb/

example usage :
echo "Your message" | mail -r receiver -s "Message Subject" email@address

