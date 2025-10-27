# Welcomme to the Izzi Website directrives
Diretrizes de criação de sites da Izzi

# Dominio
O dominio pode ser comprado através de qualquer plataforma, mas preferencialmente pelo [RegistroBR](https://registro.br/), mas deve ser [apontado para o Cloudflare](https://dash.cloudflare.com/?to=/:account/add-site).

# Ferramentas disponíveis
Todos os sites devem ser criados em HTML ou usando build de alguma das ferramentas habilitadas no [Cloudflare Workers/Pages](https://developers.cloudflare.com/pages/configuration/build-configuration/).

# Criação do repositório para o site do cliente
Utilize [Nome da empresa][Projeto] para cria-lo, como nos exemplos abaixo:
#### Bons
- izzi-langing-page
- izzi-solucoes-digitais-landingpage
- izzi-website
- izzi-admin-terraform
#### Ruins
- landingpage-izzi
- landingpage-cliente
- cliente-site
- cliente-website

# Ligue o dominio ao Cloudflare Pages
Para isso acesse a conta da empresa no [Cloudflare -> Pages -> Github](https://dash.cloudflare.com/?to=:account/pages/new/provider/github). Selecione o repositório criado e aguarde até o fim da configuração.
O projeto criado pode ser visto na lista de [Cloudflare Pages/Workers](https://dash.cloudflare.com/?to=:account/workers-and-pages). Clique no nome do projeto para edita-lo, depois em [custom domains] e adicione o dominio do cliente.
Obs: Esta ação deve ser feita após as rotas de DNS propagarem para os servidores do Cloudflare.

# Essencial para SEO
Todo website deve ser cadastrado no [Google Webmaster Tools](https://search.google.com/search-console/welcome) para ser encontrado pelo Bot que indexa o site no buscador. Para isso o site deve conter uma lista de páginas e instruções para robôs e mecanismos de buscas, para isso os deve-se criar os arquivos sitemap.xml e robots.txt.

## Exemplo desses arquivos
Segue exemplos dos arquivos necessários para SEO.

### Sitemap.xml
O sitemap.xml deve conter se parecer com:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
    <url>
        <loc>https://izzisolucoesdigitais.com.br/</loc>
    </url>
    <url>
        <loc>https://izzisolucoesdigitais.com.br/termos-e-condicoes</loc>
    </url>
    <url>
        <loc>https://izzisolucoesdigitais.com.br/politica-de-privacidade</loc>
    </url>
</urlset>
```

### Robots.txt
O robots.txt deve conter se parecer com:
```text
User-agent: *
Disallow: /admin/
Disallow: /private/
Allow: /politica-de-privacidade
Allow: /termos-e-condicoes
Allow: /

Sitemap: https://izzisolucoesdigitais.com.br/sitemap.xml
```
O link para o sitemap deve necessáriamente conter o dominio (NÃO deve-se usar caminho relativo como `/sitemap.xml`);

