### Subcategoria `Comércio e indústria`

Para esta subcategoria, é necessário preencher o parâmetro `<SubTipoImovel>` com os seguintes valores:

| `<SubTipoImovel>` | Título do anúncio |
|---------------------------------------|-------------------------|
| `Andar` | Escritório |
| `Casa Comercial` | Escritório |
| `Conjunto Comercial` | Escritório |
| `Conjunto Comercial / Sala` | Escritório |
| `Laje Comercial` | Escritório |
| `Salão Comercial` | Escritório |
| `Sobrado Comercial` | Escritório |
| `Área Comercial` | Galpão/Depósito/Armazém |
| `Galpão / Depósito / Armazém`   | Galpão/Depósito/Armazém |
| `Galpão / Depósito / Barracão`  | Galpão/Depósito/Armazém |
| `Galpão Comercial` | Galpão/Depósito/Armazém |
| `Indústria` | Galpão/Depósito/Armazém |
| `Box Garagem` | Garagem/vaga |
| `Hotel` | Hotel |
| `Hotel Residencial` | Hotel |
| `Motel` | Hotel |
| `Pousada / Chalé` | Hotel |
| `Pousada` | Hotel |
| `Barracão Comercial` | Loja Comercial |
| `Centro Comercial` | Loja Comercial |
| `Comercial` | Loja Comercial |
| `Loja` | Loja Comercial |
| `Loja Comercial` | Loja Comercial |
| `Loja de Shopping` | Loja Comercial |
| `Loja de Shopping / Centro Comercial` | Loja Comercial |
| `Loja Salão` | Loja Comercial |
| `Ponto Comercial` | Loja Comercial |
| `Prédio` | Prédio Comercial |
| `Prédio Comercial` | Prédio Comercial |
| `Prédio Inteiro` | Prédio Inteiro |
| `Sala` | Sala Comercial |
| `Sala Comercial` | Sala Comercial |


Além disso, há parâmetros específicos para esta subcategoria, que devem constar dentro do parâmetro `params` e preenchidos conforme a tabela a seguir:

| Parâmetro | Valor | Obrigatório | Descrição |
|------------------|---------|------------------|-------------|
| `<SubTipoImovel>` | Consulte tabela anterior | Sim | Define a categoria onde o anúncio estará localizado na OLX |
| `<QtdVagas>` | `0` para 0 vagas<br> `1` para 1 vaga<br> `2` para 2 vagas<br> `3` para 3 vagas<br> `4` para 4 vagas<br> `5` para 5 ou mais vagas<br> | Não | Quantidade de vagas de garagem |



Aqui está um exemplo de XML para inserção ou edição de anúncios na subcategoria `Comércio e indústria`:

```xml
<?xml version="1.0" encoding="utf-8"?>
<Carga xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <Imoveis>
        <Imovel>
            <CodigoImovel>LOJA001</CodigoImovel>
            <TituloAnuncio>Loja Espaçosa Bem No Centro Da Cidade</TituloAnuncio>
            <SubTipoImovel>Conjunto Comercial</SubTipoImovel>
            <Cidade>São Paulo</Cidade>
            <Bairro>Bela Vista</Bairro>
            <CEP>05018000</CEP>
            <PrecoVenda>800000</PrecoVenda>
            <ValorIPTU>1200</ValorIPTU>
            <QtdVagas>10</QtdVagas>
            <AreaUtil>500</AreaUtil>
            <Observacao>A melhor loja do bairro, prontinha para você montar seu negócio!\nFica perto do metrô e está cheio de vagas no estacionamento!\nMuito legal, você deveria visitar!</Observacao>
            <Fotos>
                <Foto>
                    <URLArquivo> http://www.site_da_imobiliaria.com/foto_legal.jpg</URLArquivo>
                </Foto>
                <Foto>
                    <Principal>1</Principal>
                    <URLArquivo> http://www.site_da_imobiliaria.com/foto_legal2.jpg</URLArquivo>
                </Foto>
            </Fotos>
        </Imovel>
    </Imoveis>
</Carga>
```
