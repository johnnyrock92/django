# Instalacja django na Windows
### 0. Instalacja Pythona

**a)** Wejdź na stronę: https://www.python.org/downloads/

**b)** Pobierz i zainstaluj Pythona

**c)** Otwórz wiersz polecenia i wpisz: python

Powinno ukazać się to:
```cmd
C:\Users\Janusz>python
Python 2.7.13 (v2.7.13:a06454b1afa1, Dec 17 2016, 20:42:59) [MSC v.1500 32 bit (Intel)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

### 1. Instalacja Virtualenv (Wirtualne środowisko)
**a)** Wejdź na stronę: https://pypi.python.org/pypi/virtualenv

**b)** Pobierz: virtualenv-15.1.0.tar.gz (md5, pgp)

**c)** Wypakuj pobrane archiwum: virtualenv-15.1.0.tar.gz

**d)** Otwórz wiersz poleceń i przejdź do katalogu w którym masz rozpakowane archiwum:
```cmd
C:\Users\Janusz>cd C:\Users\Janusz\Downloads\dist\virtualenv-15.1.0
```
**e)** Zainstaluj Virtualenv
```cmd
C:\Users\Janusz\Downloads\dist\virtualenv-15.1.0>python setup.py install
```

### 2. Utwórz i aktywuj wirtualne środowisko
**a)** Utwórz wirtualne środowisko nazywając je: "myenv"
```cmd
C:\Users\Janusz>python -m virtualenv myenv
C:\Users\Janusz>dir
```
**b)** Aktywuj wirtualne środowisko "myenv"
```cmd
C:\Users\Janusz>.\myenv\Scripts\activate
(myenv) C:\Users\Janusz
```

### 3. Instalacja django
**a)**
Zainstaluj django
```cmd
(myenv) C:\Users\Janusz>pip install django
Collecting django
  Downloading Django-1.11.1-py2.py3-none-any.whl (6.2MB)
    100% |################################| 6.2MB 48kB/s
Installing collected packages: django
Successfully installed django-1.11.1
(myenv) C:\Users\Janusz>
```
**b)** Otwórz wiersz polecenia i wpisz:
```cmd
(myenv) C:\Users\Janusz>python
Python 2.7.13 (v2.7.13:a06454b1afa1, Dec 17 2016, 20:42:59) [MSC v.1500 32 bit (Intel)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> import django
>>> print(django.get_version())
1.11.1
>>>
```

# Tworzenie pierwszej aplikacji
### 1. Utwórz projekt
```cmd
C:\Users\Janusz>.\myenv\Scripts\activate
(myenv) C:\Users\Janusz>django-admin startproject mysite
(myenv) C:\Users\Janusz>dir mysite
(myenv) C:\Users\Janusz>dir mysite\mysite
```
### 2. Utwórz domyślną bazę danych oraz tabele
```cmd
(myenv) C:\Users\Janusz>cd mysite
(myenv) C:\Users\Janusz\mysite>python manage.py migrate
```
### 3. Sprawdź czy baza danych została poprawnie utworzona "db.sqllite3" 
```cmd
(myenv) C:\Users\Janusz\mysite>dir
(myenv) C:\Users\Janusz>cd mysite
(myenv) C:\Users\Janusz\mysite>python manage.py migrate
```
### 3. Sprawdź czy baza danych została poprawnie utworzona "db.sqllite3" 
```cmd
(myenv) C:\Users\Janusz\mysite>dir
```
### 4. Sprawdź twój projekt django

**a)**
Uruchom serwer deweloperski
```cmd
(myenv) C:\Users\Janusz\mysite>python manage.py runserver
```

**b)**
Wejdź na stronę: http://127.0.0.1:8000/
