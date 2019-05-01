# 📅 Eventos Python no Brasil

![image](https://cnet3.cbsistatic.com/hub/i/r/2015/10/20/918344b1-977b-468f-9958-7bdc59cfe90f/thumbnail/770x433/08ea2bb4a2fc7421821cf22d37871dcf/back-to-the-future-time-circuit-board.jpg)

## Como adicionar um novo evento na agenda?

Para adicionar uma evento/meetup/conferência/etc na agenda, basta seguir os passos abaixo:

### 1. Forkar esse repositório

O primeiro passo é criar um `fork` desse respositório na sua conta do Github. Se você não sabe como fazer isso, você pode seguir um dos [guias[1]](https://help.github.com/articles/fork-a-repo/) [oficias[2]](https://guides.github.com/activities/forking/) do Github em inglês, ou pode dar uma olhada no texto que a [leportella](http://leportella.com) escreveu sobre [como contribuir com projetos open source[3]](http://leportella.com/pt-br/2017/04/17/como-contribuir-com-open-source.html).

### 2. Adicionar novo evento na agenda

Para adicionar um novo evento na agendar e no site [eventos.python.org.br](https://eventos.python.org.br), basta alterar o arquivo `conferencias.yaml` com os dados do seu evento. É preciso preencher nome, data que o evento começa e termina no padrão yyyy-mm-dd, local onde vai acontecer e url do site. Você usar o modelo abaixo como exemplo:

```yaml
- name: PyConBrasil 2006
  start: 2006-6-1
  end: 2006-6-2
  location: Brasília, DF
  url: https://manual-do-big-kahuna.readthedocs.io/en/latest/historia/pyconbrasil2.html
```

### 3. Fazer um pull request com as alterações

Pronto, agora basta fazer um pull request com as suas mudanças, quando o PR for revisador e aceito, o novo evento deverá aparecer na [agenda](https://calendar.google.com/calendar/embed?src=rougeth.com_5a9t9ilqlfumkopl3nlmmkq9kk%40group.calendar.google.com&ctz=America%2FSao_Paulo) e no site [eventos.python.org.br](https://eventos.python.org.br).

# Rodando o projeto localmente

## Requerimentos
* python3 
* python-dev e/ou python3-dev
* build-essential
* libssl-dev
* libffi-dev
* libxml2-dev
* libxslt1-dev
* zlib1g-dev
* python-pip
* python3-setuptools
* ibis-framework
* python-decouple
* Projeto no Google Calendar API
* Netlify Token

## Instalando
1. Instale os modulos e programas necessarios
    ```
        sudo apt-get install python3 python-dev python3-dev \
        build-essential libssl-dev libffi-dev \
        libxml2-dev libxslt1-dev zlib1g-dev \
        python3-pip
    ```
    ```
        pip3 install -r requirements.txt
    ```

1. Habilite seu Google Calendar API [aqui](https://developers.google.com/calendar/quickstart/python?refresh=1)

1. Crie um novo projeto Oauth2, você pode encontrar mais orientações [aqui](https://developers.google.com/api-client-library/python/guide/aaa_oauth)