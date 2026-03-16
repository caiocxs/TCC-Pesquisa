___

"In this setup, Datalog acts as a domain speciﬁc language (DSL) for deﬁning program analyses. A program is encoded into a database i.e., a set of input relations, and the program analysis constraints are deﬁned as a Datalog query. A Datalog solver acts as a programmable ﬁxed point engine that computes a least ﬁxed point solution to the program analysis constraints. Datalog enables both a succinct and modular encoding of the program analysis, while providing high eﬃciency and interoperability [\[33\]](https://doi.org/10.1145/2892208.2892226).";



"To introduce program repair to this setup, we propose a novel approach called symbolic of Datalog (SEDL). We deﬁne the repair search space by injecting symbols into the input relations representing the buggy program. These symbols denote unknown constants, unknown predicates, unknown truthfulness of facts in the database.";

"We implemented SEDL in a tool called Symlog, which utilizes the state-of-the-art Datalog engine Souﬄé [\[19\]](https://doi.org/10.1007/978-3-319-41540-6_23). Symlog transforms a given symbolic database and query into a meta-program, which, when executed using a conventional Datalog evaluator, produces the result of symbolically executing the original query on the original database.";

[Delta-Debuging](https://doi.org/10.1145/318774.318946)
[Z3](https://doi.org/10.1007/978-3-540-78800-3_24)
[Doop](https://doi.org/10.1145/1639949.1640108)
[Digger](https://doi.org/10.1145/3394451.3397206)

**Symbolic Execution of Datalog (Execução Simbólica de Datalog)**
	Pega os fatos lógicos que alimentam um programa em Datalog e injeta variáveis simbólicas neles. A partir daí, ele consegue rastrear a execução e extrair as exatas restrições lógicas e matemáticas que levam o sistema a um estado específico.

