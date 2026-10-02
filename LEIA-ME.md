# Site do Grupo Escoteiro Marechal Rondon — 194/SP

Versão de revisão — 26/09/2026. Site estático compatível com GitHub Pages. Não há mensalidade de software, painel público de edição, banco de dados ou senha embutida.

## Visualizar
Extraia todo o ZIP e abra index.html. Os links internos funcionam sem servidor. As fontes on-line exigem conexão. O Pix configurado deve ser conferido na versão hospedada, pois a leitura de JSON pode ser bloqueada ao abrir por arquivo.

## Publicar no GitHub Pages
1. Entre em sua conta GitHub e crie um repositório público para o site, no plano gratuito.
2. Envie os arquivos desta pasta para a raiz do repositório.
3. Em Settings > Pages, escolha Deploy from a branch, branch main, pasta / (root).
4. Aguarde a publicação e abra o endereço fornecido pelo GitHub. O endereço depende do usuário e do nome do repositório.
5. Ative autenticação em dois fatores na conta e mantenha somente colaboradores expressamente autorizados. Um repositório público pode ser lido, mas isso não dá aos visitantes permissão para editar.

Nenhuma conta GitHub foi conectada nem repositório foi criado nesta entrega. O site ainda não foi publicado.

## Atualizar notícias
Os relatos estão em conteudo.json, na lista posts. Duplique um item e altere slug (sem espaços/acentos), título, categoria, data, imagem, texto e URL de fonte. Coloque fotos autorizadas em assets. Execute `python gerar_site.py` para atualizar páginas e listagens. Publique os arquivos gerados. Os seis relatos iniciais são resumos, não transcrições integrais das publicações.

O arquivo gerar_site.py também contém os textos das páginas institucionais e pode ser editado para futuras atualizações. Não há edição anônima ou armazenamento de alterações de visitantes.

## Pix — pendente dos dados do grupo
Em conteudo.json, o objeto pix tem três campos vazios: payload, favorecido e qr_image.
- payload: código Pix copia e cola oficial fornecido pela conta do grupo;
- favorecido: nome exato que aparece no aplicativo bancário;
- qr_image: caminho de imagem do QR Code oficial, por exemplo assets/pix.png.
A interface só exibe o Pix quando os três campos estiverem preenchidos e o payload começar por 000201. Essa checagem não valida o destinatário nem a integridade do código: conferir o QR e o código no aplicativo bancário antes da publicação. Não gerar chave presumida a partir do CNPJ. Não há confirmação automática de pagamento. O site mostra um contato de apoio enquanto os dados não forem fornecidos.

## Conteúdo para validar com o grupo
- Horários atuais, vagas, faixas etárias e ramos ativos: a versão orienta consultar a equipe e não inventa datas ou horários.
- Logotipo original em maior resolução e fotografias originais: versão de revisão usa o símbolo público e um recorte de foto pública do grupo. Confirmar autorização para republicação antes de divulgar amplamente; substituir pelos arquivos originais para maior nitidez.
- Foto inicial: registro da publicação DcE4ADrlBTn no Instagram, agosto de 2026. A mesma foto é usada como imagem de acervo em alguns cartões; não representa necessariamente o evento específico do cartão.
- Não foram recebidos estatuto, relatórios, agenda futura, telefone institucional confirmado ou Pix. Não há documentos ou eventos fictícios.
- Grupo Padrão Ouro: anúncio do próprio grupo; edição não especificada nesta versão.

## Fontes
Instagram: https://www.instagram.com/gemarechalrondon194/
Diretoria: https://www.instagram.com/gemarechalrondon194/p/DTn-ojRgWHZ/
Foto de acervo: https://www.instagram.com/gemarechalrondon194/p/DcE4ADrlBTn/
Atividade: https://www.instagram.com/gemarechalrondon194/p/DdgezoOG3y0/
Formação: https://www.instagram.com/gemarechalrondon194/p/DcEghebFO4y/
Óleo: https://www.instagram.com/gemarechalrondon194/p/DTsLBC1Dr7S/
Grupo Padrão: https://www.instagram.com/gemarechalrondon194/p/DUB0t4lkmXe/
História: https://www.omunicipio.jor.br/wordpress/2024/04/10/grupo-marechal-rondon-completa-55-anos-de-existencia/
Ação social: https://www.omunicipio.jor.br/wordpress/2023/08/09/escoteiros-sanjoanenses-vencem-competicao-de-acao-solidaria/
Legislação: https://sapl.saojoaodaboavista.sp.leg.br/ta/2283/text

## Conferências realizadas
Sintaxe JavaScript, existência de destinos de links locais, imagens e âncoras; estrutura de títulos e metadados. A revisão visual automatizada no navegador não foi possível nesta sessão: a abertura de arquivos locais foi bloqueada pela política do navegador. Layout adaptável implementado, mas não declarar testes visuais de celular/desktop como concluídos.


## Edição de outubro de 2026

A identidade visual usa `style.css` e `editorial.css`. Execute `python gerar_site.py` para regenerar as páginas após editar textos e notícias. Os relatos completos estão em `article_sections`, no gerador; os resumos e a configuração Pix continuam em `conteudo.json`. Ao adicionar notícia, acrescente também suas seções a `article_sections`. A ilustração da abertura e as capas gráficas são elementos decorativos, não fotografias de eventos. Preserve as fontes dos relatos.
