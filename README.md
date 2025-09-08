# Jenkins Installation (ubuntu os)
NOTE: Use Root user

```
curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
```

```
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
```

```
apt-get update
apt-get install jenkins
```

### Login to Jenkins using the below URL:

http://ec2-instance-public-ip-address:8080

Note: If you are not interested in allowing `All Traffic` to your EC2 instance <br>
      1. Delete the inbound traffic rule for your instance <br>
      2. Edit the inbound traffic rule to only allow custom TCP port `8080`

After you login to Jenkins, <br>
      - Run the command to copy the Jenkins Admin Password - <br>
```
cat /var/lib/jenkins/secrets/initialAdminPassword
```
<br>
      - Copy and Enter the Administrator password

