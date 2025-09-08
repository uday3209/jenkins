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

'''
https://medium.com/@muppedaanvesh/a-hands-on-guide-to-argocd-on-kubernetes-part-1-%EF%B8%8F-7a80c1b0ac98#id_token=eyJhbGciOiJSUzI1NiIsImtpZCI6IjljNjI1MTU4Nzk1MDg0NGE2NTZiZTM1NjNkOGM1YmQ2Zjg5NGM0MDciLCJ0eXAiOiJKV1QifQ.eyJpc3MiOiJodHRwczovL2FjY291bnRzLmdvb2dsZS5jb20iLCJhenAiOiIyMTYyOTYwMzU4MzQtazFrNnFlMDYwczJ0cDJhMmphbTRsamRjbXMwMHN0dGcuYXBwcy5nb29nbGV1c2VyY29udGVudC5jb20iLCJhdWQiOiIyMTYyOTYwMzU4MzQtazFrNnFlMDYwczJ0cDJhMmphbTRsamRjbXMwMHN0dGcuYXBwcy5nb29nbGV1c2VyY29udGVudC5jb20iLCJzdWIiOiIxMTUwNjQ0NTM3MTI0NTUxMjAwNTAiLCJlbWFpbCI6InBvd2Vyc3Rhcjc2OTZAZ21haWwuY29tIiwiZW1haWxfdmVyaWZpZWQiOnRydWUsIm5iZiI6MTc1NzMzNDU5NSwibmFtZSI6IlBhdmFuIiwicGljdHVyZSI6Imh0dHBzOi8vbGgzLmdvb2dsZXVzZXJjb250ZW50LmNvbS9hL0FDZzhvY0s5SmZxOFlnT2ZlQ3JCNVdlSG0xNXFXS2dIU1VYMXcwd1VTUkE1VTJTbFdSejJPUT1zOTYtYyIsImdpdmVuX25hbWUiOiJQYXZhbiIsImlhdCI6MTc1NzMzNDg5NSwiZXhwIjoxNzU3MzM4NDk1LCJqdGkiOiI2ODZlYTc0Nzg3YTYyOTU3YzEyZjc5YjZmMWY2YWRjYTgzZWZmYTUyIn0.yajoFlaXth9ZagaOhhztl6YZI-Vjih9TgZljt244wgkvZQ8s4l__2O1TEGEfkkZeysxLA-m5AUI3xHEWy9YdFl2ppU7jI7kqCUlguDmUfg_30YIPBPDHlGHc4Og2TFz1OIAsuuDVSDZTTihzmTCrcJC_h5vv5R0NXCRl98LEjpPxT_wdRz4pKnYtQnKcjwG9xrYpgkJv7Vs6dzsbJm_nE6sWco7ykb_HsPL6m6AMKBIEEkjBQ--xZaJtorfyJfGAiQajgiRq3FeKh3Y__RggeHdysKm61dLK8XfnHLbZpG2sFbKF9nWpHUsMukLjR45QnsfIQtYqyp-GdcOOHI6OYw
'''
