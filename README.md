import os
os.system("pip install phonenumbers")
import phonenumbers
from phonenumbers import timezone, geocoder, carrier
R = '\033[1;31m'
print(R)
Ph = input('حط رقم الهاتف معا رمز الدولة : ')
phoneNumber = phonenumbers.parse(Ph)
timeZone = timezone.time_zones_for_number(phoneNumber)
Carrier = carrier.name_for_number(phoneNumber, 'en')
Region = geocoder.description_for_number(phoneNumber, 'en')
print(f'{phoneNumber} : الرقم  + رمز الدولة')
print(f'{timeZone} : القاعداة  + القاراة')
print(f'{Carrier} : الرقم تابع لهذه الشركة')
print(f'{Region} : الدولة')
#كود جمع معلومات عن رقم الهاتف دولة الرقم شركة الرقم كان عاطل صلحته وعربته شرح


