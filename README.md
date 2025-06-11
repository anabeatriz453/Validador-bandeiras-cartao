# 💳 Projeto DIO Validador de Bandeiras de Cartão de Crédito
- Este projeto é um validador de bandeiras de cartão de crédito desenvolvido em JavaScript pelo GITHUB COPILOT. Ele identifica a bandeira de um cartão com base no número fornecido, utilizando regras específicas para cada bandeira.

## Funcionalidades
- Identificação de Bandeiras: Determina a bandeira do cartão de crédito com base nos números iniciais.
- Sanitização de Entrada: Remove espaços e traços do número do cartão para garantir uma validação precisa.
- Suporte a Diversas Bandeiras:
Visa,
MasterCard,
Elo,
American Express,
Discover e
Hipercard

## Regras de Validação
- As regras para identificar cada bandeira são baseadas nos números iniciais do cartão:

## Bandeira	Regra
- Visa	Começa com o número 4.
- MasterCard	Começa com os números 51-55 ou está no intervalo 2221-2720.
- Elo	Pode começar com prefixos específicos, como 4011, 4312, 4389, etc.
- American Express	Começa com 34 ou 37.
- Discover	Começa com 6011, 65 ou está no intervalo 644-649.
- Hipercard	Geralmente começa com 6062.

# Como Usar:

## Entrada:
- O número do cartão deve ser fornecido como uma string.
Pode conter espaços ou traços, que serão removidos automaticamente.

## Saída:
- Retorna o nome da bandeira do cartão (Visa, MasterCard, etc.).
Retorna 'Invalid' se o número não corresponder a nenhuma bandeira conhecida.

## Exemplo de Uso:
- Você pode testar a função com diferentes números de cartão para verificar a bandeira.

## Requisitos
- Node.js ou qualquer ambiente que suporte JavaScript.
