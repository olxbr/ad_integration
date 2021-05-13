# Documentação para a Importação via XML para Imóveis na OLX

Este manual tem como objetivo auxiliar a implantação de importação de anúncios de XML para o segmento de Imóveis.

Para que o cliente seja elegível à integração via XML com a OLX, seus anúncios devem ser disponibilizados num arquivo XML em uma URL pública, com o devido permissionamento para seu download a qualquer hora do dia, seguindo o seguinte encoding:

```xml
<?xml version="1.0" encoding="utf-8"?>
```


## Parâmetros básicos

Para a montagem do XML, é necessário respeitar parâmetros genéricos e específicos de cada categoria e/ou subcategoria. Os parâmtros básicos são os seguintes:

| Tag XML| Valor | Obrigatório? | Descrição|
|------------------------------------|-------------------|--------------|------------------------------------|
| `<CodigoImovel>` | String de até 20 caracteres | Sim | Também conhecido como `Ref` ou `External ID`, essa tag serve para te ajudar a identificar o anúncio depois de processado na OLX. |
| `<TituloAnuncio>` | Título com até 90 caracteres | Não | Título do Imóvel, que será mostrado na listagem de resultados |
| `<Titulo>` | Título com até 90 caracteres | Não | Título do Imóvel, que será mostrado na listagem de resultados.  Se o `<TituloAnuncio>` for preenchido, a tag `<Titulo>` é ignorada.   |
| `<Bairro>` | | Não | Esse campo só é utilizado para formar o título do anúncio, caso as tags `<TituloAnuncio>` ou `<Titulo>` não tenham sido preenchidas. Não é usado em nenhum outro lugar da OLX atualmente.|
| `<Cidade>` | | Não | Esse campo só é utilizado para formar o título do anúncio, caso as tags `<TituloAnuncio>` ou `<Titulo>` não tenham sido preenchidas. Não é usado em nenhum outro lugar da OLX atualmente. |
| `<SubTipoImovel>` | Consulte a SubCategoria para saber os valores aceitos em `<SubTipoImovel>` | Sim | Define a categoria onde o anúncio vai ser encontrado. |
| `<CEP>` | Para processamento, nós vamos limpar todo caractere não-numérico enviado. | Sim | Código de localização espacial do imóvel.  |
| `<Observacao>` | Descrição com até 6 mil caracteres | Sim | Descrição do anúncio. Não aceita tags HTML. Para quebra de linha, use a tag `\n` |
| `<PrecoVenda>` | Número inteiro, sem parte decimal, sem separador de milhares | Não | Valor de venda do imóvel.  |
| `<PrecoLocacao>` | Número inteiro, sem parte decimal, sem separador de milhares | Não | Valor de aluguel do imóvel. O `<PrecoLocacao>` será ignorado, caso o campo `<PrecoVenda>` seja preenchido também. |
| `<PrecoCondominio>` | Número inteiro, sem parte decimal, sem separador de milhares  | Não | Valor do condomínio do imóvel. |
| `<ValorIPTU>` | Número inteiro, sem parte decimal, sem separador de milhares | Não | Valor mensal do IPTU do imóvel.  |
| `<AreaTotal>` | Número inteiro, sem parte decimal | Não | Tamanho em metros quadrados do imóvel.  |
| `<AreaUtil>` | Número inteiro, sem parte decimal | Não | Tamanho em metros quadrados do imóvel. Se a `<AreaTotal>` for preenchida, a tag `<AreaUtil>` é ignorada. |
| `<Foto>` `<URLArquivo>` |  | Não | URL em que a imagem está hospedada |
| `<Foto>` `<Principal>` | `1` para definir a imagem principal | Não | Valor `1` caso a imagem seja a imagem principal do anúncio |
| `<Videos>` `<Video>`<sup>1</sup> |  | Não | URL de video<sup>2</sup> que será inserida no anúncio do olx.com.br deve ser apenas do https://www.youtube.com. Aceito 1 vídeo por anúncio. |

<sup>1</sup>: **A inserção de vídeo está em fase Beta** e pode sofrer alterações com o tempo. **A disponibilidade via XML é apenas para categoria de Imóveis.**

<sup>2</sup>: Formato recomendado de URL: https://www.youtube.com/watch?v=Vt&28raiI1q5

Segue um exemplo de envio de Vídeo:

```  

 <Videos>
        <Video>https://www.youtube.com/watch?v=Vt28raiI1q5</Video>
 </Videos>
 
```

***Observações:***

*- Caso seja necessário alterar o **vídeo** do anúncio, deve-se alterar a URL e realizar uma edição em outro campo, por exemplo: Descrição e título.*

*- A tag de `<Videos>` deve estar dentro da estrutura de `<Imovel>`. Seguir a mesma estrutura para `<Fotos>`*

*- Caso seja **enviado mais de um link** de vídeo no anúncio **será publicado apenas o primeiro** da listagem.*

*- Em caso de **dúvidas entre em contato: video.experience@olxbr.com***



Cada subcategoria pode ter parâmetros específicos para cada uma delas. A documentação destas pode ser achada na página de cada subcategoria - onde também você encontrará exemplos de XMLs para cada subcategoria.

- [Apartamentos](sub_apartment.md)
- [Casas](sub_house.md)
- [Terrenos, sítios e fazendas](sub_land.md)
- [Comércio e Indústria](sub_commercial.md)
