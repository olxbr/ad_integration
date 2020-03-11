# Documentação da API de Integração de Anúncios da OLX

A API de Importação de Anúncios da OLX contempla as seguintes funcionalidades:

| Funcionalidade                       | Descrição                                                                                                             | Status             |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------|--------------------|
| [Autenticação oAuth](oauth.md)                   | Permite que anunciantes autentiquem via integrador para configurar integração com OLX                                 | Disponível            |
| [Importação (Inserção/Edição/Deleção)](import.md) | Permite gestão do inventário de anúncios publicados na OLX.                                                           | Disponível |
| [Status de Publicação](publishing_status.md)  | Informa o anunciante/integrador sobre o sucesso da publicação de um anúncio, bem como o motivo de uma não-publicação. | Disponível |
| [Marcas/Modelos de Carros/Motos](autos/car_models.md)             | Disponibiliza o catálogo de marcas e modelos de carros e motos que podem ser publicados na OLX                                | Disponível            |
| [Anúncios Publicados](published_ads.md)       | Lista todos os anúncios publicados, para o anunciante ter controle de quais anúncios estão disponívels na OLX no momento.                         | Disponível      |

# Nova API de Importação de Anúncios

A visão final da nova API traz diferentes benefícios, como expansão para diferentes cartegorias, melhor tratamento de erros, mais ferramentas internas para resolução e maior flexibilidade para futuras melhorias. Estamos prevendo duas fases para a evolução dessa API:

## **Fase 1**: Migração dos integradores para nova API
Migração de todos os integradores para a nova API, emulando contrato e funcionamento da API atual. Mais detalhes na [seção que detalha essa primeira Fase](fase1.md). 

**Status**: Concluída

## **Fase 2**: Adequação a validações assíncronas
Remoção da maior parte de validações síncronas, com necessidade do intregrador passar a utilizar novos mecanismos de consulta de status de publicação do anúncio. Expansão para novas categorias.

**Status**: Início no final de 2019, com período de adaptação até meio de 2020.


# Dúvidas e sugestões

Se tiver dificuldades ou sugestões, [abra uma Issue nesse repositório](https://github.com/olxbr/ad_integration/issues/new) e a equipe de desenvolvimento da OLX vai responder seu contato. Em casos urgentes, entre em contato com suporteintegrador@olxbr.com e você será contatado pela nossa equipe de suporte.