---
layout: post
title: Mail Harvesting With Python
subtitle: Crawl and Collect Email From A Website 
cover-img: /assets/img/thumbnail/mail-harvest.jpg
gh-repo: relarizky/mail-harvest
gh-badges: [fork, follow]
tags: [programming, python]
comments: true
---

So, kali ini gue akan kasih tau cara mengumpulkan email yang tersedia dari sebuah website dengan menggunakan script sederhana yang gue buat dengan bahasa pemrograman **Python**.

## Apa itu Mail Harvesting ?

**Mail Harvesting** adalah proses mengumpulkan daftar alamat email, biasanya untuk keperluan _spamming_. Proses ini dapat menggunakan berbagai teknik, salah satu nya yaitu _Crawling_.

**Crawling** sendiri merupakan sebuah istilah digunakan oleh bot search engine yang merujuk ke proses penelusuran website yang dilakukan oleh bot tersebut untuk tujuan pengindeksan website.

Tapi, kali ini kita akan melakukan _Crawling_ untuk mengumpulkan email yang tersedia dari sebuah website.

## Cara Kerja

Sebenernya cara kerja program ini cukup sederhana :

__Kumpulkan URL yang tersedia -> Scrap Email dari masing-masing URL -> save -> Kumpulkan URL lain dari masing-masing URL tersebut__

Dan script yang saya gunakan untuk scraping kurang lebih seperti berikut :

```python
def fetch_mail(self, url):
        ' Fetch the available mail in web page '
        regex = re.compile(r'([a-zA-Z0-9+._-]+@[a-zA-Z0-9._-]+\.[a-zA-Z0-9_-]+)')
        headers = {'user-agent' : self.user_agent}
        requests = Request.Session()

        with requests.get(url, headers = headers) as request:
            if request.status_code != 404: # If response code is not 404, we can fetch the mail
                source = request.text
                found_mail = regex.findall(source)
                found_mail = list(filter(filter_mail, found_mail))

                for mail in found_mail: # Saving all the found mail(s) into the file.
                    print(
                        self.BOLD + self.GREEN + current_time(),
                        'found', self.BOLD + self.GREEN + '{}'.format(mail),
                        'in', self.GREEN + '{}'.format(url)
                    )
                    self.save_mail(mail)
```


## Preview

Untuk Preview tools nya seperti berikut :

[![asciicast](https://asciinema.org/a/x9hPl7H4X7r2tbGDoJmpay252.svg){: .mx-auto.d-block :}](https://asciinema.org/a/x9hPl7H4X7r2tbGDoJmpay252)

Untuk tools-nya, langsung cek github saya [di sini](https://github.com/relarizky/mail-harvest).

