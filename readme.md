# Relatório sobre a Implementação de uma Blockchain em Python

### Introdução:
A blockchain é uma tecnologia de registro distribuído que permite a criação de um ledger público imutável. Este relatório discutirá a implementação de uma blockchain simples em Python, conforme demonstrado no código fornecido.

### Estrutura do Bloco:
A estrutura de um bloco na blockchain inclui índice, carimbo de data e hora, transações, prova de trabalho (proof), e o hash do bloco anterior. Cada bloco é conectado ao anterior através do hash.

### Criação da Cadeia de Blocos:
A cadeia de blocos é uma lista de blocos. O primeiro bloco, conhecido como "bloco gênesis", é criado durante a inicialização. Novos blocos são adicionados à cadeia por meio do processo de mineração.

### Mineração e Prova de Trabalho:
O algoritmo de prova de trabalho é utilizado para minerar novos blocos. Isso envolve encontrar um valor (nonce) de forma que o hash do bloco atenda a determinados critérios, como começar com zeros. A recompensa pela mineração é uma transação com um remetente fictício e o mineiro como destinatário.

### Transações:
As transações são adicionadas ao bloco por meio do método new_transaction(). Cada transação inclui remetente, destinatário e quantidade.

### Consensus e Resolução de Conflitos:
Para garantir um consenso na rede, o algoritmo de resolução de conflitos é implementado. Cada nó verifica a validade da cadeia e substitui a sua própria se uma cadeia mais longa e válida for encontrada.

### Nodes e Registro:
Os nós da rede são registrados dinamicamente através do método register_node(). Isso permite a comunicação entre os nós para atingir um consenso.

### Validação da Cadeia:
A validação da cadeia é realizada por meio do método is_valid_chain(), que verifica a integridade dos hashes e a prova de trabalho.

### Demonstração do Sistema:
O sistema foi implementado como uma aplicação Flask. Os endpoints /mine, /transactions/new, /chain, /nodes/register, e /nodes/resolve fornecem funcionalidades para mineração, criação de transações, visualização da cadeia, registro de nós e resolução de conflitos, respectivamente.

### Conclusão:
A implementação da blockchain em Python fornece uma compreensão prática dos conceitos fundamentais por trás dessa tecnologia. Este relatório destacou os principais aspectos do código e a lógica por trás da criação de uma blockchain simples. Essa implementação serve como uma base sólida para a compreensão de blockchains mais complexas.