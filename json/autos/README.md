# Documentação para a Importação via JSON para Veículos na OLX

Este manual tem como objetivo auxiliar a implantação de importação de anúncios de veículos para as subcategorias `Carros, vans e utilitários`, `Ônibus`, `Caminhões`, `Motos` e `Barcos e aeronaves`, via JSON.

### Subcategorias 

Para que o anúncio seja categorizado corretamente na OLX, é preciso que cada anúncio esteja associado à `category` correspondente:

| `category` | Categoria na OLX |
|------------|----------------------------|
| `2020` | Carros, vans e utilitários |
| `2060` | Motos |
| `2050` | Ônibus |
| `2040` | Caminhões |
| `2080` | Barcos e aeronaves |

### Parâmetros específicos por subcategoria

Cada subcategoria de Veículos tem seu conjunto de parâmetros e valores específicos. Para isso, você deverá considerar os parâmetros específicos para cada subcategoria, bem como os [parâmetros gerais para quaisquer anúncio na OLX](/json/README.md).

Exemplos de JSONs completos de cada subcategoria estão disponíveis na página de cada subcategoria.

- [Carros, vans e utilitários](sub_autos.md) (Em breve)
- [Motos](sub_motorcycle.md) (Em breve)
- [Ônibus](sub_bus.md) (Em breve)
- [Caminhões](sub_truck.md)
- [Barcos e aeronaves](sub_boat_plane.md) (Em breve)
