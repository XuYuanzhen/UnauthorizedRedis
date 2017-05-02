# UnauthorizedRedis
You should use ZMAP to scan the IPs which open redis port(6379) and save the IPs in a file, here I use the file named "output.txt" or You can use whatever.
check login for unauthorized redis


#Step1   scan the IPs open port 6379

zmap   xxx.xx.xxx.0/24 -p 6379 -o ip.txt


#Step2 check the unauthorized Redis servers

python  redis_check.py  ip.txt
