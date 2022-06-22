# Prova

Abrir o Terminal e digite;
pip install django (instalar o django)
django-admin startproject nome_do_projeto 

● Crie o banco de dados antes
de podermos usá-las. Para
fazer isso, execute o
seguinte comando:

python manage.py migrate

Para testar se o seu projeto
Django funciona:

○ python manage.py runserver

● Starting development serverat;
○ http://127.0.0.1:8000/

● Inicie o app executando essa
linha de comando:

○ python manage.py startapp nome_do_app

Criando um usuário
administrador com o
comando abaixo

○ python manage.py createsuperuser

● Agora, abra um navegador da
Web e vá para "/ admin /":
http://127.0.0.1:8000/admin
__________________________________________
from django.db import models

class Alunos(models.Model):

nome = models.CharField(max_length=100)
endereco = models.CharField(max_length=100)
email = models.CharField(max_length=100)

def __str__(self):
return self.nome
____________________________________________

from django.contrib import admin
from .models import Alunos

admin.site.register(Alunos)
_______________________________________________

python manage.py makemigrations
python manage.py migrate
















