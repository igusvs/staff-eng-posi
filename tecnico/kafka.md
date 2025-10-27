**Componente**	        **Função**

    > Producer	        > Publica eventos (mensagens) em um tópico.
    > Topic	            > Canal lógico que organiza eventos por tipo. Ex: pagamentos.aprovados.
    > Partition	        > Divide um tópico em partes para escalar e manter ordem dentro de cada partição.
    > Broker	        > Servidor Kafka que armazena fisicamente os dados das partições.
    > Consumer	        > Lê eventos de um ou mais tópicos.
    > Consumer Group	> Conjunto de consumidores que trabalham juntos para processar um tópico em paralelo.
    > Zookeeper / KRaft	> Coordena e mantém o metadata do cluster (no Kafka moderno o KRaft substitui o ZooKeeper).