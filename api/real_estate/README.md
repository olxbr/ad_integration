## Categoria de Imóveis

Para importação da categoria de Imóveis, é necessário informar a `category`, que será utilizada para que o anúncio esteja disponível na categoria correta. As subcategorias existentes são as seguintes:

| `category` | Categoria na OLX            |
|------------|-----------------------------|
| `1020`     | Apartamentos                |
| `1040`     | Casas                       |
| `1060`     | Aluguel de quartos          |
| `1080`     | Temporada                   |
| `1100`     | Terrenos, sítios e fazendas |
| `1120`     | Comércio e indústria        |

### Parâmetros específicos por subcategoria

Cada subcategoria de Imóveis tem seu conjunto de parâmetros e valores específicos. Para isso, você deverá considerar os parâmetros específicos para cada subcategoria, bem como os [parâmetros gerais para quaisquer anúncio na OLX](/api/import.md).

Exemplos de JSONs completos de cada subcategoria estão disponíveis na página de cada subcategoria.

- [Apartamentos](sub_apartment.md)
- [Casas](sub_house.md)
- [Aluguel de quartos](sub_roomrent.md)
- [Temporada](sub_season.md)
- [Terrenos, sítios e fazendas](sub_land.md)
- [Comércio e Indústria](sub_commercial.md)