---

---
##### Referências: [TLA+](https://lamport.azurewebsites.net/tla/tla.html) - [Learn TLA+](https://learntla.com/index.html)
---

#### *Breve descrição:* 
	Em um sistema de transferência para um banco, código da lógica basica:

		def transfer(from, to, amount)
			if (from.balance >= amount) # guard
			    from.balance -= amount;   # withdraw
			    to.balance += amount;     # deposit

		Em um sistema básico ele funciona, tal que só retira o que tem e adiciona, depois da retirada, na outra conta;
		Novas mudanças: 
				- Usuários 