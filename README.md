# ObraFácil v2 — Orçamentos de construção civil

Aplicação web móvel, em português de Portugal, para uso local do negócio.

## Funcionalidades
- Criar e guardar orçamentos no navegador do dispositivo.
- Catálogo por categorias, com serviços e preços editáveis.
- Quantidade direta ou cálculo por medidas: área, parede, volume, comprimento linear e parede com desconto de portas/janelas.
- Preço de venda direto ou custo + margem sobre o custo.
- Configuração do custo horário da equipa, número de trabalhadores e ajudante.
- Desconto e IVA configurável por orçamento.
- Impressão e opção do navegador “Guardar como PDF”.
- Partilha do resumo via partilha do telemóvel/WhatsApp ou cópia para colar.
- Exportação/importação de cópia de segurança JSON.
- PWA básica com cache offline.

## Fórmulas
- Área = comprimento × largura.
- Parede = comprimento × altura.
- Volume = comprimento × largura × altura/profundidade.
- Parede líquida = comprimento × altura − área de portas − área de janelas (nunca abaixo de zero).
- Custo unitário = materiais + outros custos + (horas de mão de obra × custo horário da equipa).
- Preço de venda por custo + margem = custo unitário × (1 + margem/100).
- Subtotal = soma de quantidade × preço unitário.
- Desconto = limitado ao subtotal.
- IVA acrescentado = (subtotal − desconto) × taxa de IVA.
- Se os preços já incluem IVA, o IVA é discriminado a partir do total; o total não aumenta.

A margem configurada é uma margem sobre o custo (markup), não a percentagem de margem sobre o preço final.

## Dados e segurança
Os dados são guardados no `localStorage` do navegador. Não existe sincronização na nuvem. Limpar os dados do site pode apagar orçamentos; exporte cópias de segurança regularmente. Ao importar, os dados atuais são substituídos.

Os preços iniciais são zero e os nomes são exemplos de catálogo. Introduza os seus próprios preços e confirme consumos, condições e enquadramento fiscal.

## Publicar com GitHub Pages
1. Crie um repositório no GitHub chamado `obrafacil`.
2. Carregue os ficheiros desta pasta para a raiz do repositório (`index.html`, `app.js`, `manifest.webmanifest`, `sw.js`, `icon.svg`, `README.md`).
3. No repositório, abra **Settings → Pages**.
4. Em **Build and deployment**, selecione **Deploy from a branch**.
5. Selecione a branch `main` e a pasta `/ (root)`, e guarde.
6. Aguarde pela publicação e abra o URL indicado pelo GitHub Pages.
7. No Samsung, abra esse URL no Chrome → menu ⋮ → **Instalar aplicação** ou **Adicionar ao ecrã principal**.

## Nota sobre PDF e partilha
O botão de impressão abre a função de impressão do navegador. No Android, escolha “Guardar como PDF”. O botão Partilhar envia um resumo de texto pelo menu de partilha quando suportado. Para enviar o documento completo por WhatsApp, guarde o PDF e anexe-o na conversa.
