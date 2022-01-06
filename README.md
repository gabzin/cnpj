<h1 align='center'>
CNPJ API v2.0
</h1>

<a href='https://cn-pj.tech/api'>
  <img src='https://logodownload.org/wp-content/uploads/2014/11/receita-federal-logo-1.png'/>
</a>

<p align='center'>
  <a href='https://cn-pj.tech/api'><img src='https://img.shields.io/badge/Atualiza%C3%A7%C3%A3o-22/12/2021-blue'/></a>
</p>

<p align="center">⭐️ Deixe uma estrela ⭐️</p>

<a align='center' href='https://cn-pj.tech/api'>

`GET /api`

</a>

Consultar cadastro completo do de empresas pelo CNPJ.

[Veja documentação](#cnpj)

```json
{
  "msg_ver": "CNPJ API v2.0",
  "ult_att": "06/01/2022",
  "url_doc": "https://github.com/gabzin/cnpj"
}
```

<a align='center' href='https://cn-pj.tech/localiza'>

`GET /localiza`

</a>

Consultar empresas ativas em determinada localidade, baseada em sua atividade(CNAE).

[Veja documentação](#localiza)

```json
{
  "msg_ver": "LOCALIZA CNPJ API v2.0",
  "ult_att": "06/01/2022",
  "url_doc": "https://github.com/gabzin/cnpj"
}
```

<a align='center' href='https://cn-pj.tech/socio'>

`GET /socio`

</a>

Consultar socios em empresas pelo nome.

[Veja documentação](#socio)

```json
{
  "msg_ver": "BUSCA SOCIO API v2.0",
  "ult_att": "06/01/2022",
  "url_doc": "https://github.com/gabzin/cnpj"
}
```

<table align='center' id="cnpj">

<tr><th>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Grátis&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</th><th>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Paga&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</th></tr>
<tr><td align='center'>

 <a href='https://cn-pj.tech/api/00000000000191'>`GET /api/:cnpj`</a>

 Autenticação | Limite
:-:|:-:
Não|100/dia

</td><td align='center'>

 <a href='https://cn-pj.tech/api2/00000000000191?token=...'>`GET /api2/:cnpj?token=…`</a>

 Autenticação | Limite
:-:|:-:
Sim|Sem limites

</td></tr> </table>


```json
{
  "cnpj": "13347016000117",
  "matriz_filial": "Matriz",
  "razao_social": "FACEBOOK SERVICOS ONLINE DO BRASIL LTDA.",
  "nome_fantasia": null,
  "cod_natureza_juridica": 2062,
  "natureza_juridica": "Sociedade Empresária Limitada",
  "porte": "DEMAIS",
  "simples": {
    "optante": false,
    "data_opcao": null,
    "data_exclusao": null
  },
  "mei": {
    "optante": false,
    "data_opcao": null,
    "data_exclusao": null
  },
  "data_inicio_ativ": "14/02/2011",
  "situacao_cadastral": "ATIVA",
  "data_situacao_cadastral": "14/02/2011",
  "motivo_situacao_cadastral": "SEM MOTIVO",
  "cnae_principal": {
    "7312200": "Agenciamento de espaços para publicidade, exceto em veículos de comunicação"
  },
  "cnae_secundaria": {
    "7020400": "Atividades de consultoria em gestão empresarial, exceto consultoria técnica específica",
    "7319004": "Consultoria em publicidade"
  },
  "contato": {
    "ddd": "11",
    "tel": "30736800",
    "email": "TAXCOMPLIANCEBR@FB.COM"
  },
  "endereco": {
    "cep": "4542000",
    "uf": "SP",
    "cod_municipio": 7107,
    "municipio": "SAO PAULO",
    "bairro": "ITAIM BIBI",
    "tipo_logadouro": "RUA",
    "logadouro": "LEOPOLDO COUTO DE MAGALHAES JUNIOR",
    "numero": "700",
    "complemento": "ANDAR 1/5/6/9/14 E 15     EDIF  INFINITY"
  },
  "qsa": [
    {
      "ident": "PESSOA JURÍDICA",
      "doc": "22576790000190",
      "nome": "FACEBOOK MIAMI, INC.",
      "data_entrada": "17/09/2015",
      "qualificacao": "Sócio Pessoa Jurídica Domiciliado no Exterior",
      "idade": "Não se aplica"
    },
    {
      "ident": "PESSOA FÍSICA",
      "doc": "***634408**",
      "nome": "CONRADO LEISTER",
      "data_entrada": "14/11/2018",
      "qualificacao": "Administrador",
      "idade": "41-50 Anos"
    }
  ]
}
```

<table align='center' id="localiza">

<tr><th>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Grátis&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</th><th>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Paga&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</th></tr>
<tr><td align='center'>

 <a href='https://cn-pj.tech/localiza/6920601?cidade=mirandopolis&uf=sp'>`GET /localiza/:cnae?cidade=…&uf=…`</a>

 Autenticação | Limite | Parametros(Obrigatórios)
:-:|:-:|:-:
Não|100/dia|cidade, uf

</td><td align='center'>

 <a href='https://cn-pj.tech/localiza2/6920601?cidade=mirandopolis&uf=sp&token=...'>`GET /localiza2/:cnae?cidade=…&uf=…&token…`</a>

 Autenticação | Limite | Parametros(Obrigatórios)
:-:|:-:|:-:
Sim|Sem limites|cidade, uf

</td></tr> </table>

```json
{
  "cnae": "6920601",
  "cnae_desc": "Atividades de contabilidade",
  "cidade": "MIRANDOPOLIS",
  "uf": "SP",
  "empresas": [
    "https://cn-pj.tech/api/00033913000104",
    "https://cn-pj.tech/api/11641813000187",
    "https://cn-pj.tech/api/12740493000185",
    "https://cn-pj.tech/api/12910981000274",
    "https://cn-pj.tech/api/15736855000152",
    "https://cn-pj.tech/api/18231657000125",
    "https://cn-pj.tech/api/22480235000160",
    "https://cn-pj.tech/api/51103042000199",
    "https://cn-pj.tech/api/54868351000148",
    "https://cn-pj.tech/api/59766089000144"
  ]
}
```

<table align='center' id="socio">

<tr><th>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Grátis&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</th><th>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Paga&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</th></tr>
<tr><td align='center'>

 <a href='https://cn-pj.tech/socio/JOAO%20DA%20SILVA%20PEREIRA?exato'>`GET /socio/:nome?exato`</a>

 Autenticação | Limite | Parametros(Opcionais)
:-:|:-:|:-:
Não|100/dia|exato, ativas

</td><td align='center'>

 <a href='https://cn-pj.tech/socio2/JOAO%20DA%20SILVA%20PEREIRA?exato&token=...'>`GET /socio2/:nome?token=…&exato`</a>

 Autenticação | Limite | Parametros(Opcionais)
:-:|:-:|:-:
Sim|Sem limites|exato, ativas

</td></tr> </table>

```json
{
  "nome": "JOAO PEREIRA SILVA",
  "nome_exato": true,
  "ativas": true,
  "socios": {
    "***394098**": [
      "https://cn-pj.tech/api/07927941000114"
    ],
    "***348203**": [
      "https://cn-pj.tech/api/20677542000100"
    ],
    "***855853**": [
      "https://cn-pj.tech/api/03327501000175"
    ],
    "***381638**": [
      "https://cn-pj.tech/api/24326348000131"
    ]
  }
}
```

<h1 align='center'>
Exemplo de uso com Python
</h1>

<p align='center'>Sem token</p>

```python
from requests import get

data = get('https://cn-pj.tech/api/13347016000117').json()

cnpj = data['cnpj']
nome = data['razao_social']

print(cnpj, nome)
```


<p align='center'>Com token</p>

```python
from requests import get
TOKEN = ""

data = get(f'https://cn-pj.tech/api2/13347016000117?token={TOKEN}').json()

cnpj = data['cnpj']
nome = data['razao_social']

print(cnpj, nome)
```

> Para melhor visualização dos dados no navegador:
> 
> https://chrome.google.com/webstore/detail/json-viewer/gbmdgpbipfallnflgajpaliibnhdgobh?hl=pt-BR
>
> Dados atualizados conforme atualização do banco de dados da Receita Federal.
> 
> Mais info: gabriel-tavares2009@hotmail.com
> 
