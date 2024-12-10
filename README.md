<img src="logo.png" alt="Logo do Ecologuia" width="200">


O Ecologuia é um guia eletrônico desenvolvido para reunir conteúdos e recursos didáticos diversificados sobre Educação Ambiental. Construído na plataforma Omeka-S, o guia organiza o material em coleções de itens categorizados e subcategorizados, promovendo fácil acesso e navegabilidade.

O projeto foi criado no âmbito da disciplina Governo Aberto da Escola de Artes, Ciências e Humanidades (EACH) da USP, sob a orientação da Profª. Drª. Giselle Craveiro, em parceria com a Prefeitura de São Vicente, São Paulo. Ele surgiu da necessidade identificada de materiais didáticos que pudessem apoiar a implementação da Política Nacional de Educação Ambiental nas escolas de todo o país, especificamente para o município de São Vicente.

O Ecologuia tem como objetivo principal fomentar a discussão sobre mudanças climáticas nas escolas municipais, promovendo a Educação Ambiental como ferramenta essencial de letramento climático. A plataforma busca não apenas oferecer acesso simplificado a conteúdos digitais para educadores, mas também incentivar a troca ativa de conhecimentos e experiências. Por meio dessa colaboração, espera-se que os educadores contribuam para enriquecer e retroalimentar continuamente o guia, ampliando seu impacto educativo.

---

**CONHEÇA A VERSÃO INICIAL NO SITE:**  http://letramentoclimatico.infinityfreeapp.com

Inicialmente instalado em um servidor gratuito para demonstração, possui algumas limitações de upload de arquivos nos formulários de contribuição, porém totalmente funcional num servidor local ou pago.

## 📋 **Sumário**

