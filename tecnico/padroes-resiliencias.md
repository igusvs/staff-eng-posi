Definicao de resiliencia 

Referece a capacidade de sistemas, processos ou componentes de suportar cenarios de falhas e manter sua operacao 


Resiliencia e disponibilidade

    - Resiliencia é medida partindo de quantas solicitaoces foram processadas com sucesso
    - Disponibilidade é medida por quanto tempo o sistema ficou disponivel 

    Detalhe: Resiliencia é um conjunto de formas para se manter disponivel


Timeout 

    - Aplicar e definir timeouts em integração, afim de evitar uma degradação do todo.

Estrategia de retry

    - Ato de retentar em caso de falha
    - Podendo implementar um retry com backoff, ou seja espaçar a quantidade de retentativas 

Circuit Breakers 

    - Ato de interromper o fluxo de chamada para um serviço X quando se detecta um alto numero de falhas

