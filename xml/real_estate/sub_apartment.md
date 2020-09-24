### Subcategoria `Apartamentos`

Para que o anúncio apareça nesta subcategoria, é necessário preencher o parâmetro `<SubTipoImovel>` com os seguintes valores:

| `<SubTipoImovel>` | Título do anúncio |
|-----------------------------------|-----------------------|
| `Apartamento` | Apartamento |
| `Apartamento de Condomínio` | Apartamento |
| `Apartamento Duplex Residencial` | Apartamento |
| `Apartamento Padrão` | Apartamento |
| `Apartamento Residencial` | Apartamento |
| `Apartamento Triplex Residencial` | Apartamento |
| `Conjunto Residencial` | Apartamento |
| `Padrão` | Apartamento |
| `Cobertura` | Cobertura |
| `Cobertura Duplex` | Cobertura |
| `Cobertura Residencial` | Cobertura |
| `Cobertura Triplex` | Cobertura |
| `Penthouse Residencial` | Cobertura |
| `Flat` | Loft |
| `Flat Padrão` | Loft |
| `Flat Residencial` | Loft |
| `Loft` | Loft |
| `Loft Residencial` | Loft |
| `Kitchenette / Conjugados` | Kitchenette/conjugado |
| `Kitchenette / Studio` | Kitchenette/conjugado |
| `Kitnet` | Kitchenette/conjugado |
| `Kitnet / Conjugado` | Kitchenette/conjugado |
| `Kitnet Residencial` | Kitchenette/conjugado |
| `Studio` | Studio |

Caso não seja enviado nenhum valor para `<TituloAnuncio>`, será montado um título para o anúncio baseado no `<SubTipoImovel>` e outros atributos, como número de quartos, localização, etc. 

Além disso, há parâmetros específicos para esta subcategoria, preenchidos conforme a tabela a seguir:

| Parâmetro | Valor | Obrigatório | Descrição |
|------------------|---------|------------------|-------------|
| `<SubTipoImovel>` | Consulte tabela anterior | Sim | Define a categoria onde o anúncio estará localizado na OLX |
| `<QtdDormitorios>` | `0` para 0 quartos<br> `1` para 1 quarto<br> `2` para 2 quartos<br> `3` para 3 quartos<br> `4` para 4 quartos<br> `5` para 5 ou mais quartos<br> | Sim | Quantidade de quartos |
| `<QtdBanheiros>` | `0` para 0 banheiros<br>`1` para 1 banheiro<br> `2` para 2 banheiros<br> `3` para 3 banheiros<br> `4` para 4 banheiros<br> `5` para 5 ou mais banheiros<br> | Não | Quantidade de banheiros |
| `<QtdVagas>` | `0` para 0 vagas<br> `1` para 1 vaga<br> `2` para 2 vagas<br> `3` para 3 vagas<br> `4` para 4 vagas<br> `5` para 5 ou mais vagas<br> | Não | Quantidade de vagas de garagem |
| `<ArCondicionado>`,<br>`<SalaGinastica>`,<br>`<ArmarioEmbutido>`,<br>`<Varanda>`,<br>`<AreaServico>`,<br>`<Churrasqueira>`,<br>`<QuartoWCEmpregada>`,<br>`<Piscina>`,<br>`<SalaoFestas>`,<br>`<Porteiro>`| Se o anúncio tiver essa característica, envie o parâmetro com o valor `1` | Não | Características adicionais do imóvel. Se o imóvel tem algum desses atributos, inclua esse parâmetro com valor `1`| 




Aqui está um exemplo de XML para inserção ou edição de anúncios na subcategoria `Apartamentos`:


```xml
<?xml version="1.0" encoding="utf-8"?>
<Carga xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <Imoveis>
        <Imovel>
            <CodigoImovel>APT0001</CodigoImovel>
            <TituloAnuncio>Apartamento espaçoso</TituloAnuncio>
            <SubTipoImovel>Apartamento Padrão</SubTipoImovel>
            <Cidade>São Paulo</Cidade>
            <Bairro>Perdizes</Bairro>
            <CEP>05018000</CEP>
            <PrecoVenda>500000</PrecoVenda>
            <PrecoCondominio>800</PrecoCondominio>
            <ValorIPTU>500</ValorIPTU>
            <QtdDormitorios>3</QtdDormitorios>
            <QtdVagas>2</QtdVagas>
            <QtdBanheiros>2</QtdBanheiros>
            <AreaUtil>67</AreaUtil>
            <Observacao>Residencial projetado para você em cada detalhe.\nPrédio com Piscina.\nMuito legal, você deveria visitar!</Observacao>
            <Piscina>1</Piscina>
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
        <Imovel>
            <CodigoImovel>APT0002</CodigoImovel>
            <TituloAnuncio>Apartamento espaçoso</TituloAnuncio>
            <SubTipoImovel>Apartamento Padrão</SubTipoImovel>
            <Cidade>São Paulo</Cidade>
            <Bairro>Perdizes</Bairro>
            <CEP>05018000</CEP>
            <PrecoLocacao>3500</PrecoLocacao>
            <PrecoCondominio>1000</PrecoCondominio>
            <ValorIPTU>500</ValorIPTU>
            <QtdDormitorios>2</QtdDormitorios>
            <QtdVagas>2</QtdVagas>
            <QtdBanheiros>2</QtdBanheiros>
            <AreaTotal>60</AreaTotal>
            <Observacao>Apartamentos com dois dormitórios, suíte e vaga dupla e 1 dormitório com vaga e lavabo.\nAcabamento muito acima da média, apartamentos entregues com porcelanato nas áreas frias e laminado na sala e quartos, medidores de água e gás instalados, gesso, mármore e granito nos banheiros e cozinha. Todos os apartamentos possuem churrasqueira na cozinha. - Ref.: 17-DU65009</Observacao>
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
