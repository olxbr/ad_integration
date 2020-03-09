### Subcategoria `Carros, vans e utilitários`

Para esta subcategoria, é necessário preencher o parâmetro `category` com o valor `2101`.

Além disso, há parâmetros específicos para esta subcategoria, que devem constar dentro do parâmetro `params` e preenchidos conforme a tabela a seguir:

| Parâmetro | Valor | Tipo | Obrigatório | Descrição  |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------|-------------|------------------------------------------------|
| `carcolor` | `1` para Preto<br>`2` para Branco<br>`3` para Prata<br>`4` para Vermelho<br>`5` para Cinza<br>`6` para Azul<br>`7` para Amarelo<br>`8` para Verde<br>`9` para Laranja<br>`10` para Outra | string | não | Cor do carro |
| `parts_name_cars` | `1` para Pneus<br>`2` para Rodas<br>`3` para Calotas<br>`4` para Peças automotivas<br>`5` para GPS<br>`6` para Som e multimídia<br>`7` para Tuning e Performance<br>`8` para Acessórios para interior<br>`9` para Acessórios para exterior<br>`10` para Outros | string | não<sup>1</sup> | Indica o tipo de peça |
| `condition` | `1` para Novo<br>`2` para Usado | String | sim | Produto novo ou de segunda mão  |
| `exchange` | `1` para Sim<br>`2` para Não | String | não<sup>1</sup> | Aceita troca como pagamento |

<sup>1</sup>: Se você não quer enviar um parâmetro não-obrigatório, deixe de enviar o parâmetro no payload. Se você enviar o parâmetro com valor vazio ou `0`, a operação vai falhar (a menos, é claro, que o valor `0` seja esperado para esse parâmetro).

Aqui está um exemplo de JSON para a subcategoria `Carros, vans e utilitários`:

```json
{
    "access_token": "ca18abccaadd282490e75173f98b8ec6f0c1c6c8",
    "ad_list": [
        {
            "subject": "Peça de carro em ótimo estado",
            "body": "Peça de carro do tipo X, usado no caso Y.\nPeça em excelente estado, não aceito trocas.",
            "category": 2101,
            "id": "CAR005_ROD1",
            "images": [
                "http://www.sitedeautos.com/img1.jpg",
                "http://www.sitedeautos.com/img2.jpg"
            ],
            "params": {
                "carcolor": "1",
                "parts_name_cars": "9",
                "condition": "1",
                "exchange": "2"
            },
            "price": 1000,
            "type": "s",
            "zipcode": "20521160"
        },
        {
            "subject": "Peça de carro em ótimo estado",
            "body": "Peça de carro do tipo X, usado no caso Y.\nPeça em excelente estado, não aceito trocas.",
            "category": 2101,
            "id": "CAR005_ROD2",
            "images": [
                "http://www.sitedeautos.com/img1.jpg",
                "http://www.sitedeautos.com/img2.jpg"
            ],
            "params": {
                "carcolor": "1",
                "parts_name_cars": "9",
                "condition": "1",
                "exchange": "2"
            },
            "price": 1000,
            "type": "s",
            "zipcode": "20521160"
        }
    ]
}
```
