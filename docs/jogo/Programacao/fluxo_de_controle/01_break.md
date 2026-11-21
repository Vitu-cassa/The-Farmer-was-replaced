# Break

`break` permite interromper um loop antes do fim. Quando uma instrução `break` é alcançada, ela sai imediatamente do loop mais interno e começa a executar o código após esse loop.

```python
for i in range(10):
	break
print(i)
```

Isso imprime `0` porque `i` é `0` durante a primeira iteração; em seguida, a instrução `break` encerra o loop.

Também funciona em loops `while`.

```python
while True:
	if can_harvest():
		break
harvest()
```

Este código executa o loop `while` até que `can_harvest()` seja `True`.
Ele tem o mesmo efeito que:

```python
while not can_harvest():
	pass
harvest()
```

Em loops aninhados, `break` sempre sai do loop mais interno.

```python
for i in range(10):
	for j in range(10):
		break
		print("isso nunca é impresso")
	print("isso é impresso 10 vezes")
```