- [Características](#características)
- [Pré-requisitos](#pré-requisitos)
- [Instalação](#instalação)
- [Licença](#licença)

---

## ✨ **Características**

A escolha do Omeka-S como plataforma baseou-se em suas funcionalidades adaptáveis, que atendem aos objetivos do Ecologuia. Diversos plugins foram incorporados para aprimorar a usabilidade e a colaboração, incluindo:

1. AdvancedResourceTemplate: expande as funcionalidades dos templates e dos recursos e é dependência para outros plugins.
2. Collecting: permite a criação de formulários para colaboração;
3. Common e Guest: oferecem acesso e criação de contas de usuários;
4. UserNames: gestão dos usuários
5. Comment: viabiliza comentários nos conteúdos publicados;
6. Annote: considerado para comentários, avaliações e compartilhamento;
7. Fields e Tags: facilita buscas avançadas por meio de tags associadas a palavras-chave.
8. Itens Set Tree: cria o índice automático das categorias e subcategorias e a quantidade de recursos guardados em cada coleção.
9. Menu: cria menus personalizáveis para cada seção ou página do site.
10.Mapping: permite localizar recursos do site geograficamente
11. PdfEmbed: permite incorporar arquivos PDF ao site, sem necessídade de baixá-los.
12. Derivative Media: otimiza o desempenho e a compatibilidade dos arquivos de mídia, como pré visualizações, conversão de 
    formatos e redimensionamento.
13. UniversalViewer: exibição interativa de diversos tipos de arquivos diretamente na plataforma

## 💾 GUIA PARA INSTALÇÃO
 
Esse guia explica como instalar o Omeka S (ECOLOGUIA) em um localhost (como XAMPP) e em um servidor web.

## **Pré-Requisitos**

Antes de instalar, certifique-se de que o ambiente atende aos requisitos mínimos:
(Se usar o XAMPP, desconsidere estes requisitos, pois ele possui todos acoplados)

Servidor Web: Apache recomendado.
PHP: Versão 7.4 ou superior (compatível com PHP 8.x).
Banco de Dados: MySQL 5.7 ou superior (ou MariaDB 10.1 ou superior).
Extensões PHP Necessárias: pdo_mysql, fileinfo, gd, mbstring, curl, intl, xml

## **Instalação**

**1. Em Servidor local, usando XAMPP**

Passo 1: Configurar o Ambiente

Baixe e instale o XAMPP:
Download XAMPP (para instalação talvez seja necessário desativar o firewall)
Após terminar, entre no Painel de Controle do XAMPP e ative o Apache e o MySQL
Baixe o Omeka S:
Acesse a página oficial e baixe a versão mais recente do Omeka S.
Extraia os Arquivos:
Extraia o conteúdo baixado na pasta htdocs do XAMPP.
Renomeie a pasta, por exemplo: localhost/omeka-s.

Passo 2: Configurar o Banco de Dados

Acesse o phpMyAdmin (geralmente em http://localhost/phpmyadmin).
Crie um banco de dados para o Omeka S, por exemplo: omeka_s.
Opcionalmente, crie um usuário e senha com permissões para este banco.

Passo 3: Configurar o Omeka S

Abra o arquivo config/database.ini no diretório do Omeka S.
Insira as configurações do banco de dados que você criou.

host     = "localhost"
username = "root"   ; Ou outro usuário criado
password = ""       ; senha para o root
dbname   = "omeka_s"

Passo 4: Finalizando instalação  

Clone e Substitua as seguintes pastas com os arquivos clonados no seu 
diretório htdocs do XAMPP: modules, files, themes e config (crie o database.ini manualmente com
os dados do seu banco de dados)

No navegador, vá para http://localhost/omeka-s (caminho da pasta com o Omeka-S)
Siga as instruções para configurar o administrador e finalizar a instalação.

**2. Instalação em Servidor Web**

Passo 1: Configurar o Servidor

Após baixar o Omeka-S, substitua as pastas mencionadas acima no seu diretório htdocs.
Suba os arquivos no servidor:
Use um cliente FTP (como FileZilla) ou um painel de controle para enviar os arquivos para o servidor.
Coloque os arquivos na pasta pública (geralmente public_html ou www).

Configurar as Permissões:
Garanta que as pastas files/ e logs/ sejam graváveis.

Passo 2: Configurar o Banco de Dados

Crie um banco de dados no painel de controle do seu servidor (como cPanel ou Plesk).
Anote o nome do banco, usuário e senha.

Passo 3: Configurar o Omeka S
Edite o arquivo config/database.ini e insira as credenciais do banco de dados criado

host     = "seu-servidor-database"
username = "seu-usuario"
password = "sua-senha"
dbname   = "omeka_s"

Passo 4: Finalizar a Instalação

Acesse o site no navegador (https://seu-dominio.com).
Siga as instruções para configurar o administrador.

## 🔒 **Notas de Segurança**

Nunca exponha o arquivo config/database.ini.
Altere as permissões para restringir acesso a arquivos sensíveis:
Considere usar HTTPS para proteger conexões.

## **Recursos Adicionais**

**Materiais sugeridos**

Instruções oficiais do Omeka para a configuração geral
https://omeka.org/classic/docs/Admin/Settings/ 
Instruções oficiais do Omeka para a configuração de Segurança
https://omeka.org/classic/docs/Admin/Settings/Security_Settings/ 
Instruções oficiais do Omeka para a configuração de Pesquisa
https://omeka.org/classic/docs/Admin/Settings/Search_Settings/ 
Instruções oficiais do Omeka para a configuração dos Conjuntos de elementos
 https://omeka.org/classic/docs/Admin/Settings/Element_Sets/ 
Instruções oficiais do Omeka para a configuração dos Elementos do tipo de item
https://omeka.org/classic/docs/Admin/Settings/Item_Type_Elements/ 
Instruções oficiais do Omeka para a configuração dos APIs
https://omeka.org/classic/docs/Admin/Settings/API_Settings/ 
Instruções oficiais do Omeka para criação de coleções
https://omeka.org/classic/docs/Content/Collections/ 


## 📝 **Licença**

Este projeto está licenciado sob a **Creative Commons BY-NC-SA**
Atribuição-Não Comercial-Compartilhamento pela Mesma Licença 4.0 Internacional. 
Para mais informações, visite creativecommons.org/licenses/by-nc-sa/4.0/.

O software OMEKA-S é licenciado sob a **GNU General Public License v3 (GPLv3)**.





