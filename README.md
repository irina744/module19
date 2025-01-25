python manage.py shell
from task1.models import Buyer
Buyer.objects.create(name='Ilya15', balance=1500.05, age=24)
Buyer.objects.create(name='Vasya173, balance=42.15, age=38)
Buyer.objects.create(name='Petya4215', balance=0.5, age=16)
from task1.models import Game
Game.objects.create(title='Football', cost=31, size=46.25, description='Popular sports in our country', age_limited=True)
Game.objects.create(title='Rugby', cost=5, size=0.5, description='It is a rather violent game', age_limited=False)
Game.objects.create(title='Cricket', cost=12, size=36.6, description='Cricket is a typically British game', age_limited=True)
br1 = Buyer.objects.get(id=1)
br2 = Buyer.objects.get(id=2)
br2 = Buyer.objects.get(id=2)
Game.objects.get(id=1).buyer.set([br1, br2])
Game.objects.get(id=2).buyer.set([br1, br2, br3])
Game.objects.get(id=3).buyer.set([br1])
