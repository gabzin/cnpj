<h1 align='center'>
CNPJ TECH
</h1>
<p align='center'>
  <a href='https://cn-pj.tech'>
    <img src='https://github.com/gabzin/cnpj/blob/main/cnpjtech.png?raw=true'/>
  </a>
</p>

<p align='center'>
  <a href='https://cn-pj.tech/api'><img src='https://img.shields.io/badge/Atualiza%C3%A7%C3%A3o-12/01/2022-blue'/></a>
</p>

<p align="center">⭐️ Deixe uma estrela ⭐️</p>

<h2 align="center" id="cartaocnpj">CARTÃO CNPJ EM PDF SEM RECAPTCHA</h2>

<p align="center">
  <a href='https://cn-pj.tech/'><img src='https://i.imgur.com/ZaJXZnW.png'/></a>
</p>

<h2 align="center">ENDPOINTS</h2>

<a align='center' href='https://cn-pj.tech/api'>

`GET /api`

</a>

Consultar cadastro completo do de empresas pelo CNPJ.

[Veja documentação](#cnpj)

```json
{
  "msg_ver": "CNPJ API v2.0",
  "ult_att": "12/01/2022",
  "url_doc": "https://github.com/gabzin/cnpj"
}
```



<table align='center' id="cnpj">

<tr><th>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Grátis&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</th><th>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Paga&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</th></tr>
<tr><td align='center'>

 <a href='https://cn-pj.tech/api/00000000000191'>`GET /api/:cnpj`</a>

 Autenticação | Limite
:-:|:-:
Não|25/dia

</td><td align='center'>

 <a href='https://cn-pj.tech/api2/00000000000191?token=...'>`GET /api2/:cnpj?token=…`</a>

 Autenticação | Limite
:-:|:-:
Sim|Sem limites

</td></tr> </table>


```json
{
  "cnpj": "13347016000117",
  "matriz_filial": "Filial",
  "razao_social": "FACEBOOK SERVICOS ONLINE DO BRASIL LTDA.",
  "nome_fantasia": null,
  "cod_natureza_juridica": 2062,
  "natureza_juridica": "Sociedade Empresária Limitada",
  "porte": "DEMAIS",
  "capital": 3631639.0,
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
  "data_inicio_ativ": "09/08/2012",
  "situacao_cadastral": "BAIXADA",
  "data_situacao_cadastral": "18/06/2013",
  "motivo_situacao_cadastral": "EXTINCAO POR ENCERRAMENTO LIQUIDACAO VOLUNTARIA",
  "cnae_principal": {
    "7319004": "Consultoria em publicidade"
  },
  "cnae_secundaria": {
    "null": null
  },
  "contato": {
    "ddd_1": "11",
    "tel_1": "30486800",
    "ddd_2": null,
    "tel_2": null,
    "email": "rita.nader@bakermckenzie.com"
  },
  "endereco": {
    "cep": "4542000",
    "uf": "SP",
    "cod_municipio": 7107,
    "municipio": "SAO PAULO",
    "bairro": "ITAIM BIBI",
    "tipo_logadouro": "RUA",
    "logadouro": "LEOPOLDO COUTO MAGALHAES JUNIOR",
    "numero": "700",
    "complemento": "ANDAR 5"
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
  ],
  "limites": "21/25",
  "prox_reset": "02/02/2022 ás 08:16"
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
> Mais info: https://cn-pj.tech/contato
> 
