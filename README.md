# Bugscanner Installation & Usage Guide

এই রিপোজিটরিতে `bugscanner` টুলটি ইনস্টল এবং রান করার প্রয়োজনীয় কমান্ড ও নিয়মগুলো দেওয়া রয়েছে।

## ১. সিস্টেম ও প্যাকেজ আপডেট এবং পাইথন ইনস্টলেশন
```bash
apt update && apt upgrade -y
apt install git python python-pip -y

git clone [https://github.com/aztecrabbit/bugscanner](https://github.com/aztecrabbit/bugscanner)
cd bugscanner

python3 -m pip install --upgrade pip setuptools
python3 -m pip install -r requirements.txt
pip install websocket-client loguru multithreading requests
python3 setup.py install

bugscanner -h

bugscanner --mode direct --port 80,443 --threads 10 all_companies.txt --output result.txt


