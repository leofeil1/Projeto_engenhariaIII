@startuml
left to right direction
actor Vendedor as ac1
actor Recepcionista as ac2
actor Cliente as ac3
actor Gerente as ac4

rectangle "loja de roupas" {
    actor Sistema

    ac3 --> (Comprar item)
    ac1 --> (oferece metodos de pagamento)
    ac3 --> (Realizar pagamento)
    ac3 --> (Deixar feedback) : extend
    ac1 --> (Registrar venda)
    (Registrar venda) --> Sistema
    ac1 --> (Itens comprados)
    (Itens comprados) --> Sistema
    ac1 --> (Calcular venda)
    (Calcular venda) --> Sistema
    ac1 --> (capturar informação dos itens)
    (capturar informação dos itens) --> Sistema
    ac1 --> (código de barras)
    (código de barras) --> Sistema
    ac1 --> (código do item)
    (código do item) --> Sistema
    ac1 --> (reduzir quantidade de itens)
    (reduzir quantidade de itens) --> Sistema
    ac1 --> (exibir descrição)
    (exibir descrição) --> Sistema

    ac1 --> (Log in)
    ac2 --> (Log in)
    ac3 --> (Log in)
    ac4 --> (Log in)
    (Log in) ..> Sistema : include

    ac1 --> Sistema : usa
    ac2 --> Sistema : usa
    ac3 --> Sistema : usa
    ac4 --> Sistema : usa
}

@enduml
