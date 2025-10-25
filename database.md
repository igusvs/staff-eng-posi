Banco de dados
    
    Conceitos 

        - ACID (Atomicity, consistency, isolation e durability)
            - Principal CASE ** SQL Tradicional ** Teorama CAP ** CA **
            
            - Atomicidade 
                > Garante que toda transacao deve ser escutada, ela se torna algo indivisivel (Tudo ou nada).

            - Consistencia
                > Garante que o banco sempre trabalhe com o dado integro e consistente (Ultima foto sempre)

            - Isolamento 
                > Garante que uma transacao não interfira a outra (Exemplo de locks aplicados para evitar leituras sujas)
            
            - Durabilidade
                > Garante que após acatado o Commit, o mesmo se mantera daquela forma (Confiabilidade do sistema)

        - BASE (Basicamente disponivel, Soft state e eventualmente consistente) **Cenario mais flexivel, diferente do ACID**

            > Basicamente disponivel
                > Estara acessivel na maior parte do tempo, mas pode haver indisponibilidade em alguns dados devido a falhas em particoes ou rede

            > Soft state
                > Os dados podem expirar ou não estar atualizados entao não temos garantia de consistencias 
            
            > Eventualmente consistente
                > Consistencia eventual caracteriza em uma atualização de dados async, nem sempre voce vai ter a ultimo estado do dado, o tradeoff seria ter um dado nao atualizado em alguns momentos, mas em algum momento o registro se torna consistente
            


    TEOREMA CAP 
        - C > Consistencia ? Sempre a ultima informacao do registro 

            Detalhe > Nao importa qual nó seja consultado, sempre teremos a informação mais recente daquele registro 
            
        - D > Disponibilidade ? Sempre disponivel para receber leitura ou gravacao mesmo que sacrifique a consistencia

            Detalhe > Sempre respondendo, porem sacrificando a consistencia do registro, dados sendo tratados de forma ASYNC entre leitura e escrita 


        - T > Tolerancia a particao ? Sistema operando em caso de falha de rede entre particoes

            Detalhe> Tolerante a falhas parciais


    Combinacoes "Escolha ate dois"
        CP (Consistencia e tolerancia a particoes)
            > O sistema mantem consistente atraves de todos os nos que continuam operando em caso de falhas de rede ou particoes

            ex: MongoDB _ Cassandra

        AP (Disponibilidade e Tolerancia a particoes)
            > Sistema prioriza entrega de alta disponibilidade e tolerancia a particoes, porem com reducao a consistencia

            ex: DynamoDB

        CA (Consistencia e disponibilidade)
            > Alta consistencia e alta disponibilidade porem pode irá apresentar falhas em um problema de particoes

            ex: SQL server, Mysql

