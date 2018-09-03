# Механизмы Leaky Bucket и Token Bucket

```text
Звучит легко и понятно. Но как работает на практике и реализовано в железе?  
```

Пример.  
Ограничение в 400 Мб/с — это много \(или мало\)? В среднем клиент использует только 320. Но иногда поднимается до 410 на 5 минут. А иногда до 460 на минуту. А иногда до 500 на полсекунды.  
Как договоропорядочный провайдер linkmeup может сказать — 400 и баста! Хотите больше, подключайтесь на тариф 1Гб/с+27 аниме-каналов.  
А можем повысить лояльность клиента, если это не мешает другим, разрешив такие всплески.  
Как разрешить 460Мб/с на всего лишь одну минуту, а не на 30 или навсегда?  
Как разрешить 500 Мб/с, если полоса свободна, и прижать до 400, если появились другие потребители?  
Теперь передохните, налейте ведро крепкого.

```text
Начнём с более простого механизма, используемого шейпером — протекающее ведро. 
```
