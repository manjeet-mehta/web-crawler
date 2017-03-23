import requests
from bs4 import BeautifulSoup
import urllib.request
import random

a=int(input())
b=int(input())
def download_web_image(url):
    name = random.randrange(1, 1000)
    full_name = str(name) + ".jpg"
    urllib.request.urlretrieve(url, full_name)


def my_crawler(m,n):
    for i in range(m,n):
        url = 'https://xkcd.com/' + str(i) + '/'
        source_code = requests.get(url)
        plain_text = source_code.text
        soup = BeautifulSoup(plain_text,"html.parser")

        j=0
        for link in soup.find_all('img'):
            s = link.get('src')
            hr='http:'+s
            if j==1:
                download_web_image(hr)
            j+=1

my_crawler(a,b)
