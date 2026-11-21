# Continue

`continue` interrompe a iteração atual de um loop e passa para a próxima iteração do loop mais interno.

```python
for i in range(10):
	print("isso acontece todas as vezes")
	continue
	print("isso nunca é impresso")
```

Isso executa todas as `10` iterações do loop, mas a instrução `print` após o `continue` é sempre pulada.

Também funciona em loops `while`.

```python
while True:
	if not can_harvest():
		continue

	harvest()
```

Este código chama `harvest()` somente quando `can_harvest()` é `True`.
Ele tem o mesmo efeito que:

```python
while True:
	if can_harvest():
		harvest()
```

Em loops aninhados, `continue` sempre afeta o loop mais interno.

```python
for i in range(2):
	for j in range(2):
		print("isso é impresso 4 vezes")
		continue
		print("isso nunca é impresso")
	print("isso é impresso 2 vezes")
```
