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
				- Usuários podem fazer transferências ao mesmo tempo;
		        - As transferências são não-atômicas. Uma pode começar (e terminar) 
				    enquanto uma ainda está em execução; 
		Isso causa o possível problema de retirar ao mesmo tempo uma quantia e 
	deixar o usuário com a conta negativa. Como lidar com erros assim? Tentar 
	consertar o bug para casos genéricos não garante que não aconteça mais! 
		O propósito de TLA+ é de explorar essas falhas de design.
    

#### _Estrutura_: 

	O framework possui três fases:
		- Descrever o sistema, chamado 'specification', ou 'spec'. 
			Neste exemplo, teremos:
				- Conjunto de contas, cada conta possui
					um número representando sua balança;
				- Qualquer conta pode tentar transferir
					qualquer quantia de dinheiro para outra conta;
			    - Cada transferência checa se tem a quantia
					requisitada. Se tiver, a quantia é retirada 
					da primeira conta e adicionada à segunda;
	            - Transferências são não-atômicas;
		Esta especificação tem um set de 'behaviors', ou possíveis execuções distintas;