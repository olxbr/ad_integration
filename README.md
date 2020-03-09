# Documentação para a Importação de Anúncios da OLX Brasil

A OLX hoje suporta dois tipos de importação de anúncios, para anunciantes que querem gerenciar seus anúncios a partir de um software terceiro (ou seja, sem passar pelas interfaces nativas da OLX para gestão de inventário): via API ou via arquivo (JSON ou XML).


## Status das Integrações da OLX

| Modelo de Integração | Versão em produção | Categorias atendidas | Próximos passos |
|----------------------|----------------------------|----------------------|---------------------------------------------------------------------------------------|
| [API](api/README.md) | Estável | Todas as categorias | Escrever documentação de categorias não-documentadas. Preparar comunicação e rollout da Fase 2 da nova API de Integração de Anúncios. |
| [JSON](json/README.md) | Estável | Todas as categorias | Escrever documentação de categorias não-documentadas. |
| [XML](xml/real_estate/README.md) | Estável | Imóveis | Nenhuma evolução prevista. Documentação atualizada.


## Categorias Suportadas por cada Modelo de Integração

Nem todas as categorias de anúncios na OLX são suportadas pelas integrações existentes:

| Categoria | Subcategoria | JSON | XML | API |
|-------------------------|-----------------------------------------|------|-----|-----|
| Imóveis | Apartamentos | [Sim](json/real_estate/README.md) | [Sim](xml/real_estate/README.md) | [Sim](api/real_estate/README.md) |
| Imóveis | Casas | [Sim](json/real_estate/README.md) | [Sim](xml/real_estate/README.md) | [Sim](api/real_estate/README.md) |
| Imóveis | Aluguel de quartos | [Sim](json/real_estate/README.md) | Não | Sim<sup>1</sup>  |
| Imóveis | Temporada | [Sim](json/real_estate/README.md) | Não | Sim<sup>1</sup>  |
| Imóveis | Terrenos sítios e fazendas | [Sim](json/real_estate/README.md) | [Sim](xml/real_estate/README.md) | [Sim](api/real_estate/README.md) |
| Imóveis | Comércio e indústria | [Sim](json/real_estate/README.md) | [Sim](xml/real_estate/README.md) | [Sim](api/real_estate/README.md) |
| Autos e peças | Carros vans e utilitários | Sim<sup>1</sup> | Não | [Sim](api/autos/README.md) |
| Autos e peças | Motos | Sim<sup>1</sup> | Não | [Sim](api/autos/README.md) |
| Autos e peças | Ônibus | Sim<sup>1</sup> | Não | [Sim](api/autos/README.md) |
| Autos e peças | Caminhões | [Sim](json/auto/README.md) | Não | [Sim](api/autos/README.md) |
| Autos e peças | Barcos e aeronaves | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Peças e acessórios | Carros vans e utilitários | [Sim](json/autoparts/README.md) | Não | [Sim](api/autoparts/README.md) |
| Peças e acessórios | Motos | [Sim](json/autoparts/README.md) | Não | [Sim](api/autoparts/README.md) |
| Peças e acessórios | Ônibus | [Sim](json/autoparts/README.md) | Não | [Sim](api/autoparts/README.md) |
| Peças e acessórios | Caminhões | [Sim](json/autoparts/README.md) | Não | [Sim](api/autoparts/README.md) |
| Peças e acessórios | Barcos e aeronaves | [Sim](json/autoparts/README.md) | Não | [Sim](api/autoparts/README.md) |
| Para a sua casa | Móveis | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Para a sua casa | Eletrodomésticos | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Para a sua casa | Materiais de construção e jardim | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Para a sua casa | Utilidades domésticas | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Para a sua casa | Objetos de decoração | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Eletrônicos e celulares | Videogames | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Eletrônicos e celulares | Computadores e acessórios | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Eletrônicos e celulares | Celulares e telefonia | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Eletrônicos e celulares | Áudio TV vídeo e fotografia | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Música e hobbies | Instrumentos musicais | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Música e hobbies | CDs DVDs etc | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Música e hobbies | Livros e revistas | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Música e hobbies | Antiguidades | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Música e hobbies | Hobbies e coleções | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Esportes e lazer | Esportes e ginástica | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Esportes e lazer | Ciclismo | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Artigos infantis |  | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Animais de estimação | Cachorros e acessórios | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Animais de estimação | Gatos e acessórios | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Animais de estimação | Cavalos e acessórios | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Animais de estimação | Aquários e acessórios | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Animais de estimação | Roedores e acessórios | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Animais de estimação | Outros animais e acessórios | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Moda e beleza | Beleza e saúde | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Moda e beleza | Roupas e calçados | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Moda e beleza | Bolsas malas e mochilas | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Moda e beleza | Bijouterias relógios e acessórios | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Agro e indústria | Tratores e máquinas agrícolas | [Sim](json/agro/README.md) | Não | Sim<sup>1</sup> |
| Agro e indústria | Máquinas pesadas para construção | [Sim](json/agro/README.md) | Não | Sim<sup>1</sup> |
| Agro e indústria | Máquinas para produção industrial | [Sim](json/agro/README.md) | Não | Sim<sup>1</sup> |
| Agro e indústria | Peças para tratores e máquinas | [Sim](json/agro/README.md) | Não | Sim<sup>1</sup> |
| Agro e indústria | Animais para agropecuária | [Sim](json/agro/README.md) | Não | Sim<sup>1</sup> |
| Agro e indústria | Produção Rural | [Sim](json/agro/README.md) | Não | Sim<sup>1</sup> |
| Agro e indústria | Outros itens para agro e indústria | [Sim](json/agro/README.md) | Não | Sim<sup>1</sup> |
| Comércio e escritório | Equipamentos e mobiliário | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Comércio e escritório | Trailers e carrinhos comerciais | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Comércio e escritório | Outros itens para comércio e escritório | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Serviços |  | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |
| Vagas de emprego |  | Sim<sup>1</sup> | Não | Sim<sup>1</sup> |

<sup>1</sup> A OLX suporta atualmente integração via JSON e API para essa categoria, mas a documentação ainda não está atualizada. Se deseja integrar com essa categoria, entre em contato com suporterintegrador@olxbr.com ou abra uma issue nesse repositório.

## Perguntas e Dúvidas Frequentes

Algumas das principais dúvidas relativas à integração de anúncios com a OLX podem ser vistas aqui:

- [Mudança de categoria de anúncios](faq/category.md)
- [Especificações para imagens dos anúncios](faq/images.md)
- [Inferência de Inserção, Edição e Deleção de Anúncios em Integrações via XML ou JSON](faq/xml_json_insertion.md)


## Dúvidas, Sugestões e Comentários

Caso você queria um suporte para sua integração, pode enviar email para suporteintegrador@olxbr.com.

Ou você pode [abrir uma Issue neste repo](https://github.com/olxbr/ad_integration/issues), que a equipe técnica da OLX vai olhar e responder a issue.

**Importante**: Esta documentação está focada na importação de anúncios para o portal OLX Brasil. Para importação de anúncios para os portais Autoshift e Storia Imóveis, contate suporteintegrador@olxbr.com.
